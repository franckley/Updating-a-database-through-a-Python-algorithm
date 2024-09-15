# Updating-through-a-Python-algorithm

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

## Update the file with the revised list of IP addresseses

As a final step in my algorithm, I needed to update the allow list file with the revised list of IP addresses. To do it, I needed first to convert the list back into a string. So the use of the `.join()` method for this:

![image](https://github.com/user-attachments/assets/4539d42b-8445-4cc4-9c9c-742356150109)

The `.join()` method combines all items in an iterable into a string format. The `.join()` method is applied to a string containing characters that will separate the elements in the iterable once joined into a string. IN this algorithm, I used the `.join()` method to create a string from the list `ip_addresses` so that I could pass it in as an argument to the .write() method when writing to the file "`allow_list.txt`". I used the string ("`\n`") as the separator to instruct Python to place each element on a new line.

Then, I used another `with` statement and the `.write()` method to update the file:

![image](https://github.com/user-attachments/assets/12292894-1d2b-49c4-b6a5-f2b419afb9a1)

This time, I used a second argument of "`w`" with the `open()` function in my with statement. This argument indicates that I want to open a file to write over its contents. When using this argument "`w`", I can call the `.write()` function in the body of the `with` statement. The `.write()` function writes string data to a specified file and replacses any existing file content.

In this case I wanted to write the updated allow list as a string to the file "`allow_list.txt`". This way, the restricted content will no longer be accessible to any IP addressews that were removed from the allow list. To rewrite the file, I appended the `.write()` function to the file object `file` that I identified in the with statement. I passed in the `ip_addresses` variable as the argument to specify that the contents of the file specified in the with statement should be replaced with the data in this variable.

## Summary 

The purpose behind the creation of this algorithm is to remove IP addresses identified in a `remove_list` variable from the "`allow_list`" file of approved IP addresses. This algorithm involved opening the file, converting it to a string for it to be read, and then converting this string to a list stored in the variable `ip_addresses`. I then iterated through the ip_addresses list. If it was, I applied the `.remove()` method to it to remove the element form `ip_addresses`. After this, I used the `.join()` method to it to convert the `ip_address` back into a string so that I could write over the contents of the "`allow_list.txt `" file with the revised list of IP addresses.
