# CALCD
Grub4dos script with extensions to grub4dos' function calc

CALCD.G4B v0.3.2 (20240613), by deomsh

Output  Echood, if exists in variables 'result' 'MR' 'R' 'resrnd' and 'message'
Prefix  Functions: SUM PRODUCT MEAN VARP VARS STDEVP STDEVS FACT Pnr Cnr "==" ">=" "<=" COUNT MIN MAX COUNTIF JOIN
Use     CALCD.G4B [switch] function number1 [number2]|number1 number2|args
Infix   Operators: + - * / ^  Functions: ROUND DECI DIGI FIX
Use     CALCD.G4B [switch] number1 operator|function number2|NUMBER
Postfix Functions: INV SQRT SQ CBRT CB LN LOG EX 10X ABS HEX BIN[S] THSEP|TS
Use     CALCD.G4B [switch] number function
Memory  Functions: MS (Min), MP (M+), MN (M-), SRM (R/M), MC (clear), Placeholders for number: MR R
Numbers ±10exp-18 - 2exp63-1, 0!-20!, a'b:c, en, pi, MR, R (signed 64-bit integers hex/ bin too; decimals: dot)
Help    CALCD.G4B help|--help|/? [function|operator|mem|ver]

Using parenthes is possible with frontend PCALCD.G4B, a modification of Wonko the Sane's PCALC.G4B
Available on: http://reboot.pro/index.php?showtopic=23030#entry222994

History:

v0.3.2
Help updated
Better protection of invalid input with 'pi' and 'en'
New: postfix function 'ABS' (Modulus: |a|)
New: input of hexa-decimal/ binary numbers taken with minus sign if in Two's Complement format
New: output of negative numbers with HEX/ BIN[S] in Two's Complement format (signed 64-bits only)
Bugfix: parsing of ++/--/+-/-+ at beginning of command-line
Bugfix: output variable R not 'good' after BIN[S]
Bugfix: number 'e' not compatible with hexadecimal input, changed to 'en' (Eulers Number)
Bugfix: division of two numbers with decimals only with dividend > 9 digits and divisor with more than 7 digits and more three zeros before

v0.3.1
Better protection in case of very long command-line
Only natural numbers supported inside fractions
Much higher precision of small numbers in LN, LOG and broken Powers

v0.3
New (input) number formats:
Fractions: a'b:c (fractional output not supported)
Negative exponent supported (p.d1^-q.d2)
Decimals in exponent supported (p.d1^q.d2)
Binary: 63-bits (starting with 0b)
Full post-operators: k, m, g, e, pi
New prefix function: JOIN (removes spaces)
New postfix functions:
10X: exponential function with base 10
EX: exponential function with base e
LOG: common logarithm
LN: natural logarithm
BIN[S]: output binary (starting with 0b), BINS splits too in 0b nibbles (R is unsplit)
New infix function: ROUNDUP
New switch: --no-parse (faster - also full grub4dos command-line now , about max 1535 chars)
Switches now starting with --
Memory functions renamed: M => MS, M+ => MP, M- => MN, RM => SRM
Parsing of command-line: (almost) no spaces needed around operators/ functions
 (but max chars on command-line after parsing about max 511)
Update Help: aliases of thousand sepator THSEP
Bugfix: no result with division if dividend is zero
Bugfix: not working with 'debug off'/ 'debug 0'

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

FRACTION.G4B v0.2.1 (20240609), by deomsh
Function:   Calculations with a'b:c fractions
Use:        FRACTION.G4B [--Q|--V] fraction1 operator fraction2
Switch:     '--Q': quiet operation OR '--V': echos sub-results
Operators:  +  -  *  /  ^ (no fractioned exponents supported)
Numbers:    ±2exp63-1 (hex-decimal input of a, b or c allowed)
Dependency: For operator ^ needed CALCD.G4B >=v0.3 (in same directory)
Exports:    Variable 'result'/ 'message' (if error)
Reduction:  Supported up to divider 9999
Example 1:  FRACTION.G4B 3:4 * 2:3
Example 2:  FRACTION.G4B 1'3:4 + 2:3
Example 3:  FRACTION.G4B 1'3:4 ^ 2
Example 4:  FRACTION.G4B 7:8/1:8
Example 5:  FRACTION.G4B 7:8-1:8
Example 6:  FRACTION.G4B 7:8--1:8
Example 7:  FRACTION.G4B 1'1:9/3'1:18 ;; CALCD.G4B %result%

History
v0.2.1
Changes to smallhelp
v0.2
First published version
