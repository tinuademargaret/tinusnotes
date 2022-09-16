## Mutability and Immutability 

Everything in python is an object and an object's type is unchangeable
The value of some objects can change -> mutable objects
objects with unchangeable values -> immutable objects
It's like a rhyme for every python programmer that python has only 3 mutable data structres; Lists sets and dictionaries while tuples and strings are immutable
Some objects contain references to other objects, these objects such as lists, dictionaries , tuples etc are called containers. The references are a part of the container object's values. We mostly refer to the values of the container as the values of the objects that it holds for example when performing an itereation on a list, it's the values of the objects of the list that we deal with. But when we talk about mutability we are referring to the identities of the contained objects. So if an immutable container such as a tuple contains a reference to a mutable object, its value changes if that mutable object is changed. This does not make a tuple mutable since the objects themselves that it contains do not change. 
One reason this is not immediately ovious is that we tend to attach the attribute of immutability to data structres, when it is infact an attribute of objects and data structres are only objects in python. 
Hence Integer, float , functions can also have this attribute. An Integer is immutable for example. so if you store integer values in a tuple, then the values cannot be changed since integer objects are also immutable. But what if you store list objects in a tuple?
<code snippet here>
 Another interesting behaviour is seen with classes. 
  
