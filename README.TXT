# CALCD
Grub4dos script with extensions to grub4dos' function calc

CALCD.G4B v.2.0 (20221018), by deomsh

Output  Echood, if exists in variables 'result' 'MR' 'R' 'resrnd' and 'message'
Prefix  Functions: SUM PRODUCT MEAN VARP VARS STDEVP STDEVS FACT Pnr Cnr "==" ">=" "<=" COUNT
Use     CALCD.G4B [switch] function number1 [number2]|number1 number2|args
Infix   Operators: + - * / ^  Functions: ROUND DECI DIGI FIX
Use     CALCD.G4B [switch] number1 operator|function number2|NUMBER
Postfix Functions: INV SQRT SQ CBRT CB HEX THSEP
Use     CALCD.G4B [switch] number function
Memory  Functions: M M+ M- RM  Clear: MC  Placeholders for number: MR R
        ± 10exp-18 - 2exp63-1, 0!-20!, MR, R (integers hex too, decimals: dot)
Help    CALCD.G4B help|--help|/? [function|operator|mem|ver]

BTW After Aborting errors text above is showed always - if you do not like it (anymore) use line 89 instead of remaked line 88
