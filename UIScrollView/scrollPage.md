<img width="693" alt="image" src="https://user-images.githubusercontent.com/81428296/213557595-c29d7be0-e290-430c-a3c9-dd6b68aeb873.png">
## The easiest way to implement the stopping and drawing back animation is to use page of scrollView. 
## Set the size of scrollView to the size of page for each scroll

link: https://stackoverflow.com/questions/1220354/uiscrollview-horizontal-paging-like-mobile-safari-tabs/1373096#1373096

<img width="678" alt="image" src="https://user-images.githubusercontent.com/81428296/213556457-6a5d0135-8802-4151-a441-e03ee1ae7640.png">
<img width="691" alt="image" src="https://user-images.githubusercontent.com/81428296/213556685-f4aefd74-9e50-428d-a550-f9453f813fca.png">

Another post (not testing if it works well): https://stackoverflow.com/questions/6813270/uiscrollview-custom-paging-size

## However, there are associated potential problems.
## Since the scrollView is not the entire screen anymore. The rest part of scrollView is the screen is outside the bounds of scrollView. Hence, any events happens on them won't be passed to the scrollView, and thus is not scrollable.
## solution 1: we can create a parent View of scrollView and override the hitTest function of the partentView (we named ClipView below)
### explanation: we need to first get reference to the child scrollView in the clipview. Then return scrollView as the receiver
### However, if there is specific button (or anything interactive) within the scrollView, you should call super.hitTest (the original method of hitTest, and it will return its correct subview). If the view is not nil, return the view. otherwise, return the scrollView
    class ClipView: UIView {
        override func hitTest(_ point: CGPoint, with event: UIEvent?) -> UIView? {
            if let scrollView = self.viewWithTag(1) as? UIScrollView{
                let view = super.hitTest(point, with: event)

                if view is UIImageView {
                    return view
                }else{
                    return scrollView
                }
            }
            return nil
        }
    }
    
### offical doc about hitTest
<img width="953" alt="image" src="https://user-images.githubusercontent.com/81428296/213560084-43c5b475-5902-49d4-9756-63b701c3a185.png">
<img width="946" alt="image" src="https://user-images.githubusercontent.com/81428296/213560276-2dc9e69e-bb4e-41cb-a226-b03cb20c4b89.png">
<img width="944" alt="image" src="https://user-images.githubusercontent.com/81428296/213560349-34f95910-31a2-4f04-8738-02fa5951d644.png">

### solution 2: get a reference to scrollview which may be out of bounds, convert the event point to coordinate system of the parent view to the point in the coordiate system of the scrollView. Below is another example
link of post: https://zendesk.engineering/ios-how-to-capture-touch-events-outside-uiview-bounds-bc7461970788
<img width="704" alt="image" src="https://user-images.githubusercontent.com/81428296/213562291-953273fd-d07f-47ca-bd57-71d2a9bbaa52.png">


## another problem is that: there may be Interactive component outside of bounds of the scrollView or clipView
### in my case, this issue is even trickier. since this issue will occur once the Interactive component be outside of bounds of waveView, scrollView, or clipView. (waveViews is overlapped on each other on the scrollView which is embedded in the clipView)
### Hence, I have to adjust these three one by one. 
#### First, I create a new wave image so that the button in wont be outside of the waveView
<img width="436" alt="image" src="https://user-images.githubusercontent.com/81428296/213565114-426fdcf8-f1cb-4e03-9d58-b7f065168d8e.png">
#### Second, I increase the vertical position of clipview, so that when user scroll, the center button is always within the bounds of clipView
<img width="289" alt="image" src="https://user-images.githubusercontent.com/81428296/213565467-a7c47212-b2ca-4d14-ba87-1fc2e9b1774e.png">
