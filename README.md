# swift-storyboard-basic
These are my notes about the basic of swift storyboard

- [NSAttributedString](NSAttributedString/) 
  * [Add attributes to plain text](NSAttributedString/Add_Attributes.md)      
  * [Change font of NSAttributedString](NSAttributedString/Changing_font_size_of_attributed_String.md)    
  * [Useful link 1](https://www.hackingwithswift.com/articles/113/nsattributedstring-by-example)   
  * [Add an underline](NSAttributedString/AddUnderline.md)
  * [Add more than one attribute to different places of a NSAttributedString (including detecting range of sub-text)](NSAttributedString/Bold_Parts_Of_String_At_Different_Places_Within_A_String.md)
  * [Useful link 2 (which including extending UILabel class)](https://newbedev.com/make-part-of-a-uilabel-bold-in-swift)     
- [UILabel](UILabel/) 
  * [Add hyperlinks](UILabel/AddHyperLinks)
  * [How to programmatically add tapGesture](UILabel/tapGesture.md)
- [Animation, transition and other visual effect](Animation/)
  * [UIView Animation with completion closure](Animation/UIViewAnimation.md)
  * [Transition](Animation/transition.md)
  * [Add Advanced Shadow](Animation/advancedShadow.md)
- [Debug and logging](Debug_and_logging/) 
  * [What is logging? print, NSLog, os_log](https://stevenpcurtis.medium.com/logging-in-swift-d9b59146ff00) 
  * [Why is logging needed?](https://developer.apple.com/videos/play/wwdc2020/10168/) 
- [TableView](TableView/) 
  * [How embed a tableView inside a tableView](TableView/EmbeddedTableView.md)
  * [Ways to set custom tableViewCell](TableView/Ways_To_Set_Custom_TableViewCell.md)
  * [Scroll to certain row](TableView/Scroll_To_Certain_Row.md)
  * [Scroll not working and causing VC losing data passed by parent VC](TableView/ScrollCausingBugs.md)
  * [Register custom nib cell into tableView](TableView/Register_Nib_Cell_Into_tableView.md)
  * [Cell Set selected initially](TableView/Certain_Row/Cell_Selected_Initially.md)
  * [Error: this_class_is_not_key_value_coding-compliant](TableView/Error:this_class_is_not_key_value_coding-compliant.md)
  * [Error: Outlets cannot be connected to repeating content iOS (dynamic prototypes VS static cells)](TableView/Error:Outlets_cannot_be_connected_to_repeated_content.md)
  * [TableView with multiple sections and headers for sections]https://www.youtube.com/watch?v=AHY09z-XS9s
  * [Deselecting the table view row when returning](TableView/deselect_when_returnBack.md)
  * [TextField in tableView](TableView/textField.md)
  * [Tricks of adding simple header and footer to tableView](TableView/trickHeaderFooter.md)
- [UIButton and ToolBar items](Button_ToolBar/) 
  * [Make ToolBar_Button Item unusable and invisiable](Button_ToolBar/Make_Button_Item_invisiable.md)
  * [Create a radio button](Button_ToolBar/Create_Radio_Button.md)
  * [Set title text color of UIbutton](Button_ToolBar/Set_TitleTextColor_of_Button.md)
  * [Change line space of title of UIbutton](Button_ToolBar/Set_lineSpace_of_Button.md)
  * [Why change button title font size doesn't work?](Button_ToolBar/fontSizeUpdate.md)
  * [Customization: iOS 15: UIButton.configuration](https://sarunw.com/posts/new-way-to-style-uibutton-in-ios15/)
  * [Padding image, title and subtitle](Button_ToolBar/padding.md)
  * [Easy but tricky -- UIbuttonImage != UIButtonBackgroundImage -- how to set button title top of an image in button](Button_ToolBar/backgroundImage.md)
  * [How to make UIButton programmatically](Button_ToolBar/addAction.md)
  * [Very misleading -- states of button: selected, hightlighted and normal](Button_ToolBar/stateButton.md)
  * [How to set color of title of Button](Button_ToolBar/titleColor.md)
  * [How to programmatically add action/gesture to button](Button_ToolBar/addTarget.md)
  * [How to add GestureRecoginzer/Action to View or Label](Button_ToolBar/addActionToView.md)
- [UISegmentControl](UISegmentControl/)
  * [Is it possible to have both title and image? The official doc says no] (UISegmentControl/have_titleAndImage.md)
  * [How to create custom Segmented Controller](UISegmentControl/createCustomSegmentControl.md)
- [TextField/TextView](TextField&TextView/) 
  * [Difference between TextField and TextView](TextField&TextView/Difference_between_TextField_and_TextView.md)
- [UIScrollView](UIScrollView/)
  * [The secrete of UIScrollView](UIScrollView/tutorial.md)
  * [An easy way to adjust/update the background of the scrollView](UIScrollView/adjustBackground.md)
  * [Scroll to the top](UIScrollView/scrollToTop.md)
- [Firebase](FireBase/) 
  * [How to store dictionary in Swift to FireBase](FireBase/How_To_Store_Dictiionary_To_FireBase.md)
  * [Rule of Security of FireBase](FireBase/Rule_Security.md)
  * [How to choose between Cloud FireStore and Realtime FireBase](https://firebase.google.com/docs/database/rtdb-vs-firestore)
- [UINavigationController](UINavigationController/)
  * [Intro](UINavigationController/Intro.md)
  * [Official document -- very useful](https://developer.apple.com/documentation/uikit/uinavigationcontroller)
  * [QuickStart: setup navVC using storyboard vs programmatically](UINavigationController/quickStart.md)
  * [Depth: setup navVC](UINavigationController/Depth_navVC.md)
  * [Change Title Of UINavgationBar](UINavigationController/Change_title_of_navigationBar.md)
  * [Customize the Appearance of NavgationBar](UINavigationController/customize_navigationBar.md)
  * [Tricky -- Customize the backBarButton](UINavigationController/customize_backBarButton.md)
  * [!Update NavigationBarItem](UINavigationController/updateNavBarItem.md)
  * [How to show image in bar button item as it is](UINavigationController/barItemImage.md)
  * [Replace RootVC of NavigationViewController](UINavigationController/ReplaceRootVC.md)
  * [Set UINavVC as the Root VC of the Window/App](UINavigationController/SetNavAsRoot.md)
  * [How to run certain code before nav back](UINavigationController/runCodeBeforeNavBack.md)
  * [How to pass data through navigation back button](UINavigationController/passDataViaNavBack.md)
- [Storyboard and Segue](Storyboard_segue/)
  * [Intro to Segue](Storyboard_segue/Intro_Segue.md)
  * [Official Document of Segue](Storyboard_segue/Official_document_Unwind_Segue.md)
  * [Lifecycle of Segue](Storyboard_segue/lifeCycle_segue.md)
  * [Styles of Action Segue](Storyboard_segue/styles_actionSegue.md)
  * [Unwind Segue and Passing Info Back](Storyboard_segue/Unwind_Segue.md)
  * [Tips of using storyboard](Storyboard_segue/Small_tricky_tips_of_storyboard.md)
- [Container View Controllers & Container View](Container_View_Controller/)
  * [Overview of ContainerViewControllers](Container_View_Controller/Overview_of_Container_VC.md)
  * [Add and remove childVC programmatically](Container_View_Controller/Add_Remove_ChildVC_Programmatically.md)
  * [When & How to Embed child VC into ContainerView using Storyboard and embeded segues](Container_View_Controller/When_How_EmbedChildVC_using_storyboard.md)
  * [Addtional Support & Official Document](Container_View_Controller/Additional_Official_Doc.md)
  * [Access child view](Container_View_Controller/AccessChildView.md)
  * [Communication between parent and child view](Container_View_Controller/Communication_bwt_parent_and_child.md)
  * [youtubeTutorial](Container_View_Controller/tutorial.md)
- [UISplitViewController](UISplitViewController/)
  * [Tutorial](UISplitViewController/tutorial.md)
- [Play Video & Audio](Video_audio/)
  * [Play video locally](Video_audio/video.md)
  * [Set size/autolayout of UIView for video](Video_audio/autolayout_audio.md)
  * [Cannot find filePath - make sure to add file into bundle](Video_audio/add_into_bundle.md)
  * [How to stop playing and replay from beginning](Video_audio/stop_replay.md)
  * [CMTime](Video_audio/CMTime.md)
  * [AddObserver - how to know if video is ready to be player (does not mean it has been fully downloaded)](Video_audio/addObserver.md)
  * [How to make playback controller](Video_audio/playbackController.md)
  * [How to play forward/backward](Video_audio/playforwardBackward.md)
- [Notification](notification/)
  * [Local Notification]  (notification/local.md)
  * [Push Notification]. (notification/push.md)
  * [Handle Notification in Foreground](notification/handleInForeGround.md)
  * [Schedule Repeatly](notification/repeat.md)
- [Hierachy of ViewController](Hierachy_of_ViewController/)
  * [How to Set Root View Controller Programmatically](Hierachy_of_ViewController/HowSetRootViewControllerProgrammatically.md)
- [Cocoa Touch Class and Nib](Cocoa_Nib/)
  * [How to load UIView from nib](Cocoa_Nib/How_to_load_nib.md)
  * [How to load VC from nib](Cocoa_Nib/load_VC_from_nib.md)
  * [AwakeFromNib is not called again unless the hosting VC is changed](Cocoa_Nib/awakeFromNibNotCalled.md)
- [Communication betweeb VCs](Communication/)
  * [Protocol, Completion, NotificationCenter](Communication/Protocol_Completion_NOtificationCenter.md)
  * [Getting reference and casting](Communication/Getting_reference_casting.md)
  * [Part 1 - How to pass data back/inform parent VC -- in case of using segue](UINavigationController/passDataViaNavBack.md)
  * [Part 2 - How to pass data back/inform parent VC -- in case of using present method](Communication/present_method.md)
- [Synchronization and asynchronization](SyncAsync/)
  * [How to perform a code after delay](SyncAsync/performCodeAfterDelay.md)
  * [How to cancel previous delayed code](SyncAsync/cancelDelayedCode.md)
- [Animation, Transition, Presentation](AnimationTransitionPresentation/)
  * [Custome Present Style](AnimationTransitionPresentation/presentStyle.md)
- [App LifeCycle - AppDelegate & SceneDelegate](appLifeCycle/)
  * [Difference]. (appLifeCycle/difference.md)
- [Special issues](special/)
  * [Supporting Dark Mode](special/supportDarkMode.md)
- [Swift Grammar](Swift_Grammar/)
  * [Strong vs weak](Swift_Grammar/strong_weak.md)
  * [Class-type protocol and memory leaking](Swift_Grammar/class_protocol.md)
  * [Lazy](Swift_Grammar/lazy.md)
  * [!!!Struct vs class -- constant data vs constant address](Swift_Grammar/struct_class.md)
  * [Access control](Swift_Grammar/access_control.md)
  * [Array sort]
  * [Stored Property vs Computed Property(getter&setter) vs Observer(willSet & didSet)](Swift_Grammar/computed_property.md)
  * [How to get the name of enumeration value which rawValue is not string](Swift_Grammar/enum.md)
  * [Tuple](Swift_Grammar/tuple.md)
  * [get absolute value -- abs()](Swift_Grammar/abs.md)
  * [Cheatsheet of Dictionary -- remove and iterate through](Swift_Grammar/dict.md)
- [Xcode Tips](Xcode_tips/)
  * [Error after Changing Deploy Target -- why no simulator shown](Xcode_tips/Deploy_target.md)
  * [Don't forget to Enter when using storyboard](Storyboard_segue/Small_tricky_tips_of_storyboard.md)
- [App Deployment](App_deployment/)
  * [App deployment to App Store](App_deployment/Deploy_AppStore.md)
- [Git and version controll](VersionControll/)
  * [Solve the conflicts of storyboard](VersionControll/solveConflictsStoryboard.md)
