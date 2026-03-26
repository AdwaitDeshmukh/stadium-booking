# COBOL Basics Guide

COBOL (Common Business-Oriented Language) is a high-level programming language primarily used in business, finance, and administrative systems for companies and governments. A typical COBOL program is organized into four divisions, each serving a specific purpose. In this guide, we will detail each of these divisions and provide examples for better understanding.

## 1. Identification Division
The Identification Division is the first division in a COBOL program. It is used to specify the program's name and to provide other metadata.

### Example:
```cobol
IDENTIFICATION DIVISION.
PROGRAM-ID. HelloWorld.
AUTHOR. John Doe.
DATE-WRITTEN. 2026-03-26.
```

## 2. Environment Division
The Environment Division is the second division. It describes the environment in which the program will run, including configuration for input and output.

### Example:
```cobol
ENVIRONMENT DIVISION.
INPUT-OUTPUT SECTION.
FILE-CONTROL.
    SELECT InputFile ASSIGN TO "input.txt".
    SELECT OutputFile ASSIGN TO "output.txt".
```

## 3. Data Division
The Data Division is where you define all the variables that the program will use. This includes file structures and various data types.

### Example:
```cobol
DATA DIVISION.
WORKING-STORAGE SECTION.
01  Customer-Name  PIC A(30).
01  Customer-Amount  PIC 9(5)V99.
```

## 4. Procedure Division
The Procedure Division is the main part of the program. It contains the actual business logic, handling data processing, and flow control.

### Example:
```cobol
PROCEDURE DIVISION.
    DISPLAY 'Hello, World!'
    MOVE 'John Doe' TO Customer-Name
    MOVE 100.50 TO Customer-Amount
    DISPLAY Customer-Name
    DISPLAY Customer-Amount.
    STOP RUN.
```

## Summary
COBOL has a structured format that helps in the organization of code and separates concerns within a program. Understanding these four divisions is essential for effective COBOL programming. This basic guide serves as a starting point for anyone looking to learn COBOL.