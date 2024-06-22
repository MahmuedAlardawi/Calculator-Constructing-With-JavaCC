# Construct-Calculator-With-JavaCC
King AbdulAziz Universality - Compiler Construction (CPCS-302)

This project is a group assignment for the CPCS-302-CS1 and CS2 courses at King Abdulaziz University. The goal of the project is to create a calculator using the Java Compiler Compiler (JavaCC) tool, which enhances our skills in working with lexical analyzers and parser generator tools.

Problem Statement
The project requires writing a program to construct a calculator using the lexical analyzer and parser generator tool, JavaCC. The program should accept any arithmetic expression containing integers or real numbers separated by the +, -, *, /, ( ) operators.

Lexical Specifications
javacc
Copy code
SKIP : { " " }
TOKEN : { < EOL : "\n" | "\r" | "\r\n" > }
TOKEN : { < PLUS : "+" > }
TOKEN : { < MINUS : "-" > }
TOKEN : { < TIMES : "*" > }
TOKEN : { < DIVIDE : "/" > }
TOKEN : { < OPEN_PAR : "(" > }
TOKEN : { < CLOSE_PAR : ")" > }
TOKEN : { < NUMBER : < DIGITS > | < DIGITS > "." < DIGITS > | < DIGITS > "." | "." < DIGITS > > }
TOKEN : { < #DIGITS : (["0"-"9"])+ > }
Parser Specifications
javacc
Copy code
Start → (Expression EOL) * EOF
Expression → Term (PLUS Term | MINUS Term) *
Term → (TIMES Primary | DIVIDE Primary) *
Primary → NUMBER | OPEN_PAR Expression CLOSE_PAR
Sample Input and Output
Sample Input
Copy code
2 * 3 + 4 * 5
Sample Output
Copy code
26
Important Notes
Every group should consist of a maximum of 3 students.
Any kind of plagiarism/cheating will result in 0 marks.
No late submission will be accepted.
Only one student of each group should upload the solution (compressed files: .zip, .7z, or .rar containing all JavaCC-related files) on Blackboard on or before the due date.
Write ID, Name, and Email of each member of the group as a comment in the Calculator.jj file.
No solution will be accepted through email.
Solutions in any other file format (e.g., .pdf, .docx) will not be entertained and will result in 0 marks.
Your program should take any expression as input at runtime and display the correct value of that expression, considering the precedence of operators.
