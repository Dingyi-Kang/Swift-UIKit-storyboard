
To add a shadow to the words within a label, you can use the NSAttributedString class and its NSShadow attribute. Here is an example of how to do this:

          let label = UILabel()

          // Create an attributed string with the desired text and shadow
          let shadow = NSShadow()
          shadow.shadowColor = UIColor.black
          shadow.shadowOffset = CGSize(width: 2, height: 2)
          shadow.shadowBlurRadius = 2

          let attributes: [NSAttributedString.Key: Any] = [
              .shadow: shadow
          ]

          let attributedString = NSAttributedString(string: "Label Text", attributes: attributes)

          // Set the attributed text on the label
          label.attributedText = attributedString

Note: you don't have to configure all nsattributesOfString programmatically here. Instead, you configure those editable features of text in storyboard/xib
