n Python, `enumerate()` is a built-in function that adds a counter to an iterable (such as a list, tuple, or string) and returns it as an `enumerate` object, which can then be used in loops. It provides both the index and the corresponding element from the iterable, making it easier to keep track of positions when iterating through a collection.

fruits = ['apple', 'banana', 'cherry']

# Using enumerate to get index and value
for index, fruit in enumerate(fruits):
    print(index, fruit)
