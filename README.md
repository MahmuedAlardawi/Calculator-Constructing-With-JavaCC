# Construct-Calculator-With-JavaCC
King AbdulAziz Universality - Compiler Construction (CPCS-302)

## Table of Contents

- [Objective](#objective)
- [Student Outcome Covered](#student-outcome-covered)
- [Course Learning Objective Covered](#course-learning-objective-covered)
- [Problem Statement](#problem-statement)
  - [Lexical Specifications](#lexical-specifications)
  - [Parser Specifications](#parser-specifications)
- [Sample Input and Output](#sample-input-and-output)
- [Important Notes](#important-notes)
- [Group Members](#group-members)
- [Submission](#submission)

## Objective

- Learn how to make a calculator using the JavaCC tool.
- Enhance skills in working with JavaCC.
- Learn how to collaborate effectively as a team.

## Student Outcome Covered

- **SO #1**: Analyze a complex computing problem and apply principles of computing and other relevant disciplines to identify solutions.

## Course Learning Objective Covered

- **CLO #10**: Learn lexical analyzer and parser generator tools: JavaCC and/or Lex, YACC.

## Problem Statement

The project requires writing a program to construct a calculator using the lexical analyzer and parser generator tool, JavaCC. The program should accept any arithmetic expression containing integers or real numbers separated by the +, -, *, /, ( ) operators.

### Lexical Specifications

```javacc
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
