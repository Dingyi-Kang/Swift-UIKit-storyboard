# important: if there is update of view constraints, need call layoutIfNeed at the end of animation code, like below
![image](https://user-images.githubusercontent.com/81428296/156084723-5ac1763d-5edb-4806-94ba-6560b68932c9.png)

## Note: animation code cannot be a code and assigning boolean value. It has to be
### like below view.isHidden = false wont work. Instead, view.alpha = 0 will work
![image](https://user-images.githubusercontent.com/81428296/151677571-ce5bd869-4f1b-4d6e-a0c8-bef6b061cc56.png)

## Reasons:
![image](https://user-images.githubusercontent.com/81428296/151677739-944ca818-2741-4577-b2f8-65eb96345dc8.png)
![image](https://user-images.githubusercontent.com/81428296/151677988-3bd2db7b-57d3-428b-9d00-4291714af345.png)

## Other link:
https://gist.github.com/fxm90/723b5def31b46035cd92a641e3b184f6
## great tutorial
Link: https://www.raywenderlich.com/5255-basic-uiview-animation-tutorial-getting-started


