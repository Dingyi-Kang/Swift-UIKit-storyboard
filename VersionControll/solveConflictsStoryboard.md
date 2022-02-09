## First, revert the push causing conflicts in storyboard
![image](https://user-images.githubusercontent.com/81428296/153118466-180d9f7a-2d12-492d-9042-fcc8dedd7243.png)

## Then, on other side, make a branch
![image](https://user-images.githubusercontent.com/81428296/153119923-80c32dbe-0165-421f-8c0e-1e0b29456eb1.png)

## Your head is on the branch now
![image](https://user-images.githubusercontent.com/81428296/153119984-88f63e4c-e453-45c2-91b3-6130d70f66de.png)

## Then delete the main branch
![image](https://user-images.githubusercontent.com/81428296/153120174-5aefddce-3bba-4307-8e96-c6349ca5da1d.png)

## Usually, you cannot solve the conflicts of storyboard in Xcode because it will show error (file cannot be opened) when trying to displaying the storyboard file
## Hence, you need to use terminal command to use git.
![image](https://user-images.githubusercontent.com/81428296/153120450-f05c7475-524d-41b8-a0ed-a07ddb374c5f.png)
## You need to open the storyboard file in editor, manually solve the conflicts, and manually mark the sovled file as resolution
![image](https://user-images.githubusercontent.com/81428296/153120580-f6b8a26c-169b-45e5-9ba2-929c58286ef7.png)

## the <<<<< means beginning of the conflicts, >>>>>> means end of the conflicts, ===== is seperator
<img width="693" alt="Screen Shot 2022-02-08 at 9 01 34 PM" src="https://user-images.githubusercontent.com/81428296/153120809-db520085-21c7-41f9-bbfd-406a2471eb84.png">

## after manually solving the conflicts, you can mark resolution
![image](https://user-images.githubusercontent.com/81428296/153121005-6f484b8c-05be-4378-a5ce-d04894638b1e.png)

## Then commit 
![image](https://user-images.githubusercontent.com/81428296/153121119-303ffd1f-e740-44af-9919-b97faba79ec9.png)

## Then, you can push in either terminal or Xcode
