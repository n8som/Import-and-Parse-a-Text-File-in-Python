# Import-and-Parse-a-Text-File-in-Python

<h2>Introduction</h2>

Security logs are often stored in text files. To analyze the security logs in these files, security analysts have to import and parse these files. Python has some functions that come in handy for these tasks, allowing analysts to efficiently access information from text files.

In this lab, I'll practice using functions and other syntax in Python to import and parse text files.

<h2>Scenario</h2>

In this lab, I'm working as a security analyst. I'm responsible for preparing a security log file for analysis and creating a text file with IP addresses that are allowed to access restricted information.

<h2>Task 1</h2>

In this task, I'll import a security log text file and store it as a string to prepare it for analysis.

In Python, a ```with``` statement is often used in file handling to open a file and then automatically close the file after reading it.

I'm given a variable named ```import_file``` that contains the name of the log file that I want to import. Start by writing the first line of the ```with``` statement in the following code cell. Use the open() function, setting the second parameter to ```"r"```. 

Note that running this code will produce an error because it will only contain the first line of the ```with``` statement; I'll complete this ```with``` statement in the task after this.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/fdce7506-f704-4339-8d89-593c7a61da48)

<h2>Task 2</h2>

Now, I'll use the ```.read()``` method to read the imported file, and I'll store the result in a variable named ```text```. Afterward, display the ```text``` and explore what it contains by running the cell.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/f9648bb3-0b57-439f-9abd-d929f19bfff7)

<h2>Task 3</h2>

The output in the previous step is one big string. In this task, I'll explore how I can split the string that contains the entire imported log file into a list of strings, one string per line.

Use the ```.split()``` method to perform this split and then display the result. 

Note that displaying ```.split()``` doesn’t change what is stored in the text variable. Variable reassignment would be necessary if I want to store the result after splitting.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/6134dfd1-e238-4f34-9637-958df3004602)

Before using the .split() method, the output is one long string containing all of the lines from the log file. After using the .split() method, the output is a list of strings; each string corresponds to a line from the log file.

<h2>Task 4</h2>

There is a missing entry in the log file. I'll need to account for that by appending it to the log file. I'm given the missing entry stored in a variable named ```missing_entry```.

Use the ```.write()``` method and the parameter ```"a"``` in the open() function.

After the portion of the code that writes to the file, another with statement uses the ```.read()``` method to read the updated file into the ```text``` variable and then display it.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/54b5078e-4312-4528-8bd2-4f98b4518d7b)

The additional entry was added to the end of the log file, so it appears in the last line of the output.

<h2>Task 5</h2>

The next task I'm responsible for is creating a text file. This text file should include a list of IP addresses that are allowed to access restricted information. Documenting this in a text file will help me communicate my findings to my security team.

Start by creating a variable named ```import_file``` that stores the name of the file, which should be ```"allow_list.txt"```.

I'm also given a variable named ip_addresses that stores a string containing the IP addresses that are allowed.

Run the code to display the two variables and explore what they contain.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/71f6447a-9ee3-4022-9474-cf33f1f5ddaa)

<h2>Task 6</h2>

My next goal is to create a ```with``` statement to write the IP addresses to the text file I created in the previous step.

I'll first open the file using the ```"w"``` parameter. Then, I'll write the IP addresses to the file.

Note that the code cell will contain a ```with``` statement that writes to a file but does not display information on the screen, so running it will not produce an output.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/ac9990a9-b90f-425f-b4a5-0b98558339c8)

<h2>Task 7</h2>

In this final step, I'll complete the code I've been writing up to this point. I'll add code to read the file containing IP addresses.

Complete a ```with``` statement that reads the text file and stores it in a new variable called ```text```.

Afterward, display the contents of ```text``` and run the cell to explore the result.

![image](https://github.com/n8som/Import-and-Parse-a-Text-File-in-Python/assets/110139109/feea3021-f2cf-4c8c-9011-301b1fccb7c1)

<h2>Conclusion</h2>

What are the key takeaways from this lab?

- Python has functions and syntax that help me import and parse text files.
  - The ```with``` statement allows me to efficiently handle files.
  - The ```open()``` function allows me to import or open a file. It takes in the name of the file as the first parameter and a string that indicates the purpose of opening the file as the second parameter.
    - Specify ```"r"``` as the second parameter if I'm opening the file for reading purposes.
    - Specify ```"a"``` as the second parameter if I'm opening the file for appending purposes.
    - Specify ```"w"``` as the second parameter if I'm opening the file for writing purposes.
  - The ```.read()``` method allows me to read in a file.
  - The ```.write()``` method allows me to append or write to a file.
- The ```.split()``` method in Python allows me to convert a string to a list.

