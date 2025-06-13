# TASK-4-CPP-COMPILER-DESIGN

COMPANY: CODTECH IT SOLUTIONS

NAME: SOUMIK SAHA

INTERN ID: CTO4DN437

DOMAIN: C++ PROGRAMMING 

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

DESCRIPTION: 
This project is a fundamental implementation of basic compiler design, focusing on parsing and evaluating arithmetic expressions using C++. The primary objective was to simulate a simple compiler that can take an arithmetic expression as input, parse it, and compute its result by applying operator precedence and associativity rules.

The compiler handles expressions involving integer values and operators such as +, -, *, and /. The parsing mechanism uses two stacks — one for operands (numbers) and another for operators — mimicking the way expressions are processed in actual compilers.

Objective:
(i) To design a basic compiler model that can:

(ii) Parse simple arithmetic expressions from left to right

(iii) Handle operator precedence and associativity correctly

(iv) Evaluate and output the result like an interpreter

Key Features:
(i) Supports multi-digit integers

(ii) Operator precedence: *, / > +, -

(iii) Safe division (avoids division by zero)

(iv) Modular function structure for readability and maintainability

(v) Uses standard C++ libraries (<stack>, <string>, <iostream>)

How It Works:
1) Tokenization & Parsing:
The input string is scanned character by character. Numbers are extracted and pushed onto the operand stack, while operators are pushed onto the operator stack.

2) Operator Handling:
Before pushing a new operator, the program checks if any previously pushed operators have higher or equal precedence. If so, it evaluates them first.

3) Evaluation:
Once the entire expression is parsed, any remaining operations in the stacks are processed to compute the final result.

This project served as a foundational exercise in understanding how compilers parse and evaluate expressions, making it a perfect entry-level demonstration of compiler functionality for internship work.

Technologies Used:
C++, Stack Data Structure, Standard Libraries

OUTPUT:
![Image](https://github.com/user-attachments/assets/ffc82b80-523f-451c-96fb-a019a130657c)
