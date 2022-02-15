## If the constraint of groundImage is set to 0, namely aligning to bottom of the superview/scrollView, there will be white space which is the color of the superview, namely the scrollView
![image](https://user-images.githubusercontent.com/81428296/153996639-9b7b47f7-ae94-46de-bbaa-ce8f0bd7c0e5.png)

## Instead of changing the background color or backgroundView of the superView/scrollView (even do so, there will still be annoying white seperating line. Beside it will impact the color of navigationVC)
![image](https://user-images.githubusercontent.com/81428296/153996932-e1bd3a9a-4a87-4145-9568-ef9b1d39c4be.png)

## We just extend the background image of the scrollView beyong its container/superview/scrollView, like below
![image](https://user-images.githubusercontent.com/81428296/153996216-a21f4967-e755-4e4c-a97a-86b08ebf75af.png)

