First thing need to be repeatedly noted is: doing the navigation bar configuration in viewDidLoad wont work. ViewDidLoad in the view lifecycle just happens once in the initialization stage.
Even before it is pushed to the navigationViewController

<img width="859" alt="image" src="https://user-images.githubusercontent.com/81428296/178326110-1d310e34-80ed-442d-a0e5-cc7750ef47c7.png">


In constrast, we can configure it in viewWillAppear and viewWillDisappear, Note!!! in the tabBarController's navigationItem instead of self.navigationItem? because it is the tabBarController assoicated with the the navController (and these tabVC is embedded inside the tabBarController)

<img width="739" alt="image" src="https://user-images.githubusercontent.com/81428296/178326293-e38c7575-5d2f-4ac6-a5e5-f64cd8b30e49.png">

similarly, if you wanna configure navigationBar background color(this is associated with navigationController) or rightBarItem (this is associated with the navigationItem of the puhsed VC)
<img width="989" alt="image" src="https://user-images.githubusercontent.com/81428296/178327716-3197c449-6cd5-4195-892a-8db23f7a1e95.png">


Here is the post which saved me from this: https://stackoverflow.com/questions/48696116/change-navigation-bar-title-when-different-tab-is-selected

<img width="750" alt="image" src="https://user-images.githubusercontent.com/81428296/178326756-7a3632c6-5e74-46f9-a057-3978da210f63.png">

