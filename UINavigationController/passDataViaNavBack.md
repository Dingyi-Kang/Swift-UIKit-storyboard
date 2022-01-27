### Link: https://stackoverflow.com/questions/34955987/pass-data-through-navigation-back-button

## One way is use delegate to tell parentVC that the childVC is gonna disappear
![image](https://user-images.githubusercontent.com/81428296/151442470-9e1b27d3-5c9d-4717-ac4c-4b5baed1b59d.png)

## Or, use navigationDelegate and keep track of previous VC. link: https://stackoverflow.com/questions/27713747/execute-action-when-back-bar-button-of-uinavigationcontroller-is-pressed
![image](https://user-images.githubusercontent.com/81428296/151443580-24039890-d591-48f3-84bb-306cc2377d2f.png)

    func navigationController(_ navigationController: UINavigationController, willShow viewController: UIViewController, animated: Bool) {
        if viewController == self.previousViewController {
            // You are going back
        }
    }
