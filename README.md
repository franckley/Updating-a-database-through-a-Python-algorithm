# Updating-a-through-a-Python-algorithm

## Project description
MY organisation manages access to restricted content using an allow list of IP addresses. The file "`allow_list.txt`" identifies these IP addresses. The addresses that should no longer have access to this content. I created an algorithm to automate updating the "`allow_list.txt`" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this restricted content. I created an algorithm to autoamte updating the "`allow_list.txt`" file and remove these IP addresses that should no longer have access.

## Open the file that contains the allow list
At first the algorithm, I opened the `allow_list.txt`file. First, I assigned this file name as a string to the import_file variable:
![image](https://github.com/user-attachments/assets/0fa27a31-991e-4380-85c2-f006a0b922de)

Then, I utilize a `with` statement to open the file:
![image](https://github.com/user-attachments/assets/0b803a47-c5b1-4e90-b0f6-efbf0fb810ac)

In my algorithm, the use of a `with` statement with the `.open()` function in read more serve to open the allow list file for the purpose of reading it. The purpose of opening the file is to allow me to access the IP addresses stored in the purpose lf reading it. The reason for opening the file is to allow me to access the content aka the IP addresses stored in the allow list file. The `with` keyword will help manage the resources by closing the file after exiting with the `with` statement. In the code `with open(import_fiel, "r") as file:` the open() function has two parameters. The first identifies teh file to import, and thenn the second indicates what I want to do with the file. In this case, `"r"` indicates that I want to read it. The code also uses the `as` keyword to assign a var named `file`: `file` stores the output of the `.open()` function while I work within the `with` statement.

## Read the file content
For me to read the file content I used the .read() methode to convert it into the string.
![image](https://github.com/user-attachments/assets/d1d462fe-629d-459a-8e8b-f830d9fd60ba)

When using an `.open()` function that includes the argument "`r`" for read method converts the file into a string and allows me to read it. I applied the `.read()` method to the file variable next to the `with` statement. Then, I assigned the string output of this method to the variable `ip_addresses`.

In short, this code reads the contents of the "`allow_list.txt`" file into a string format that allows 
