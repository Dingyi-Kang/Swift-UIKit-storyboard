- Multiple lines of codes:                    

            let attributedString = NSMutableAttributedString(string: textString)
            attributedString.addAttribute(NSAttributedString.Key.underlineStyle, value: NSUnderlineStyle.single.rawValue,
                                          range: NSRange(location: 0, length: attributedString.length))
            attributedText = attributedString
- Single line of codes:                    

            label.attributedText = NSAttributedString(string: "Text", attributes:[.underlineStyle: NSUnderlineStyle.single.rawValue])
