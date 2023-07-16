                           SSENABULYA DENIS KLEIN 
                           M23D14/017

1. Problem Statement, Sub-Problems, and Sub-Solutions:
Problem Statement: Develop a program for slow learning that can track the progress of students and provide feedback based on their performance.
Sub-Problems:
1. Tracking Student Progress
2. Generating Feedback
3. Storing and Retrieving Data
Sub-Solutions:
1. Tracking Student Progress:
   a) Define Variables:
      - student Name (string)
      - progress Percentage (float)
      - lessons Completed (integer)
    b) Control Structures:
      - Conditional:
        - if progress Percentage < 50:
          - Print "Keep going! You're making progress, but there's room for improvement."
        - else if 50 <= progress Percentage <= 75:
          - Print "Great job! You're doing well. Keep up the good work!"
        - else:
          - Print "Congratulations! You've made excellent progress. Keep it up!"
2. Generating Feedback:
   a) Define Variables:
      - student Grade (integer)
      - feedback Message (string)
      - weak Areas (string)
 b) Control Structures:
      - Conditional:
        - if student Grade < 60:
          - Set feedback Message as "Your grade is below average. Focus on improving your understanding in the following areas:"
          - Iterate over weak Areas and print each area
        - else:
          - Set feedback Message as "Congratulations on your achievement! Your understanding is strong in the following areas:"
          - read over strong Areas and print each area
3. Storing and Retrieving Data:
   a) Define Variables:
      - student Data (string)
 b) Control Structures:
      - Conditional:
        - if student Name exists in student Data:
          - Print "Student data found!"
          - Retrieve progress Percentage and lessons Completed for the student
        - else:
          - Print "Student data not found!"
          - Add student Name to student Data with progress Percentage and lessons Completed as values
2. Necessary Functions:
Below is a list of necessary functions required for the program:

i.	track_student_progress (student name: str, progress percentage: float, lessons completed: int) -> None:
   # Function to track the progress of a student
   #   - student name: Name of the student
   #   - progress percentage: Percentage of progress made by the student
   #   - lessons completed: Number of lessons completed by the student
ii.	generate feedback (student grade: int, weak areas: string, strong areas: string) -> str:
   # Function to generate feedback based on student's grade and identified weak and strong area
   #   - student grade: Grade achieved by the student
   #   - weak areas: List of weak areas identified for improvement
   #   - strong areas: List of strong areas identified
iii.	store_student_data (student data: string, student name: str, progress percentage: float, lessons completed: int) -> None:
   # Function to store student data 
   #   - student data: Dictionary to store student data
   #   - student name: Name of the student
   #   - progress percentage: Percentage of progress made by the student
   #   - lessons completed: Number of lessons completed by the student
iv.	retrieve_student_data (student data: dict, student_name: str) -> tuple:
   # Function to retrieve student data from the student data dictionary
   #   - student data: Dictionary containing student data
   #   - student_name: Name of the student
   # Returns:
   #   - list containing progress percentage and lessons completed for the student


3. Variable Definitions:
For each function, let's identify the variables required, determine the appropriate data types, and provide initial values:

i.	track_student_progress:
   - student_name (str): Name of the student (input)
   - progress percentage (float): Percentage of progress made by the student (input)
   - lessons completed (int): Number of lessons completed by the student (input)
ii.	generate feedback:
   - student grade (int): Grade achieved by the student (input)
   - weak areas (list): List of weak areas identified for improvement (input)
   - strong areas (list): List of strong areas identified (input)
iii.	store_student_data:
   - student data (dict): Dictionary to store student data (input/output)
   - student_name (str): Name of the student (input)
   - progress percentage (float): Percentage of progress made by the student (input)
   - lessons completed (int): Number of lessons completed by the student (input)
iv.	. retrieve_student_data:
   - student data (dict): Dictionary containing student data (input)
   - student_name (str): Name of the student (input)
   - progress percentage (float): Percentage of progress made by the student (output)
   - lessons completed (int): Number of lessons completed by the student (output)
4. Function Definitions with Comments:
I.	track_student_progress (student_name: str, progress percentage: float, lessons completed: int) -> None:
   Function to track the progress of a student
     - student_name: Name of the student
     - progress percentage: Percentage of progress made by the student
     - lessons completed: Number of lessons completed by the student
    if progress percentage < 50:
       print ("Keep going! You're making progress, but there's room for improvement.")
   else if 50 <= progress percentage <= 75:
       print ("Great job! You're doing well. Keep up the good work!")
   else:
       print ("Congratulations! You've made excellent progress. Keep it up!")
II.	generate feedback (student grade: int, weak areas: list, strong areas: list) -> str:
   Function to generate feedback based on student's grade and identified weak and strong areas
     - student grade: Grade achieved by the student
     - weak areas: List of weak areas identified for improvement
     - strong areas: List of strong areas identified
   Returns:
     - Feedback message as a string
   if student grade < 60:
       feedback message = "Your grade is below average. Focus on improving your understanding in the following areas:"
       for area in weak areas:
           print(area)
   else:
       feedback message = "Congratulations on your achievement! Your understanding is strong in the following areas:"
       for area in strong areas:
           print(area)
   return feedback message
III.	store_student_data (student data: dict, student_name: str, progress percentage: float, lessons completed: int) -> None:
 
  Function to store student data in the student data dictionary
     - student data: Dictionary to store student data
     - student_name: Name of the student
     - progress percentage: Percentage of progress made by the student
     - lessons completed: Number of lessons completed by the student
  student data[student_name] = {'progress percentage': progress percentage, 'lessons completed': lessons completed}
IV.	retrieve_student_data (student data: dict, student_name: str) -> list:
Function to retrieve student data from the student data dictionary
     - student data: Dictionary containing student data
     - student_name: Name of the student
   Returns:
     - list containing progress percentage and lessons completed for the student
 if student_name in student data:
       student info = student data[student_name]
       return student info ['progress percentage'], student info ['lessons completed']
   else:
       return None, None

