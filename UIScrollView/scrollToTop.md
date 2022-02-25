## dont forget to put it inside dispatchQueue (if you call a delegate of another VC to do task related to UI, the task will be run in background which will cause bugs. Hence, you need to put them in main thread.)
![image](https://user-images.githubusercontent.com/81428296/155663983-54cc275a-30b6-421f-9991-98920618ab31.png)

https://stackoverflow.com/questions/5542680/how-to-get-a-uitableview-to-go-to-the-top-of-page-on-reload
