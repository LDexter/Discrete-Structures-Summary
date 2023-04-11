# $\color{dodgerblue}\text{CAB203: Discrete Structures Summary}$

$\textit{Author not responsible for consequences caused by any innacuracies.}$

## $\color{steelblue}\text{Markdown Setup}$

Open in Visual Studio Code and install Markdown Preview Enhanced:
https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced

## $\color{steelblue}\text{Typesetting Powered by} \thickspace \KaTeX$

$\KaTeX$ documentation: https://katex.org/
which uses $\LaTeX\textit{-like}$ syntax to display mathematical syxbols

## $\color{steelblue}\text{Axioms}$

### $\color{teal}\text{Natural Numbers}$

$\text{If } x, y \text{ and } z \text{ are natural numbers:}\\[1em]$

1. $0 \text{ is a natural number} \\[1em]$

2. $x = x \\[1em]$

3. $\text{if } x = y \text{ then } y = x \\[1em]$

4. $\text{if } x = y \text{ and } y = z \text{ then } x = z \\[1em]$

5. $\text{if } x = w \text{ then } w \text{ is a natural number} \\[1em]$

6. $S(y) \text{ is a natural number} \\[1em]$

7. $S(x) = S(y) \text{ then } x = y \\[1em]$

8. $S(x) = 0 \text{ is always false}\\[1em]$

### $\color{teal}\text{Other Axioms}$

WIP

## $\color{steelblue}\text{Equivalence}$

- $\textbf{Equals: } \quad =$
- $\textbf{Greater than: } \quad >$
- $\textbf{Greater than or equal to: } \quad \ge$
- $\textbf{Less than: } \quad <$
- $\textbf{Less than or equal to: } \quad \le$
- $\textbf{Not equal to: } \quad \not =$

## $\color{steelblue}\text{Division}$

- $a\mid b$

- $a \text{ divides } b$

- $b \text{ is divisible by } a$

- $\text{there exists some integer } c \text{ such that } ac = b$

## $\color{steelblue}\text{Definitions}$

May either replace term with its definition, or replace definition with its term:

- $\text{the term } 2 \cdot 3 = 6 \text{ may be replaced by } 2\mid6 \text{, while } 3 \text{ becomes } c \\[1em]$

- $\text{the definition } 2\mid6 \text{ may be replaced with "there is some integer } c \text{ such that } 2c = 6 \text{"}$

## $\color{steelblue}\text{Parity}$

Integers have one of two $\textit{parities:}$

- $x \text{ is \textit{even} means } 2\mid x$
- $x \text{ is \textit{odd} means } 2\mid(x-1)$

Properties:

- $\text{even} \pm \text{even} = \text{even}$
- $\text{even} \pm \text{odd} = \text{odd}$
- $\text{odd} \pm \text{odd} = \text{even}$

Therefore, two numbers have same parity if difference is even.

## $\color{steelblue}\text{Clock Arithmetic}$

- $10\ o'clock + 5h = 3\ o'clock$
- $\text{the } o'clock \text{ remains unaffected by multiples of } 12h$

## $\color{steelblue}\text{Modular Arithmetic}$

$\textit{Modular arithmetic}$ is an abstraction of parity and clock arithmetic.

- $\text{parity is } arithmetic\mod 2$
- $\text{clocks use } arithmetic\mod 12$
- $\text{generally, can have } arithmetic\mod n \text{ for any positive integer } n$

Modular arithmetic extends upon integers by adding a new relation (modular equivalence)

### $\color{teal}\text{Modular Equivalence}$

Modular arithmetic works by replacing equality with $\textit{modular equivalence}$, also called $\textit{modular congruence}$:

$\text{if } n\mid(a-b) \text{, then } a \text{ and } b \text{ are \textit{equivalent modulo n}, such that } a \equiv b\quad (\bmod\ n)$

$\text{if } a \equiv b\ (\bmod\ n) \text{ and } c \equiv\ d\ (\bmod\ n) \text{, then:}$

- $a + c \equiv b + d$
- $a - c \equiv b-d\quad (\bmod\ n)$
- $ac \equiv\ bd\quad (\bmod\ n)$

### $\color{teal}\text{Mod Operator}$

$a \bmod n \text{ is the smallest non-negative } b \text{ such that }\quad a \equiv b\quad (\bmod\ n)$

- $\text{Equivalently, } a \mod n \text{ is the remainder from } \dfrac{a}{n}$
- $example: 17 \mod 4 = 1 \text{ because } 17 = 4(4)+1$

Python:

```python
print(17 % 4) # Prints 1 to the console
# 1
```

### $\color{teal}\text{Modulo Lemma}$

A $\textit{lemma}$ is a short statement that is true in mathematical theory, derived from its axioms. We can show that it is true by using a $\textit{proof}$ that shows the steps from the axioms to the statement. Other axioms with existing proofs may be used in the proof.

### $\color{teal}\text{Proof of Lemma}$

$$
\text{Let integers } a \text{ and } b \text{ be given such that } a \mod b = 0 \text{.} \\
\text{Then from the definition of the mod operator:}
\\[1em]
a \equiv 0\quad (\bmod\ b)
\\[1em]
\text{From the definiton of modular equivalence:}
\\[1em]
b\mid(a-0)
\\[1em]
\text{From a well known lemma observe that } a-0=a \text{ for any integer, so } b\mid a \text{.}
$$

This is frequently used to determine divisibility or test if a number is even when programming.

## $\color{steelblue}\text{Exponents}$

- $a^3 \text{ means } a \cdot a \cdot a$
- $a^n \text{ means multiply } a \text{ together } n \text{ times}$
  - $a \text{ is called the base}$
  - $n \text{ is called the exponent}$

### $\color{teal}\text{Laws of Exponents}$

- $(ab)^n = a^n \cdot b^n \\[1em]$
- $a^m \cdot a^n = a^{m+n} \\[1em]$
- $a^{m-n} = \dfrac{a^m}{a^n}\quad (\text{when } a \not= 0) \\[1em]$
- $a^{-n} = \dfrac{1}{a^n}\quad (\text{when } a \not= 0) \\[1em]$
- $a^0 = 1$
- $(a^m) = a^{m \cdot n}$

