## change of NavigationBar is global while change in navigationItem is local to each VC

Second half of this tutorial: https://guides.codepath.com/ios/Navigation-Controller

![image](https://user-images.githubusercontent.com/81428296/148630310-17811861-11b7-400f-8fff-74a68b7f3298.png)
## official doc: https://developer.apple.com/documentation/uikit/uinavigationcontroller/customizing_your_app_s_navigation_bar

## set the navBar appearance
### There are many ways
### set before navVC is initiated
![image](https://user-images.githubusercontent.com/81428296/155462917-93e2996a-6011-459d-ace4-84bdde382e02.png)
### or our example
![image](https://user-images.githubusercontent.com/81428296/155462999-62c41d83-ca34-4521-aea6-1b16a87bcdc0.png)

## set the navBarItem  --- very tricky -- update the navBarItem in the previous VC instead of the presenting VC
### excellent tutorial: https://www.google.com/search?q=how+to+custome+back+button+navigation+bar+item+swift&rlz=1C5CHFA_enUS977US977&sxsrf=APq-WBtPao_wdQp_5gGIlkJiMjzSYttbWg%3A1645666390794&ei=VuAWYonZL4ioqtsPtpKQ8AE&ved=0ahUKEwiJ3JCFmZf2AhUIlGoFHTYJBB4Q4dUDCA4&uact=5&oq=how+to+custome+back+button+navigation+bar+item+swift&gs_lcp=Cgdnd3Mtd2l6EAMyBQgAEKIEMgUIABCiBDIFCAAQogQyBQgAEKIEOgcIABBHELADOgQIIRAKSgQIQRgASgQIRhgAUJwSWO8yYP83aARwAXgAgAFjiAH6B5IBAjEzmAEAoAEByAEIwAEB&sclient=gws-wiz#kpvalbx=_7w4XYo_LDpusqtsPjd2gsAU18
![image](https://user-images.githubusercontent.com/81428296/155463404-b4450951-fd17-429f-a3bb-b1d15381b443.png)
![image](https://user-images.githubusercontent.com/81428296/155464269-bdf01bf7-047c-48d6-a8b5-a8122717e5dd.png)

![image](https://user-images.githubusercontent.com/81428296/155462673-78f095d4-03df-4a49-b669-d066f604c3d6.png)
![image](https://user-images.githubusercontent.com/81428296/155462744-b22437d5-bbfa-4d8d-ab9a-8c7927e56ba8.png)
