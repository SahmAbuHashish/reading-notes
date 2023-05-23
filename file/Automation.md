# Reading Questions


### How can you use regular expressions in Python to search for specific patterns in a string, and what is the primary library to work with them?

- In Python, you can use regular expressions to search for specific patterns in strings using the re library. 
- The re library provides functions and methods to work with regular expressions. You can define a pattern using special characters and syntax, and then use functions like re.search() or re.findall() to find matches in the given string. Regular expressions enable you to search for patterns like specific text sequences, character classes, repetition, alternation, and more.


---

### What is the purpose of the shutil library in Python, and provide an example of a common use case for file or directory management with this library?

- The shutil (shell utilities) library in Python provides a high-level interface for file and directory operations. It offers various functions to manipulate files and directories, such as:
copying, moving, renaming, archiving, and deleting. 
- The primary purpose of the shutil library is to simplify common file and directory management tasks in Python.
- A common use case for the shutil library is copying files or directories. 

>>>import shutil
>>>shutil.copy('source/file.txt', 'destination/file.txt')
>>>shutil.copytree('source/directory', 'destination/directory')

---

### Explain one automation idea from the assigned material and describe how it can be implemented using Python’s regular expressions and shutil libraries.

One automation idea from the assigned material is to create a script that automatically organizes files in a directory based on their file extensions. 

     import os
     import re
     import shutil
     
     source_dir = 'source_directory'
     
     # Get all files in the source directory
     files = os.listdir(source_dir)
     
     for file in files:
         # Extract the file extension using regular expressions
         extension = re.search(r'\.(\w+)$', file)
     
         if extension:
             extension = extension.group(1)
             destination_dir = os.path.join(source_dir, extension)
    
             if not os.path.exists(destination_dir):
              os.mkdir(destination_dir)
     
             # Move the file to the destination directory
             shutil.move(os.path.join(source_dir, file), os.path.join(destination_dir, file))
