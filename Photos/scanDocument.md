good tutorial:
https://mistergrizzly.medium.com/scanning-documents-with-vision-and-visionkit-on-ios-13-913c0a6f9392

## Note: the completion handler is descripted at the request but the handler

<img width="725" alt="image" src="https://user-images.githubusercontent.com/81428296/216223097-b7c313b6-20a5-4cf2-8bef-a882dfb388ab.png">


    func documentCameraViewController(_ controller:            VNDocumentCameraViewController, didFinishWith scan: VNDocumentCameraScan) {
    // Process the scanned pages
    for pageNumber in 0..<scan.pageCount {
        let image = scan.imageOfPage(at: pageNumber)
    }

    // You are responsible for dismissing the controller.
    controller.dismiss(animated: true)
    }
    
    
    func documentCameraViewControllerDidCancel(_ controller: VNDocumentCameraViewController) {
    // You are responsible for dismissing the controller.
    controller.dismiss(animated: true)
    }
    
    
    func documentCameraViewController(_ controller: VNDocumentCameraViewController, didFailWithError error: Error) {
    // You should handle errors appropriately in your app.
    print(error)

    // You are responsible for dismissing the controller.
    controller.dismiss(animated: true)
    }
