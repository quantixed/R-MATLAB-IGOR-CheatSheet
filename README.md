R for MATLAB users
==================

### Help

| R/S-Plus | MATLAB/Octave | Description |
|---|---|---|
| <tt title="R">help.start()</tt> | <tt title="matlab">doc</tt>
<span class="clone"><tt title="Octave">help -i % browse with Info</tt></span> | Browse help interactively |
| <tt title="R">help()</tt> | <tt title="matlab">help help</tt> <span class="alt">or</span> <tt title="matlab">doc doc</tt> | Help on using help |
| <tt title="R">help(plot)</tt> <span class="alt">or</span> <tt title="R">?plot</tt> | <tt title="matlab">help plot</tt> | Help for a function |
| <tt title="R">help(package='splines')</tt> | <tt title="matlab">help splines</tt> <span class="alt">or</span> <tt title="matlab">doc splines</tt> | Help for a toolbox/library package |
| <tt title="R">demo()</tt> | <tt title="matlab">demo</tt> | Demonstration examples |
| <tt title="R">example(plot)</tt> | Example using a function |

### Searching available documentation

| R/S-Plus              | MATLAB/Octave  | Description                           |
|-----------------------|----------------|---------------------------------------|
| `help.search('plot')` | `lookfor plot` | Search help files                     |
| `apropos('plot')`     |                | Find objects by partial name          |
| `library()`           | `help`         | List available packages               |
| `find(plot)`          | `which plot`   | Locate functions                      |
| `methods(plot)`       |                | List available methods for a function |

### Using interactively

| R/S-Plus                        | MATLAB/Octave                             | Description          |
|---------------------------------|-------------------------------------------|----------------------|
| `Rgui`                          | <span class="clone">`octave -q`</span>    | Start session        |
| `source('foo.R')`               | `foo(.m)`                                 | Run code from file   |
| `history()`                     | <span class="clone">`history`</span>      | Command history      |
| `savehistory(file=".Rhistory")` | `diary on [..] diary off`                 | Save command history |
| `q(save='no')`                  | `exit` <span class="alt">or</span> `quit` | End session          |

### Operators

| R/S-Plus       | MATLAB/Octave | Description             |
|----------------|---------------|-------------------------|
| `help(Syntax)` | `help -`      | Help on operator syntax |

### Arithmetic operators

| R/S-Plus       | MATLAB/Octave  | Description                   |
|----------------|----------------|-------------------------------|
| `a<-1; b<-2`   | `a=1; b=2;`    | Assignment; defining a number |
| `a + b`        | `a + b`        | Addition                      |
| `a - b`        | `a - b`        | Subtraction                   |
| `a * b`        | `a * b`        | Multiplication                |
| `a / b`        | `a / b`        | Division                      |
| `a ^ b`        | `a .^ b`       | Power, *a*<sup>*b*</sup>      |
| `a %% b`       | `rem(a,b)`     | Remainder                     |
| `a %/% b`      |                | Integer division              |
| `factorial(a)` | `factorial(a)` | Factorial, *n*!               |

### Relational operators

| R/S-Plus | MATLAB/Octave | Description           |
|----------|---------------|-----------------------|
| `a == b` | `a == b`      | Equal                 |
| `a < b`  | `a < b`       | Less than             |
| `a > b`  | `a > b`       | Greater than          |
| `a <= b` | `a <= b`      | Less than or equal    |
| `a >= b` | `a >= b`      | Greater than or equal |
| `a != b` | `a ~= b`      | Not Equal             |

### Logical operators

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `a && b` | `a && b` | Short-circuit logical AND |
| `a || b` | `a || b` | Short-circuit logical OR |
| `a & b` | `a & b` <span class="alt">or</span> `and(a,b)` | Element-wise logical AND |
| `a | b` | `a | b` <span class="alt">or</span> `or(a,b)` | Element-wise logical OR |
| `xor(a, b)` | `xor(a, b)` | Logical EXCLUSIVE OR |
| `!a` | `~a` <span class="alt">or</span> `not(a)`
<span class="clone">`~a` <span class="alt">or</span> `!a`</span> | Logical NOT |
 `any(a)` | True if any element is nonzero |
 `all(a)` | True if all elements are nonzero |
 
