This is a demo of how to bold parts of string in different positions.    
First, you need to use NSAttributedString instead of plain string
Then:

        guard let fullText = self.bottomMessage.attributedText?.string else {return}
        let firstRange = (fullText as NSString).range(of: "What can you do?")
        let secondRange = (fullText as NSString).range(of: "Learn More")
        let fullString = NSMutableAttributedString(string: fullText)
        fullString.addAttributes([NSAttributedString.Key.font : UIFont.boldSystemFont(ofSize: 16)], range: firstRange)
        fullString.addAttributes([NSAttributedString.Key.font: UIFont.boldSystemFont(ofSize: 16)], range: secondRange)
        self.bottomMessage.attributedText = fullString
