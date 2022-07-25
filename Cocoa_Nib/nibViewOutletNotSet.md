### When you create a new nib and delete the default UIView of this nib, copy a UIView from somewhere else and paste it into this newly created nib, then this error will occur:

<img width="688" alt="image" src="https://user-images.githubusercontent.com/81428296/180856413-4fe88b6f-f769-44ee-aa9e-26a5dc8ccfe4.png">
<img width="690" alt="image" src="https://user-images.githubusercontent.com/81428296/180856688-7c801772-7f74-4500-b920-affa97bf4d0c.png">
<img width="645" alt="image" src="https://user-images.githubusercontent.com/81428296/180860352-75c78ce7-b948-4f01-b60d-2048ffa1bd45.png">

## there is also a case in which you cannot find view property. That is because you only add UIview in the nib interface builder instead of UIviewControll. Instead, the file owner should be a viewController

<img width="739" alt="image" src="https://user-images.githubusercontent.com/81428296/180861693-eac593b5-1e85-4e19-b222-ca246a2e0832.png">

## In nib, the fileOwner has a must property - view. And the added UIview in the nib should be assigned the view property of the fileOwner, so that they can build connection with this nib
<img width="682" alt="image" src="https://user-images.githubusercontent.com/81428296/180862625-41092901-6e0b-4f12-b588-5f7e47862c94.png">

<img width="1516" alt="image" src="https://user-images.githubusercontent.com/81428296/180863196-5d8b4a29-774c-4e08-a3d4-2e7259abb009.png">


link:https://stackoverflow.com/questions/4763519/loaded-nib-but-the-view-outlet-was-not-set

official doc of nib: https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/LoadingResources/CocoaNibs/CocoaNibs.html
