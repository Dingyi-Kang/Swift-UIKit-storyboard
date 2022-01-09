![image](https://user-images.githubusercontent.com/81428296/148670859-a8cf44ae-fe19-4c33-a659-0b4d6e4f0fbb.png)

    // Create a child view controller and add it to the current view controller.
    let storyboard = UIStoryboard(name: "Main", bundle: .main)
    if let viewController = storyboard.instantiateViewController(identifier: "imageViewController")
                                        as? ImageViewController {
       // Add the view controller to the container.
       addChild(viewController)
       view.addSubview(viewController.view)

       // Create and activate the constraints for the child’s view.
       onscreenConstraints = configureConstraintsForContainedView(containedView: viewController.view,
                                 stage: .onscreen)
       NSLayoutConstraint.activate(onscreenConstraints)

       // Notify the child view controller that the move is complete.       
       viewController.didMove(toParent: self)
    }
    
    
![image](https://user-images.githubusercontent.com/81428296/148670903-cba35e8d-7fb2-499a-824b-a3bd8e627411.png)
