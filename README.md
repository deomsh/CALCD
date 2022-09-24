# CALCD
Grub4dos script with extensions to grub4dos' function calc

CALCD.G4B v.0.1.20 (20220924), by deomsh (first public version)

Output: Echood, if exists always in variables 'result' 'rounded' and 'message'

Functions: SUM, PRODUCT, COUNT, FAC, MEAN, SQRT, INV, VARP, VARS, STDEVP, STDEVS, "==", ">=", "<=", Pnr, Cnr, CRT
 
Use: CALCD.G4B <function> <number1> [<number2> ...]|<number1> <number2>

Operators:  +  ,  -  ,  *  ,  /  , ^ . Special: ROUND , DECI , DIGI , FIX

Use: CALCD.G4B <number1> <operator> <number2> [<operator> <number3> ...]

Quasi-operators: SQRT and INV if used after result/ number

Use: CALCD.G4B <number1> <SQRT|INV>

Memory: MC , M , M+ , M- , MR , RM

Help: Function-/ operator-/ memory-/ syntaxis-specific

Use: CALCD.G4B <help> <function>|<operator>|mem|syntax

Remark: Arguments are space-separated, without '<' and '>', '[..]' is optional
 Switches: /echo or /echoM or /echoR or /V (debug msg=3). Before argument
 Order of calculation: from left to right. NO brackets allowed
 Highest supported result: 9223372036854775807, about 19 integer digits + 18 decimals
 Highest input depends on function/ operator: see Help
 Lowest number: 0.0000000000000000001 (decimals: dot, no comma allowed)
 Error-messages are echood, while 'result' and 'rounded' are deleted
 Input of hexa-decimal integers allowed. Decimals: decimal numbers only
 New function/ calculation after '\\'
 Names and switches are case-insensitive

Example CALCD.G4B 38 + 2.5 - 27.315 * 1.2895 / 3.1239 ^ 3 SQRT - 1 ROUND 4

Example CALCD.G4B SUM 3 2.5 2.3 1.2 3.1 / 5 M \\ STDEVP 0.5 1 2 3 4 5 6 + MR 
