
link: https://www.youtube.com/watch?v=O7u9nYWjvKk 

Code with Christ


## 1. add this data model file and name it with the name of the project
![image](https://user-images.githubusercontent.com/81428296/156957291-3f4a6959-d683-4a4f-87f8-e87f4b8335be.png)

### Then you will have this
![image](https://user-images.githubusercontent.com/81428296/156957382-0d8aafb2-0aa5-4382-a98d-efcc79693cdf.png)

## 2. copy the below code to your appDelegate file
### dont forget to import coreData library in your appDelegate file
### dont forget to update the name of NSPersistentContainer

    
      // MARK: - Core Data stack

      lazy var persistentContainer: NSPersistentContainer = {
          /*
           The persistent container for the application. This implementation
           creates and returns a container, having loaded the store for the
           application to it. This property is optional since there are legitimate
           error conditions that could cause the creation of the store to fail.
          */
          let container = NSPersistentContainer(name: "PatternMaster")
          container.loadPersistentStores(completionHandler: { (storeDescription, error) in
              if let error = error as NSError? {
                  // Replace this implementation with code to handle the error appropriately.
                  // fatalError() causes the application to generate a crash log and terminate. You should not use this function in a shipping application, although it may be useful during development.

                  /*
                   Typical reasons for an error here include:
                   * The parent directory does not exist, cannot be created, or disallows writing.
                   * The persistent store is not accessible, due to permissions or data protection when the device is locked.
                   * The device is out of space.
                   * The store could not be migrated to the current model version.
                   Check the error message to determine what the actual problem was.
                   */
                  fatalError("Unresolved error \(error), \(error.userInfo)")
              }
          })
          return container
      }()

      // MARK: - Core Data Saving support

      func saveContext () {
          let context = persistentContainer.viewContext
          if context.hasChanges {
              do {
                  try context.save()
              } catch {
                  // Replace this implementation with code to handle the error appropriately.
                  // fatalError() causes the application to generate a crash log and terminate. You should not use this function in a shipping application, although it may be useful during development.
                  let nserror = error as NSError
                  fatalError("Unresolved error \(nserror), \(nserror.userInfo)")
              }
          }
      }
