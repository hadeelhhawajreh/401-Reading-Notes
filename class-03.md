
**What Is a File?**

is a contiguous set of bytes used to store data.
This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.
file systems are composed of three main parts:

+ Header: metadata about the contents of the file (file name, size, type, and so on)

+ Data: contents of the file as written by the creator or editor

+ End of file (EOF): special character that indicates the end of the file


*The file path: is a string that represents the location of a file. It’s broken up into three major parts:* 
Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

File Name: the actual name of the file

Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQhIO2KcqDNm1j30kntj11q_6btAZfF752AVQ&usqp=CAU)

```
file = open('dog_breeds.txt')
```
![img](https://image2.slideserve.com/5055646/opening-files-l.jpg)
```


reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```


**Python Exception Handling**

Error in Python can be of two types i.e. Syntax errors and Exceptions. Errors are the problems in a program due to which the program will stop the execution. On the other hand, exceptions are raised when some internal events occur which changes the normal flow of the program.

![img](https://files.realpython.com/media/try_except_else_finally.a7fac6c36c55.png)

![img](https://overiq.com/media/uploads/2017/09/28/exception-class-hierarchy.png)
