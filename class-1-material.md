The following identifiers are used as reserved words, or keywords of the language, and cannot be used as ordinary identifiers. 
They must be typed exactly as written here:

False      class      finally    is         return
None       continue   for        lambda     try
True       def        from       nonlocal   while
and        del        global     not        with
as         elif       if         or         yield
assert     else       import     pass
break      except     in         raise


In Python we don’t specify what kind of data we are going to put in a variable. So you can directly write a = 1 and a will become an integer datatype. 
If you write a = 1.0 a will become of floating type. Here is a small program to add two given numbers

```

>>> a = 13
>>> b = 23
>>> a + b
36

```

To print a string in Python we simply do the following:

```

print("Hello, It's RayLabs Technologies")

```

## Reading input from the Keyboard

In Python we use input function to do input. input(“String to show”) , this will return a string as output. Let us write a program to read a number from the keyboard and check if it is less than 100, the same program we did in the class today.

```
number = int(input("Enter an integer: "))
if number < 100:
    print("Your number is smaller than 100")
else:
    print("Your number is greater than 100")
```

