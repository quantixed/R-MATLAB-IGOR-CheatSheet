R-MATLAB-IGOR Cheat Sheet
=========================

This is a short guide to translate commands in three IDE softwares. R, MATLAB and IGOR Pro equivalents are given for commands, gathered under a set of headings. This work is mainly by Vidar Bronken Gundersen and Ben Gallarda, see [Credits](#credits) for details.

If you can contribute to this cheat sheet (edits, corrections, more categories etc.), please use [GitHub's fork/pull/propose changes facility](https://help.github.com/articles/editing-files-in-another-user-s-repository/). The fields with *?* need attention.

Note that some commands use IGOR Pro 7 and are not compatible with IGOR Pro 6.3 or lower.

----

*Table of contents*: [**Help**](#help) |[**Searching available documentation**](#searching-available-documentation) |[**Using interactively**](#using-interactively) |[**Operators**](#operators) |[**Arithmetic operators**](#arithmetic-operators) |[**Relational operators**](#relational-operators) |[**Logical operators**](#logical-operators) |[**root and logarithm**](#root-and-logarithm) |[**Round off**](#round-off) |[**Mathematical constants**](#mathematical-constants) |[**Missing values**](#missing-values) |[**Complex numbers**](#complex-numbers) |[**Trigonometry**](#trigonometry) |[**Generate random numbers**](#generate-random-numbers) |[**Vectors**](#vectors) |[**Sequences**](#sequences) |[**Concatenation (vectors)**](#concatenation-vectors) |[**Repeating**](#repeating) |[**Miss those elements out**](#miss-those-elements-out) |[**Maximum and minimum**](#maximum-and-minimum) |[**Vector multiplication**](#vector-multiplication) |[**Matrices**](#matrices) |[**Concatenation (matrices); rbind and cbind**](#concatenation-matrices-rbind-and-cbind) |[**Array creation**](#array-creation) |[**Reshape and flatten matrices**](#reshape-and-flatten-matrices) |[**Shared data (slicing)**](#shared-data-slicing) |[**Indexing and accessing elements (Python: slicing)**](#indexing-and-accessing-elements-python-slicing) |[**Assignment**](#assignment) |[**Transpose and inverse**](#transpose-and-inverse) |[**Sum**](#sum) |[**Sorting**](#sorting) |[**Maximum and minimum**](#maximum-and-minimum) |[**Matrix manipulation**](#matrix-manipulation) |[**Equivalents to “size”**](#equivalents-to-size) |[**Matrix- and elementwise- multiplication**](#matrix--and-elementwise--multiplication) |[**Find; conditional indexing**](#find;-conditional-indexing) |[**Multi-way arrays**](#multi-way-arrays) |[**File input and output**](#file-input-and-output) |[**Plotting**](#plotting) |[**Basic x-y plots**](#basic-x-y-plots) |[**Axes and titles**](#axes-and-titles) |[**Log plots**](#log-plots) |[**Filled plots and bar plots**](#filled-plots-and-bar-plots) |[**Functions**](#functions) |[**Polar plots**](#polar-plots) |[**Histogram plots**](#histogram-plots) |[**3d data**](#3d-data) |[**Contour and image plots**](#contour-and-image-plots) |[**Perspective plots of surfaces over the x-y plane**](#perspective-plots-of-surfaces-over-the-x-y-plane) |[**Scatter (cloud) plots**](#scatter-(cloud)-plots) |[**Save plot to a graphics file**](#save-plot-to-a-graphics-file) |[**Data analysis**](#data-analysis) |[**Set membership operators**](#set-membership-operators) |[**Statistics**](#statistics) |[**Interpolation and regression**](#interpolation-and-regression) |[**Non-linear methods**](#non-linear-methods) |[**Polynomials, root finding**](#polynomials-root-finding) |[**Differential equations**](#differential-equations) |[**Fourier analysis**](#fourier-analysis) |[**Symbolic algebra; calculus**](#symbolic-algebra-calculus) |[**Programming**](#programming) |[**Loops**](#loops) |[**Conditionals**](#conditionals) |[**Debugging**](#debugging) |[**Working directory and OS**](#working-directory-and-os) |[**Credits**](#credits) |

----

### Help

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Browse help interactively | `help.start()` | `doc` | `F1`<br>Help > Igor Help Browser |
| Help on using help | `help()` | `help help` *or* `doc doc` | `DisplayHelpTopic "Help"` |
| Help for a function | `help(plot)` *or* `?plot` | `help plot` | Right-click function name "Help for function" *or* `⎇`+`⌘`+`F1` |
| Help for a toolbox/library package | `help` | `help splines` *or* `doc splines` |  |
| Demonstration examples | `demo()` | `demo` | File > Example Experiments |
| Example using a function | `example(plot)` | | Example using a function |

### Searching available documentation

| Description | R              | MATLAB  | IGOR                           |
|---|---|---|---|
| Search help files | `help.search('plot')` | `lookfor plot` | `F1`<br>Help > Igor Help Browser                     |
| Find objects by partial name | `apropos('plot')`     |                |   |
| List available packages | `library()`           | `help`         |    |
| Locate functions | `find(plot)`          | `which plot`   | Help > Command Help                      |
| List available methods for a function | `methods(plot)`       |                |  |

### Using interactively

| Description | R                        | MATLAB                             | IGOR          |
|---|---|---|---|
| Start session | `Rgui`                          |     | File > New Experiment *or*<br>`⌘`+`N`        |
| Run code from file | `source('foo.R')`               | `foo(.m)`                                 | `FunctionName()`   |
| Command history | `history()`                     |       | See History Area      |
| Save command history | `savehistory(file=".Rhistory")` | `diary on [..] diary off`                 | `CreateHistoryCarbonCopy()` |
| End session | `q(save='no')`                  | `exit` *or* `quit` | `quit()` *or* `⌘`+`Q`          |

### Operators

| Description | R       | MATLAB | IGOR             |
|---|---|---|---|
| Help on operator syntax | `help(Syntax)` | `help -`      | `DisplayHelpTopic "Operators"` *or*<br>`DisplayHelpTopic "MatrixOP"` |

### Arithmetic operators

| Description | R       | MATLAB  | IGOR                   |
|---|---|---|---|
| Assignment; defining a number | `a<-1; b<-2`   | `a=1; b=2;`    | `Variable a=1, b=2` |
| Addition | `a + b`        | `a + b`        | `a + b`                       |
| Subtraction | `a - b`        | `a - b`        | `a - b`                   |
| Multiplication | `a * b`        | `a * b`        | `a * b`                |
| Division | `a / b`        | `a / b`        | `a / b`                      |
| Power, *a*<sup>*b*</sup> | `a ^ b`        | `a .^ b`       | `a ^ b`      |
| Remainder | `a %% b`       | `rem(a,b)`     | `mod(a,b)`                     |
| Integer division | `a %/% b`      |                |              |
| Factorial, *n*! | `factorial(a)` | `factorial(a)` | `factorial(a)`              |

### Relational operators

| Description | R | MATLAB | IGOR           |
|---|---|---|---|
| Equal | `a == b` | `a == b`      | `a == b`                 |
| Less than | `a < b`  | `a < b`       | `a < b`             |
| Greater than | `a > b`  | `a > b`       | `a > b`          |
| Less than or equal | `a <= b` | `a <= b`      | `a <= b`    |
| Greater than or equal | `a >= b` | `a >= b`      | `a >= b` |
| Not Equal | `a != b` | `a ~= b`      | `a != b`             |

### Logical operators

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Short-circuit logical AND | `a && b` | `a && b` | `a && b` |
| Short-circuit logical OR | `a || b` | `a || b` | `a || b` |
| Element-wise logical AND | `a & b` | `a & b` *or* `and(a,b)` | `a & b` |
| Element-wise logical OR | `a | b` | `a | b` *or* `or(a,b)` | `a | b` |
| Logical EXCLUSIVE OR | `xor(a, b)` | `xor(a, b)` | `%^` |
| Logical NOT | `!a` | `~a` *or* `not(a)` | `!a` |
| True if any element is nonzero | | `any(a)` |  |
| True if all elements are nonzero | | `all(a)` |  |
 
### root and logarithm

| Description | R   | MATLAB | IGOR                   |
|---|---|---|---|
| Square root | `sqrt(a)`  | `sqrt(a)`     | `sqrt(a)`                   |
| Logarithm, base *e* (natural) | `log(a)`   | `log(a)`      | `ln(a)` |
| Logarithm, base 10            | `log10(a)` | `log10(a)`    | `log(a)`            |
| Logarithm, base 2 (binary)    | `log2(a)`  | `log2(a)`     | `log2(a)`    |
| Exponential function          | `exp(a)`   | `exp(a)`      | `exp(a)`          |

### Round off

| Description | R   | MATLAB | IGOR        |
|---|---|---|---|
| Round              | `round(a)` | `round(a)`    | `round(a)`  |
| Round up           | `ceil(a)`  | `ceil(a)`     | `ceil(a)`   |
| Round down         | `floor(a)` | `floor(a)`    | `floor(a)`  |
| Round towards zero |            | `fix(a)`      | `trunc(a)`  |

### Mathematical constants

| Description | R | MATLAB | IGOR    |
|---|---|---|---|
| *π* = 3.141592 | `pi`     | `pi`          | `pi` |
| *e* = 2.718281 | `exp(1)` | `exp(1)`      | `e` |

### Missing values

| Description | R | MATLAB | IGOR  |
|---|---|---|---|
| Not a Number |          | `NaN`         | `NaN` |
| Infinity, ∞  |          | `Inf`         | `inf`  |

### Complex numbers

| Description | R                       | MATLAB | IGOR                |
|---|---|---|---|
| Imaginary unit             | `1i`                | `i`           | `i`             |
| A complex number, 3 + 4*i* | `z <- 3+4i`         | `z = 3+4i`    | `variable/c z = cmplx(3,4)` |
| Absolute value (modulus)   | `abs(3+4i)` *or* `Mod(3+4i)` | `abs(z)`      | `sqrt(magSqr(z)`   |
| Real part                  | `Re(3+4i)`          | `real(z)`     | `real(z)`                 |
| Imaginary part             | `Im(3+4i)`          | `imag(z)`     | `imag(z)`             |
| Argument                   | `Arg(3+4i)`         | `arg(z)`      |                    |
| Complex conjugate          | `Conj(3+4i)`        | `conj(z)`     | `conj(z)`          |

### Trigonometry

| Description | R     | MATLAB | IGOR                 |
|---|---|---|---|
| Arctangent, arctan(*b*/*a*) | `atan2(b,a)` | `atan(a,b)`   | `atan2(b,a)` |

### Generate random numbers

| Description | R                  | MATLAB    | IGOR                      |
|---|---|---|---|
| Uniform distribution             | `runif(10)`               | `rand(1,10)`     | `Make/N=10 wave0 = 0.5 + enoise(0.5)`             |
| Uniform: Numbers between 2 and 7 | `runif(10, min=2, max=7)` | `2+5*rand(1,10)` | `Make/N=10 wave0 = 2+ + abs(enoise(5))` |
| Uniform: 6,6 array               | `matrix(runif(36),6)`     | `rand(6)`        | `Make/N=(6,6) wave0 = enoise(1)`               |
| Normal distribution              | `rnorm(100,0,1)`               | `randn(100,1)`    | `Make/N=100 wave0 = gnoise(1)`              |

### Vectors

| Description | R                 | MATLAB       | IGOR                   |
|---|---|---|---|
| Row vector, 1 × *n*-matrix    | `a <- c(2,3,4,5)`        | `a=[2 3 4 5];`      | `Make/N=4 a = {2, 3, 4, 5}`    |
| Column vector, *m* × 1-matrix | `adash <- t(c(2,3,4,5))` | `adash=[2 3 4 5]';` | `Make/N=(1,4) adash = {2, 3, 4, 5}` |

### Sequences

| Description | R                                       | MATLAB      | IGOR                          |
|---|---|---|---|
| 1,2,3, … ,10                         | `seq(10)` *or* `1:10`   | `1:10`             | `make/N=10 a = p+1`                         |
| 0.0,1.0,2.0, … ,9.0                  | `seq(0,length=10)`                             | `0:9`              | `Make/N=10 a = p`                  |
| 1,4,7,10                             | `seq(1,10,by=3)`                               | `1:3:10`           | `Make/N=4 a = p*3+1`                             |
| 10,9,8, … ,1                         | `seq(10,1)` *or* `10:1` | `10:-1:1`          | `make/N=10 a = 10-p`                         |
| 10,7,4,1                             | `seq(from=10,to=1,by=-3)`                      | `10:-3:1`          | `Make/N=4 a = 10-(p*3)`                             |
| Linearly spaced vector of n=7 points | `seq(1,10,length=7)`                           | `linspace(1,10,7)` | `Make/N=2 a = {1,10}`<br>`Interpolate2/T=1/N=7/Y=a_L a` |
| Reverse                              | `rev(a)`                                       | `reverse(a)`       | `Reverse a`                             |
| Set all values to same scalar value  |                                                | `a(:) = 3`         | `a = 3`  |

### Concatenation (vectors)

| Description | R   | MATLAB | IGOR             |
|---|---|---|---|
| Concatenate two vectors | `c(a,a)`   | `[a a]`       | `Concatenate {a,a}, b` |
|                         | `c(1:4,a)` | `[1:4 a]`     | `Make/N=4 b = 1 + p`<br>`Concatenate {b,a}, c`                       |

### Repeating

| Description | R         | MATLAB | IGOR         |
|---|---|---|---|
| 1 2 3, 1 2 3        | `rep(a,times=2)` | `[a a]`       | `Concatenate/NP {a,a}, b`       |
| 1 1 1, 2 2 2, 3 3 3 | `rep(a,each=3)`  |               | `Concatenate {a,a,a},b`<br>`MatrixTranspose b`<br>`Redimension/N=9 b` |
| 1, 2 2, 3 3 3       | `rep(a,a)`       |               |        |

### Miss those elements out

| Description | R          | MATLAB  | IGOR            |
|---|---|---|---|
| miss the first element | `a[-1]`           | `a(2:end)`     | `a[1,*]` |
| miss the tenth element | `a[-10]`          | `a([1:9])`     | `a[0,numpnts(a)-2]` |
| miss 1,4,7, …          | `a[-seq(1,50,3)]` |                | `a[0,*;3]`          |
| last element           |                   | `a(end)`       | `a[numpnts(a)-1]`           |
| last two elements      |                   | `a(end-1:end)` | `a[numpnts(a)-2,*]`      |

### Maximum and minimum

| Description | R                          | MATLAB    | IGOR                      |
|---|---|---|---|
| pairwise max                     | `pmax(a,b)`                       | `max(a,b)`       | `max(a,b)`                     |
| max of all values in two vectors | `max(a,b)`                        | `max([a b])`     | `max(wavemax(a),wavemax(b))` |
| | `v <- max(a) ; i <- which.max(a)` | `[v,i] = max(a)` | `WaveStats a`<br>v = V\_max, i = V\_maxRowLoc                               |

### Vector multiplication

| Description | R | MATLAB | IGOR                   |
|---|---|---|---|
| Multiply two vectors          | `a*a`    | `a.*a`        | `MatrixOp b = a * a`          |
| Vector dot product, *u* ⋅ *v* |          | `dot(u,v)`    | `MatrixOp b = u . v` |

### Matrices

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Define a matrix | `rbind(c(2,3),c(4,5))`<br>`array(c(2,3,4,5), dim=c(2,2))` | `a = [2 3;4 5]` | `Make/N=(2,2) a = {{2,4},{3,5}}` |

### Concatenation (matrices); rbind and cbind

| Description | R         | MATLAB  | IGOR                          |
|---|---|---|---|
| Bind rows                            | `rbind(a,b)`     | `[a ; b]`      | `Concatenate/NP=1 {a,b}, c`                            |
| Bind columns                         | `cbind(a,b)`     | `[a , b]`      | `Concatenate/NP=0 {a,b}, c`                         |
| Concatenate matrices into one vector |                  | `[a(:), b(:)]` | *?* |
| Bind rows (from vectors)             | `rbind(1:4,1:4)` | `[1:4 ; 1:4]`  | `Make/N=(2,4) a = 1 + q`             |
| Bind columns (from vectors)          | `cbind(1:4,1:4)` | `[1:4 ; 1:4]'` | `Make/N=(4,2) a = 1 + p`          |

### Array creation

| Description | R                                                      | MATLAB   | IGOR             |
|---|---|---|---|
| 0 filled array          | `matrix(0,3,5)` *or* `array(0,c(3,5))` | `zeros(3,5)`    | `Make/N=(3,5) a = 0`          |
| 1 filled array          | `matrix(1,3,5)` *or* `array(1,c(3,5))` | `ones(3,5)`     | `Make/N=(3,5) a = 1`          |
| Any number filled array | `matrix(9,3,5)` *or* `array(9,c(3,5))` | `ones(3,5)*9`   | `Make/N=(3,5) a = 9` |
| Identity matrix         | `diag(1,3)`                                                   | `eye(3)`        | Identity matrix         |
| Diagonal                | `diag(c(4,5,6))`                                              | `diag([4 5 6])` | `Make/N=(3,3) a = 4+p`<br>`MatrixOp b = diagonal(a)`                |
| Magic squares; Lo Shu   |                                                               | `magic(3)`      | *?*   |

### Reshape and flatten matrices

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Reshaping (rows first) | `matrix(1:6,nrow=3,byrow=T)` | `reshape(1:6,3,2)';` | *?* |
| Reshaping (columns first) | `matrix(1:6,nrow=2)`<br>`array(1:6,c(2,3))` | `reshape(1:6,2,3);` | *?* |
| Flatten to vector (by rows, like comics) | `as.vector(t(a))` | `a'(:)` | *?* |
| Flatten to vector (by columns) | `as.vector(a)` | `a(:)` | `Redimension/N=(numpnts(a)) a` |
| Flatten upper triangle (by columns) | `a[row(a) <= col(a)]` | `vech(a)` | *?* |

### Shared data (slicing)

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Copy of a   | `b = a`  | `b = a`       | `Duplicate a, b`   |

### Indexing and accessing elements (Python: slicing)

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Input is a 3,4 array | `a <- rbind(c(11, 12, 13, 14),`<br>`c(21, 22, 23, 24),`<br>`c(31, 32, 33, 34))` | `a = [ 11 12 13 14 ...`<br>`21 22 23 24 ...`<br>`31 32 33 34 ]` | `Make/N=(4,3) a = {{11,12,13,14},{21,22,23,24},{31,32,33,34}}`<br>`MatrixTranspose a` |
| Element 2,3 (row,col) | `a[2,3]` | `a(2,3)` | `a[1][2]` |
| First row | `a[1,]` | `a(1,:)` | `a[0][]` |
| First column | `a[,1]` | `a(:,1)` | `a[][0]` |
| Array as indices | | `a([1 3],[1 4]);` | *?* |
| All, except first row | `a[-1,]` | `a(2:end,:)` | `a[1,*][]` |
| Last two rows | | `a(end-1:end,:)` | `a[dimsize(a,0)-2,][]` |
| Strides: Every other row | | `a(1:2:end,:)` | `a[0,*;2][]` |
| All, except row,column (2,3) | `a[-2,-3]` | | *?* |
| Remove one column | `a[,-2]` | `a(:,[1 3 4])` | `DeletePoints/M=1 0,1,a` |

### Assignment

| Description | R               | MATLAB          | IGOR                            |
|---|---|---|---|
| | `a[,1] <- 99`          | `a(:,1) = 99`          | `a[][1] = 99`                      |
| | `a[,1] <- c(99,98,97)` | `a(:,1) = [99 98 97]'` | `a[][1] = {99,98,97}` *or* `a[][1] = 99 - p`                         |
| Clipping: Replace all elements over 90 | `a[a>90] <- 90`        | `a(a>90) = 90;`        | `a = (a[p][q] > 90) ? 90 : a[p][q]` |

### Transpose and inverse

| Description | R           | MATLAB                                    | IGOR             |
|---|---|---|---|
| Transpose               | `t(a)`             | `a'`                                             | `MatrixTranspose a`               |
| Non-conjugate transpose |                    | `a.'` *or* `transpose(a)` | `MatrixTranspose/H a` |
| Determinant             | `det(a)`           | `det(a)`                                         | `MatrixDet a` *or* `MatrixOp b = det(a)`            |
| Inverse                 | `solve(a)`         | `inv(a)`                                         | `MatrixInverse a`                 |
| Pseudo-inverse          | `ginv(a)`          | `pinv(a)`                                        | `MatrixInverse/P a`          |
| Norms                   |                    | `norm(a)`                                        | `norm(a)`                   |
| Eigenvalues             | `eigen(a)$values`  | `eig(a)`                                         | `MatrixEigenV a`             |
| Singular values         | `svd(a)$d`         | `svd(a)`                                         | `MatrixSVD a`         |
| Cholesky factorization  |                    | `chol(a)`                                        | `MatrixOp chol(a)`  |
| Eigenvectors            | `eigen(a)$vectors` | `[v,l] = eig(a)`                                 | `MatrixEigenV a`            |
| Rank                    | `rank(a)`          | `rank(a)`                                        | `MatrixRank(a)`                    |

### Sum

| Description | R            | MATLAB | IGOR              |
|---|---|---|---|
| Sum of each column       | `apply(a,2,sum)`    | `sum(a)`      | `MatrixOp b = sumCols(a)`       |
| Sum of each row          | `apply(a,1,sum)`    | `sum(a')`     | `MatrixOp b = sumRows(a)`          |
| Sum of all elements      | `sum(a)`            | `sum(sum(a))` | `Sum(a)`      |
| Cumulative sum (columns) | `apply(a,2,cumsum)` | `cumsum(a)`   | `MatrixOp b = sumCols(a)`<br>`Integrate/DIM=1 b` |

### Sorting

| Description | R             | MATLAB                   | IGOR              |
|---|---|---|---|
|              |  `a <- rbind(c(4,3,2),c(2,8,6),c(1,4,7))`   | `a = [ 4 3 2 ; 2 8 6 ; 1 4 7 ]` | `Make/N=(3,3) a = {{4,2,1},{3,8,4},{2,6,7}}`             |
| Flat and sorted          | `t(sort(a))`         | `sort(a(:))`                    | `Redimension/N=9 a`<br>`Sort a,a`          |
| Sort each column         | `apply(a,2,sort)`    | `sort(a)`                       | `SortColumns keywaves={a},sortwaves={a}`         |
| Sort each row            | `t(apply(a,1,sort))` | `sort(a')'`                     | `SortColumns` following `MatrixTranspose`            |
| Sort rows (by first row) |                      | `sortrows(a,1)`                 | *?* |
| Sort, return indices     | `order(a)`           |                                 | `MakeIndex a,b` *?*     |

### Maximum and minimum

| Description | R                    | MATLAB    | IGOR        |
|---|---|---|---|
| max in each column | `apply(a,2,max)`            | `max(a)`         | `MatrixOp b=maxCols(a)` |
| max in each row    | `apply(a,1,max)`            | `max(a')`        | `MatrixOp b=a^t`<br>`MatrixOp c=maxCols(b)`    |
| max in array       | `max(a)`                    | `max(max(a))`    | `MatrixOp b=maxVal(a)`<br>*or* `WaveStats a`       |
| return indices, i  | `i <- apply(a,1,which.max)` | `[v i] = max(a)` | return indices, i  |
| pairwise max       | `pmax(b,c)`                 | `max(b,c)`       | `max(b,c)`       |
| | `apply(a,2,cummax)`         | `cummax(a)`      | `max(sum(b),sum(c))`                   |

### Matrix manipulation

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Flip left-right | `a[,4:1]` | `fliplr(a)` | `MatrixOp b=reverseRows(a)` |
| Flip up-down | `a[3:1,]` | `flipud(a)` | `MatrixOp b=reverseCols(a)` |
| Rotate 90 degrees | | `rot90(a)` | `MatrixOp b=a^t` |
| Repeat matrix: [ a a a ; a a a ] | `kronecker(matrix(1,2,3),a)` | `repmat(a,2,3)` | `Concatenate/NP=1 {a,a,a},b`<br>`Concatenate/NP=0 {b,b},c` |
| Triangular, upper | `a[lower.tri(a)] <- 0` | `triu(a)` | *?* |
| Triangular, lower | `a[upper.tri(a)] <- 0` | `tril(a)` | *?* |

### Equivalents to “size”

| Description | R         | MATLAB                                       | IGOR                    |
|---|---|---|---|
| Matrix dimensions              | `dim(a)`         | `size(a)`                                           | `WaveInfo(a)` *or* see Data Browser              |
| Number of columns              | `ncol(a)`        | `size(a,2)` *or* `length(a)` | `dimsize(a,1)`              |
| Number of elements             | `prod(dim(a))`   | `length(a(:))`                                      | `numpnts(a)`             |
| Number of dimensions           |                  | `ndims(a)`                                          | `WaveDims(a)`          |
| Number of bytes used in memory | `object.size(a)` |                                                     | `WaveInfo(a)` *or* see Data Browser |

### Matrix- and elementwise- multiplication

| Description | R                                                  | MATLAB | IGOR                                                                     |
|---|---|---|---|
| Elementwise operations                                                          | `a * b`                                                   | `a .* b`      | Elementwise operations                                                          |
| Matrix product (dot product) | `a %*% b`                                                 | `a * b`       | Matrix product (dot product)                                                    |
| Outer product | `outer(a,b)` *or* `a %o% b`        |               | Outer product                                                                   |
| Cross product | `crossprod(a,b)` *or* `t(a) %*% b` |               | Cross product                                                                   |
| Kronecker product | `kronecker(a,b)`                                          | `kron(a,b)`   | Kronecker product                                                               |
| Matrix division, *b* ⋅ *a*<sup>−1</sup>                                         |                                                           | `a / b`       | Matrix division, *b* ⋅ *a*<sup>−1</sup>                                         |
| Left matrix division, *b*<sup>−1</sup> ⋅ *a*<br>(solve linear equations) | `solve(a,b)`                                              | `a \ b`       | Left matrix division, *b*<sup>−1</sup> ⋅ *a*<br>(solve linear equations) |

### Find; conditional indexing

| Description | R                                     | MATLAB       | IGOR                      |
|---|---|---|---|
| Non-zero elements, indices | `which(a != 0)`                              | `find(a)`           | `Duplicate a,b` `b = (a != 0) ? p : NaN`<br>`WaveTransform zapnans b`       |
| Non-zero elements, array indices | `which(a != 0, arr.ind=T)`                   | `[i j] = find(a)`   | Write a loop |
| Vector of non-zero values | `ij <- which(a != 0, arr.ind=T); v <- a[ij]` | `[i j v] = find(a)` | `a = (a[p][q] != 0) ? a[p][q] : NaN`<br>`Redimension/N=(numpnts(a)) a`<br>`WaveTransform a`      |
| Condition, indices               | `which(a>5.5)`                               | `find(a>5.5)`       | `Duplicate a,b` `b = a[p][q] > 5.5 ? p : NaN`<br>`WaveTransform zapnans b`               |
| Return values | `ij <- which(a>5.5, arr.ind=T); v <- a[ij]`  |                     | `Duplicate a,b` `b = a[p][q] > 5.5 ? a[p][q] : NaN`<br>`WaveTransform zapnans b`                    |
| Zero out elements above 5.5 |                                              | `a .* (a>5.5)`      | `a = (a[p][q] > 5.5) ? 0 : a[p][q]`      |

### Multi-way arrays

| Description | R | MATLAB                        | IGOR          |
|---|---|---|---|
| Define a 3-way array |          | `a = cat(3, [1 2; 1 2],[3 4; 3 4]);` | `Make/N=(2,2,2) a={{{1,1},{2,2}},{{3,3},{4,4}}}` |
| |          | `a(1,:,:)`                           | `Make/N=(1,2,2) b`<br>`b[0][][]=a[p][q][r]` |

### File input and output

| Description | R                                    | MATLAB                  | IGOR                  |
|---|---|---|---|
| Reading from a file (2d)     | `f <- read.table("data.txt")`               | `f = load('data.txt')`         | Reading from a file (2d)     |
| Reading from a file (2d)     | `f <- read.table("data.txt")`               | `f = load('data.txt')`         | Reading from a file (2d)     |
| Reading fram a CSV file (2d) | `f <- read.table(file="data.csv", sep=";")` | `x = dlmread('data.csv', ';')` | Reading fram a CSV file (2d) |
| Writing to a file (2d)       | `write(f,file="data.txt")`                  | `save -ascii data.txt f`       | Writing to a file (2d)       |

###Plotting
### Basic x-y plots

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| 1d line plot | `plot(a, type="l")` | `plot(a)` | 1d line plot |
| 2d scatter plot | `plot(x[,1],x[,2])` | `plot(x(:,1),x(:,2),'o')` | 2d scatter plot |
| Two graphs in one plot | | `plot(x1,y1, x2,y2)` | Two graphs in one plot |
| Overplotting: Add new plots to current | `plot(x1,y1)`<br>`matplot(x2,y2,add=T)` | `plot(x1,y1)`<br>`hold on`<br>`plot(x2,y2)` | Overplotting: Add new plots to current |
| subplots | | `subplot(211)` | subplots |
| Plotting symbols and color | `plot(x,y,type="b",col="red")` | `plot(x,y,'ro-')` | Plotting symbols and color |

### Axes and titles

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Turn on grid lines | `grid()` | `grid on` | Turn on grid lines |
| 1:1 aspect ratio | `plot(c(1:10,10:1), asp=1)` | `axis equal` | 1:1 aspect ratio |
| Set axes manually | `plot(x,y, xlim=c(0,10), ylim=c(0,5))` | `axis([ 0 10 0 5 ])` | Set axes manually |
| Axis labels and titles | `plot(1:10, main="title",`<br>`xlab="x-axis", ylab="y-axis")` | `title('title')`<br>`xlabel('x-axis')`<br>`ylabel('y-axis')` | Axis labels and titles |

### Log plots

| Description | R              | MATLAB | IGOR              |
|---|---|---|---|
| logarithmic y-axis       | `plot(x,y, log="y")`  | `semilogy(a)` | logarithmic y-axis       |
| logarithmic x-axis       | `plot(x,y, log="x")`  | `semilogx(a)` | logarithmic x-axis       |
| logarithmic x and y axes | `plot(x,y, log="xy")` | `loglog(a)`   | logarithmic x and y axes |

### Filled plots and bar plots

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Filled plot | `plot(t,s, type="n", xlab="", ylab="")`<br>`polygon(t,s, col="lightblue")`<br>`polygon(t,c, col="lightgreen")` | `fill(t,s,'b', t,c,'g')` | Filled plot |
| Stem-and-Leaf plot | `stem(x[,3])` | | Stem-and-Leaf plot |


### Functions

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Defining functions | `f <- function(x) sin(x/3) - cos(x/5)` | `f = inline('sin(x/3) - cos(x/5)')` | Defining functions |
| Plot a function for given range | `plot(f, xlim=c(0,40), type='p')` | `ezplot(f,[0,40])`<br>`fplot('sin(x/3) - cos(x/5)',[0,40])` | Plot a function for given range |


### Polar plots

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| | | `theta = 0:.001:2*pi;`<br>`r = sin(2*theta);` | |
| | | `polar(theta, rho)` | |


### Histogram plots

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| | `hist(rnorm(1000))` | `hist(randn(1000,1))` | *?* |
| | `hist(rnorm(1000), breaks= -4:4)` | `hist(randn(1000,1), -4:4)` | *?* |
| | `hist(rnorm(1000),`<br>`breaks=c(seq(-5,0,0.25),`<br>`seq(0.5,5,0.5)), freq=F)` | | *?* |
| | `plot(apply(a,1,sort),type="l")` | `plot(sort(a))` | *?* |


### 3d data

### Contour and image plots

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Contour plot | `contour(z)` | `contour(z)` | `Display; AppendMatrixContour z` |
| Filled contour plot | `filled.contour(x,y,z,`<br>`nlevels=7, color=gray.colors)` | `contourf(z); colormap(gray)` | `Display; AppendMatrixContour z`<br>`ModifyContour z fill=1` |
| Plot image data | `image(z, col=gray.colors(256))` | `image(z)`<br>`colormap(gray)` | `newimage z` *or*<br>`display;appendimage z` |
| Direction field vectors | | `quiver()` | `DisplayHelpTopic "ModifyGraph for Traces"` |

### Perspective plots of surfaces over the x-y plane

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| | `f <- function(x,y) x*exp(-x^2-y^2)`<br>`n <- seq(-2,2, length=40)`<br>`z <- outer(n,n,f)` | `n=-2:.1:2;`<br>`[x,y] = meshgrid(n,n);`<br>`z=x.*exp(-x.^2-y.^2);` |
| Mesh plot | `persp(x,y,z,`<br>` theta=30, phi=30, expand=0.6,`<br>` ticktype='detailed')` | `mesh(z)` | `ImageInterpolate/CMSH voronoi a`<br>`AppendToGizmo surface=root:a,name=surface0`<br>`ModifyGizmo ModifyObject=surface0,objectType=surface,property={ fillMode,3}` |
| Surface plot | `persp(x,y,z,`<br>` theta=30, phi=30, expand=0.6,`<br>` col='lightblue', shade=0.75, ltheta=120,`<br>` ticktype='detailed')` | `surf(x,y,z)` *or* `surfl(x,y,z)` | `Concatenate {x,y,z},wave3D`<br>`NewGizmo`<br>`AppendToGizmo Scatter=root:wave3d,name=surface0` |


### Scatter (cloud) plots

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| 3d scatter plot | `cloud(z~x*y)` | `plot3(x,y,z,'k+')` | `Concatenate {x,y,z},wave3D`<br>`NewGizmo`<br>`AppendToGizmo Scatter=root:wave3d,name=scatter0` |


### Save plot to a graphics file

| Description | R | MATLAB | IGOR |
| --- | --- | --- | --- |
| PostScript | `postscript(file="foo.eps")`<br>`plot(1:10)`<br>`dev.off()` | `plot(1:10)`<br>`print -depsc2 foo.eps` | `SavePict/E=-3 as "foo.eps"` |
| PDF | `pdf(file='foo.pdf')` |  | `SavePict/E=-2 as "foo.pdf"` |
| SVG (vector graphics for www) | `devSVG(file='foo.svg')` |  | `SavePict/E=-9 as "foo.svg"` |
| PNG (raster graphics) | `png(filename = "Rplot%03d.png"` | `print -dpng foo.png` | `SavePict/E=-5 as "foo.png"` |


### Data analysis

### Set membership operators

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Create sets | `a <- c(1,2,2,5,2)`<br>`b <- c(2,3,4)` | `a = [ 1 2 2 5 2 ];`<br>`b = [ 2 3 4 ];` | Create sets |
| Set unique | `unique(a)` | `unique(a)` | `FindDuplicates/RN=c a` |
| Set union | `union(a,b)` | `union(a,b)` | *?* via loop |
| Set intersection | `intersect(a,b)` | `intersect(a,b)` | *?* via loop |
| Set difference | `setdiff(a,b)` | `setdiff(a,b)` | *?* via loop |
| Set exclusion | `setdiff(union(a,b),intersect(a,b))` | `setxor(a,b)` | *?* via loop |
| True for set member | `is.element(2,a)` *or* `2 %in% a` | `ismember(2,a)` | `FindValue/I=2 a` |

### Statistics

| Description | R            | MATLAB | IGOR             |
|---|---|---|---|
| Average                 | `apply(a,2,mean)`   | `mean(a)`     | `mean(a)`<br>Note:`WaveStats a` *or* `ImageStats a` gives many statistics                 |
| Median                  | `apply(a,2,median)` | `median(a)`   | `median(a)` *or* `statsmedian(a)`                  |
| Standard deviation      | `apply(a,2,sd)`     | `std(a)`      | `WaveStats a`      |
| Variance                | `apply(a,2,var)`    | `var(a)`      | `Variance(a)`                |
| Correlation coefficient | `cor(x,y)`          | `corr(x,y)`   | `StatsCorrelation x,y` *or* `Correlate x,y` |
| Covariance              | `cov(x,y)`          | `cov(x,y)`    | `MatrixCorr/COV x,y`              |

### Interpolation and regression

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Straight line fit | `z <- lm(y~x)`<br>`plot(x,y)`<br>`abline(z)` | `z = polyval(polyfit(x,y,1),x)`<br>`plot(x,y,'o', x,z ,'-')` | `CurveFit line b /X=a /D ` |
| Linear least squares <br>_y_ = _a__x_ + _b_ | `solve(a,b)` | `a = x\y` | `MatrixLLS a,b` |
| Polynomial fit | | `polyfit(x,y,3)` | `CurveFit Poly2D 3 a /Ywave=b  |

### Non-linear methods

### Polynomials, root finding

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Find zeros of polynomial | `polyroot(c(1,-1,-1))` | `roots([1 -1 -1])` | *?* |
| Find a zero near _x_ = 1 | | `f = inline('1/x - (x-1)')`<br>`fzero(f,1)` | *?* |
| Solve symbolic equations | | `solve('1/x = x-1')` | *?* |
| Evaluate polynomial | | `polyval([1 2 1 2],1:10)` | *?* |
 
### Differential equations

| Description | R | MATLAB | IGOR                                             |
|---|---|---|---|
| Discrete difference function and approximate derivative |          | `diff(a)`     | *?* |
| Solve differential equations                            |          |               | `Differentiate a` *?*                            |

### Fourier analysis

| Description | R               | MATLAB | IGOR               |
|---|---|---|---|
| Fast fourier transform    | `fft(a)`               | `fft(a)`      | `FFT a`    |
| Inverse fourier transform | `fft(a, inverse=TRUE)` | `ifft(a)`     | `IFFT a` |

### Symbolic algebra; calculus

| Description | R | MATLAB | IGOR   |
|---|---|---|---|
| Factorization | `FUN <- function(x) {`<br>`x <- as.integer(x)`<br>`div <- seq_len(abs(x))`<br>`factors <- div[x %% div == 0L]`<br>`factors <- list(neg = -factors, pos = factors)`<br>`return(factors)`<br>`}`         | `factor()`    | Only `PrimeFactors a` |

### Programming

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| Script file extension | `.R` | `.m` | `.ipf` |
| Comment symbol (rest of line) | `#` | `%` | `//` |
| Import library functions | `library(RSvgDevice)` | `% must be in MATLABPATH` | `#include "Name"`<br>without .ipf extension.<br>Must be in User Procedures Folder |
| Eval | `string <- "a <- 234"`<br>`eval(parse(text=string))` | `string='a=234';`<br>`eval(string)` | `String a = "234"`<br>`str2num(a)` |

### Loops

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| for-statement | `for(i in 1:5) print(i)` | `for i=1:5; disp(i); end` | `for(i=0;i<10;i+=1)`<br>`print i`<br>`endfor` |
| Multiline for statements | `for(i in 1:5) {`<br>`print(i)`<br>`print(i*2)`<br>`}` | `for i=1:5`<br>`disp(i)`<br>`disp(i*2)`<br>`end` |  |

### Conditionals

| Description | R            | MATLAB                 | IGOR                      |
|---|---|---|---|
| if-statement                     | `if (1>0) a <- 100` | `if 1>0 a=100; end`           | `if (1 > 0)`<br>`a = 100`<br>`endif`                     |
| if-else-statement                |                     | `if 1>0 a=100; else a=0; end` | `if (1 < 0)`<br>`a = 100`<br>`else`<br>`a=0 endif`                |
| Ternary operator (if?true:false) | `ifelse(a>0,a,0)`   |                               | `a = a[] > 0 ? a[p] : 0` |

### Debugging

| Description | R      | MATLAB                                       | IGOR                       |
|---|---|---|---|
| Most recent evaluated expression  | `.Last.value` | `ans`                                               | Arrow up  |
| List variables loaded into memory | `objects()`   | `whos` *or* `who`            | Data > Data Browser |
| Clear variable *x* from memory    | `rm(x)`       | `clear x` *or* `clear [all]` | `KillVariables` *or* `KillStrings`*or*`KillWaves`    |
| Print                             | `print(a)`    | `disp(a)`                    | `Print a`               |

### Working directory and OS

| Description | R | MATLAB | IGOR |
|---|---|---|---|
| List files in directory | `list.files()` *or* `dir()` | `dir` *or* `ls` | Data > Data Browser |
| List script files in directory | `list.files(pattern="\.r$")` | `what` | Window > Procedure Window |
| Displays the current working directory | `getwd()` | `pwd` | `GetDataFolder(0)` |
| Change working directory | `setwd('foo')` | `cd foo` | `SetDataFolder $expDataFolderName` |
| Invoke a System Command | `system("notepad")` | `!notepad` | `Execute "command"` |

---

##Credits

1. The original R-MATLAB cheat sheet was taken from [©2006 Vidar Bronken Gundersen, /mathesaurus.sf.net](http://mathesaurus.sourceforge.net/)
2. An edited version with added IgorPro commands was made by [Ben Gallarda](http://www.igorexchange.com/node/2804)