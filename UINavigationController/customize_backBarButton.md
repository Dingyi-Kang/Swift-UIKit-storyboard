## self.navigationItem.backBarButtonItem is for the back button that appears on the view pushed by the view controller. So you need to move that line to the previous view controller.
![image](https://user-images.githubusercontent.com/81428296/155463217-758a38c4-f269-4774-af12-00816c435279.png)
![image](https://user-images.githubusercontent.com/81428296/155463146-d2014c31-9183-4a1a-98d8-ebd55a6dbaa8.png)
![image](https://user-images.githubusercontent.com/81428296/155463170-764f71aa-6aeb-4feb-a86d-1b6d3908b500.png)

### Link: https://stackoverflow.com/questions/4964276/navigationitem-backbarbuttonitem-not-working-why-is-the-previous-menu-still-sho

## set the navBarItem  --- very tricky -- update the navBarItem in the previous VC instead of the presenting VC
![image](https://user-images.githubusercontent.com/81428296/155462673-78f095d4-03df-4a49-b669-d066f604c3d6.png)
![image](https://user-images.githubusercontent.com/81428296/155462744-b22437d5-bbfa-4d8d-ab9a-8c7927e56ba8.png)
