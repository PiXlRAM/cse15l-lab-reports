## Lab 1 Blog Post

# Part 1

StringServer code:
![image](https://user-images.githubusercontent.com/35607410/215358740-b7fc687e-17c1-48e9-9be1-3b87da40af11.png)

lmaooo

First add-message:
![image](https://media.discordapp.net/attachments/1033930534004477983/1069377704060792982/image.png)
1. The handleRequest and start methods are called
2. The handleRequest method has one arg which is the URL, and has other fields such as str (contains string that is displayed), and parameters which contains the query of the URL. The start method has 2 args, port and handler. Port is the port on which the server runs, and handler establishes a connection with the port.
3. The URL field value changes because it has a specific query, which is to add Hello. The variable str value changes as well because it now has Hello appended to it. The values of parameters also changes because the message being appended to the string changes, and in this case it's Hello. The port field value doesn't change because it's still being run on port 4000, and handler doesn't change as well.

Second add-message:
![image](https://user-images.githubusercontent.com/35607410/215358791-049c6eb1-2db5-4874-9834-015f42f43588.png)
1. The handleRequest and start methods are called
2. The handleRequest method has one arg which is the URL, and has other fields such as str (contains string that is displayed), and parameters which contains the query of the URL. The start method has 2 args, port and handler. Port is the port on which the server runs, and handler establishes a connection with the port.
3. The URL field value changes because it has a specific query, which is to add How are you. The variable str value changes as well because it now has How are you appended to it. The values of parameters also changes because the message being appended to the string changes, and in this case it's How are you. The port field value doesn't change because it's still being run on port 4000, and handler doesn't change as well.

# Part 2

1. Failure inducing input for buggy code:
![image](https://user-images.githubusercontent.com/35607410/215367864-0bfdd764-4c43-4b33-ac90-ec683d416b17.png)
buggy code:
'''
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
'''

2. Input that doesn't create failure for same buggy code above:
![image](https://user-images.githubusercontent.com/35607410/215368203-3f10259f-e803-45ba-9496-973cf7c271b8.png)

3. JUnit tests for above 2 inputs:
![image](https://user-images.githubusercontent.com/35607410/215368350-125a3497-2067-4793-9739-c19ddda1cf0c.png)

4. The buggy vs fixed code:
'''
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
'''
  
'''
static void reverseInPlace(int[] arr) {
  int[] temp=new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    temp[i] = arr[arr.length - i - 1];
  }
  for(int i = 0; i < arr.length; i += 1){
    arr[i]=temp[i];
  }
    
}
'''

  The problem with reverseInPlace is that the first half copies the reverse of the second half, and then the second half repeats since it just copies the overwritten values in the first half. For example, {1,2,3} becomes {1,2,1}. The fixed code just creates a temporary new array so that no values get overwritten.

# Part 3
I learned how to create and run GitHub pages, which was something I didn't know how to do before. I also learned some basic markdown commands. Additionally, I understood how to use GitHub desktop to track and commit changes. 
