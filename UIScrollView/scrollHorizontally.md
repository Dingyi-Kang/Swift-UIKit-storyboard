most of the steps are same as those of setting scrollVertically view

Just as the Vertical scrollView, the content layout view of scrollView need the inside content to know high and how wide it should be

The horizontal scrollView's content layout View also needs its height and width based on the constraints of inside UI component

The difference is that for horizontal scroll view the height of the content layout view will be same/close to the height of frame while the width of content layout will be longer than that of frame.
The specific width is up the the inside content or the constraint

<img width="756" alt="image" src="https://user-images.githubusercontent.com/81428296/180821803-8625affa-8a0f-4d61-895b-d350d92eec15.png">


Also, the height of content layout doesn't need to be same as the height of frame layout. we can set it smaller so as to add some footer below the content view

<img width="760" alt="image" src="https://user-images.githubusercontent.com/81428296/180822374-62c24fc5-12db-47ff-b3e7-d62882b9f6cd.png">
