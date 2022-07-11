The title color is managed by the navigationController not the embedded VC
Hence, we need to get access the navigation controller

This could be even trickier if the embbed vc is the tabBarController

In this case, the navigation controller (and navigation item) is not accessible directly from this tab VC (it will return nil). Instead, it is accessible only via self.tabBarController

Like below example
<img width="1055" alt="image" src="https://user-images.githubusercontent.com/81428296/178330526-01797458-5f03-4cb3-899a-bd7cef09eb58.png">


Here is the link of the post:
https://stackoverflow.com/questions/43706103/how-to-change-navigationitem-title-color

<img width="761" alt="image" src="https://user-images.githubusercontent.com/81428296/178330603-9c2d6970-4075-4ee7-b877-a1f69db790ef.png">

<img width="618" alt="image" src="https://user-images.githubusercontent.com/81428296/178330727-cc15a92d-051d-4654-b189-28f3289a010b.png">

          if #available(iOS 13.0, *) {
              navigationController?.navigationBar.standardAppearance.titleTextAttributes = [.foregroundColor: UIColor.white]
          } else {
              navigationController?.navigationBar.titleTextAttributes = [.foregroundColor: UIColor.white]
          }
          
or custom color

          UINavigationBar.appearance().titleTextAttributes = [NSAttributedString.Key.foregroundColor : UIColor(red: 0.7415059209, green: 0.5448099971, blue: 0.5051562786, alpha: 1)]
