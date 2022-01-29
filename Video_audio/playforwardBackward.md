## Below is an example of moving forward for 5 seconds
                  if let duration = avPlayer?.currentItem?.duration{
                      let playerCurrentTime = CMTimeGetSeconds(avPlayer!.currentTime())
                      let newTime = playerCurrentTime + 5
                      if newTime < CMTimeGetSeconds(duration){
                      let selectime = CMTimeMake(value: Int64(newTime*1000 as Float64), timescale: 1000)
                          avPlayer?.seek(to: selectime)}
                  }
                  
                  
## Tutorial Link: 
https://santoshkumarjm.medium.com/how-to-design-a-custom-avplayer-to-play-audio-using-url-in-ios-swift-439f0dbf2ff2
                  
              
