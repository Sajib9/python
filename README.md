# python
x = 5
y = 'abc'
print(x + y)
#Not Possible add number with string Instead ,print(x,y)

# global key word inside function allow use varible out side of the function
  def myFun():
    global x
    x = 5
    print("Number:", x)
myFun()
print("new:",x) 
# Data type
  dict looks like object, x = {'name':'sajib'} key , value pair.
   ->set without key , value pair x = {"apple", "banana"},<br>
   ->list looks like array, myList = ['apple','banana'].<br>
   ->List-From Python's perspective, lists are defined as objects with the data type 'list'.<br>
   ->We can access range of indexes from list ,ex- myList = ['a','b','c','d'] print(mylist[1:3]) result ['b','c'] index 3 not included.<br>
   ->append() method add item end of list, myList.append('e').<br>
   ->insert() method add item into specific index, myList.insert(5,'e').<br>
   ->extend() To append elements from another list to the current list, this methode allow to add any iterable like tuple,set.<br>
   ->remove() method removes the specified item.<br>
   ->list ordered & changable.
   
# for loop
  ->for loops cannot be empty, but if you for some reason have a for loop with no content, put in the pass statement to avoid getting an error,<br>
  for x in [0, 1, 2]: <br>
    pass <br>
  # having an empty for loop like this, would raise an error without the pass statement.
    ->newlist = [expression for item in iterable if condition == True]<br>
  # tuple
    ->orded but unchangable<br>
    mytuple = ("apple", "banana", "cherry") <br>
    ->Tuple items are indexed
    
  # set 
    ->A set is a collection which is unordered, unchangeable*, and unindexed <br>
    ->do not allow duplicate values
    
    
# array
  ->Python does not have built-in support for Arrays <br>
   ->to work with arrays in Python you will have to import a library, like the NumPy library "import numpy as np"
   ->Join two arrays ,np.concatenate((arr1, arr2)) ,arr1 = np.array([1, 2, 3]) ,arr2 = np.array([4, 5, 6]).
   ->We use array_split() for splitting arrays
