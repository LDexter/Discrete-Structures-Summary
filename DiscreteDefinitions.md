# $\color{dodgerblue}\text{CAB203: Discrete Structures Definitions}$

$\textit{Author not responsible for consequences caused by any innacuracies.}$

## $\color{steelblue}\text{Markdown Setup}$

Open in Visual Studio Code and install Markdown Preview Enhanced:
https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced

## $\color{steelblue}\text{Typesetting Powered by} \thickspace \KaTeX$

$\KaTeX$ documentation: https://katex.org/
which uses $\LaTeX\textit{-like}$ syntax to display mathematical syxbols

## $\color{steelblue}\text{Equivalence}$

$$
\begin{align}
    \text{Equals: } &\quad =\\[1em]
    \text{Greater than: } &\quad >\\[1em]
    \text{Greater than or equal to: } &\quad \ge\\[1em]
    \text{Less than: } &\quad <\\[1em]
    \text{Less than or equal to: } &\quad \le\\[1em]
    \text{Not equal to: } &\quad \not =\\[1em]
    \text{Modular equivalence: } &\quad \equiv\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Operators}$

$$
\begin{align}
    \text{Multiply: } &\quad \cdot\\[1em]
    \text{Mod: } &\quad \bmod\\[1em]
    \text{Implication: } &\quad \models\\[1em]
    \textit{NOT: } &\quad \lnot\\[1em]
    \textit{AND, } &\quad \wedge\\[1em]
    \textit{OR, } &\quad \vee\\[1em]
    \textit{XOR, } &\quad \oplus\\[1em]
    \textit{IF..THEN: } &\quad \rarr\\[1em]
    \textit{IF AND ONLY IF: } &\quad \harr\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Formula Classification}$

$$
\begin{align}
    \textbf{Tautologies: } &\quad always T\\[1em]
    \textbf{Contradictions: } &\quad always F\\[1em]
    \textbf{Contingent formulas: } &\quad T\ or\ F\quad \text{depending on variables} \\[1em]
    \textbf{Satisfiable formulas: } &\quad \textit{tautologies }\ or\ \textit{ contingent formulas}\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Set Theory Abstractions}$

$$
\begin{align}
    \text{Set: }&\quad S\\[1em]
    \text{Universe: }&\quad U\\[1em]
    \text{Member in set: }&\quad \in\\[1em]
    \text{Not member in set: }&\quad \notin\\[1em]
    \textbf{Real, } \textit{any number: }&\quad \Bbb R\\[1em]
    \textbf{Integer, } \textit{only whole: }&\quad \Bbb Z\\[1em]
    \textbf{Natural}\ _0\textbf{, } \textit{whole non-negatives: }&\quad \Bbb N_0\\[1em]
    \textbf{Natural}\ _1\textbf{, } \textit{whole positives: }&\quad \Bbb N_1\\[1em]
    \text{Subset: } &\quad A\subseteq B\\[1em]
    \text{Proper subset: } &\quad A\subset B\\[1em]
    \text{Equality through subsets: } &\quad S\subseteq T \And T\subseteq S\\[2em]
\end{align}
$$

## $\color{steelblue}\text{Set Constructors}$

$$
  \begin{align}
     \nonumber\textbf{Set listing: }\\
     SMALLPRIMES=\ &\set{1,2,3,5,7}\\[2em]
     \nonumber\textbf{Implied pattern: }&\textit{(bad practice)}\\
     EVENS=\ &\set{2,4,6,8,\dots}\\[2em]
     \nonumber\textbf{Setbuilder notation: }&\text{\textquotedblleft set comprehension"}\\
     \nonumber\text{Subset of elements, }&\text{that match a condition}\\
     \set{x\in S&:\phi(x)}\\
     SQUARES=\ \set{x\in \Bbb{Z}&:x=y^2 \text{ for some }y\in \Bbb{Z}}\\[2em]
     \nonumber\textbf{Setbuilder notation: }&\text{\textquotedblleft replacement"}\\
     \nonumber\text{Apply a theory to }&\text{each member and collect results}\\
     \set{f(x)&:x\in S}\\
     SQUARES=\ \set{x^2&:x\in \Bbb{Z}}\\[2em]
  \end{align}
$$

## $\color{steelblue}\text{Set Operators}$

$$
\begin{align}
   \nonumber\textbf{Union: }&\text{everything in either}\\
   \nonumber\text{Must define }A\cup B &\text{ to be the smallest set, such that }A\subseteq S \And B\subseteq S\\
   \text
   A\cup B=\ &\set{x:x\in A\vee x\in B}\\[1em]
   \nonumber\textbf{Intersection: }&\text{everything in \textit{both} sides}\\
   A\cap B=\ &\set{x\in A: x\in B}\\[1em]
   \nonumber\textbf{Difference: }&\text{remove items in one set from the other}\\
   A\setminus B=\ &\set{x\in A: x\notin B}\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Predicates}$

$$
\begin{align}
    \text{Existential quantification, }\textit{there exists: }\quad \exists\\[1em]
    \text{Universal quantification, }\textit{for all:}\quad \forall\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Exponents}$

