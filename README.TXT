# CALCD
Grub4dos script with extensions to grub4dos' function calc

CALCD.G4B v.2.0 (20221018), by deomsh

Output: Echood, if exists in variables 'result' 'MR' 'R' 'resrnd' and 'message'

Prefix\tFunctions: SUM PRODUCT MEAN VARP VARS STDEVP STDEVS FACT Pnr Cnr "==" ">=" "<=" COUNT
Use\tCALCD.G4B [switch] function number1 [number2]|number1 number2|args
Infix\tOperators: + - * / ^  Functions: ROUND DECI DIGI FIX
Use\tCALCD.G4B [switch] number1 operator|function number2|NUMBER
Postfix\tFunctions: INV SQRT SQ CBRT CB HEX THSEP
Use\tCALCD.G4B [switch] number function
Memory\tFunctions: M M+ M- RM  Clear: MC  Placeholders for number: MR R
\xF1 10exp-18 - 2exp63-1, 0!-20!, MR, R (integers hex too, decimals: dot)
Help\tCALCD.G4B help|--help|/? [function|operator|mem|ver]
