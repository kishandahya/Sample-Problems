# aporeto
This repository contains three sample problems I completed for my application to be an intern at Aporeto.

Problem 1: 
This is a shell program that creates a file that has all 50 states listed in it. Each state is on its own line and is sorted in alphabetical order. The name of the file is the first argument the user input.

options:
	-h or —-help  will tell you what the program does and how to use it
	—-no-prompt   this option will overwrite the filename you put without alerting you if it exists or not
	—verbose      this option will print out extra documentation for when the file is removed, created and already exists\n

The usage format is 
sh test1.sh [--help|-h]
sh test1.sh <filename> [--no-prompt] [--verbose]

A sample for how it may look in terminal is:

	sh problem1.sh file.txt --no-prompt --verbose

Problem notes: I account for users wanting to put in only two arguments where the second is the verbose option. Overall, I tested 14 test cases, which I could provide if needed, and my program passed all of them. It was fun learning about Bash shell scripting. For this one, the first input is automatically the file name, so you don't have to type --create-file= before typing it. 


Problem 2:

This program takes in a file name and content of that file into another file. It only takes unique instances though. Thus, the output file will not have any duplicate values.
The program can be used with this general structure

options:
    uniquify [--help|-h]
    uniquify --file=<filename> --output=<output-filename> [-verbose]
    uniquify --file=<filename> --output=<output-filename> 
    uniquift <filename> <output_filename>
    
   
    
The verbose option will tell you when the file is created and if it overwrites another file. An example of how to call the program in terminal may look like this: 

    python problem2.py --file=input_file.txt --output=<output_file.txt -verbose
     
 Problem notes: 1. If the file does not exist then Python automatically throws an error at the user saying the file or directory does not exist, so I did not find it necessary to include my own check for that. 
 2. I use a set to store all the sentences that come in from the large file. That way any duplicate copy is already deleted without me having to compare it.
 3. The Big O time complexity is still Big O(n) because you have to go through each value of the first file to make sure it is not unique. Using a set data structure does make it much easier to handle unique values.
 4. The Big O space complexity is also Big O(n)
 5. The user can choose to not type out --file= and --output= if that makes it easier for them to use the program
 6. Some assumptions I make are that there is enough space on the computer to run the large input file and that the user has reading and writing permissions.
