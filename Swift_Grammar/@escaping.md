## excellent article: https://www.donnywals.com/what-is-escaping-in-swift/

<img width="805" alt="image" src="https://user-images.githubusercontent.com/81428296/176233738-31cfdb9a-e8e3-4489-bbfb-a6dadbda56ea.png">

## good answer: https://stackoverflow.com/questions/39618803/swift-optional-escaping-closure-parameter

## 讲人话：
      Escaping Closure: An escaping closure is a closure that’s called after the function it was passed to returns. 
      In other words, it outlives the function it was passed to. 
      Non-escaping closure: A closure that’s called within the function it was passed into, i.e. before it returns.
<img width="665" alt="image" src="https://user-images.githubusercontent.com/81428296/210117662-94bc39fc-e733-4cf9-a84f-aa78ba824dd6.png">

## why optional function parameter is implicit @escaping -- it is enum type
<img width="693" alt="image" src="https://user-images.githubusercontent.com/81428296/176234724-3b771d45-19f8-41af-a08f-f96055f420ad.png">
<img width="993" alt="image" src="https://user-images.githubusercontent.com/81428296/176235490-a9a4b2c5-e1ef-4c87-a2a2-6d851426fd60.png">

link of above article: https://www.jessesquires.com/blog/2018/06/10/why-optional-swift-closures-are-escaping/
