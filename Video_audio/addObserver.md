# This is about how to know when a video is ready to play, so that we may stop loading indicator and hide the PauseControlerView


## Note: somehow below code doesn't work for me (i.e., the addObserver func will make a creash)
![image](https://user-images.githubusercontent.com/81428296/151301430-c729cd91-a354-48f3-8f68-b5ced2dce041.png)
Link:https://stackoverflow.com/questions/5401437/knowing-when-avplayer-object-is-ready-to-play

## Instead this code and tutorial works for me (i.e., the addPeriodicObserver func)
![image](https://user-images.githubusercontent.com/81428296/151306882-32a359ef-f6d0-4c4e-99e9-e3d479948ed4.png)

## link to this useful tutorial: https://santoshkumarjm.medium.com/how-to-design-a-custom-avplayer-to-play-audio-using-url-in-ios-swift-439f0dbf2ff2
![image](https://user-images.githubusercontent.com/81428296/151306991-edf474ac-10de-474f-9f31-71d2fac3c60a.png)

## below is the offical doc
![image](https://user-images.githubusercontent.com/81428296/151301845-265bb4d8-4c75-4a4d-9d8e-656cb39367d5.png)
link: https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/AVFoundationPG/Articles/02_Playback.html