### root and logarithm

| R/S-Plus   | MATLAB/Octave | Description                   |
|------------|---------------|-------------------------------|
| `sqrt(a)`  | `sqrt(a)`     | Square root                   |
| `log(a)`   | `log(a)`      | Logarithm, base *e* (natural) |
| `log10(a)` | `log10(a)`    | Logarithm, base 10            |
| `log2(a)`  | `log2(a)`     | Logarithm, base 2 (binary)    |
| `exp(a)`   | `exp(a)`      | Exponential function          |

### Round off

| R/S-Plus   | MATLAB/Octave | Description        |
|------------|---------------|--------------------|
| `round(a)` | `round(a)`    | Round              |
| `ceil(a)`  | `ceil(a)`     | Round up           |
| `floor(a)` | `floor(a)`    | Round down         |
|            | `fix(a)`      | Round towards zero |

### Mathematical constants

| R/S-Plus | MATLAB/Octave | Description    |
|----------|---------------|----------------|
| `pi`     | `pi`          | *π* = 3.141592 |
| `exp(1)` | `exp(1)`      | *e* = 2.718281 |

### Missing values; IEEE-754 floating point status flags

| R/S-Plus | MATLAB/Octave | Description  |
|----------|---------------|--------------|
|          | `NaN`         | Not a Number |
|          | `Inf`         | Infinity, ∞  |

### Complex numbers

| R/S-Plus                                            | MATLAB/Octave | Description                |
|-----------------------------------------------------|---------------|----------------------------|
| `1i`                                                | `i`           | Imaginary unit             |
| `z <- 3+4i`                                         | `z = 3+4i`    | A complex number, 3 + 4*i* |
| `abs(3+4i)` <span class="alt">or</span> `Mod(3+4i)` | `abs(z)`      | Absolute value (modulus)   |
| `Re(3+4i)`                                          | `real(z)`     | Real part                  |
| `Im(3+4i)`                                          | `imag(z)`     | Imaginary part             |
| `Arg(3+4i)`                                         | `arg(z)`      | Argument                   |
| `Conj(3+4i)`                                        | `conj(z)`     | Complex conjugate          |

### Trigonometry

