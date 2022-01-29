## Link: https://www.hackingwithswift.com/example-code/system/how-to-cancel-a-delayed-perform-call

## Cancel specific one
![image](https://user-images.githubusercontent.com/81428296/151674781-9a9e94a6-d1de-4f28-830b-9e3347a96969.png)

    // set up a delayed call…
    perform(#selector(yourMethodHere), with: nil, afterDelay: 1)

    // …then immediately cancel it
    NSObject.cancelPreviousPerformRequests(withTarget: self, selector: #selector(yourMethodHere), object: nil)
![image](https://user-images.githubusercontent.com/81428296/151674850-c80ede89-3c42-4998-a140-4cd933ed9013.png)

## Cancel very specific one
![image](https://user-images.githubusercontent.com/81428296/151674802-dc1642d2-5313-4ceb-a4a0-5a9a97fb1520.png)

      myObj.perform(#selector(yourMethodHere), with: nil, afterDelay: 1)
      NSObject.cancelPreviousPerformRequests(withTarget: myObj, selector: #selector(yourMethodHere), object: nil)
## or cancel all associated with a target
![image](https://user-images.githubusercontent.com/81428296/151674798-3306cf54-b76c-4599-986f-a8dbd108461e.png)
