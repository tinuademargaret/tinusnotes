## Subtle Immutability 

"Python has only 3 mutable data structres; lists sets and dictionaries while tuples and strings are immutable." A rhyme for every beginner python programmer, but is that all that there is to mutability and immutability in python?

Everything in python is an object and while an object's type is unchangeable, the value of some objects can change(mutable objects) and the other objects have their values unchangeable(immutable objects). The value of some objects are references to other objects. These objects such as lists, dictionaries, tuples etc are called containers. When we make use of containers, we mostly refer to the values of the container as the values of the objects that they reference. For example while iterating through a list object, it's the value of the objects  contained in the list that we access and not references to the objects. But when we talk about mutability, what we refer to are the identities of the contained objects in a container. You can think of the identity of an object as something like it's memory location. So if an immutable container such as a tuple contains a reference to a mutable object, its value changes if that mutable object is changed. This does not make a tuple mutable since the references to the objects themselves that it contains does not change. 
One reason this is not immediately obvious is that we tend to attach the attribute of immutability to data structures, when it is infact an attribute of objects and data structres are only objects in python. 

Integers, floats and even functions can also have this attribute. An Integer is immutable for example. If you store integer values in a tuple, then the values cannot be changed since integer objects are also immutable. But what if you store list objects in a tuple and the values in the list changes?

```
>>> a = [1, 2]
>>> b = [3, 4]
>>> c = (a, b)
>>> print(c)
([1, 2], [3, 4])
>>> a.pop()
2
>>> print(c)
([1], [3,4])
```
Although tuples are immutable but the list object stored in the tuple is mutable, hence if we change the values in the list the values in the tuples would change as well. Immutability can be subtle, just because an object is immutable does not mean that it's values cannot change.
