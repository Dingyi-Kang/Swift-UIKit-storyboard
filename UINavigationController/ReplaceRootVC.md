
        func changeRootVC() {
        if let newVC  = self.storyboard?.instantiateViewController(withIdentifier: "MyStoryboardID"), let nc = self.navigationController {
            nc.setViewControllers([newVC], animated: true)
        }

        }
        
Note1: if the rootVC is replaced, the NavBarItem associated with the original rootVC will disappear as well (because each Navbaritem is associated with a presented VC in the navStack)

So, we need to assign the NavBarItem to the newVC'a navBar like below
![image](https://user-images.githubusercontent.com/81428296/148462883-9341338f-5183-4d1b-814a-36a58c8c4d33.png)

### above is very important and tricky. If you configure the navBarItem in the newVC's viewDidLoad, it won't work since when it is initialized its navigationController and navigationItem are nil. Instead, you should configure new VC' barItem after it has been linked/inserted into the navVC
<img width="941" alt="image" src="https://user-images.githubusercontent.com/81428296/176546597-d21003d8-d67c-4713-969d-066b63172a99.png">




Note2: we cannot directly push the new NavBarItem into the UInavigationVC's navBar. or, the error will show: "Cannot call pushNavigationItem:animated: directly on a UINavigationBar managed by a controller."

But we have to use func -- "pushItem" when the UINavigationViewController still doesn't have any embedded VC (namely, in the initial stage), like below:
![image](https://user-images.githubusercontent.com/81428296/148462750-61512f29-fb7d-4c4b-bb88-dcb45e7a836d.png)

More info about NavBarItem: https://github.com/Dingyi-Kang/Swift-storyboard-basic/blob/main/UINavigationController/updateNavBarItem.md