| R/S-Plus     | MATLAB/Octave | Description                 |
|--------------|---------------|-----------------------------|
| `atan2(b,a)` | `atan(a,b)`   | Arctangent, arctan(*b*/*a*) |

### Generate random numbers

| R/S-Plus                  | MATLAB/Octave    | Description                      |
|---------------------------|------------------|----------------------------------|
| `runif(10)`               | `rand(1,10)`     | Uniform distribution             |
| `runif(10, min=2, max=7)` | `2+5*rand(1,10)` | Uniform: Numbers between 2 and 7 |
| `matrix(runif(36),6)`     | `rand(6)`        | Uniform: 6,6 array               |
| `rnorm(10)`               | `randn(1,10)`    | Normal distribution              |

### Vectors

| R/S-Plus                 | MATLAB/Octave       | Description                   |
|--------------------------|---------------------|-------------------------------|
| `a <- c(2,3,4,5)`        | `a=[2 3 4 5];`      | Row vector, 1 × *n*-matrix    |
| `adash <- t(c(2,3,4,5))` | `adash=[2 3 4 5]';` | Column vector, *m* × 1-matrix |

### Sequences

| R/S-Plus                                       | MATLAB/Octave      | Description                          |
|------------------------------------------------|--------------------|--------------------------------------|
| `seq(10)` <span class="alt">or</span> `1:10`   | `1:10`             | 1,2,3, … ,10                         |
| `seq(0,length=10)`                             | `0:9`              | 0.0,1.0,2.0, … ,9.0                  |
| `seq(1,10,by=3)`                               | `1:3:10`           | 1,4,7,10                             |
| `seq(10,1)` <span class="alt">or</span> `10:1` | `10:-1:1`          | 10,9,8, … ,1                         |
| `seq(from=10,to=1,by=-3)`                      | `10:-3:1`          | 10,7,4,1                             |
| `seq(1,10,length=7)`                           | `linspace(1,10,7)` | Linearly spaced vector of n=7 points |
| `rev(a)`                                       | `reverse(a)`       | Reverse                              |
|                                                | `a(:) = 3`         | Set all values to same scalar value  |

### Concatenation (vectors)

| R/S-Plus   | MATLAB/Octave | Description             |
|------------|---------------|-------------------------|
| `c(a,a)`   | `[a a]`       | Concatenate two vectors |
| `c(1:4,a)` | `[1:4 a]`     |                         |

### Repeating

| R/S-Plus         | MATLAB/Octave | Description         |
|------------------|---------------|---------------------|
| `rep(a,times=2)` | `[a a]`       | 1 2 3, 1 2 3        |
| `rep(a,each=3)`  |               | 1 1 1, 2 2 2, 3 3 3 |
| `rep(a,a)`       |               | 1, 2 2, 3 3 3       |

### Miss those elements out

| R/S-Plus          | MATLAB/Octave  | Description            |
|-------------------|----------------|------------------------|
| `a[-1]`           | `a(2:end)`     | miss the first element |
| `a[-10]`          | `a([1:9])`     | miss the tenth element |
| `a[-seq(1,50,3)]` |                | miss 1,4,7, …          |
|                   | `a(end)`       | last element           |
|                   | `a(end-1:end)` | last two elements      |

### Maximum and minimum

| R/S-Plus                          | MATLAB/Octave    | Description                      |
|-----------------------------------|------------------|----------------------------------|
| `pmax(a,b)`                       | `max(a,b)`       | pairwise max                     |
| `max(a,b)`                        | `max([a b])`     | max of all values in two vectors |
| `v <- max(a) ; i <- which.max(a)` | `[v,i] = max(a)` |                                  |

### Vector multiplication

| R/S-Plus | MATLAB/Octave | Description                   |
|----------|---------------|-------------------------------|
| `a*a`    | `a.*a`        | Multiply two vectors          |
|          | `dot(u,v)`    | Vector dot product, *u* ⋅ *v* |

### Matrices

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `rbind(c(2,3),c(4,5))`
`array(c(2,3,4,5), dim=c(2,2))` | `a = [2 3;4 5]` | Define a matrix |

### Concatenation (matrices); rbind and cbind

| R/S-Plus         | MATLAB/Octave  | Description                          |
|------------------|----------------|--------------------------------------|
| `rbind(a,b)`     | `[a ; b]`      | Bind rows                            |
| `cbind(a,b)`     | `[a , b]`      | Bind columns                         |
|                  | `[a(:), b(:)]` | Concatenate matrices into one vector |
| `rbind(1:4,1:4)` | `[1:4 ; 1:4]`  | Bind rows (from vectors)             |
| `cbind(1:4,1:4)` | `[1:4 ; 1:4]'` | Bind columns (from vectors)          |

### Array creation

| R/S-Plus                                                      | MATLAB/Octave   | Description             |
|---------------------------------------------------------------|-----------------|-------------------------|
| `matrix(0,3,5)` <span class="alt">or</span> `array(0,c(3,5))` | `zeros(3,5)`    | 0 filled array          |
| `matrix(1,3,5)` <span class="alt">or</span> `array(1,c(3,5))` | `ones(3,5)`     | 1 filled array          |
| `matrix(9,3,5)` <span class="alt">or</span> `array(9,c(3,5))` | `ones(3,5)*9`   | Any number filled array |
| `diag(1,3)`                                                   | `eye(3)`        | Identity matrix         |
| `diag(c(4,5,6))`                                              | `diag([4 5 6])` | Diagonal                |
|                                                               | `magic(3)`      | Magic squares; Lo Shu   |

### Reshape and flatten matrices

| R/S-Plus | MATLAB/Octave | Description |
| --- | ---| --- |
| <tt title="R">matrix(1:6,nrow=3,byrow=T)</tt> | <tt title="matlab">reshape(1:6,3,2)';</tt> | Reshaping (rows first) |
| <tt title="R">matrix(1:6,nrow=2)</tt>
<tt title="R">array(1:6,c(2,3))</tt> | <tt title="matlab">reshape(1:6,2,3);</tt> | Reshaping (columns first) |
| <tt title="R">as.vector(t(a))</tt> | <tt title="matlab">a'(:)</tt> | Flatten to vector (by rows, like comics) |
| <tt title="R">as.vector(a)</tt> | <tt title="matlab">a(:)</tt> | Flatten to vector (by columns) |
| <tt title="R">a[row(a) <= col(a)]</tt> | <tt title="matlab">vech(a)</tt> | Flatten upper triangle (by columns) |

### Shared data (slicing)

| R/S-Plus | MATLAB/Octave | Description |
|----------|---------------|-------------|
| `b = a`  | `b = a`       | Copy of a   |

### Indexing and accessing elements (Python: slicing)

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `a <- rbind(c(11, 12, 13, 14), c(21, 22, 23, 24),c(31, 32, 33, 34))` | `a = [ 11 12 13 14 ... 21 22 23 24 ... 31 32 33 34 ]` | Input is a 3,4 array |
| `a[2,3]` | `a(2,3)` | Element 2,3 (row,col) |
| `a[1,]` | `a(1,:)` | First row |
| `a[,1]` | `a(:,1)` | First column |
 `a([1 3],[1 4]);` | Array as indices |
| `a[-1,]` | `a(2:end,:)` | All, except first row |
 `a(end-1:end,:)` | Last two rows |
 `a(1:2:end,:)` | Strides: Every other row |
| `a[-2,-3]` | All, except row,column (2,3) |
| `a[,-2]` | `a(:,[1 3 4])` | Remove one column |

### Assignment

| R/S-Plus               | MATLAB/Octave          | Description                            |
|------------------------|------------------------|----------------------------------------|
| `a[,1] <- 99`          | `a(:,1) = 99`          |                                        |
| `a[,1] <- c(99,98,97)` | `a(:,1) = [99 98 97]'` |                                        |
| `a[a>90] <- 90`        | `a(a>90) = 90;`        | Clipping: Replace all elements over 90 |

### Transpose and inverse

| R/S-Plus           | MATLAB/Octave                                    | Description             |
|--------------------|--------------------------------------------------|-------------------------|
| `t(a)`             | `a'`                                             | Transpose               |
|                    | `a.'` <span class="alt">or</span> `transpose(a)` | Non-conjugate transpose |
| `det(a)`           | `det(a)`                                         | Determinant             |
| `solve(a)`         | `inv(a)`                                         | Inverse                 |
| `ginv(a)`          | `pinv(a)`                                        | Pseudo-inverse          |
|                    | `norm(a)`                                        | Norms                   |
| `eigen(a)$values`  | `eig(a)`                                         | Eigenvalues             |
| `svd(a)$d`         | `svd(a)`                                         | Singular values         |
|                    | `chol(a)`                                        | Cholesky factorization  |
| `eigen(a)$vectors` | `[v,l] = eig(a)`                                 | Eigenvectors            |
| `rank(a)`          | `rank(a)`                                        | Rank                    |

### Sum

| R/S-Plus            | MATLAB/Octave | Description              |
|---------------------|---------------|--------------------------|
| `apply(a,2,sum)`    | `sum(a)`      | Sum of each column       |
| `apply(a,1,sum)`    | `sum(a')`     | Sum of each row          |
| `sum(a)`            | `sum(sum(a))` | Sum of all elements      |
| `apply(a,2,cumsum)` | `cumsum(a)`   | Cumulative sum (columns) |

### Sorting

| R/S-Plus             | MATLAB/Octave                   | Description              |
|----------------------|---------------------------------|--------------------------|
|                      | `a = [ 4 3 2 ; 2 8 6 ; 1 4 7 ]` | Example data             |
| `t(sort(a))`         | `sort(a(:))`                    | Flat and sorted          |
| `apply(a,2,sort)`    | `sort(a)`                       | Sort each column         |
| `t(apply(a,1,sort))` | `sort(a')'`                     | Sort each row            |
|                      | `sortrows(a,1)`                 | Sort rows (by first row) |
| `order(a)`           |                                 | Sort, return indices     |

### Maximum and minimum

| R/S-Plus                    | MATLAB/Octave    | Description        |
|-----------------------------|------------------|--------------------|
| `apply(a,2,max)`            | `max(a)`         | max in each column |
| `apply(a,1,max)`            | `max(a')`        | max in each row    |
| `max(a)`                    | `max(max(a))`    | max in array       |
| `i <- apply(a,1,which.max)` | `[v i] = max(a)` | return indices, i  |
| `pmax(b,c)`                 | `max(b,c)`       | pairwise max       |
| `apply(a,2,cummax)`         | `cummax(a)`      |                    |

### Matrix manipulation

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `a[,4:1]` | `fliplr(a)` | Flip left-right |
| `a[3:1,]` | `flipud(a)` | Flip up-down |
 `rot90(a)` | Rotate 90 degrees |
| `kronecker(matrix(1,2,3),a)` | `repmat(a,2,3)`
<span class="clone">`kron(ones(2,3),a)`</span> | Repeat matrix: [ a a a ; a a a ] |
| `a[lower.tri(a)] <- 0` | `triu(a)` | Triangular, upper |
| `a[upper.tri(a)] <- 0` | `tril(a)` | Triangular, lower |

### Equivalents to “size”

| R/S-Plus         | MATLAB/Octave                                       | Description                    |
|------------------|-----------------------------------------------------|--------------------------------|
| `dim(a)`         | `size(a)`                                           | Matrix dimensions              |
| `ncol(a)`        | `size(a,2)` <span class="alt">or</span> `length(a)` | Number of columns              |
| `prod(dim(a))`   | `length(a(:))`                                      | Number of elements             |
|                  | `ndims(a)`                                          | Number of dimensions           |
| `object.size(a)` |                                                     | Number of bytes used in memory |

### Matrix- and elementwise- multiplication

| R/S-Plus                                                  | MATLAB/Octave | Description                                                                     |
|-----------------------------------------------------------|---------------|---------------------------------------------------------------------------------|
| `a * b`                                                   | `a .* b`      | Elementwise operations                                                          |
| `a %*% b`                                                 | `a * b`       | Matrix product (dot product)                                                    |
| `outer(a,b)` <span class="alt">or</span> `a %o% b`        |               | Outer product                                                                   |
| `crossprod(a,b)` <span class="alt">or</span> `t(a) %*% b` |               | Cross product                                                                   |
| `kronecker(a,b)`                                          | `kron(a,b)`   | Kronecker product                                                               |
|                                                           | `a / b`       | Matrix division, *b* ⋅ *a*<sup>−1</sup>                                         |
| `solve(a,b)`                                              | `a \ b`       | Left matrix division, *b*<sup>−1</sup> ⋅ *a* \\newline (solve linear equations) |

### Find; conditional indexing

| R/S-Plus                                     | MATLAB/Octave       | Description                      |
|----------------------------------------------|---------------------|----------------------------------|
| `which(a != 0)`                              | `find(a)`           | Non-zero elements, indices       |
| `which(a != 0, arr.ind=T)`                   | `[i j] = find(a)`   | Non-zero elements, array indices |
| `ij <- which(a != 0, arr.ind=T); v <- a[ij]` | `[i j v] = find(a)` | Vector of non-zero values        |
| `which(a>5.5)`                               | `find(a>5.5)`       | Condition, indices               |
| `ij <- which(a>5.5, arr.ind=T); v <- a[ij]`  |                     | Return values                    |
|                                              | `a .* (a>5.5)`      | Zero out elements above 5.5      |

### Multi-way arrays

| R/S-Plus | MATLAB/Octave                        | Description          |
|----------|--------------------------------------|----------------------|
|          | `a = cat(3, [1 2; 1 2],[3 4; 3 4]);` | Define a 3-way array |
|          | `a(1,:,:)`                           |                      |

### File input and output

| R/S-Plus                                    | MATLAB/Octave                  | Description                  |
|---------------------------------------------|--------------------------------|------------------------------|
| `f <- read.table("data.txt")`               | `f = load('data.txt')`         | Reading from a file (2d)     |
| `f <- read.table("data.txt")`               | `f = load('data.txt')`         | Reading from a file (2d)     |
| `f <- read.table(file="data.csv", sep=";")` | `x = dlmread('data.csv', ';')` | Reading fram a CSV file (2d) |
| `write(f,file="data.txt")`                  | `save -ascii data.txt f`       | Writing to a file (2d)       |

###Plotting
### Basic x-y plots

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `plot(a, type="l")` | `plot(a)` | 1d line plot |
| `plot(x[,1],x[,2])` | `plot(x(:,1),x(:,2),'o')` | 2d scatter plot |
| | `plot(x1,y1, x2,y2)` | Two graphs in one plot |
| `plot(x1,y1)`<p>`matplot(x2,y2,add=T)` | `plot(x1,y1)`<p>`hold on`<p>`plot(x2,y2)` | Overplotting: Add new plots to current |
| | `subplot(211)` | subplots |
| `plot(x,y,type="b",col="red")` | `plot(x,y,'ro-')` | Plotting symbols and color |

### Axes and titles

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `grid()` | `grid on` | Turn on grid lines |
| `plot(c(1:10,10:1), asp=1)` | `axis equal`<p>`axis('equal')`<p>`replot` | 1:1 aspect ratio |
| `plot(x,y, xlim=c(0,10), ylim=c(0,5))` | `axis([ 0 10 0 5 ])` | Set axes manually |
| `plot(1:10, main="title",`<p>`xlab="x-axis", ylab="y-axis")` | `title('title')`<p>`xlabel('x-axis')`<p>`ylabel('y-axis')` | Axis labels and titles |

### Log plots

| R/S-Plus              | MATLAB/Octave | Description              |
|-----------------------|---------------|--------------------------|
| `plot(x,y, log="y")`  | `semilogy(a)` | logarithmic y-axis       |
| `plot(x,y, log="x")`  | `semilogx(a)` | logarithmic x-axis       |
| `plot(x,y, log="xy")` | `loglog(a)`   | logarithmic x and y axes |

### Filled plots and bar plots

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `plot(t,s, type="n", xlab="", ylab="")`
`polygon(t,s, col="lightblue")`
`polygon(t,c, col="lightgreen")` | `fill(t,s,'b', t,c,'g')`
<span class="clone">`% fill has a bug?`</span> | Filled plot |
| `stem(x[,3])` | Stem-and-Leaf plot |


### Functions

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `f <- function(x) sin(x/3) - cos(x/5)` | `f = inline('sin(x/3) - cos(x/5)')` | Defining functions |
| `plot(f, xlim=c(0,40), type='p')` | `ezplot(f,[0,40])`
`fplot('sin(x/3) - cos(x/5)',[0,40])`
<span class="clone">`% no ezplot`</span> | Plot a function for given range |


### Polar plots

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
 `theta = 0:.001:2*pi;`
`r = sin(2*theta);` |
 `polar(theta, rho)` |


### Histogram plots

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `hist(rnorm(1000))` | `hist(randn(1000,1))` |
| `hist(rnorm(1000), breaks= -4:4)` | `hist(randn(1000,1), -4:4)` |
| `hist(rnorm(1000), breaks=c(seq(-5,0,0.25), seq(0.5,5,0.5)), freq=F)` |
| `plot(apply(a,1,sort),type="l")` | `plot(sort(a))` |


### 3d data

### Contour and image plots

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `contour(z)` | `contour(z)` | Contour plot |
| `filled.contour(x,y,z,`
` nlevels=7, color=gray.colors)` | `contourf(z); colormap(gray)` | Filled contour plot |
| `image(z, col=gray.colors(256))` | `image(z)`
`colormap(gray)` | Plot image data |
 `quiver()` | Direction field vectors |

### Perspective plots of surfaces over the x-y plane

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `f <- function(x,y) x*exp(-x^2-y^2)`
`n <- seq(-2,2, length=40)`
`z <- outer(n,n,f)` | `n=-2:.1:2;`
`[x,y] = meshgrid(n,n);`
`z=x.*exp(-x.^2-y.^2);` |
| `persp(x,y,z,`
` theta=30, phi=30, expand=0.6,`
` ticktype='detailed')` | `mesh(z)` | Mesh plot |
| `persp(x,y,z,`
` theta=30, phi=30, expand=0.6,`
` col='lightblue', shade=0.75, ltheta=120,`
` ticktype='detailed')` | `surf(x,y,z)` <span class="alt">or</span> `surfl(x,y,z)`
<span class="clone">`% no surfl()`</span> | Surface plot |


### Scatter (cloud) plots

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `cloud(z~x*y)` | `plot3(x,y,z,'k+')` | 3d scatter plot |


### Save plot to a graphics file

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `postscript(file="foo.eps")`
`plot(1:10)`
`dev.off()` | `plot(1:10)`
`print -depsc2 foo.eps`
<span class="clone">`gset output "foo.eps"`
`gset terminal postscript eps`
`plot(1:10)`</span> | PostScript |
| `pdf(file='foo.pdf')` | `` | PDF |
| <tt title="R; RSvgDevice">devSVG(file='foo.svg')`</tt> | `` | SVG (vector graphics for www) |
| `png(filename = "Rplot%03d.png"` | `print -dpng foo.png` | PNG (raster graphics) |


### Data analysis


### Set membership operators

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `a <- c(1,2,2,5,2)`
`b <- c(2,3,4)` | `a = [ 1 2 2 5 2 ];`
`b = [ 2 3 4 ];` | Create sets |
| `unique(a)` | `unique(a)` | Set unique |
| `union(a,b)` | `union(a,b)` | Set union |
| `intersect(a,b)` | `intersect(a,b)` | Set intersection |
| `setdiff(a,b)` | `setdiff(a,b)` | Set difference |
| `setdiff(union(a,b),intersect(a,b))` | `setxor(a,b)` | Set exclusion |
| `is.element(2,a)` <span class="alt">or</span> `2 %in% a` | `ismember(2,a)` | True for set member |

### Statistics

| R/S-Plus            | MATLAB/Octave | Description             |
|---------------------|---------------|-------------------------|
| `apply(a,2,mean)`   | `mean(a)`     | Average                 |
| `apply(a,2,median)` | `median(a)`   | Median                  |
| `apply(a,2,sd)`     | `std(a)`      | Standard deviation      |
| `apply(a,2,var)`    | `var(a)`      | Variance                |
| `cor(x,y)`          | `corr(x,y)`   | Correlation coefficient |
| `cov(x,y)`          | `cov(x,y)`    | Covariance              |

### Interpolation and regression

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `z <- lm(y~x)`
`plot(x,y)`
`abline(z)` | `z = polyval(polyfit(x,y,1),x)`
`plot(x,y,'o', x,z ,'-')` | Straight line fit |
| `solve(a,b)` | `a = x\y` | Linear least squares <span class="math inline">_y_ = _a__x_ + _b_</span> |
 `polyfit(x,y,3)` | Polynomial fit |

### Non-linear methods

### Polynomials, root finding

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `polyroot(c(1,-1,-1))` | `roots([1 -1 -1])` | Find zeros of polynomial |
 `f = inline('1/x - (x-1)')`
`fzero(f,1)` | Find a zero near <span class="math inline">_x_ = 1</span> |
 `solve('1/x = x-1')` | Solve symbolic equations |
 `polyval([1 2 1 2],1:10)` | Evaluate polynomial |
 
### Differential equations

| R/S-Plus | MATLAB/Octave | Description                                             |
|----------|---------------|---------------------------------------------------------|
|          | `diff(a)`     | Discrete difference function and approximate derivative |
|          | ``            | Solve differential equations                            |

### Fourier analysis

| R/S-Plus               | MATLAB/Octave | Description               |
|------------------------|---------------|---------------------------|
| `fft(a)`               | `fft(a)`      | Fast fourier transform    |
| `fft(a, inverse=TRUE)` | `ifft(a)`     | Inverse fourier transform |

### Symbolic algebra; calculus

| R/S-Plus | MATLAB/Octave | Description   |
|----------|---------------|---------------|
|          | `factor()`    | Factorization |

### Programming

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `.R` | `.m` | Script file extension |
| `#` | `%`
<span class="clone">`%` <span class="alt">or</span> `#`</span> | Comment symbol (rest of line) |
| `library(RSvgDevice)` | `% must be in MATLABPATH`
<span class="clone">`% must be in LOADPATH`</span> | Import library functions |
| `string <- "a <- 234"`
`eval(parse(text=string))` | `string='a=234';`
`eval(string)` | Eval |

### Loops

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `for(i in 1:5) print(i)` | `for i=1:5; disp(i); end` | for-statement |
| `for(i in 1:5) {`
`print(i)`
`print(i*2)`
`}` | `for i=1:5`
`disp(i)`
`disp(i*2)`
`end` | Multiline for statements |

### Conditionals

| R/S-Plus            | MATLAB/Octave                 | Description                      |
|---------------------|-------------------------------|----------------------------------|
| `if (1>0) a <- 100` | `if 1>0 a=100; end`           | if-statement                     |
|                     | `if 1>0 a=100; else a=0; end` | if-else-statement                |
| `ifelse(a>0,a,0)`   |                               | Ternary operator (if?true:false) |

### Debugging

| R/S-Plus      | MATLAB/Octave                                       | Description                       |
|---------------|-----------------------------------------------------|-----------------------------------|
| `.Last.value` | `ans`                                               | Most recent evaluated expression  |
| `objects()`   | `whos` <span class="alt">or</span> `who`            | List variables loaded into memory |
| `rm(x)`       | `clear x` <span class="alt">or</span> `clear [all]` | Clear variable *x* from memory    |
| `print(a)`    | `disp(a)`                                           | Print                             |

### Working directory and OS

| R/S-Plus | MATLAB/Octave | Description |
| --- | --- | --- |
| `list.files()` <span class="alt">or</span> `dir()` | `dir` <span class="alt">or</span> `ls` | List files in directory |
| `list.files(pattern="\.r$")` | `what` | List script files in directory |
| `getwd()` | `pwd` | Displays the current working directory |
| `setwd('foo')` | `cd foo` | Change working directory |
| `system("notepad")` | `!notepad`
<span class="clone">`system("notepad")`</span> | Invoke a System Command |

---

##Credits

1. The original R-MATLAB cheat sheet was taken from [©2006 Vidar Bronken Gundersen, /mathesaurus.sf.net](http://mathesaurus.sourceforge.net/)
2. An edited version with added IgorPro commands was made by [Ben Gallarda](http://www.igorexchange.com/node/2804)