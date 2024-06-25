# Student self-graded homework workflow

Author: Dr. Matthew Ford (mattford@uw.edu) [Website](https://dashdotrobot.com/)

A secure, scalable approach to student-graded homework for self-reflection.

Use this script to compare student self-graded scores to instructor scores and enter final grades into the Canvas gradebook.

## Creating an assignment
1. Assign homework on Canvas: Create a zero-point assignment called "Homework X - submit to Gradescope"
2. Create Gradescope assignment: Create a Gradescope assignment with the correct number of problems. Each problem should have a point value of 0. Link the Gradescope assignment to the Canvas assignment.
3. Create a Canvas quiz (Classic Quizzes) called "Homework X - enter your own grade". The first "question" should be a text-only question with links to the homework solutions and grading rubrics.
4. Add a Numerical Answer question for each homework problem. Name each problem "Problem X" where "X" is an integer. Set the "answer" to -1, and set the point value to the correct number. Optionally add a file upload question at the end for students to upload their filled-out rubric.
5. Set the quiz "Available from" date to just shortly after the homework is due.

## Grading an assignment
1. Students complete the "Homework X - enter your own grade" assignment on Canvas, entering their numeric score as the "answer" for each question.
2. Instructors grade the "check problem" on Gradescope and sync grades to Canvas.
3. After students have submitted their own scores, run the IPython script to compare and synchronize grades. The script will automatically create a new Canvas assignment "Homework X - final grade".
