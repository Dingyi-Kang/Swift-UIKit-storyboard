
By default, there is a wide space between sections. Note, it is not footer or header.

<img width="681" alt="image" src="https://user-images.githubusercontent.com/81428296/178079146-5b68a5ac-8578-4f30-8f64-89db370a2c55.png">

here is the link to the post: https://stackoverflow.com/questions/30364067/space-between-sections-in-uitableview

After iOS15, you can reduce this gap using the new API property:
    if #available(iOS 15.0, *) {
        tableView.sectionHeaderTopPadding = 0
    }
    
    
    
However, for version before 15, I still didn't figure out how to reduce this space. An alternative way to get around is to make the background color of the table view be the color of your header and dismiss the configuration of the color of your header, to make the seperation invisible

#### Hence, this is one case the UITableViewController is not preferable. 
If the background color of the tableview of UITableViewController is switched to color like gray, the whole screen including the tab bar will be impacted. It is even not tolerant to low opacity color since it doesn't have any backgound color anymore. Thus, it will just display dark. In contrast, if we embedded a uitableView in a VC, since this tableView has background view which is at least content view, it can be assigned with background color of low opacity. 
<img width="394" alt="image" src="https://user-images.githubusercontent.com/81428296/178079521-d13f3a90-31b9-4eff-88ed-2d1d94d53ccf.png">

