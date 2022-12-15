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
   
# for loop
  ->for loops cannot be empty, but if you for some reason have a for loop with no content, put in the pass statement to avoid getting an error,<br>
  for x in [0, 1, 2]: <br>
    pass <br>
  # having an empty for loop like this, would raise an error without the pass statement.
    ->newlist = [expression for item in iterable if condition == True]<br>
  # mytuple = ("apple", "banana", "cherry")  <br>
