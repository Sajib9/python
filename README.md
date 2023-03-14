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
   
 # First class function
    .python function are object
    .can store function in variable
    .pass function as argument in another function
    .can return the fron another function
   
  # Functions can be passed as arguments to other functions:
        def shout(text):
          return text.upper()

        def yell(text):
          return text.lower()

        def greet(func):
          print('I am greet');
          greetings = func("I am Higer order function")
          print(greetings)

        greet(shout)
        greet(yell)
     
  # Functions can return another function:
    def add(x):
      temp = 10
      print(x)
      def adder(y):
        print('value of x in inner function:',x)
        return x+y+temp
      return adder
    x = add(10)
    print(x) // return reference
    print(x(15))
  # What is Python *args ?
     . With *args, any number of extra arguments can be tacked on to your current formal parameters.
     . we want to make a multiply function that takes any number of arguments and is able to multiply them all together. It can be done using *args.
     . Using the * the variable that we associate with the * becomes an iterable meaning you can do things like iterate over it, run some higher-order functions such           as map and filter, etc.
     
     def non_key_arg(*value):
        for data in value:
        print(data)

     non_key_arg("sajib","moin","mahmud")
     
     //another exmple
     def non_key_arg(value1,*value):
        print(value1)
        for data in value:
          print(data)

      non_key_arg("sajib","moin","mahmud")
   
  # What is Python **kwargs?
    .kwargs as being a dictionary that maps each keyword to the value that we pass alongside it.
    .we can iterate over them
    
    def non_key_arg(value1,**kwarg):
      print(value1)
      for key,data in kwarg.items():
          print(key,data)

    non_key_arg('Hello',name="sajib",age=30)
  # *args receives arguments as a tuple.
  **kwargs receives arguments as a dictionary.
  
  # yeild vs return :
    *Return sends a specified value back to its caller whereas Yield can produce a sequence of values. We should use yield when we want to iterate over a sequence, but         don’t want to store the entire sequence in memory
   # Enumerate() :
      . Enumerate() method adds a counter to an iterable and returns it in a form of enumerating object.
      enumerate(iterable, start=0)
   # Generator():
      .A generator function is defined just like a normal function, but whenever it needs to generate a value, it does so with the yield keyword rather than return. If the body of a def contains yield, the function automatically becomes a generator function. Generator functions return a generator object
      def sumTwoNum():#generator function
            i= 5
            while True:
                yield i
                i += 2

        for num in sumTwoNum():
            if num > 30:
                break;
            print(num)
            
        def fibonacci(limit):
              a,b = 0,1

              while a < limit:
                  yield a
                  a,b = b, a + b

          for value in fibonacci(20):
              print (value)
