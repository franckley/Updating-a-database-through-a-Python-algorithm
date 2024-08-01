# Updating-a-through-a-Python-algorithm

## Project description
MY organisation manages access to restricted content using an allow list of IP addresses. The file "`allow_list.txt`" identifies these IP addresses. The addresses that should no longer have access to this content. I created an algorithm to automate updating the "`allow_list.txt`" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this restricted content. I created an algorithm to autoamte updating the "`allow_list.txt`" file and remove these IP addresses that should no longer have access.

## Open the file that contains the allow list
At first the algorithm, I opened the `allow_list.txt`file. First, I assigned this file name as a string to the import_file variable:

![image](https://github.com/user-attachments/assets/0fa27a31-991e-4380-85c2-f006a0b922de)

Then, I utilize a `with` statement to open the file:

![image](https://github.com/user-attachments/assets/0b803a47-c5b1-4e90-b0f6-efbf0fb810ac)

In my algorithm, the use of a `with` statement with the `.open()` function in read more serve to open the allow list file for the purpose of reading it. The purpose of opening the file is to allow me to access the IP addresses stored in the purpose lf reading it. The reason for opening the file is to allow me to access the content aka the IP addresses stored in the allow list file. The `with` keyword will help manage the resources by closing the file after exiting with the `with` statement. In the code `with open(import_fiel, "r") as file:` the open() function has two p  arameters. The first identifies teh file to import, and thenn the second indicates what I want to do with the file. In this case, `"r"` indicates that I want to read it. The code also uses the `as` keyword to assign a var named `file`: `file` stores the output of the `.open()` function while I work within the `with` statement.

## Read the file content
For me to read the file content I used the .read() methode to convert it into the string.
![image](https://github.com/user-attachments/assets/d1d462fe-629d-459a-8e8b-f830d9fd60ba)

When using an `.open()` function that includes the argument "`r`" for read method converts the file into a string and allows me to read it. I applied the `.read()` method to the file variable next to the `with` statement. Then, I assigned the string output of this method to the variable `ip_addresses`.

In short, this code reads the contents of the "`allow_list.txt`" file into a string format thatpermits me later to use the string to organize and extract data in my PYthon program.

## Convert the string into a list
In order to remove individual IP addresses from the allow list, I needed it to be first in list format. Therefored, I next used the `.split()` method to convert the `ip_addresses` string into a list:

![image](https://github.com/user-attachments/assets/ff2fbaea-48a0-4141-a5b9-415fc27efe74)

The `.split()` function is called by appending it to a string variable. It works by converting the contents of a list . The purpose of splitting `ip)addresses` into a list format is to make it easier to remove IP addresses from the allow list. By default, the `.split()` function splits the text by whitespace into list elements. In this algorithm, the `.split()` function takes the data stored in the variable `ip_addresses`, which is a string of  IP addresses that are separated by a whitespac, and  it converts this string into a list of IP addreseses. To store this list, I reassigned it back to the variable `ip_addresses`.

## Iterate through the remove list
One of the most important part of my algorithm involves iterating through the IP addresses that are elements in the `remove_list`. To do so, I added a `for` loop:

![image](https://github.com/user-attachments/assets/fc25a3c3-879c-4d3d-8cc7-0dd9b4ee913e)

The `for` loop in Python repeats code for a specified sequence. The overall purpose of the `for` loop in a Python algorithm like this is to apply specific code statements to all elements in a sequence. The `for` keyword starts the `for` loop. It is followed by the loop variable `element` and the keyword `in`. The keyword `in` indicates to iterate through the sequence `ip_addresses` and assign each value to the loop variable `element`.

## Remove IP addresses that are on the remove list

A algorithm requires the removal of any IP address from the allow list, `ip_addresses`, that is also contained in the variable `remove_list`. Because there were not any duplicates in `ip_addresses`, I was able to use the following code to do the following:
![image](https://github.com/user-attachments/assets/5388cb3b-911f-4098-b958-ef0b2ec6e9a2)

First, within my `for` loop, I created a conditional that evaluated whether or not the loop variable `element` was found in the `ip_addresses` list. I did this because applying `.remove()` to elements that were not found in `ip_addresses`.
d3d3d3d
