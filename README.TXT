# CALCD
Grub4dos script with extensions to grub4dos' function calc

CALCD.G4B v0.2.1 (20221211), by deomsh

Output  Echood, if exists in variables 'result' 'MR' 'R' 'resrnd' and 'message'
Prefix  Functions: SUM PRODUCT MEAN VARP VARS STDEVP STDEVS FACT Pnr Cnr "==" ">=" "<=" COUNT MIN MAX COUNTIF
Use     CALCD.G4B [switch] function number1 [number2]|number1 number2|args
Infix   Operators: + - * / ^  Functions: ROUND DECI DIGI FIX
Use     CALCD.G4B [switch] number1 operator|function number2|NUMBER
Postfix Functions: INV SQRT SQ CBRT CB HEX THSEP
Use     CALCD.G4B [switch] number function
Memory  Functions: M M+ M- RM  Clear: MC  Placeholders for number: MR R
Numbers ± 10exp-18 - 2exp63-1, 0!-20!, MR, R (integers hex too, decimals: dot)
Help    CALCD.G4B help|--help|/? [function|operator|mem|ver]

BTW After Aborting errors text above is showed always - if you do not like it (anymore) use remarked line 89 instead of line 88

Known bugs:
CALCD.G4B is not working with 'debug off'/ 'debug 0'. So set minimal 'debug 1' on the grub4dos' command-line before use. Will be fixed in next release.

History:

v0.2.1
Bugfixes (especially in Cubic Root)
Cubic Root (CBRT) gives 18 decimals now (but not rounded)
Function CRT renamed to CBRT
Function FAC renamed to FACT
Simpler handling of multiple calculations on command-line:
- Continue/ restart calculation with \\ only needed after COUNT
- Functions INV, SQRT and M cannot be used before there argument anymore
- Function CBRT must now be used after argument
- Single number on command-line allowed (including MR, R and 0!-20!)
Help has been rewritten, about 250 examples
New funtions:
HEX: convert number/ result to hexa-decimal number (rounddown!)
THSEP: adds thousands-comma-separator to last number/ result (input with thousands-comma's allowed too)
SQ: Square of number
CB: Cubic of number
MIN: lowest number on command-line/ (md)
MAX: highest number on command-line/ (md)
COUNTIF: count of numbers on command-line/ (md) 'satisfying' if-condition
New switch: /Q for quiet operation
Display of 'smallhelp' after (syntax-)error

v0.1.20
First published version

BONUS



v0.2
First published version

