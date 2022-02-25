## Sometime, scrollToRow which do not work will some bugs, like the hosting VC lost the data passed by its parent VC or child VC

## when you call a delegate of another VC to do task related to UI, the task will be run in background which will cause bugs (withour crash!!). Hence, you need to put them in main thread.

## the reason is: you didn't put that function into dispatchQueue
![image](https://user-images.githubusercontent.com/81428296/155664861-bdecf1cf-6958-4808-82e3-bcf9b4b84dcc.png)

https://www.hackingwithswift.com/read/9/4/back-to-the-main-thread-dispatchqueuemain
