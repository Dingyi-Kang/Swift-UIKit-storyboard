# First -- draw shadow of the UIView

Given UIStackView is a nonrendering(/non-drawing) subclass of UIView, we need to put a background view with color below it
<img width="659" alt="image" src="https://user-images.githubusercontent.com/81428296/183530782-9252f9f1-7cf9-4472-a0b3-83741c83ab06.png">

## You can either embed the UIStackView with a UIView, or add a underneath UIView aligned with its bounds, or add a subview within the UIStack like this tutorial (very good):
<img width="759" alt="image" src="https://user-images.githubusercontent.com/81428296/183531814-5f9dd3ee-803b-488a-ab4d-ed0f815c2702.png">
link: https://useyourloaf.com/blog/stack-view-background-color/

## if you embed the UIStackView into a UIView like this (emmbed background uiview is similar, but it cannot use maskToBounds func of parent view):
<img width="599" alt="image" src="https://user-images.githubusercontent.com/81428296/183532443-8ff6c577-218f-4f9f-b9c8-84b6de933fa5.png">

### 1.1 you can draw shadow using below code (path and offset is not necessary, and path is for better performance):

        poseSwitchView.layer.shadowOpacity = 0.5
        poseSwitchView.layer.shadowRadius = 5.0
        let path = UIBezierPath.init(roundedRect: poseSwitchView.bounds, cornerRadius: 8.0)
        poseSwitchView.layer.shadowPath = path.cgPath
        poseSwitchView.layer.shadowOffset = CGSize.zero

### 1.2 then you need to make corners. if you make corners like this:
<img width="468" alt="image" src="https://user-images.githubusercontent.com/81428296/183532834-bc32f4a3-8dfa-4176-a153-93af137d3711.png">

### you will get this (because the content of above views (child views) cover the cornered background view):  
<img width="367" alt="image" src="https://user-images.githubusercontent.com/81428296/183532894-51642f21-f20d-48de-b755-f72e30abc7d7.png">

### However, there will be is a conflict. In order to make the subviews not exceed the bounds, we need to set this parent view (backgroundView to maskToBound to true).But, if we do so, no only the child views but also the drawn shadows will be clipped (in this example, shadow will disappear)
<img width="976" alt="image" src="https://user-images.githubusercontent.com/81428296/183533511-7a6277cf-e770-4c66-b4f9-e0a98bc48521.png">



