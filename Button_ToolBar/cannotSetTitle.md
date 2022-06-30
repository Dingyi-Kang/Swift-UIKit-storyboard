## According to the document, below is why the setTitle func doesn't work
### why means the title of button you want to set already has a nsAttributed title. So, no matter what plain title you set using setTitle func, it will be ignored
<img width="996" alt="image" src="https://user-images.githubusercontent.com/81428296/176726890-2bd2911c-3c55-4da2-96f7-cfa5458f69b1.png">

### instead use the setAttributeTitle func like below
      confirmButton.setAttributedTitle(NSAttributedString(string: "SAVE",
      attributes: [NSAttributedString.Key.foregroundColor : UIColor.white, 
      NSAttributedString.Key.font: UIFont(name: "Menlo Bold", size: 20)!]), for: .normal)
