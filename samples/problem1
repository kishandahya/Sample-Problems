

function state_file () {

my_var=$1
no_prompt=$2
verbose=$3
flag=1



while [ $flag -eq 1 ]
do

if [ -f $my_var ] && [ "$no_prompt" != "--no-prompt" ]
then
printf "File exists. Overwrite (y/n) ?\n"
read file_exists
fi

if [ -f $my_var ] && [ "$verbose" == "--verbose" ]
	then
		printf "File already exists\n"
	fi


if [ ! -f $my_var ] || [ "$file_exists" == "y" ] || [ "$no_prompt" == "--no-prompt" ]
then
	if [ -f $my_var ] && [ "$verbose"  == "--verbose" ]
	then
		printf "File removed\n"
		printf "File created\n"
	elif [ ! -f $my_var ] && [ "$verbose" == "--verbose" ]
	then
		printf "File created\n"
	fi

printf "Alabama
Alaska
Arizona
Arkansas
California
Colorado
Connecticut
Delaware
Florida
Georgia
Hawaii
Idaho
Illinois
Indiana
Iowa
Kansas
Kentucky
Louisiana
Maine
Maryland
Massachusetts
Michigan
Minnesota
Mississippi
Missouri
Montana
Nebraska
Nevada
New Hampshire
New Jersey
New Mexico
New York
North Carolina
North Dakota
Ohio
Oklahoma
Oregon
Pennsylvania
Rhode Island
South Carolina
South Dakota
Tennessee
Texas
Utah
Vermont
Virginia
Washington
West Virginia
Wisconsin
Wyoming\n" > $my_var

flag=2

elif [ "$file_exists" == "n" ]
then
printf "Thank you for running the program!\n"
flag=2

else
printf "ERROR: the the input must be y or n\n"
fi
done


exit 0

}


if [ $# -eq 1 ] && ([ "$1" != "-h" ] && [ "$1" != "--help" ])
then
state_file $1 $2 $3
elif [ $# -eq 2 ] && [ "$2" == "--no-prompt" ]
then
state_file $1 $2 $3
elif [ $# -eq 2 ] && [ "$2" == "--verbose" ]
then
state_file $1 "prompt" $2
elif [ $# -eq 3 ] &&  [ "$2" == "--no-prompt" ] && [ "$3" == "--verbose" ]
then
state_file $1 $2 $3
else
printf "The user either made an error in your arg entry or requested the help option. This program creates a file that has all 50 states listed in it. Each state is on its own line and is sorted in alphabetical order. The name of the file is the first argument the user input.

options:
	-h or —-help  will tell you what the program does and how to use it
	—-no-prompt   this option will overwrite the filename you put without alerting you if it exists or not
	—verbose      this option will print out extra documentation for when the file is removed, created and already exists\n

The usage format is 
sh test1.sh [--help|-h]
sh test1.sh <filename> [--no-prompt] [--verbose] \n

A sample for how it may look in terminal is:

	sh test1.sh file.txt --no-prompt --verbose\n"

exit 3
fi





