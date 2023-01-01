## First class citizens.

In programming languages, first class citizens are entities that have the abiltiy to operate like all other entities. Generally first class 
citizens have the following attributes defined by [Robin Popplestone](https://en.wikipedia.org/wiki/Robin_Popplestone):
- [ ] They can be actual parameters of functions
- [ ] They can be returned as a result of functions
- [ ] They can be subject of assignment statements
- [ ] They can be tested for equality
 
Entities that are first class citizens differ from one programming language to another. In python every object that can be named can be classified as a 
first class citizens. This means that *functions*, *classes*, *methods*, *modules* and virtually all data types have the attributes described above.

This concept is important because it allows programmers to write code in a way that is more modular and reusable. Let's look at some illustrations below.

- A function that takes another function as aparameter and returns a function as a result.

```
def compose(f, g):
    # A nested function that applies f and g to a given argument
    def h(x):
        return f(g(x))
    # Return the nested function
    return h

# Define some simple functions


def square(x):
    return x ** 2


def inc(x):
    return x + 1


# Compose the functions and assign the result to a variable
f = compose(square, inc)

# Test the composed function
print(f(5))  # 36
print(f(10))  # 121

```

It is easy to see that this concept is the reason why the decrorator design pattern exists. When making use of this concept it is important to make sure your code is readable.
