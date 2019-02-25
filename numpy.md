NumPy is a Python package. It stands for 'Numerical Python'. 
It is a library consisting of multidimensional array objects and a collection of routines for processing of array.


**Using NumPy, a developer can perform the following operations −**
Mathematical and logical operations on arrays.
Fourier transforms and routines for shape manipulation.
Operations related to linear algebra. NumPy has in-built functions for linear algebra and random number generation.


NumPy supports a much greater variety of numerical types than Python does. The following table shows different scalar data types defined in NumPy.
Sr.No.	Data Types & Description
1	
bool_

Boolean (True or False) stored as a byte

2	
int_

Default integer type (same as C long; normally either int64 or int32)

3	
intc

Identical to C int (normally int32 or int64)

4	
intp

Integer used for indexing (same as C ssize_t; normally either int32 or int64)

5	
int8

Byte (-128 to 127)

6	
int16

Integer (-32768 to 32767)

7	
int32

Integer (-2147483648 to 2147483647)

8	
int64

Integer (-9223372036854775808 to 9223372036854775807)

9	
uint8

Unsigned integer (0 to 255)

10	
uint16

Unsigned integer (0 to 65535)

11	
uint32

Unsigned integer (0 to 4294967295)

12	
uint64

Unsigned integer (0 to 18446744073709551615)

13	
float_

Shorthand for float64

14	
float16

Half precision float: sign bit, 5 bits exponent, 10 bits mantissa

15	
float32

Single precision float: sign bit, 8 bits exponent, 23 bits mantissa

16	
float64

Double precision float: sign bit, 11 bits exponent, 52 bits mantissa

17	
complex_

Shorthand for complex128

18	
complex64

Complex number, represented by two 32-bit floats (real and imaginary components)

19	
complex128

Complex number, represented by two 64-bit floats (real and imaginary components)

NumPy numerical types are instances of dtype (data-type) objects, each having unique characteristics. 
The dtypes are available as np.bool_, np.float32, etc.

**Examples**

import numpy as np 
dt = np.dtype(np.int32) 
print dt

#int8, int16, int32, int64 can be replaced by equivalent string 'i1', 'i2','i4', etc. 
import numpy as np 
dt = np.dtype('i4')
print dt

import numpy as np 
dt = np.dtype([('age',np.int8)]) 
print dt 


#now apply it to ndarray object 
import numpy as np 
dt = np.dtype([('age',np.int8)]) 
a = np.array([(10,),(20,),(30,)], dtype = dt) 
print a

#file name can be used to access content of age column 
import numpy as np 
dt = np.dtype([('age',np.int8)]) 
a = np.array([(10,),(20,),(30,)], dtype = dt) 
print a['age']

import numpy as np 
student = np.dtype([('name','S20'), ('age', 'i1'), ('marks', 'f4')]) 
print student

import numpy as np 
student = np.dtype([('name','S20'), ('age', 'i1'), ('marks', 'f4')]) 
a = np.array([('abc', 21, 50),('xyz', 18, 75)], dtype = student) 
print a

**Each built-in data type has a character code that uniquely identifies it.**
'b' − boolean
'i' − (signed) integer
'u' − unsigned integer
'f' − floating-point
'c' − complex-floating point
'm' − timedelta
'M' − datetime
'O' − (Python) objects
'S', 'a' − (byte-)string
'U' − Unicode
'V' − raw data (void)

**Input arrays for performing arithmetic operations such as add(), subtract(), multiply(), and divide() must be either of the same shape or should conform to array broadcasting rules.**
```
import numpy as np 
a = np.arange(9, dtype = np.float_).reshape(3,3) 

print 'First array:' 
print a 
print '\n'  

print 'Second array:' 
b = np.array([10,10,10]) 
print b 
print '\n'  

print 'Add the two arrays:' 
print np.add(a,b) 
print '\n'  

print 'Subtract the two arrays:' 
print np.subtract(a,b) 
print '\n'  

print 'Multiply the two arrays:' 
print np.multiply(a,b) 
print '\n'  

print 'Divide the two arrays:' 
print np.divide(a,b)
```

**Matplotlib**
```
import numpy as np 
from matplotlib import pyplot as plt 

x = np.arange(1,11) 
y = 2 * x + 5 
plt.title("Matplotlib demo") 
plt.xlabel("x axis caption") 
plt.ylabel("y axis caption") 
plt.plot(x,y) 
plt.show()
```
```
import numpy as np 
from matplotlib import pyplot as plt 

x = np.arange(1,11) 
y = 2 * x + 5 
plt.title("Matplotlib demo") 
plt.xlabel("x axis caption") 
plt.ylabel("y axis caption") 
plt.plot(x,y,"ob") 
plt.show() 
```

```
import numpy as np 
import matplotlib.pyplot as plt  

# Compute the x and y coordinates for points on a sine curve 
x = np.arange(0, 3 * np.pi, 0.1) 
y = np.sin(x) 
plt.title("sine wave form") 

# Plot the points using matplotlib 
plt.plot(x, y) 
plt.show() 
```

```
from matplotlib import pyplot as plt 
x = [5,8,10] 
y = [12,16,6]  

x2 = [6,9,11] 
y2 = [6,15,7] 
plt.bar(x, y, align = 'center') 
plt.bar(x2, y2, color = 'g', align = 'center') 
plt.title('Bar graph') 
plt.ylabel('Y axis') 
plt.xlabel('X axis')  

plt.show()
```

**The ndarray objects can be saved to and loaded from the disk files. The IO functions available are −**

load() and save() functions handle /numPy binary files (with npy extension)

loadtxt() and savetxt() functions handle normal text files

NumPy introduces a simple file format for ndarray objects. This .npy file stores data, shape, dtype and other information required to reconstruct the ndarray in a disk file such that the array is correctly retrieved even if the file is on another machine with different architecture.

numpy.save()
The numpy.save() file stores the input array in a disk file with npy extension.

import numpy as np 
a = np.array([1,2,3,4,5]) 
np.save('outfile',a)
To reconstruct array from outfile.npy, use load() function.

import numpy as np 
b = np.load('outfile.npy') 
print b 
It will produce the following output −

array([1, 2, 3, 4, 5])
The save() and load() functions accept an additional Boolean parameter allow_pickles. A pickle in Python is used to serialize and de-serialize objects before saving to or reading from a disk file.

savetxt()
The storage and retrieval of array data in simple text file format is done with savetxt() and loadtxt() functions.

Example
import numpy as np 

a = np.array([1,2,3,4,5]) 
np.savetxt('out.txt',a) 
b = np.loadtxt('out.txt') 
print b 
It will produce the following output −

[ 1.  2.  3.  4.  5.] 
The savetxt() and loadtxt() functions accept additional optional parameters such as header, footer, and delimiter.
