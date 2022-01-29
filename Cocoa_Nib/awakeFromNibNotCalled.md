### Once a nib is loaded into memory for a ViewController, the func of awakeFromNin won't be called
### Hence, to recover to the default setting of the nib after certain actions, like scroll back to the custom tableView cell, we need to talk with hosting View controller

### below wont work if the VC is not changed (below is the code in class VideoCell:TableViewCell)
![image](https://user-images.githubusercontent.com/81428296/151680868-3fcfcfe4-1a89-4ee5-9c9d-459961de8a2f.png)
### hence, we need to talk with VC for the setting (below is the code in class LessonVC: ViewController)
![image](https://user-images.githubusercontent.com/81428296/151680914-df891ffc-b849-48c2-9575-d77e33ea2ec1.png)
