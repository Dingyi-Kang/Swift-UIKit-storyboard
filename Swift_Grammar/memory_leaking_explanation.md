### auto reference counting
### retain cycle
### memory leaking

Official doc: https://docs.swift.org/swift-book/LanguageGuide/AutomaticReferenceCounting.html

Good youtube tutorial: https://youtu.be/VcoZJ88d-vM

## More tricky -- the memory leaks in closure: https://stremsdoerfer.medium.com/understanding-memory-leaks-in-closures-48207214cba
#### note: below, onButtonTap is a property instead of func, which causes retain cycle.   what about func?? (if it is func, it wont refer to anything but itself)
<img width="742" alt="image" src="https://user-images.githubusercontent.com/81428296/177029224-d123236b-aca8-4fae-b26e-9cc89e51984c.png">
<img width="790" alt="image" src="https://user-images.githubusercontent.com/81428296/177029229-b8add70a-a8b8-4e37-809d-9c14bebbe151.png">

## the key is to ask who owns the closure
## another important part is: if the owner's property gets assigned/changed, or just a function gets called within a closure of the owner. If it is just self's func get called, it doesn't make sense for the owener of the closure to keep reference to self after calling the func. So, the reference of self will be dropped by the owner, and there won't be cycle. In contrast, if there owner's property gets changed, it needs to keep referencing the self because the property will go along with owner until it is discarded
<img width="748" alt="image" src="https://user-images.githubusercontent.com/81428296/177029406-c8fc5979-ad86-41ca-be8b-40a3d4da75eb.png">
<img width="794" alt="image" src="https://user-images.githubusercontent.com/81428296/177029437-1993a874-5201-4f0f-aa92-1bd9e88fe0a7.png">
