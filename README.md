# Python Script to Find the Student with the Highest GWA from Text File
This Python program prints the name of the student with the highest GWA (along with the GWA) after reading a file containing the names and GWAs of 20 students. The program expects that the input file is not empty and that it is correctly formatted with names and GWA separated by commas on each line.

## Usage 
Using Command Prompt: 

1. Open the Start menu and search for "Command Prompt".
2. Click on "Command Prompt" to open the command prompt window.
3. Use the cd command to navigate to the directory containing the script file. For example, if the script file is located in the "Documents" folder, type: cd Documents
4. Type the command python script_name.py to run the script. Replace "script_name.py" with the actual name of the script file.
5. Press Enter to run the script.
6. The script will run and output the name and GWA of the student with the highest GWA.

Alternatively, you can also run the script using the Python IDLE environment:

1. Open the Start menu and search for "Python".
2. Click on "Python" to open the Python IDLE environment.
3. Click on "File" at the top of the window and select "Open".
4. Navigate to the directory containing the script file and select it.
5. Click on "Run" at the top of the window and select "Run Module" or press the F5 key.
6. The script will run and output the name and GWA of the student with the highest GWA.

## Example
The students.txt file should have one student name and GWA per line, separated by a comma. Example:

<img width="600" alt="image" src="https://user-images.githubusercontent.com/129574374/233823148-3232c666-6399-4efc-b4f8-7dbdd2eb96c7.png">

The output of the script for the provided input would be:

<img width="600" alt="image" src="https://user-images.githubusercontent.com/129574374/233823166-da29a4db-4d12-407f-a7b7-7e79b810ec1e.png">

Note that the script will only consider lines that contain exactly two values separated by a comma. Any lines that do not meet this criteria will be skipped.

## Code Explanation

<img width="600" alt="image" src="https://user-images.githubusercontent.com/129574374/233823223-c9d239ed-e19e-4560-9c0a-a6678f0b7f11.png">

By assigning the file object to the variable f, the line open the students.txt file in read-only mode. The file is automatically closed when it has been read because to the application of a with statement, which ensures that errors won't prevent the process from working. Then, set the student_name and highest_gwa variables to their initial values. To guarantee that any valid GWA will be less than this amount, highest_gwa is set to an intentionally high value of 100. An empty string is used as student_name's initial value.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/129574374/233823294-7405b5c2-b5e3-41e0-926c-de5744793f6e.png">

The script then uses a for loop to repeatedly iterate through each line of the input file. divides the line at the comma delimiter, removing any leading or following whitespace before saving the resulting list of strings in the name_gwa variable. The presence of exactly two values in the name_gwa list is also checked. If not, the continue statement moves on to the next line in the file and skips the current iteration of the loop. Additionally, assigns the name_gwa list's first element to name and its second element to gwa using tuple unpacking. Also, it changes the GWA variable from a string to a float so that mathematical comparisons can be performed.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/129574374/233823378-7e1fc7d1-0dc4-4659-b837-c5339a6b1eea.png">

The current GWA is compared to the highest_gwa in these lines to see if it is lower. If so, the student_name variable and highest_gwa variable are updated with the most recent GWA and name, respectively. In this way, the student with the highest GWA will have their name and GWA in the student_name and highest_gwa variables, respectively, at the end of the loop.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/129574374/233823420-aee7e4f8-4b04-401b-a8db-d9f694c03c5c.png">

Lastly, it prints the name and GWA of the student with the highest GWA using an f-string.

## Potential Improvements
- Adding some input validation to ensure that the input file is correctly formatted before attempting to read it.
- Adding a check for an empty input file and producing an appropriate error message.
- Outputting all students with the highest GWA, or by randomly selecting one of the tied students.
- The current script iterates over each line of the input file and splits each line at the comma delimiter, even if the line has already been processed. This can be inefficient if the input file is very large. It would be a good idea to optimize the script by skipping lines that have already been processed or have errors.

## Conclusion
In conclusion, this script provides an intuitive and simple way to identify the student with the highest GWA among a list of students' names and GWAs. However, there are certain restrictions with the present version, such as the fact that it assumes the input file is appropriately formatted and not empty. Additionally, the script does not handle ties; it simply prints the student's name and GWA who has the highest GWA.
