### auto reference counting
### retain cycle
### memory leaking

Official doc: https://docs.swift.org/swift-book/LanguageGuide/AutomaticReferenceCounting.html

Good youtube tutorial: https://youtu.be/VcoZJ88d-vM

More tricky -- the memory leaks in closure: https://stremsdoerfer.medium.com/understanding-memory-leaks-in-closures-48207214cba
#### note: below, onButtonTap is a property instead of func, which causes retain cycle.   what about func?? (if it is func, it wont refer to anything but itself)
<img width="742" alt="image" src="https://user-images.githubusercontent.com/81428296/177029224-d123236b-aca8-4fae-b26e-9cc89e51984c.png">
<img width="790" alt="image" src="https://user-images.githubusercontent.com/81428296/177029229-b8add70a-a8b8-4e37-809d-9c14bebbe151.png">
