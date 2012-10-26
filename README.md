=BDL Python=

Typesafe Python - sometimes a little Bondage and Discipline is fun.

bdl is the begining of what I hope will become a collection of
decorators and a rich domain specific lanugage to describe the
acceptable types for parameters and return values.  Right now its
usage is limited to a single @returns dectorator that confirms the
return type of a function - its not very flexiable.

Example usage:
````
>>> from bdl import returns
>>> @returns(int)
... def a():
...     return 1
... 
>>> a()
1
>>> @returns(str)
... def b():
...     return 1
... 
>>> b()
TypeError: Expected a return value of <type 'str'>, returned a <type 'int'> instead
````