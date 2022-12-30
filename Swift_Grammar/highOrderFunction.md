### Link of the tutorial: https://www.codingem.com/swift-function-as-parameter/

## 1. pass function as parameter
For instance, this function accepts two regular parameters and a function parameter:

        func operate(x: Double, y: Double, function: (Double, Double) -> Double) {
          return function(x, y)
        }
        
<img width="665" alt="image" src="https://user-images.githubusercontent.com/81428296/210117143-a79f8d14-9e1e-4217-8c3d-f6ec5b112f82.png">


## 2. closure
<img width="647" alt="image" src="https://user-images.githubusercontent.com/81428296/210117194-6fedb777-ba58-4c5b-817a-8a658693a996.png">
Let’s continue with calculate() function from the previous example:

        func calculate(_ x: Double, _ y: Double, _ function: (Double, Double) -> Double) {
            print(function(x,y))
        }
<img width="649" alt="image" src="https://user-images.githubusercontent.com/81428296/210117256-cb5bc6fa-d572-4db2-b273-2648ecce468b.png">

## 3. how to simplify closure
<img width="661" alt="image" src="https://user-images.githubusercontent.com/81428296/210117300-2db31215-d569-4299-90ff-5ace3529dcb7.png">
<img width="654" alt="image" src="https://user-images.githubusercontent.com/81428296/210117321-72d53396-122c-457c-8a6d-ccc54e4cc55a.png">
<img width="664" alt="image" src="https://user-images.githubusercontent.com/81428296/210117327-2abf3e15-cdc5-4dce-9c2d-af80f8b676d0.png">
<img width="650" alt="image" src="https://user-images.githubusercontent.com/81428296/210117346-c5701ac0-307d-4bd7-ae02-3361ff8cd56a.png">
### another example of using closure
<img width="625" alt="image" src="https://user-images.githubusercontent.com/81428296/210117395-fb0bb8c2-972a-4a6c-be44-bfd889ad786b.png">