### $\color{teal}\text{Exponents in Computer Science}$

- $\textbf{kilo: }\quad 2^{10}\\[1em]$
- $\textbf{mega: }\quad 2^{20} = (2^{10})^2\\[1em]$
- $\textbf{giga: }\quad 2^{30} = (2^{10})^3\\[1em]$
- $\textbf{tera: }\quad 2^{40} = (2^{10})^4\\[1em]$
- $\textbf{peta: }\quad 2^{50} = (2^{10})^5\\[1em]$
- $\textbf{exa: }\quad 2^{60} = (2^{10})^6\\[1em]$

For example, one kilobit is $1024 = 2^{10}$ bits.

- $2^3 = 8 \text{ bits in a byte}\\[1em]$
- $2^{10} = 1024 \text{ bytes in a kilobyte}\\[1em]$
- $2^{10} \cdot 2^3 = 2^{10+3} \text{ bits in a kilobyte}\\[1em]$
- $32 = 2^5 \text{ or } 64 = 2^6 \text{ bit processors}\\[1em]$
- $256 = 2^8 = 2^{2^3} \text{ possible 8-bit characters}\\[1em]$

## $\color{steelblue}\text{Logarithms}$

- $\text{logarithms are the \textit{inverse} of exponents}$
- $\text{if } n=\log_a x \text{ then } a^n = x$
- $\text{so } \log_a \text{ tells what exponent is needed to make } x \text{ from } a:$
  $$a^{\log_a x} = x$$

### $\color{teal}\text{Laws of Logarithms}$

- $\log_a 1 = 0 \\[1em]$
- $\log_a a = 1 \\[1em]$
- $\log_a (x \cdot y) = \log_a x + \log_a y \\[1em]$
- $\log_a x^y = y \log_a x \\[1em]$
- $\log_a \dfrac{1}{y} = - \log_a y \\[1em]$
- $\log_a \dfrac{x}{y} \\[1em]$
- $\log_b x = (\log_b a) \cdot \log_a x \\[1em]$

### $\color{teal}\text{Base Transformation Law}$

- $\log_a x = \dfrac{\log_b x}{\log_b a}$
- $\text{use base transformation to calculate } \log_2 \text{, etc...}$

### $\color{teal}\text{Ceiling and Floor}$

- $\textbf{Ceiling, round up:} \quad \lceil a \rceil \text{ is the next integer above } a \\[1em]$
- $\textbf{Floor, round down:} \quad \lfloor a \rfloor \text{ is the next integer below } a \\[1em]$
- $\lceil \log_2 5000 \rceil = 13 \text{ address lines}$

### $\color{teal}\text{Exponent and Logs in Python}$

```python
>>> import math         # Must import math library
>>> math.log2(8)        # log2 means log base 2 and returns a float (decimal)
# 3.0
>>> 2 ** 3              # ** is exponentiation
# 8
>>> math.log2(100) / math.log2(10)  # base transformation
# 2.0
```

## $\color{steelblue}\text{Operators}$

An operator is a mathematical object that transforms other objects:

- $+$ is a binary operator (transforms two objects, ie: $1+2$ into $3$ )
- $-$ combines two operators
  - As a binary operator: $1-2$
  - As a unary operator: $-1$ (negative number)

## $\color{steelblue}\text{Bits}$

### $\color{teal}\text{Bit String Notation}$

- $\textbf{String: } \quad \overline{x} \\[1em]$
- The set of all strings of length $n$ (aka $n$-bit strings) is: $\quad \lbrace 0,1 \rbrace^n \\[1em]$
- All bit strings of all length are members of: $\quad \lbrace 0,1 \rbrace^* \\[1em]$
- The $j$th bit in $\overline{x}$ is: $\quad \overline{x}_j \quad$ $(j$ goes from $0$ to $n - 1)\\[1em]$
- Bit strings are most often counted from the $\textit{right}$, so the furthest right is: $\quad \overline{x}_0 \\[1em]$
- $2^n$ possible bit strings of length $n \\[1em]$

### $\color{teal}\text{Bit Operations}$

Two types of bit operations:

- Operations on a single bit or pairs of bits
- operations on bit strings

### $\color{teal}\text{NOT}$

NOT, aka $\textit{bit flip}: \quad 0$ becomes $1$ and vice versa.

$$
\def\arraystretch{1.5}
   \begin{array}{c:c}
   x & \text{\large\textasciitilde}x \\ \hline
   0 & 1 \\
   \hdashline
   1 & 0
\end{array}
$$

### $\color{teal}\text{AND}$

AND is similar to multiplication.

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c}
   x & y & x \And y \\ \hline
   0 & 0 & 0 \\
   \hdashline
   0 & 1 & 0 \\
   \hdashline
   1 & 0 & 0 \\
   \hdashline
   1 & 1 & 1
\end{array}
$$

### $\color{teal}\text{OR}$

OR is similar to addition, yet $2$ is condensed to $1$.

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c}
   x & y & x \mid y \\ \hline
   0 & 0 & 0 \\
   \hdashline
   0 & 1 & 1 \\
   \hdashline
   1 & 0 & 1 \\
   \hdashline
   1 & 1 & 1
\end{array}
$$

### $\color{teal}\text{XOR}$

XOR is also similar to addition, yet $2$ is now condensed to $0$, like parity.

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c}
   x & y & x \wedge y \\ \hline
   0 & 0 & 0 \\
   \hdashline
   0 & 1 & 1 \\
   \hdashline
   1 & 0 & 1 \\
   \hdashline
   1 & 1 & 0
\end{array}
$$

### $\color{teal}\text{Bitwise Operations}$

Bit operations may be applied bitwise to strings of the same length.
$\\[1em] \text{if }\overline{x} \And \overline{y} \text{ then}$
$$\overline{z}_j = \overline{x}_j \And \overline{y}_j$$

Operations are performed on pairs of bits.

