# Dictionary is not directly prvodied by core data
## you might create custom data type like dictionary [String:Int] in transformable

# However, more reasonale solution is oragnize data as entity (of course, it must contain its key info itself) in core data, and we can oranize them into dictionary once we fetched them from core data
# namely, stored these entity as the values of the dictionary, this ditionary is not saved in core data

## for example, pattern master
## dictionary information including keys and values are saved in CMInch entity, and these entities are associated a certain dictionary of a model. Once we fectch them from core data, we can then re-organize them in dictionary

## similary, in fearlessTherapeutics,
## dictionary information (keys and values) are both stored in the entity of practices. All these practices entity are associated with the user and further re-organized as dictionary (given it contains both key and value info)

![image](https://user-images.githubusercontent.com/81428296/158006720-aa3a8d2c-ed31-4d39-be27-a8cc00227d42.png)
