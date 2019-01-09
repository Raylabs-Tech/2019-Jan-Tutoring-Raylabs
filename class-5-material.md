## Control flow

Need to vary computation steps as values change

Control flow — determines order in which

statements are executed

#Conditional execution
Repeated execution — loops
Function definitions

#Conditional execution
```
if m%n != 0:
 (m,n) = (n,m%n)
``` 

Second statement is executed only if the condition
m%n != 0 is True

Indentation demarcates body of if — must be uniform
if condition:
 statement_1 # Execute conditionally
 statement_2 # Execute conditionally
statement_3 # Execute unconditionally
Alternative execution
```
if m%n != 0:
 (m,n) = (n,m%n)
else:
 gcd = n
```

else: is optional

Shortcuts for conditions

Numeric value 0 is treated as False

Empty sequence ""
, [] is treated as False

Everything else is True
```
if m%n:
 (m,n) = (n,m%n)
else:
 gcd = n
```

Multiway branching, elif:
```
if x == 1:
 y = f1(x)
else:
 if x == 2:
 y = f2(x)
 else:
 if x == 3:
 y = f3(x)
 else:
 y = f4(x)
if x == 1:
 y = f1(x)
elif x == 2:
 y = f2(x)
elif x == 3:
 y = f3(x)
else:
 y = f4(x)
``` 

## Loops: repeated actions

Repeat something a fixed number of times

for i in [1,2,3,4]:
 y = y*i
 z = z+1

Again, indentation to mark body of loop

Repeating n times

Often we want to do something exactly n times

for i in [1,2,..,n]:
 . . .
range(0,n) generates sequence 0,1,…,n-1

for i in range(0,n):
 . . .

range(i,j) generates sequence i,i+1,…,j-1