### $\color{teal}\text{Concatonation}$

$\text{if } \overline{x} \text{ is an \textit{n}-bit string and } \overline{y} \text{ is a \textit{m}-bit string, then } \overline{z} = \overline{xy} \text{ is a } (n+m)\text{-bit string}$

### $\color{teal}\text{Lexicographic Ordering}$

- $0$ before $1$
- Compare strings one bit at a time, left to right
- At first bit where strings differ, 0 goes first
- Shorter strings are padded with empty spaces to the right

## $\color{steelblue}\text{ASCII}$

- 7 bit strings
- 128 characters
- Upper, lower case Latin chars, numbers, punctuation, maths symbols, space, newline, etc
- Special characters BEL, ESC, NUL, etc
- Relational blocks
- Upper vs lower is just one bit
- Letters and numbers ordered lexicographically

### $\color{teal}\text{USASCII Code Chart}$

$$
\def\arraystretch{1.5}
   \begin{array}{c|c|c|c|c||c:c:c:c:c:c:c:c}
   b_7 \substack{\rarr} & b_6 \substack{\rarr} & b_5 \substack{\rarr} & \Longrightarrow & \Longrightarrow & \tt000 & \tt001 & \tt010 & \tt011 & \tt100 & \tt101 & \tt110 & \tt111 \\ \hline
   b_4 \substack{\darr} & b_3 \substack{\darr} & b_2 \substack{\darr} & b_1 \substack{\darr} & r\substack\darr c\substack\rarr & 0 & 1 & 2 & 3 & 4 & 5 & 6 & 7 \\
   \hline
   \hline
   \tt0 & \tt0 & \tt0 & \tt0 & 0 & \tt NUL & \tt DLE & \tt SP & 0 & @ & \sf P & ` & \sf p \\
   \hdashline
   \tt0 & \tt0 & \tt0 & \tt1 & 1 & \tt SOH & \tt DC1 & ! & 1 & \sf A & \sf Q & \sf a & \sf q \\
   \hdashline
   \tt0 & \tt0 & \tt1 & \tt0 & 2 & \tt STX & \tt DC2 & " & 2 & \sf B & \sf R & \sf b & \sf r \\
   \hdashline
   \tt0 & \tt0 & \tt1 & \tt1 & 3 & \tt ETX & \tt DC3 & \sf \# & 3 & \sf C & \sf S & \sf c & \sf s \\
   \hdashline
   \tt0 & \tt1 & \tt0 & \tt0 & 4 & \tt EOT & \tt DC4 & \$ & 4 & \sf E & \sf T & \sf d & \sf t \\
   \hdashline
   \tt0 & \tt1 & \tt0 & \tt1 & 5 & \tt ENQ & \tt NAK & \% & 5 & \sf F & \sf U & \sf e & \sf u \\
   \hdashline
   \tt0 & \tt1 & \tt1 & \tt0 & 6 & \tt ACK & \tt SYN & \& & 6 & \sf G & \sf V & \sf f & \sf v \\
   \hdashline
   \tt0 & \tt1 & \tt1 & \tt1 & 7 & \tt BEL & \tt ETB & ' & 7 & \sf H & \sf W & \sf g & \sf w \\
   \hdashline
   \tt1 & \tt0 & \tt0 & \tt0 & 8 & \tt BS & \tt CAN & ( & 8 & \sf I & \sf X & \sf h & \sf x \\
   \hdashline
   \tt1 & \tt0 & \tt0 & \tt1 & 9 & \tt HT & \tt EM & ) & 9 & \sf J & \sf Y & \sf i & \sf y \\
   \hdashline
   \tt1 & \tt0 & \tt1 & \tt0 & 10 & \tt LF & \tt SUB & * & : & \sf K & \sf Z & \sf j & \sf z \\
   \hdashline
   \tt1 & \tt0 & \tt1 & \tt1 & 11 & \tt VT & \tt ESC & + & ; & \sf L & [ & \sf k & \{ \\
   \hdashline
   \tt1 & \tt1 & \tt0 & \tt0 & 12 & \tt FF & \tt FS & , & < & \sf M & \setminus & \sf l & \mid \\
   \hdashline
   \tt1 & \tt1 & \tt0 & \tt1 & 13 & \tt CR & \tt GS & - & = & \sf N & ] & \sf m & \} \\
   \hdashline
   \tt1 & \tt1 & \tt1 & \tt0 & 14 & \tt SO & \tt RS & . & > & \sf O & \text{\textasciicircum} & \sf n & \sim \\
   \hdashline
   \tt1 & \tt1 & \tt1 & \tt1 & 15 & \tt SI & \tt US & / & ? & \sf Q & \_ & \sf o & \tt END \\
   \hdashline
\end{array}
$$

## $\color{steelblue}\text{UNICODE}$

- About 137 000 characters
- Most modern and some historic writing systems
- Mathematical symbols, punctuation, emoji, etc
- Multiple encodings for a common set of characters

### $\color{teal}\text{UNICODE Encodings}$

Unicode assigns a code point (a hexidecimal string) for each character. There are several diﬀerent encodings from code points to bit strings:

- UTF32 uses 32 bits for each character, encoding code points directly
- UTF16 uses one or two 16-bit strings per code point, making it a variable length encoding
- UTF8 uses between one and four 8-bit stings per code point, and is hence also a variable length encoding.
- It is backwards compatible with ASCII for the original 7-bit ASCII character set
  - UTF8 is the most common encoding. Python strings are UTF-8 encoded by default.

### $\color{teal}\text{UTF-8 in Python}$

```python
>>> ord('A')    # Convert character to UTF code point
# 65
>>> chr(65)     # Convert UTF code point to character
# 'A'
```

## $\color{steelblue}\text{Numbers}$

### $\color{teal}\text{Binary Representation}$

Binary numbers are analogous to base-$10$ notation:

- Starts at position $0$, the right-most numeral
- Position $j$ gets a multiplier of $2^j$
- Add up all values

Example, $\tt1010$, starting from position $0$:

- $0 \text{ has multiplier of } 2^0 = 1$
- $1 \text{ has multiplier of } 2^1 = 2$
- $0 \text{ has multiplier of } 2^2 = 4$
- $1 \text{ has multiplier of } 2^3 = 8$
- $\text{total is } 10$

### $\color{teal}\text{4-Bit Binary}$

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c:c}
   base-10 & base-2 & base-10 & base-2 \\ \hline
   0 & \tt0000 & 8 & \tt1000 \\
   \hdashline
   1 & \tt0001 & 9 & \tt1001 \\
   \hdashline
   2 & \tt0010 & 10 & \tt1010 \\
   \hdashline
   3 & \tt0011 & 11 & \tt1011 \\
   \hdashline
   4 & \tt0100 & 12 & \tt1100 \\
   \hdashline
   5 & \tt0101 & 13 & \tt1101 \\
   \hdashline
   6 & \tt0110 & 14 & \tt1110 \\
   \hdashline
   7 & \tt0111 & 15 & \tt1111
\end{array}
$$

### $\color{teal}\text{8-Bit Binary}$

Storing positive numbers $(0 ... 255)$, as 8-bit strings:

$$
\stackrel{7}{\sum_{\substack{j=0}}}
2^j\overline{x}_j
$$

### $\color{teal}\text{Adding Binary Numbers}$

Adding two 1-bit numbers:

$$
\begin{align}
0+0&=0 \\
1+0&=1 \\
0+1&=1 \\
1+1&=10
\end{align}
$$

### $\color{teal}\text{Bit Operations}$

Given two 1-bit numbers, $\overline{x}$ and $\overline{y}$, their binary sum is a 2-bit string $\overline{z}$ where:

$$
\begin{align}
   \overline{z}_0 &= \overline{x}_0 \wedge \overline{y}_0 \\[1em]
   \overline{z}_1 &= \overline{x}_0 \And \overline{y}_0
\end{align}
$$

For $n$-bit binary numbers $\overline{x}$ and $\overline{y}$, the sum in binary $\overline{z}$ is a $n+1$-bit binary number where:

$$
\begin{align}
   \overline{z}_j &= \overline{x}_j \wedge \overline{y}_j \wedge \overline{c}_j
   \\[1em]
   \overline{c}_{j+1} &= (\overline{x}_j \And \overline{y}_j) \mid (\overline{x}_j \And \overline{c}_j) \mid (\overline{y}_j \And \overline{c}_j)
\end{align}
$$

The string $\overline{c}$ is the carry bits (take $\overline{c}_0$ to be $0$). The equation for $\overline{c}_{j+1}$ says it is 1 when $\overline{x}_j + \overline{y}_j + \overline{c}_j$ is 2 or 3.

### $\color{teal}\text{Negative Numbers}$

Properties of 2's complement:

- For $n$ bits, can represent $-2^{n-1}$ through to $2^{n-1}-1$
- Leftmost bit is $1$ for negative numbers
- Addition is $\mod 2^n$
- Positive numbers $0$ to $2^{n-1}-1$ are unchanged

### $\color{teal}\text{3-Bit 2's Complement}$

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c}
   \text{bit string} & \text{2's comp interpretation} & \text{binary interpretation} \\ \hline
   \tt000 & 0 & 0 \\
   \hdashline
   \tt001 & 1 & 1 \\
   \hdashline
   \tt010 & 2 & 2 \\
   \hdashline
   \tt011 & 3 & 3 \\
   \hdashline
   \tt100 & -4 & 4 \\
   \hdashline
   \tt101 & -3 & 5 \\
   \hdashline
   \tt110 & -2 & 6 \\
   \hdashline
   \tt111 & -1 & 7
\end{array}
$$

### $\color{teal}\text{Hexadecimal}$

- Base-64 number system - number in position $j$ gets a multiplier of $16^j$.
- Compact method for writing bit strings

### $\color{teal}\text{4-Bit Hex}$

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c||c:c:c}
   \text{symbol} & \text{bit string} & \text{base-10} & \text{symbol} & \text{bit string} & \text{base-10} \\ \hline
   0 & \tt0000 & 0 & 8 & \tt1000 & 8 \\
   \hdashline
   1 & \tt0001 & 1 & 9 & \tt1001 & 9 \\
   \hdashline
   2 & \tt0010 & 2 & \sf A & \tt1010 & 10 \\
   \hdashline
   3 & \tt0011 & 3 & \sf B & \tt1011 & 11 \\
   \hdashline
   4 & \tt0100 & 4 & \sf C & \tt1100 & 12 \\
   \hdashline
   5 & \tt0101 & 5 & \sf D & \tt1101 & 13 \\
   \hdashline
   6 & \tt0110 & 6 & \sf E & \tt1110 & 14 \\
   \hdashline
   7 & \tt0111 & 7 & \sf F & \tt1111 & 15
\end{array}
$$

### $\color{teal}\text{Interpreting Hex}$

$\text{given:}$
$\sf4F = 4 \rarr \tt0100\; \text{ and }\; \sf F \rarr \tt1111 = 01001111$
$\\[1em]\text{then:}$
$\sf4F = \tt01001111$

- Shorter than bit strings
- One hex numeral is always exactly 4 bits
- Easy to work with individual bits

### $\color{teal}\text{Python Hex}$

```python
>>> hex(65532)                          # Hex string from integer
# '0xfffc'
>>> "The number is {:x}".format(65532)  # Alternative method
# 'The number is fffc'
>>> 0xfffc                              # Hex literal integer
# 65532
```

### $\color{teal}\text{Scientific Notation}$

$$
\begin{align}
   \pm a.bc&\times10^e
\end{align}
$$

- $\textbf{Sign: } \quad \pm$
- $\textbf{Significant digits: } \quad a.bc$
- $\textbf{Exponent: } \quad e$
- $\textbf{Base: } \quad 10$

The base is always shared across the significant digits

### $\color{teal}\text{Scientific Notation in Base 2}$

- Significant digits are bits
- Exponent is written in binary

$$
\begin{align}
   \mathtt{1.1010} &\times 2^{10}
\end{align}
$$

### $\color{teal}\text{Floting Point Numbers}$

Computers represent scientific notation as floating point numbers, encoding in binary:

- Significant digits
- Exponent
- Sign (positive or negative)
- With base 2

### $\color{teal}\text{IEEE Half-Precision}$

IEEE 754 floating point standard for 16 bits:

$$
\begin{align}
   \overbrace{0}^s &\overbrace{10101}^e \overbrace{1010101010}^f
\end{align}
$$

- $\textbf{Sign: } \quad s$ (1-bit)
- $\textbf{Exponent: } \quad e$ (5 bits)
- $\textbf{Significant digits: } \quad f$ (10 bits dropping leading 1)

### $\color{teal}\text{Python Numers}$

Basic number types:

- $\tt int$
  - Arbitrary length integers
  - Special base-$2^{30}$
- $\tt float$
  - IEEE 754 double precision
    - 64-bit floating point

```python
>>> 9/2     # Regular division always returns float
# 4.5
>>> 9//2    # Floor division returns integer
# 4
```

## $\color{steelblue}\text{Recursion}$

### $\color{teal}\text{Recursive Definitions}$

Factorial function on $\Bbb{N}$ defined as:

$$
\begin{align}
   n! = \stackrel{n}{\prod_{\substack{j=1}}}j
   &= 1\cdot 2 \cdots (n-1) \cdot n
\end{align}
$$

Also $n$! recursively:

$$
\begin{align}
   n! &= \begin{cases}
      1 &: n=1 \\
      n(n-1)! &: n>1
   \end{cases}
\end{align}
$$

Two main parts:

- $\textbf{Base case:}$ evaluated without reference to object
  - Required, though potentially multiple
- $\textbf{Recursive case:}$ refer back to object definition
  - More complex than base

### $\color{teal}\text{Fibonacci Sequence}$

Fibonacci sequence is classic example of recursion:

$$
\begin{align}
   f(n) &= \begin{cases}
      1 &: n=1 \\
      1 &: n=2 \\
      f(n-1)+f(n-2) &: n>2
   \end{cases}
\end{align}
$$

### $\color{teal}\text{Fibonacci in Python}$

```python
def F(n):
   if n == 1: return 1
   elif n == 2: return 1
   else: return F(n-1) + F(n-2)
