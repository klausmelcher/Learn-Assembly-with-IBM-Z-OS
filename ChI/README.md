# Exercises from the Chapter I    
Assembler Language Programming
for
IBM System z TM Servers
Version 2.00
John R. Ehrman

The author did not intend to use assembly programs in this chapter,
however I guess the best way to learn assembly is writing assembly programs.
Doing so by using ETEMPL as starting template is quite easy.

## How to use ETEMPL

There are only a few things I need to know:

  1. put the value to display in a line like <br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RValue,=F'123'` or<br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RValue,=XL4'1AB'` or<br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RValue,=BL4'01101'`<br>
  Hexadecimal and binary numbers must use the length modifier `L4` to
be represented using 32 bits. Octal number base is not available here.

  2. if I want to change the number base used for output, use <br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RBase,Hex`&nbsp;&nbsp;or<br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RBase,Octal`&nbsp;&nbsp;or<br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RBase,Binary`&nbsp;&nbsp;or<br>
  `L`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RBase,Decimal`<br>
  The number base used for output does not depend in any way on the
number base used in 1.

  3. now put this line:<br>
  `BAS`&nbsp;&nbsp;&nbsp;&nbsp;`Rret,DigStr`

  4. if one wants to start a new line now, use:<br>
  `BAS`&nbsp;&nbsp;&nbsp;&nbsp;`Rret,PrtLn`<br>
  this line must always be the last line before the comment "exercise ends".

  5. continue at 1. until all values are done.

It is possible to display several numbers in one line. It is also
possible to display an empty line by repeating 4.

The number of digits used for all the numbers displayed is in the line
starting with `DigLen  DC` which can be found near the end of the
ETEMPL2 file.

It is also possible to display a character string:<br>
  `LA`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`RValue,=C'Ehrman'`<br>
  `BAS`&nbsp;&nbsp;&nbsp;&nbsp;`Rret,CharStr`

Observe the use of `LA` instead of `L`. Only `DigLen` characters are displayed. If the string has more than `DigLen` characters, the remaining characters do not appear.

## Exercises missing here

Some exercises are quite impossible to solve as Assembly programs. They are:

- Exercise 2.2.5: Octal numbers cannot be interpreted by Assembler
- Exercise 2.3.6: Octal numbers cannot be interpreted by Assembler 