$$
\begin{align}
    \text{Exponent in }a^3: &\quad 3\\[1em]
    \text{Base in }a^3: &\quad a\\[1em]
    \text{kilo: }&\quad 2^{10}\\[1em]
    \text{mega: }&\quad 2^{20} = (2^{10})^2\\[1em]
    \text{giga: }&\quad 2^{30} = (2^{10})^3\\[1em]
    \text{tera: }&\quad 2^{40} = (2^{10})^4\\[1em]
    \text{peta: }&\quad 2^{50} = (2^{10})^5\\[1em]
    \text{exa: }&\quad 2^{60} = (2^{10})^6\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Laws of Exponents}$

$$
\begin{align}
    (ab)^n &= a^n \cdot b^n \\[1em]
    a^m \cdot a^n &= a^{m+n} \\[1em]
    a^{m-n} &= \dfrac{a^m}{a^n}\quad (\text{when } a \not&= 0) \\[1em]
    a^{-n} &= \dfrac{1}{a^n}\quad (\text{when } a \not&= 0) \\[1em]
    a^0 &= 1 \\[1em]
    (a^m)^n &= a^{m \cdot n} \\[1em]
\end{align}
$$

## $\color{steelblue}\text{Laws of Logarithms}$

$$
\begin{align}
    \log_a 1 &= 0 \\[2em]
    \log_a a &= 1 \\[2em]
    \log_a (x \cdot y) &= \log_a x + \log_a y \\[2em]
    \log_a x^y &= y \log_a x \\[2em]
    \log_a \dfrac{1}{y} &= - \log_a y \\[2em]
    \log_a \dfrac{x}{y} \\[2em]
    \log_b x &= (\log_b a) \cdot \log_a x \\[2em]
\end{align}
$$

## $\color{steelblue}\text{Ceiling and Floor}$

$$
\begin{align}
    \text{Ceiling, round up:} &\quad \lceil a \rceil\\[1em]
    \text{Floor, round down:} &\quad \lfloor a \rfloor\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Bits}$

$$
\begin{align}
    \text{Bit string: } &\quad \overline{x}\\[1em]
    \text{Mod: } &\quad \bmod\\[1em]
    \texttt{NOT: } &\quad \backsim\\[1em]
    \texttt{AND: } &\quad \And\\[1em]
    \texttt{OR: } &\quad \mid\\[1em]
    \texttt{XOR: } &\quad \text{\large\textasciicircum}\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Scientific Notation}$

$$
\begin{align}
    \text{Sign: } &\quad \pm\\[1em]
    \text{Significant digits: } &\quad a.bc\\[1em]
    \text{Exponent: } &\quad e\\[1em]
    \text{Base: } &\quad 10\\[1em]
\end{align}
$$

## $\color{steelblue}\text{IEEE Half-Precision}$

$$
\begin{align}
   \overbrace{0}^s &\overbrace{10101}^e \overbrace{1010101010}^f\\[2em]
\text{Sign: } &\quad s (1-bit)\\[1em]
\text{Exponent: } &\quad e (5 bits)\\[1em]
\text{Significant digits: } &\quad f \text{(10 bits dropping leading 1)}\\[1em]
\end{align}
$$

## $\color{steelblue}\text{Recursion}$

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

Fibonacci sequence:

$$
\begin{align}
   f(n) &= \begin{cases}
      1 &: n=1 \\
      1 &: n=2 \\
      f(n-1)+f(n-2) &: n>2
   \end{cases}
\end{align}
$$

## $\color{steelblue}\text{Python}$

```python
"""
MODULO OPERATOR
"""

print(17 % 4) # Prints 1 to the console
# 1



"""
EXPONENTS AND LOGARITHMS
"""

>>> import math         # Must import math library
>>> math.log2(8)        # log2 means log base 2 and returns a float (decimal)
# 3.0
>>> 2 ** 3              # ** is exponentiation
# 8
>>> math.log2(100) / math.log2(10)  # base transformation
# 2.0



"""
UFT-8
"""

>>> ord('A')    # Convert character to UTF code point
# 65
>>> chr(65)     # Convert UTF code point to character
# 'A'



"""
HEXADECIMAL
"""

>>> hex(65532)                          # Hex string from integer
# '0xfffc'
>>> "The number is {:x}".format(65532)  # Alternative method
# 'The number is fffc'
>>> 0xfffc                              # Hex literal integer
# 65532



"""
NUMBERS
"""

>>> 9/2     # Regular division always returns float
# 4.5
>>> 9//2    # Floor division returns integer
# 4



"""
FIBONACCI
"""

def F(n):
if n == 1: return 1
elif n == 2: return 1
else: return F(n-1) + F(n-2)



"""
SET THEORY
"""

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



"""
PREDICATES AND QUANTIFIERS
"""

>>> def p(x,y):      # Any function that returns T/F to be used as predicate
   return x >= y
>>> p(2,1)
# True

>>> def p(x): return x >= 0
>>> S = { -1, 0, 1 }; T = { 0, 1, 2 }
>>> Sp = [ p(x) for x in S ]  # List of booleans
>>> Tp = [ p(x) for x in T ]  # List of booleans
>>> all(Tp)                   # Check for all: ALL True
# True
>>> all(Sp)                   # Check there  exists: at least ONE True
# True
>>> any(p(x) for x in S)      # Generator expression
# True
```
