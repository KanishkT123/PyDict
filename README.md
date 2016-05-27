# PyDict
A Simple Python Dictionary

Works from the Unix command line:
Run chmod a+x
Run with pydict [function] [arg1] [arg2]
Eg: 
pydict add "Hello" "World"

Outputs to Command Line stdout:
Eg:
pydict look "Hello"
>> Hello
>> World

Stores data in dictionary file. If file doesn't exist, creates is. Dictionary file should not be deleted as it is a running account of all the data.


Dependencies:
ast, sys
