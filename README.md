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
   set without key , value pair x = {"apple", "banana"}
