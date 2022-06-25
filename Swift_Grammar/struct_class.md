based on the tutorial: https://youtu.be/ObIxxHy8yY8
## pass by value vs pass by reference
## Analogy about struct and class
### creating and passing a class is like creating and sharing a google sheet. Whatever receivers do reflect on your "sheet". It is a good way to build communication, like delegate. Also, it is useful when you want use an shared instance everywhere instead copying or creating new ones everytime and everywhere. 
### In contrast, creating and share a struct is like creating and sharing a copy of file. Receivers can do whatever they want and it won't impact us. It is very useful when you just wanna pass the info and dont wanna callback, and don't wanna others change your files arbitarily. Noted is that struct does not support inheritance, due to which struct is light-weight, clean, having better performance relative to class. So, it is highly recommanded for organizing data and pass information.
### Another thing needs to be mentioned is the "let" definition/target of struct vs class are different. let of struct means the content of variable is constant while let of class means address of class is constant. That is why they are correpsondingly called passed by value and pass by reference.


![image](https://user-images.githubusercontent.com/81428296/148630391-c26d9453-7aa0-4e21-a0f1-936ddaee5854.png)

![image](https://user-images.githubusercontent.com/81428296/148630394-13993f38-0721-40e7-ae84-5b3449513a03.png)


Another tutorial:
![image](https://user-images.githubusercontent.com/81428296/149710076-26b26b71-b321-4a68-905f-e61e5f64e2c2.png)
![image](https://user-images.githubusercontent.com/81428296/149710169-99c9dea0-2abd-4f50-88d7-b1e4e413c605.png)