```

### $\color{teal}\text{Arithmetic Expression}$

Programming languages often expressed as multiple types in recursion:

$$
\begin{align}
   EXPR &:= \begin{cases}
      VALUE\\
      EXPR\; \text{\textquotedblleft}+"\ VALUE\\
      EXPR\; \text{\textquotedblleft}-"\ VALUE
   \end{cases}\\[1em]
   VALUE &:= \begin{cases}
      CONSTANT\\
      VARIABLE
   \end{cases}
\end{align}
$$

## $\color{steelblue}\text{Propositional Logic}$

- Propositions are true or false statements
- Logical connectives use propositions to build larger ones
- $p$ and $q$ often represent propositions

### $\color{teal}\text{Atomic and Compound Propositions}$

- $\textbf{Atomic: } \quad \text{"It is raining"}$
- $\textbf{Compound: } \quad \text{"It is raining and cloudy"}$

## $\color{steelblue}\text{Logical Operators}$

- $\textit{NOT, } \textbf{negates truth: } \quad \lnot$
- $\textit{AND, } \textbf{requires both: } \quad \wedge$
- $\textit{OR, } \textbf{allows either: } \quad \vee$
- $\textit{XOR, } \textbf{requires either: } \quad \oplus$
- $\textit{IF..THEN: } \quad \rarr$
- $\textit{IF AND ONLY IF: } \quad \harr$

### $\color{teal}\text{IF..THEN}$

- $p \rarr q$ means $q$ must be true whenever $p$ is, regardless of $p$
- When $p$ is false, $p \rarr q$ is always true
- $(p \rarr q)\space =\space (\text{if } p \text{ then } q)\space =\space (p \text{ implies } q)$

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c}
   p & q & p \rarr q \\ \hline
   T & T & T \\
   \hdashline
   T & F & F \\
   \hdashline
   F & T & T \\
   \hdashline
   F & F & T
\end{array}
$$

### $\color{teal}\text{IF AND ONLY IF}$

- $p \harr q$ means both must have the same truth value
- $(p \harr q)\space =\space ((p \rarr q)\wedge(q \rarr p))\space =\space (p \text{ if and only if } q)$

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c}
   p & q & p \harr q \\ \hline
   T & T & T \\
   \hdashline
   T & F & F \\
   \hdashline
   F & T & F \\
   \hdashline
   F & F & T
\end{array}
$$

## $\color{steelblue}\text{Formulas}$

$\textit{Boolean formulas}$ are strings of symbols to build compond propositions.

$\textbf{Formula rules (listed by precedence):}$

- $T$, $F$ and lower case letters are all formulas
- If $A$ and $B$ are formulas then so are:
  - $(A)$
  - $\lnot A$
  - $A \oplus B$
  - $A \wedge B$
  - $A \vee B$
  - $A \rarr B$
  - $A \harr B$
- No other strings are formulas

### $\color{teal}\text{Formula Truth Value}$

- Fill in truth table
- Evaluate logical connectives from innermost parentheses outwards

When $p = T$ and $q = F$:

$$
\begin{equation}
\begin{split}(p\vee q)\rarr (q\oplus p)
   &=(T\vee F) \rarr (F\oplus T)\\
   &=T\rarr T\\
   &=T
\end{split}
\end{equation}
$$

### $\color{teal}\text{Formula Classification}$

- $\textbf{Tautologies: } \quad$ always $T\\[1em]$
- $\textbf{Contradictions: } \quad$ always $F\\[1em]$
- $\textbf{Contingent formulas: } \quad T$ OR $F$ depending on variables $\\[1em]$
- $\textbf{Satisfiable formulas: } \quad \textit{tautologies}$ OR $\textit{contingent formulas}\\[1em]$

## $\color{steelblue}\text{Logical Equivalence}$

$$
\begin{align}
   A \rarr B &\equiv \lnot A \vee B
\end{align}
$$

$$A \equiv B\ \text{ is the same as stating: \textquotedblleft} A \harr B\ \text{ is a \textit{tautology}"}$$

$$
\begin{equation}
\begin{split}A\rarr B
   &\equiv \lnot A\wedge B\\
   &\equiv B\wedge \lnot A\\
   &\equiv \lnot(\lnot B)\wedge \lnot A\\
   &\equiv \lnot B \rarr \lnot A
\end{split}
\end{equation}
$$

## $\color{steelblue}\text{Set Theory}$

- $\textbf{Set: }\quad S$
- $\textbf{In set: }\quad \in$
- $\textbf{Not in set: }\quad \notin$

  $$
  \begin{align}
     \nonumber\textbf{Set listing: }\\
     SMALLPRIMES=\ &\set{1,2,3,5,7}\\[2em]
     \nonumber\textbf{Implied pattern: }& \textit{(bad practice)}\\
     EVENS=\ &\set{2,4,6,8,\dots}\\[2em]
     \nonumber\textbf{Setbuilder notation: }& \text{\textquotedblleft set comprehension"}\\
     \nonumber\text{Subset of elements, } &\text{that match a condition}\\
     &\set{x\in S:\phi(x)}\\
     SQUARES=\ &\set{x\in \Bbb{Z}:x=y^2 \text{ for some }y\in \Bbb{Z}}\\[2em]
     \nonumber\textbf{Setbuilder notation: }& \text{\textquotedblleft replacement"}\\
     \nonumber\text{Apply a theory to } &\text{each member and collect results}\\
     &\set{f(x):x\in S}\\
     SQUARES=\ &\set{x^2:x\in \Bbb{Z}}\\[2em]
  \end{align}
  $$

### $\color{teal}\text{Set Equality}$

$S=T$ when:

- Every element $x\in S$ is in $T$
- Every element $x\in T$ is in $S$
- Regardless of order, repetition, and representation:

$$
\begin{align}
   \set{1,2,3} &= \set{3,2,1}\\
   \set{1,1,1} &= \set{1}\\
   \set{x\in \Bbb{Z}:x^2=4} &= \set{2,-2}
\end{align}
$$

### $\color{teal}\text{Set Size}$

$$
\begin{align}
   |\set{1,2,3}|&=3\\
   |\set{1,1,1}|&=1
\end{align}
$$

### $\color{teal}\text{Sub Sets}$

- $\textbf{Subset: }\quad \text{every }x\in A \text{ is in }B:\quad A\subseteq B\\[1em]$
- $\textbf{Proper subset: }\quad A \text{ is subset of, yet not equal to }B:\quad A\subset B\\[1em]$
- $\textbf{Equality through subsets: }\quad S\subseteq T \And T\subseteq S\\[1em]$

Subset equivalence:

$$
\begin{align}
   A\subset B&\equiv A\subseteq B \wedge A\not = B
\end{align}
$$

The set of all subsets of a set $S$ is called the $\textit{power set}$ of $S$:

$$
\begin{align}
   P(\set{1,2})&=\set{\emptyset,\set{1},\set{2},\set{1,2}}
\end{align}
$$

### $\color{teal}\text{Set Operations}$

$$
\begin{align}
   \nonumber\textbf{Union: }&\text{everything in either}\\
   \nonumber\text{Must define }A\cup B &\text{ to be the smallest set, such that }A\subseteq S \And B\subseteq S\\
   \text
   A\cup B=\ &\set{x:x\in A\vee x\in B}\\[1em]
   \nonumber\textbf{Intersection: }&\text{everything in \textit{both} sides}\\
   A\cup B=\ &\set{x\in A: x\in B}\\[1em]
   \nonumber\textbf{Difference: }&\text{remove items in one set from the other}\\
   A\setminus B=\ &\set{x\in A: x\notin B}\\[1em]
\end{align}
$$

### $\color{teal}\text{Universe Sets}$

- The universe $U$ is the set containing all elements of concern
- Enables definition of complements:

$$
\begin{align}
   \overline{S} &= \set{x\in U: x\notin S}
\end{align}
$$

Set comprehensions without specifying the set, as with $U=\Bbb{Z}^+$:

$$
\begin{align}
   COMPOSITES &= \overline{PRIMES}\\
   EVENS &= \set{x:x=2y}\\
   ODDS &= \overline{EVENS}\\
\end{align}
$$

### $\color{teal}\text{Characteristic Vectors}$

Universes of manageable size may be represented as bit strings (characteristic vectors):

- Let $n=|U|$
- Number elements like so, $U=\set{e_1,e_2,\dots e_n}$
- $XS = XS_1XS_2\dots XS_n$ where:
  $$
  \begin{align}
     XS_j&=
     \begin{cases}
        0\quad e_j\notin S\\
        1\quad e_j\in S
     \end{cases}
  \end{align}
  $$
  - Example: $\ U=\set{1,2,3}$ then $\ X_{\set{1,3}}=\tt101$, $\ X_{\set{2}}=\tt010$
  - Set operations such as $\cup$ and $\cap$ become bitwise operators

### $\color{teal}\text{Python Sets}$

```python
>>> S = {1,2,3}; T = {1,3,5}     # Braces define sets
>>> S.add(4); print(S)           # Sets are mutable
# {1, 2, 3, 4}
>>> S.remove(4); print(S)
# {1, 2, 3}

