## my code -- part 1

    @objc private func addImageTapped(){
          let cameraAvailable = UIImagePickerController.isSourceTypeAvailable(UIImagePickerController.SourceType.camera)
          if cameraAvailable {
              let alertController = UIAlertController()
              alertController.addAction(UIAlertAction(title: "Gallery", style: .default, handler: { action in
                  self.openPhotoAlbum()
                  print("Gallery Opened")
              }))
              alertController.addAction(UIAlertAction(title: "Camera", style: .default, handler: { action in                self.startImageCapture()
                  print("Camera Opened")
              }))
              alertController.addAction(UIAlertAction(title: "Cancel", style: .cancel, handler: { action in
                  print("Cancel selected")
              }))
              self.present(alertController, animated: true, completion: nil)

          } else {
              self.openPhotoAlbum()
              print("Gallery Opened")

          }
      }
      
## part 2
     private func startImageCapture() {  
          let pickerVC = UIImagePickerController()
          pickerVC.delegate = self
          pickerVC.sourceType = .camera
          DispatchQueue.main.async {
              self.present(pickerVC, animated: true)
          }
      }
    
    private func openPhotoAlbum() {
        func openGallery() {
            var config = PHPickerConfiguration()
            config.filter = PHPickerFilter.any(of: [.images])
            config.selectionLimit = 1 // limit to only choose one photo
            let picker = PHPickerViewController(configuration: config)
            picker.delegate = self
            DispatchQueue.main.async {
                self.present(picker, animated: true)
            }
        }
        
        let status = PHPhotoLibrary.authorizationStatus(for: .readWrite)
        switch status {
        case .authorized, .limited:
            openGallery()
        case .notDetermined, .denied:
            PHPhotoLibrary.requestAuthorization(for: .readWrite) { authorized in
                guard authorized == .authorized else { return }
                openGallery()
            }
        default:
            break;
        }
    }
      
 ### About the delegate of UIImagePickerViewController:
 #### note: its delegate has to conform both two below protocols
 <img width="1029" alt="image" src="https://user-images.githubusercontent.com/81428296/210666481-7b2f824f-ca13-4346-8a9d-5d1b001285bc.png">

     extension AddGalleryImageViewController: UIImagePickerControllerDelegate, UINavigationControllerDelegate {
        func imagePickerController(_ picker: UIImagePickerController, didFinishPickingMediaWithInfo info: [UIImagePickerController.InfoKey : Any]) {
            DispatchQueue.main.async {
                if let image = info[.originalImage] as? UIImage {
                    print("Adding image")
                    self.addedImageView.image = image
                    self.addedImageView.isHidden = false
                    picker.dismiss(animated: true)
                }
            }
        }

        func imagePickerControllerDidCancel(_ picker: UIImagePickerController) {
            picker.dismiss(animated: true)
        }
    }
    
   ### About the delegate of PHPickerViewController:
       extension AddGalleryImageViewController: PHPickerViewControllerDelegate {
        private static let imageUti: String = "public.image"

        func picker(_ picker: PHPickerViewController, didFinishPicking results: [PHPickerResult]) {

            let itemProviders = results.map(\.itemProvider)
            for item in itemProviders {
                if item.canLoadObject(ofClass: UIImage.self) {
                    item.loadObject(ofClass: UIImage.self) { (image, error) in

                        if error != nil{
                            print(error!)
                        }

                        DispatchQueue.main.async {
                            if let image = image as? UIImage {
                                self.addedImageView.image = image
                                self.addedImageView.isHidden = false
                                print("Gallery Image Selected")
                            }
                        }
                    }
                }
            }
            //should put this code outside since this method is also fired when cancel button of the picker view is tapped
            picker.dismiss(animated: true)
        }

    }
