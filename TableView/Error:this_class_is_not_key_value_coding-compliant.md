UITableViewCell error - this class is not key value coding-compliant for the key

What causes this issue?
This is caused by one of the following issues, the Storyboard or the XIB file is expecting to be connected to an IBOutlet and during run time it is not able to find that outlet so it crashes. It could also be due to the Storyboard referencing the incorrect class.

Perfect link for explanation:https://programmingwithswift.com/fix-this-class-is-not-key-value-coding-compliant-for-the-key/

"Make sure that File's Owner in the nib is set to NSObject and also make sure that there are no outlets wired up to File's Owner."

"Check all of the elements in your nib to be sure their not referencing something that no longer exists. Right click on them to see what is pointing at what. There will be something in there for sure.

"Looks like you have linked a UILabel in your nib with an IBOutlet that is not existing anymore in your code (descriptionLabel).So check your nib file again. I had this error several times too and this was the solution for me
