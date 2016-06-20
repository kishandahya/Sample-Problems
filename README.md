
This repository contains three sample problems I completed.

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

Problem notes: 

1. I account for users wanting to put in only two arguments where the second is the verbose option. 
2. Overall, I tested 14 test cases, which I could provide if needed, and my program passed all of them. 
3. It was fun learning about Bash shell scripting and I look forward to continue learning it in the future 
4. For this program, the first argument is automatically the file name, so the user does not have to type "--create-file=" before typing in the file name he or she wants 


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
     
 Problem notes: 
 
 1. If the file does not exist then Python automatically throws an error at the user saying the file or directory does not exist, so I did not find it necessary to include my own check for that. 
 2. I use a set to store all the sentences that come in from the large file. That way any duplicate copy is already deleted without me having to compare it.
 3. The Big O time complexity is still Big O(n) because you have to go through each value of the first file to make sure it is not unique. Using a set data structure does make it much easier to handle unique values.
 4. The Big O space complexity is also Big O(n)
 5. The user can choose to not type out "--file=" and "--output=" if that makes it easier for them to use the program
 6. Some assumptions I make are that there is enough space on the computer to run the large input file and that the user has reading and writing permissions.
 

Problem 3: 

This program generates a work table of any url listing a keyword and how many times it appears on the page. It can take is multiple urls at the same time. A word only contains the character A-Z, a-z, or 0-9. The files will be stored as url1.txt, url2.txt and etc. They will look like this: 
url: <url>
	word1: number
	word2: number

This program can be used with this general structure:
 	problem3.go [-help|-h]
 	problem3.go -urls=<comma-separated-one-or-more-urls>
 	problem3.go <comma-separated-one-or-more-urls>

sample view of what to type in terminal:
 
	go run problem3.go -urls=https://blog.golang.org/go-maps-in-action,https://raw.githubusercontent.com/aporeto-inc/internship2016/master/samples/problem2/uniquified_file.txt

Problem notes:

1. The main data structure I used was a map with a key for every unique word and a value that is the number of times the word appears on the url.
2. The time complexity is Big O(n)
3. The space complexity is also Big O(n)
4. I made use of functions more in this problems because breaking down the problem into smaller chunks made it much more manageable and easier to test 
5. This was my first time ever programming in Go, so I basically learned it really fast, which shows that I am a very fast learner. 
6. My next goal is to process the URLs in parallel to increase speed