>>> 1 in S                       # Testing membership
# True
>>> 4 in S
# False

>>> S.issubset({1,2,3,4,5})      # Testing subset
# True
>>> S <= {1,2,3,4,5}             # Alternative subset test
# True

>>> S.union(T)                   # Using union
# {1, 2, 3, 5}
>>> S|T                          # Alternative union
# {1, 2, 3, 5}
>>> S.union(T, {8,9}, {10,11})   # Multiple union
# {1, 2, 3, 5, 8, 9, 10, 11}
>>> someSets = [S, T, {8,9}, {10,11}]
>>> set.union(*someSets)         # Splat operator
# {1, 2, 3, 5, 8, 9, 10, 11}

>>> S.intersection(T)            # Splat and multi-sets would also work
# {1, 3}
>>> S & T                        # Alternative intersection
# {1, 3}

>>> S - T                        # Testing difference
# {2}

>>> S.isdisjoint(T)              # is S & T empty?
# False

>>> len(S)                       # Size of S
# 3

# Setbuilder notation combines of comprehension and replacement:
>>> S = {0, 2, 4, 6, 8}
>>> def p(x): return x % 2 == 0
...
>>> def p(x): return x * 5
...
>>> { f(x) for x in S if p(x) }
# {0, 40, 10, 20, 30}
>>> { s * 5 for s in range(0, 10) if s % 2 == 0 }
# {0, 40, 10, 20, 30}
```

### $\color{teal}\text{Zermelo-Fraenkel Set Theory}$

ZF set theory, seven axioms to define set behaviour:

1. Two sets containing same elements are equal
   $\\[2em]$
2. Every set S other than $\emptyset$ contains at least one element $y$, also $S$ and $y$ are disjoint
   $\\[2em]$
3. If $S$ is a set and $\phi(x)$ is a formula, then there is a set that contains exactly the elements of $S$ that satisfies $\phi(x)$
   $\\[2em]$
4. If $S_1, S_2,\dots$ are sets, then there is a set that contains all of the elements of every $S_j$
   - $\textit{Allows unions}$
     $\\[2em]$
5. If $S$ is a set and $f(x)$ is a function, then there is a set that contains $f(x)$ for every $x\in S$
   - $\textit{Allows replacements such as:}\ \set{f(x):x\in S}$
     $\\[2em]$
6. Given $S_0=\emptyset$ and $S_j={S_{j-1}}$, there is a set that contains every $S_j$
   $\\[2em]$
7. For a set $S$, there is a set containing every possible subset of $S$
   - $\textit{Allows power sets}$

### $\color{teal}\text{Replacements From ZF Axioms}$

ZF replacements from axioms 1, 3, and 5:

- Start with set $S$ and function $f(x)$
- Use axiom 5 to obtain set $A$ containing $f(x)$ whenever $x\in S$
- Create formula $\phi(y)$ so $x\in S$, such that $f(x)=y$
- Use axiom 3 to obtain set $A'$ containing every $y\in A$ such that $\phi(y)$ is true

$A'$ is the resulting set.

### $\color{teal}\Bbb{Z}_{\ge0}\text{ From Set Theory}$

Peano's axioms to construct set of non-negative integers:

- What is 0
- A successor function $S(\cdot)$ that takes a number to the next one: $\\ S(1)=2, S(2)=3\dots$
  Define empty set, $\emptyset$, as $0$ and define a successor function by $S(n)=n\cup \{n\}$:
- $\text{\textquotedblleft}0'':=\emptyset=\{\}$
- $\text{\textquotedblleft}1'':=S(\text{\textquotedblleft}0'')=\text{\textquotedblleft}0''\cup\{\emptyset\}=\{\{\}\}$
- $\text{\textquotedblleft}2'':=S(\text{\textquotedblleft}1'')=\text{\textquotedblleft}1''\cup\{\text{\textquotedblleft}1''\}=\{\emptyset,\{\emptyset\}\}=\{\{\},\{\{\}\}\}$
  $\vdots$
- $S(n)=n\cup\{n\}$

## $\color{steelblue}\text{Syllogisms}$

Syllogisms are deductive reasoning upon sets:

- Start with $\textit{premises}$ (statements), taken to be true
- Apply valid form of argument
- Draw conclusion
- If $\textit{premises}$ are true, then impossible for conclusion to be false:

$$
\begin{align}
   \nonumber\text{All humans are mortal } &\textit{(major premise)}\\
   \nonumber\text{Socrates is human } &\textit{(minor premise)}\\
   \hline
   \text{Socrates is mortal } &\textit{(conclusion)}
\end{align}
$$

### $\color{teal}\text{Set Theoric Syllogisms}$

$$
\begin{align}
   \nonumber HUMANS &\subseteq MORTALS\\
   \nonumber s &\in HUMANS\\
   \hline
   s &\in MORTALS
\end{align}
$$

### $\color{teal}\text{Syllogism Types}$

Abstracted to $\textit{syllogism type:}$

$$
\begin{align}
   \nonumber A &\subseteq B\\
   \nonumber x &\in A\\
   \hline
   x &\in B
\end{align}
$$

This is $\textit{valid}$ type, so works for any $A, B, x$ provided the $\textit{premises}$ are true

24 valid sylligism types in total, such as:

$$
\begin{align}
   \nonumber\text{All trees are plants}&\quad (A\subseteq B)\\
   \nonumber\text{Some trees are tall}&\quad (A\cap C\not =\emptyset)\\
   \hline
   \text{Some plants are tall}&\quad (B\cap C\not =\emptyset)
\end{align}
$$

$\\[2em]$

$$
\begin{align}
   \nonumber\text{All cats are mammals}&\quad (A\subseteq B\ and\ A\not =\emptyset)\\
   \nonumber\text{All cats are carnivores}&\quad (A\subseteq C)\\
   \hline
   \text{Some mammals are carnivores}&\quad (B\cap C\not =\emptyset)
\end{align}
$$

$\\[2em]$

## $\color{steelblue}\text{Logical Implication}$

- From $A \wedge B$, can conclude $A$
- From $(A\to B)\wedge A$, can conclude $B$
- $\textbf{Implication: }\quad A\models B$

If from $A$, can conclude $B$, then $A\models B$, then $A\to B$ is a tautology

Whenever $A$ is true, so is $A\vee B$, thus $\ A\models A\vee B$:

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:cc}
   A & B & A \vee B \\ \hline
   T & T & T & \larr\\
   \hdashline
   T & F & T & \larr\\
   \hdashline
   F & T & T & (ignore)\\
   \hdashline
   F & F & F
\end{array}
$$

Given $A\models A\wedge B$, then $A\to A\vee B$ is a tautology

$$
\def\arraystretch{1.5}
   \begin{array}{c:c:c:c}
   A & B & A \vee B & A\to A\vee B\\ \hline
   T & T & T & T \\
   \hdashline
   T & F & T & T \\
   \hdashline
   F & T & T & T \\
   \hdashline
   F & F & F & T
\end{array}
$$

### $\color{teal}\text{Implication Substitutions}$

- Given $A\wedge B\models A$, if just $A\wedge B$ is true, then may replace with $A$
- From $\text{\textquotedblleft it is cloudy and raining"}$, can conclude $\text{\textquotedblleft it is raining"}$

## $\color{steelblue}\text{Proofs}$

Given:

- Socrates is mortal or Socrates is not human
- Socrates is human

...then conclude:

- Socrates is not human or Socrates is mortal
  - $\textit{equivalence}$
- Socrates is mortal
  - $\textit{logical implication}$

A proof is a list of formulas starting with premises and every formula must be:

- Logically equivalent to a formula above
- Logically implied by a formula above
- The $AND$ of some formulas above
- Logicaly implied by the $AND$

A proof produces $P\models Q$, where:

- $P$ is the $AND$ of all premises
- $Q$ is the last line of the proof

Proof says: assuming all premises are true, the conclusion is also true

Socrates proof: $\quad(M\vee \lnot H)\wedge H\models M:\\[2em]$

$$
\begin{align}
   \nonumber &1\quad M\vee \lnot H\quad &\text{premise}\\[0.1em]
   \nonumber &2\quad H\quad &\text{premise}\\[0.1em]
   \hline
   \nonumber &3\quad \lnot H\vee M\quad &\text{equivalent to line 1 using } A\vee B\equiv B\vee A\\[0.1em]
   \nonumber &4\quad\lnot\lnot H\quad &\text{equivalent to line 1 using } A\equiv\lnot\lnot A\\[0.1em]
   &5\quad M\quad &\text{implication of line 3 } AND \text{ 4 using }\\\nonumber&&(A\vee B)\wedge\lnot A\models B \text{, with }A\models\lnot H\; AND\; B=M \\[0.1em]
\end{align}
$$

## $\color{steelblue}\text{Predicate Logic}$

### $\color{teal}\text{Parameters and Predicates}$

Generalise propositions by allowing $\textit{parameters}$:

$$
\begin{align}
   A(x)&=x \text{ is a cat }\\
   B(x,y)&=x \text{ and } y \text{ have the same birthday}\\
   C(x,y)&=x=y+1\\
\end{align}
$$

- Parameters allow generic references to propositions that share a common form and meaning

- Predicates are propositions with one or more variables

Form complex predicates from smaller ones:

- $A(x)\wedge B(x) \quad\text{ understood that }x\text{ is the same for both}\\[1em]$
- $A(x)\vee B(y) \quad\text{ can have different parameters}\\[1em]$
- $A(x)\to B(x)\\[1em]$
- $A((x)\to B(y))\wedge A(x)\\[1em]$

To evaluate truths, must fill parameters:

- Suppose $\, A(x)$ is $x^2=1$.
  - Then $A(1)$ is True, but $A(2)$ is False.$\\[1em]$
- Suppose $\, A(x)$ is $x\text{ is a flower}\to x\text{ smells nice}$.
  - Then $A(rose)$ is True, but $A(raffelesia)$ is False.$\\[1em]$
- Suppose $\, A(x)$ is $\text{if }x\text{ is human then }x\text{ is mortal}$.
  - Then $A(Socrates)$ is True$\\[1em]$

Predicates with all variables defined, become regular propositions with truth values

### $\color{teal}\text{Quantifiers}$

Quantifiers are symbols that refer to parameters within predicates:

- $\textbf{Existential quantification, }\textit{there exists: }\quad \exists\\[1em]$
- $\textbf{Universal quantification, }\textit{for all:}\quad \forall\\[1em]$

Quantifiers allow propositions out of predicates without parameter values

### $\color{teal}\text{Existential Quantification}$

$$
\begin{align}
   \nonumber\exists x\in \Bbb{Z}(&x^2=4)\\
   \text{there exists an }x\text{ from }\Bbb{Z}\text{ such that } &x^2=4\\[1em]
   \nonumber\exists x\in S\ p(&x)\\
   \text{there exists an }x\text{ in }S\text{ such that } p(&x)\text{ is True}\\[1em]
   \nonumber\exists x\in ANIMALS(&x \text{ is a fish}) \\
   \text{there exists an }x\text{ in }ANIMALS\text{ such that } &x\text{ is a fish}\\[1em]
   \nonumber\exists x\in \Bbb{R}(&x\in \Bbb{Z})\\
   \text{there exists some real number }x\text{ such that } &x\text{ is an integer}\\[1em]
\end{align}
$$

### $\color{teal}\text{Universal Quantification}$

$$
\begin{align}
   \nonumber\forall x\in \Bbb{Z}(&x^2)\\
   \text{for every }x\text{ in }\Bbb{Z},\ &x^2\text{ is non-negative}\\[1em]
   \nonumber\forall x\in S\ p(&x)\\
   \text{for all }x\text{ from }S,\ p(&x)\text{ is True }\\[1em]
   \nonumber\forall x\in ANIMALS(&x \text{ is a fish})\\
   \text{for all }x\text{ in }ANIMALS,\ &x\text{ is a fish}\\[1em]
   \nonumber\forall x\in \Bbb{Z}(&x\in \Bbb{R})\\
   \text{all integers are }&\text{real numbers }\\[1em]
\end{align}
$$

### $\color{teal}\text{Quantify Over Sets}$

Explicit set specification, to quantify over $S$:

$$
\begin{align}
   \forall x\in S\ p(&x)
\end{align}
$$

Implicit set specification, to quantify over a set, $\textit{out of context}$:

$$
\begin{align}
   \forall x\ p(&x)
\end{align}
$$

### $\color{teal}\text{Parameters in Predicates}$
