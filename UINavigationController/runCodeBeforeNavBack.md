First, there is no way to use unwind segue because navigation controller "independent" from view controller

I found two ways: viewWillDisappear()  I have tried and i worked

Second, viewWillMove(). I haven't tried yet and I need to do more research on meaning of "parent"

Link: https://stackoverflow.com/questions/28760541/programmatically-go-back-to-previous-viewcontroller-in-swift
