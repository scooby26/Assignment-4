# CS6620: Advanced Computer Organization and Architecture with Lab
# Lab Assignment-4 

## Character-Coded Data (Submission Deadline:24/10/19)

### Part 1
Compare two strings of ASCII characters to see which is larger (i.e., which
follows the other in alphabetical ordering). Both strings have the same
length as defined by the **LENGTH** variable. The strings’ starting addresses
are defined by the **START1** and **START2** variables. If the string defined by
**START1** is greater than or equal to the other string, clear the **GREATER**
variable; otherwise set the variable to all ones ***(0xFFFFFFFF)***.


For example:

|         |           |    Test A   |    Test B   |    Test C   |
|:-------:|:---------:|:-----------:|:-----------:|:-----------:|
|  Input: |   LENGTH  |      3      |      3      |      3      |
|         |   START1  |   String1   |   String1   |   String1   |
|         |   START2  |   String2   |   String2   |   String2   |
|         | *String1* |  0x43 ('C') |  0x43 ('C') |  0x43 ('C') |
|         |           |  0x41 ('A') |  0x41 ('A') |  0x41 ('A') |
|         |           |  0x54 ('T') |  0x54 ('T') |  0x54 ('T') |
|         |           |             |             |             |
|         | *String2* | 0x42 ('B')  | 0x43 ('C')  | 0x43 ('C')  |
|         |           |  0x41 ('A') |  0x41 ('A') |  0x55 ('U') |
|         |           |  0x54 ('T') |  0x54 ('T') |  0x54 ('T') |
| Output: |  GREATER  |  0x00000000 |  0x00000000 |  0xFFFFFFFF |
|         |           | (CAT > BAT) | (CAT = CAT) | (CAT < CUT) |


### Part 2
Given two strings, check whether the second string is a substring of the First
one. The starting addresses of two strings are defined by the **STRING** and
**SUBSTR** variables, respectively. If the string defined by SUBSTR is not
present in the string defined by **STRING**, clear the **PRESENT** variable;
else set the variable with the position of the First occurrence of the
second string in the First string.


For example:

|        |           |    Test A    |   Test B   |   Test C   |
|:------:|:---------:|:------------:|:----------:|:----------:|
| Input: |   STRING  |    String1   |   String1  |   String1  |
|        |   SUBSTR  |    String2   |   String2  |   String2  |
|        | *String1* |  0x43 (“C”)  |    (“C”)   | 0x43 ('C') |
|        |           | 0x53 (“S”)   | 0x53 (“S”) | 0x53 (“S”) |
|        |           |  0x36 (“6”)  | 0x36 (“6”) | 0x36 (“6”) |
|        |           |  0x36 (“6”)  | 0x36 (“6”) | 0x36 (“6”) |
|        |           |  0x32 (“2”)  | 0x32 (“2”) | 0x32 (“2”) |
|        |           | 0x30 (“0”)   | 0x30 (“0”) | 0x30 (“0”) |
|        |           |              |            |            |
|        | *String2* | 0x53 (“S”)   | 0x36 (“6”) | 0x36 (“6”) |
|        |           |  0x53 (“S”)  | 0x32 (“2”) | 0x55 ('U') |
|        |           |              | 0x30 (“0”) |            |
|        |           |              |            |            |
| Ouput: | PRESENT   | (0x00000000) | 0x00000004 | 0x00000003 |


**Add necessary comments to your program for easy readability.**

***no starter code will be provided***
