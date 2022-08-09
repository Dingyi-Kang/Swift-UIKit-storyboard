The difficulties is due to UIStackView is non-redering type, and thus can make corner on it but cannot make/draw shadow on it; However, if we add a background view to dispaly the shadow, the above UIStackView or subviews of UIStackView will cover the shadow. What is more, we cannot make the maskToBounds of the backgroundView to be ture, or it will clip the shadow as well.

# First -- draw shadow of the UIView

Given UIStackView is a nonrendering(/non-drawing) subclass of UIView, we need to put a background view with color below it
<img width="659" alt="image" src="https://user-images.githubusercontent.com/81428296/183530782-9252f9f1-7cf9-4472-a0b3-83741c83ab06.png">

## You can either embed the UIStackView with a UIView, or add a underneath UIView aligned with its bounds, or add a subview within the UIStack like this tutorial (very good):
<img width="759" alt="image" src="https://user-images.githubusercontent.com/81428296/183531814-5f9dd3ee-803b-488a-ab4d-ed0f815c2702.png">
link: https://useyourloaf.com/blog/stack-view-background-color/

## if you embed the UIStackView into a UIView like this (this solution is similar for the other two backgroundView layout ways):
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

### to solve this issue, we can corner the UIStackView instead of the BackgroundView (still use backgroundView to draw shadow, and thus we need to make the maskToBounds of the backgroundView false in order to show shadow. And make the maskToBounds of UIStackView to ture in order to make corner). 
<img width="604" alt="image" src="https://user-images.githubusercontent.com/81428296/183535776-6edf4520-d8a3-4888-b9e7-c0d37ad4d811.png">

### Then you will get this:
<img width="410" alt="image" src="https://user-images.githubusercontent.com/81428296/183534255-37c29302-18ab-498c-abff-3f13aeef17b1.png">

### why there are corner gaps? because the backgroundView's background color is white! After setting it to clear color, you will get: perfect!
<img width="385" alt="image" src="https://user-images.githubusercontent.com/81428296/183534444-26a3c0a4-6b51-466b-b184-587c280e2eea.png">

### 2 if you embed the backgroundView for drawing shadow at the bottom of the UIStack view, you need to make the UIStackView maskToBounds false, and make above UIViews maskToBounds to be true in order to get the corner, and importantly, make the backgroundView's background color be clear

### 3 Also, you can embed the UIStackView in another intermidiate view (between UIStackView and parent backgroundView) in order to make corner without setting the maskToBounds of the parent backgroundView to be true. (in this way, no need to set the background color of the parentView to clear)
### note: you need to make both corner and shadow of the most parent view, and just make corner the intermiate view. the corner radius should be same
<img width="1299" alt="image" src="https://user-images.githubusercontent.com/81428296/183535278-b36277b6-0b9e-42b4-9adc-2540ba91ce3f.png">
<img width="578" alt="image" src="https://user-images.githubusercontent.com/81428296/183536630-bec39aec-5bca-4975-b24e-1df7bd3b5284.png">

#### maskToBounds and clipToBounds in this case has the same effect
<img width="604" alt="image" src="https://user-images.githubusercontent.com/81428296/183535428-004f031a-0d60-447c-8b04-045c98c0196c.png">

