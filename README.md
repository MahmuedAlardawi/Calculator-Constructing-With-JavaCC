# Construct-Calculator-With-JavaCC
King AbdulAziz Universality - Compiler Construction (CPCS-302)

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
