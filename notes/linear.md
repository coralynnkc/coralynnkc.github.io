---
layout: note
type: note
title: Linear Algebra
---

# 1.1.1 - SYSTEMS OF LINEAR EQUATIONS

## WRITING SYSTEM

Instead of multiple variables, only $x$ is used.

- $x_1 + x_2 = 5$
- $3x_1 - 2x_2 = 10$

COEFFICIENT MATRIX.

$$
\begin{bmatrix}
1 & 1 \\
3 & 2 \\
\end{bmatrix}
$$

AUGMENTED MATRIX.

$$
\left[\begin{array}{c c:c}
1 & 1 & 5 \\
3 & 2 & 10 \\
\end{array}\right]
$$

### SOLUTION 1

$$
\begin{array}{c c c c c c}
& 2x_1 & + & 2x_2 & = & 10 \\
+ & 3x_1 & - & 2x_2 & = & 10 \\
\hline
& 5x_1 & & & = & 20 \\
\end{array}
$$

$$x_1 = 4$$

### SOLUTION 2

$$
\left[\begin{array}{cc:c}
1 & 1 & 5 \\
3 & 2 & 10 \\
\end{array}\right]
$$

$2R_1 + R_2 \rightarrow R_1$

$$
\left[\begin{array}{cc:c}
5 & 0 & 20 \\
3 & 2 & 10 \\
\end{array}\right]
$$

$\frac{1}{5} R_1 \rightarrow R_1$

$$
\left[\begin{array}{cc:c}
1 & 0 & 4 \\
3 & 2 & 10 \\
\end{array}\right]
$$

$-3R_1 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{cc:c}
1 & 0 & 4 \\
0 & -2 & -2 \\
\end{array}\right]
$$

$-\frac{1}{2} R_2 \rightarrow R_2$

$$
\left[\begin{array}{cc:c}
1 & 0 & 4 \\
0 & 1 & 1 \\
\end{array}\right]
$$

$$x_1 = 4$$

$$x_2 = 1$$

## TERMINOLOGY

LINEAR EQUATION. An equation that can be written as $a_1x_1 + a_2x_2 + a_3x_3 + ... + a_nx_n = b$

- $a_1, a_2, ... a_n, b$ are real or complex numbers.

SYSTEM OF LINEAR EQUATIONS. A collection of two or more liear equations using the same variables.

SOLUTION. A list of numbers $(S_1, S_2, S_3...)$ that makes each equation in the system true when substituted for $x_1, x_2, x_3...$ respectively.

SOLUTION SET. The set of all possible solutions to a system.

## TYPES OF SYSTEMS

INCONSISTENT. No solution.

CONSISTENT. At least one solution.

## ROW OPERATIONS

REPLACEMENT. Replace one row by the sum of itself and a multiple of another row.

INTERCHANGE. Swap two rows.

SCALING. Multiply a row by a non-zero constant.

## EXAMPLE 1

$$x_1 - 2x_2 + x_3 = 0$$

$$2x_2 - 8x_3 = 8$$

$$-4x_1 + 5x_2 + 9x_3 = -9$$

### SOLUTION 1

$4 * (x_1 - 2x_2 + x_3 = 0) \rightarrow 4x_1 - 8x_2 + 4x_3 = 0$

$$
\begin{array}{cccccccc}
& 4x_1 & - & 8x_2 & + & 4x_3 & = & 0 \\
+ & -4x_1 & + & 5x_2 & + & 9x_3 & = & -9 \\
\hline
& & & -3x_2 & + & 13x_3 & = & -9
\end{array}
$$

$3 * (2x_2 - 8x_3 = 8) \rightarrow 6x_2 - 24x_3 = 24$

$2 * (-3x_2 + 13x_3 = -9) \rightarrow -6x_2 + 26 x_3 = -18$

$$
\begin{array}{cccccc}
& 6x_2 & - & 24x_3 & = & 24 \\
+ & -6x_2 & + & 26x_3 & = & -18 \\
\hline
& & & 2x_3 & = & 6
\end{array}
$$

$$x_3 = 3$$

$2x_2 -8(3) = 8$

$$x_2 = 16$$

$x_1 - 2(16) + 3 = 0$

$$x_1 = 29$$

### SOLUTION 2

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
-4 & 5 & 9 & -9 \\
\end{array}\right]
$$

STRATEGY: Create a diagonal of ones. Values below that diagonal should be zeroes.

$4R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
0 & -3 & 13 & -9 \\
\end{array}\right]
$$

$\frac{1}{2}R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & -3 & 13 & -9 \\
\end{array}\right]
$$

$3R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & 0 & 1 & 3 \\
\end{array}\right]
$$

TRIANGULAR FORM. (GAUSSIAN ELIMINATION).

BACK SUBSTITUTION. Turning the matrix back into a system of linear equations.

$$x_3 = 3$$

$4R_3 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & 0 & 16 \\
0 & 0 & 1 & 3 \\
\end{array}\right]
$$

$$x_2 = 16$$

$2R_2 + R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & 0 & 1 & 32 \\
0 & 1 & 0 & 16 \\
0 & 0 & 1 & 3 \\
\end{array}\right]
$$

$-R_2 + R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & 0 & 0 & 29 \\
0 & 1 & 0 & 16 \\
0 & 0 & 1 & 3 \\
\end{array}\right]
$$

$$x_1 = 29$$

## EXISTENCE AND UNIQUENESS

Determine whether the system is CONSISTENT. Does a solution exist.

Determine if the solution is UNIQUE. Is there only one solution.

$x_2 - 4x_3 = 8$

$2x_1 - 3x_2 + 2x_3 = 1$

$4x_1 - 8x_2 + 12x_3 = 1$

$$
\left[\begin{array}{ccc:c}
0 & 1 & -4 & 8 \\
2 & -3 & 2 & 1 \\
4 & -8 & 12 & 1 \\
\end{array}\right]
$$

$R_1 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
2 & -3 & 2 & 1 \\
0 & 1 & -4 & 8 \\
4 & -8 & 12 & 1 \\
\end{array}\right]
$$

$\frac{1}{2} R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & -\frac{3}{2} & 1 & \frac{1}{2} \\
0 & 1 & -4 & 8 \\
4 & -8 & 12 & 1 \\
\end{array}\right]
$$

$-4R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -\frac{3}{2} & 1 & \frac{1}{2} \\
0 & 1 & -4 & 8 \\
0 & -2 & 8 & -1 \\
\end{array}\right]
$$

$2R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -\frac{3}{2} & 1 & \frac{1}{2} \\
0 & 1 & -4 & 8 \\
0 & 0 & 0 & 15 \\
\end{array}\right]
$$

$$0x_1 + 0x_2 + 0x_3 = 15$$

INCONSISTENT SYSTEM.

## EXAMPLE 2

$$x_1 - 2x_2 + x_3 = 0$$
$$2x_2 - 8x_3 = 8$$
$$5x_1 - 5x_3 = 10$$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 2 & -8 & 8 \\
5 & 0 & -5 & 10 \\
\end{array}\right]
$$

$-5R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & 10 & -10 & 10 \\
\end{array}\right]
$$

$\frac{1}{2} R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & 10 & -10 & 10 \\
\end{array}\right]
$$

$-10R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & 0 & 30 & -30 \\
\end{array}\right]
$$

$\frac{1}{30}R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & 1 & 0 \\
0 & 1 & -4 & 4 \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

$2R_2 + R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -7 & 8 \\
0 & 1 & -4 & 4 \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

$4R_3 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -7 & 8 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

$7R_3 + R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

$$(1, 0, 1)$$

# 1.1.2 - SOLVE SYSTEMS OF LINEAR EQUATIONS IN AUGMENTED MATRICES USING ROW OPERATIONS

$$x - 2y - 2z = b_1$$

$$2x - 5y - 4z = b_2$$

$$4x - 9y - 8z = b_3$$

$$
\left[\begin{array}{ccc:c}
1 & -2 & -2 & b_1 \\
2 & -5 & -4 & b_2 \\
4 & -9 & -8 & b_3 \\
\end{array}\right]
$$

$-2R_1 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & -2 & -2 & b_1 \\
0 & -1 & 0 & b_2 - 2b_1 \\
4 & -9 & -8 & b_3 \\
\end{array}\right]
$$

$-4R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & -2 & b_1 \\
0 & -1 & 0 & b_2-2b_1 \\
0 & -1 & 0 & b_3-4b_1 \\
\end{array}\right]
$$

$-R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & -2 & -2 & b_1 \\
0 & 1 & 0 & 2b_1 - b_2 \\
0 & -1 & 0 & b_3-4b_1 \\
\end{array}\right]
$$

$R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & -2 & -2 & b_1 \\
0 & 1 & 0 & 2b_1 - b_2 \\
0 & 0 & 0 & b_3 - b_2 - 2b_1 \\
\end{array}\right]
$$

If $-2b_1-b_2+b_3 \neq 0 \rightarrow$ NO SOLUTIONS.

If $-2b_1 - b_2 + b_3 = 0$

$$
\left[\begin{array}{ccc:c}
1 & -2 & -2 & b_1 \\
0 & 1 & 0 & 2b_1 - b_2 \\
0 & 0 & 0 & 0 \\
\end{array}\right]
$$

$2R_2 + R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -2 & 5b_1 - 2b_2 \\
0 & 1 & 0 & 2b_1-b_2 \\
\end{array}\right]
$$

PIVOT VARIABLES $x$ and $y$ in this case.

FREE VARIABLE. $z$ in this case.

PARTICULAR SOLUTION. Setting the free variable equal to zero.

- $Ax = b$
- $z = 0$

$$
x_p =
\left[\begin{array}{c}
5b_1 - 2b_2 \\
2b_1 - b_2 \\
0 \\
\end{array}\right]
$$

SPECIAL SOLUTION. Setting all but one of the free variables equal to zero, and one to one.

- $Ax = 0$
- $z = 1$

$$
x_s =
\left[\begin{array}{c}
2 \\
0 \\
1 \\
\end{array}\right]
$$

ALL SOLUTIONS. $\overrightarrow{x} = \overrightarrow{x_p} + C * \overrightarrow{x_s}$

# 1.2.1 - ROW REDUCTION AND ECHELON FORM.

ECHELON FORM. 'TRIANGLE FORM'

1. All non-zero rows are above all zero rows.
2. Each leading entry of a row is in a column to the right of the leading entry of the row above it.
3. All entries in a column below a leading entry are zeroes.

REDUCED ROW ECHELON FORM. RREF. All conditions above and:

1. The leading entry in each non-zero row equals one.
2. Each leading 1 is the only non-zero entry in the column.

PIVOT. Non-zero number in pivot posistion used to create zeros in row operations.

- PIVOT POSITION. Corresponds to the leading 1 in RREF.
- PIVOT COLUMN. The column that contains the pivot.

## ROW REDUCTION ALGORITHM

1. Begin at leftmost non-zero column, which is a pivot column. Select a nonzero entry as pivot and interchange. If necdessary, to move that entry into the pivot position (Row 1).

$$x_1 - 3x_3 = 8$$

$$2x_1 + 2x_2 + 9x_3 = 7$$

$$x_2 + 5x_3 = -2$$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -3 & 8 \\
2 & 2 & 9 & 7 \\
0 & 1 & 5 & -2 \\
\end{array}\right]
$$

2. Use Row operations to create zeroes in entries below the pivot.

$-2R_1 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -3 & 8 \\
0 & 2 & 15 & -9 \\
0 & 1 & 5 & -2 \\
\end{array}\right]
$$

3. Repeat this process for remaining rows, ignoring rows you've already applied the algorithm to.

$\frac{1}{2}R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -3 & 8 \\
0 & 1 & \frac{15}{2} & -\frac{9}{2} \\
0 & 1 & 5 & -2 \\
\end{array}\right]
$$

$-R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -3 & 8 \\
0 & 1 & \frac{15}{2} & -\frac{9}{2} \\
0 & 0 & -\frac{5}{2} & \frac{5}{2} \\
\end{array}\right]
$$

$-\frac{2}{5}R_3 \rightarrow R_3$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -3 & 8 \\
0 & 1 & \frac{15}{2} & -\frac{9}{2} \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

4. Ensure each pivot is a 1, using scaling as necessary.
5. Beginning with the rightmost pivot and working upwards and to the left, use row operations to create zeroes above each pivot.

$-\frac{15}{2}R_3 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & 0 & -3 & 8 \\
0 & 1 & 0 & 3 \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

$3R_3 + R_1 \rightarrow R_1$

$$
\left[\begin{array}{ccc:c}
1 & 0 & 0 & 5 \\
0 & 1 & 0 & 3 \\
0 & 0 & 1 & -1 \\
\end{array}\right]
$$

$$(5,3,-1)$$

# 1.2.2 - SOLUTION SETS AND FREE VARIABLES

$$
\left[\begin{array}{ccc:c}
1 & 0 & -5 & 1 \\
0 & 1 & 1 & 4 \\
0 & 0 & 0 & 0 \\
\end{array}\right]
$$

$x_1 - 5x_3 = 1 \rightarrow x_1 = 5x_3 + 1$

$x_2 + x_3 = 4 \rightarrow x_2 = 4 - x_3$

$0 = 0 \rightarrow x_3$ is free

FREE VARIABLES can take on any value. Once you choose a value for your free variable, it will determine the values of the other (BASIC) variables.

Let $x_3 = 2$ :

$$x_1 = 5(2) + 1 = 10 + 1 = 11$$

$$x_2 = 4 - 2 = 2$$

$$(11, 2, 2)$$

Let $x_3 = -6$ :

$$x_1 = 5(-6) + 1 = -30 + 1 = -29$$

$$x_2 = -6 -2 = -8$$

$$(-29, -8, -6)$$

## FIND THE GENERAL SOLUTION TO THE SYSTEM

$$x_1-2x_2-x_3+3x_4=0$$

$$-2x_1+4x_2+5x_3-5x_4=3$$

$$3x_1-6x_2-6x_3+8x_4=2$$

$$
\left[\begin{array}{cccc:c}
1 & -2 & -1 & 3 & 0 \\
-2 & 4 & 5 & -5 & 3 \\
3 & -6 & -6 & 8 & 2 \\
\end{array}\right]
$$

$2R_1 + R_2 \rightarrow R_2$

$-3R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{cccc:c}
1 & -2 & 1 & 3 & 0 \\
0 & 0 & 3 & 1 & 3 \\
0 & 0 & -3 & -1 & 2 \\
\end{array}\right]
$$

$R_2 + R_3 \rightarrow R_2$

$$
\left[\begin{array}{cccc:c}
1 & -2 & 1 & 3 & 0 \\
0 & 0 & 0 & 0 & 5 \\
0 & 0 & -3 & -1 & 2 \\
\end{array}\right]
$$

$0 \neq 5$ - INCONSISTENT SYSTEM.

## EXERCISE 1

Find the general solution of the augmented matrix:

$$
\left[\begin{array}{ccc:c}
1 & 3 & 4 & 7 \\
3 & 9 & 7 & 6 \\
\end{array}\right]
$$

$-3R_1 + R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & 3 & 4 & 7 \\
0 & 0 & -5 & -15 \\
\end{array}\right]
$$

$-\frac{1}{5}R_2 \rightarrow R_2$

$$
\left[\begin{array}{ccc:c}
1 & 3 & 4 & 7 \\
0 & 0 & 1 & 3 \\
\end{array}\right]
$$

$$x_1 + 3x_2 + 4x_3 = 7$$

$$x_3 = 3$$

$x_1 + 3x_2 + 4(3) = 7$

$x_1 + 3x_2 = -5$

$x_1 = -5 - 3x_2$

$x_2$ is free

$x_3 = 3$

# 1.3.1 - VECTOR EQUATIONS

VECTOR. An ordered list of numbers.

COLUMN VECTOR. A vector with only one column.

- We often use these for ordered pairs, triples, etc.

VECTORS in $\mathbb{R}^2$. The set of all vectors with two entries.

- $\mathbb{R} \rightarrow$ real numbers
- $2 \rightarrow$ number of entries

This is the set of all points in a plane.

OPERATIONS WITH VECTORS. Same as with other matrices:

- SCALAR. Multiply vector by a constant.
- ADDITION. Add corresponding values.
- MULTIPLICATION. Nope! Dimensions don't work.

## EXAMPLE 1

If

$$
\overrightarrow{u} =
\left[\begin{array}{c}
2 \\
3 \\
\end{array}\right]
$$

and

$$
\overrightarrow{v} =
\left[\begin{array}{c}
-1 \\
2 \\
\end{array}\right]
$$

Find $\overrightarrow{u} + \overrightarrow{v}$ and $-2\overrightarrow{u} + 4\overrightarrow{v}$

$$
\left[\begin{array}{c}
2 \\
3 \\
\end{array}\right]
+
\left[\begin{array}{c}
-1 \\
2 \\
\end{array}\right]
=
\left[\begin{array}{c}
1 \\
5 \\
\end{array}\right]
$$

![example one a](images/fiveexonea.png)

PARALLELOGRAM RULE FOR ADDITION. Fourth point of the parallelogram made up by the point (0, 0) and the two vectors being added together.

$$
-2
\left[\begin{array}{c}
2 \\
3 \\
\end{array}\right]
+ 4
\left[\begin{array}{c}
-1 \\
2 \\
\end{array}\right]
$$

$$
\left[\begin{array}{c}
-4 \\
-6 \\
\end{array}\right]
+
\left[\begin{array}{c}
-4 \\
8 \\
\end{array}\right]
=
\left[\begin{array}{c}
-8 \\
2 \\
\end{array}\right]
$$

![example one b](images/fiveexoneb.png)

## VECTORS IN $\mathbb{R}^n$

If $n \in \mathbb{R}$, then $\mathbb{R}^n$ is the collection of all lists of ordered n-tuples of n real numbers written as $n*1$ column matrices.

$$
\overrightarrow{u} =
\left[\begin{array}{c}
u_1 \\
u_2 \\
u_3 \\
. \\
u_n \\
\end{array}\right]
$$

ZERO VECTOR. The vector whose entries are all zero, denoted by 0.

$$
\overrightarrow{v} =
\left[\begin{array}{c}
0 \\
0 \\
0 \\
0 \\
\end{array}\right]
$$

## ALGEBRAIC PROPERTIES OF $\mathbb{R}^n$

These properties correspond to properties of real numbers and pertain to vectors $u$, $v$ and $w$ and scalars $c$ and $d$.

COMMUTATIVE PROPERTY. $\overrightarrow{u} + \overrightarrow{v} = \overrightarrow{v} + \overrightarrow{u}$

ASSOCIATIVE PROPERTY. $(\overrightarrow{u} + \overrightarrow{v}) + \overrightarrow{w} = \overrightarrow{u} + (\overrightarrow{v} + \overrightarrow{w} )$

ADDITIVE IDENTITY PROPERTY. $\overrightarrow{u} + 0 = 0 + \overrightarrow{u} = \overrightarrow{u}$

INVERSE PROPERTY. $\overrightarrow{u} + -\overrightarrow{u} = -\overrightarrow{u} + \overrightarrow{u} = 0$

DISTRIBUTIVE PROPERTY. $c(\overrightarrow{u} + \overrightarrow{v}) = c \overrightarrow{u} + c \overrightarrow{v}$

DISTRIBUTIVE PROPERTY. $(c + d)\overrightarrow{u} = c \overrightarrow{u} + d \overrightarrow{u}$

DISTRIBUTIVE PROPERTY. $c(d \overrightarrow{u}) = (cd)\overrightarrow{u}$

IDENTITY PROPERTY. $1 \overrightarrow{u} = \overrightarrow{u}$

## EXERCISE 1

Let

$$
\overrightarrow{u} =
\left[\begin{array}{c}
-5 \\
4 \\
\end{array}\right]
$$

Display the vectors $\overrightarrow{u}, 2 \overrightarrow{u}$ and $\frac{1}{2} \overrightarrow{u}$ on a graph.

![exercise one a](images/fiveextwoa.png)

![exercise one b](images/fiveextwob.png)

![exercise one c](images/fiveextwoc.png)

# 1.3.2 - LINEAR COMBINATIONS

The vector defined by $y = c_1v_1 + c_2v_2 + ... + c_nv_n$ where $c_i$ are scalars and $v_i$ are vectors is called a linear combination of $\overrightarrow{v_1}, \overrightarrow{v_2}, ... \overrightarrow{v_n}$ with weights $c_1, c_2, ..., c_n$.

If

$$
\overrightarrow{v_1} =
\left[\begin{array}{c}
1 \\
5 \\
\end{array}\right]
$$

and

$$
\overrightarrow{v_2} =
\left[\begin{array}{c}
-3 \\
4 \\
\end{array}\right]
$$

Estimate the linear combination that generates vectors $\overrightarrow{u}$ and $\overrightarrow{w}$

![six example one](images/sixexone.png)

$\overrightarrow{u} = 2v_1 - v_2$

$\overrightarrow{w} =  -\frac{1}{4}v_1 + \frac{5}{3}v_2$

## EXAMPLE 1

If

$$
\overrightarrow{v_1} =
\left[\begin{array}{c}
1 \\
-2 \\
-5 \\
\end{array}\right]
$$

and

$$
\overrightarrow{v_2} =
\left[\begin{array}{c}
2 \\
5 \\
6 \\
\end{array}\right]
$$

determine whether

$$
b =
\left[\begin{array}{c}
7 \\
4 \\
-3 \\
\end{array}\right]
$$

can be written as a linear combination of $\overrightarrow{v_1}$ and $\overrightarrow{v_2}$. Then determine the weighs such that $c_1v_1 + c_2v_2 = b$.

$c_1v_1 + c_2v_2 = b$

$$
c_1
\left[\begin{array}{c}
1 \\
-2 \\
-5
\end{array}\right]
+
c_2
\left[\begin{array}{c}
2 \\
5 \\
6 \\
\end{array}\right]
=
\left[\begin{array}{}
7 \\
4 \\
-3 \\
\end{array}\right]
$$

$$
\left[\begin{array}{c}
c_1 \\
-2c_1 \\
-5c_1 \\
\end{array}\right]
+
\left[\begin{array}{c}
2c_2 \\
5c_2 \\
6c_2 \\
\end{array}\right]
=
\left[\begin{array}{c}
7 \\
4 \\
-3 \\
\end{array}\right]
$$

$$
\left[\begin{array}{cc:c}
1 & 2 & 7 \\
-2 & 5 & 4 \\
-5 & 6 & -3 \\
\end{array}\right]
$$

$2R_1+R_2 \rightarrow R_2$

$5R_1+R_3 \rightarrow R_3$

$$
\left[\begin{array}{cc:c}
1 & 2 & 7 \\
0 & 9 & 18 \\
0 & 16 & 32 \\
\end{array}\right]
$$

$\frac{1}{9}R_2 \rightarrow R_2$

$$
\left[\begin{array}{cc:c}
1 & 2 & 7 \\
0 & 1 & 2 \\
0 & 16 & 32 \\
\end{array}\right]
$$

$-2R_2 + R_1 \rightarrow R_1$

$-16R_2+R_3 \rightarrow R_3$

$$
\left[\begin{array}{cc:c}
1 & 0 & 3 \\
0 & 1 & 2 \\
0 & 0 & 0 \\
\end{array}\right]
$$

$c_1 = 3$

$c_2 = 2$

$$
3
\left[\begin{array}{c}
1 \\
-2 \\
-5 \\
\end{array}\right]
+ 2
\left[\begin{array}{c}
2 \\
5 \\
6 \\
\end{array}\right]
=
\left[\begin{array}{c}
7 \\
4 \\
-3 \\
\end{array}\right]
$$

## SPANS

A vector equation $x_1\overrightarrow{a_1} + x_2 \overrightarrow{a_2} + ... + x_n \overrightarrow{a_n} = \overrightarrow{b}$ has the same solution set as the linear system whose augmented matrix is $[\overrightarrow{a_1},\overrightarrow{a_2}...\overrightarrow{a_n}|\overrightarrow{b}]$. Therefore, a vector equation only has a solution if the system is consistent.

If $\overrightarrow{v_1},\overrightarrow{v_2}...\overrightarrow{v_p}$ are in $\mathbb{R}^n$, then the set of linear combination is denoted SPAN $\{\overrightarrow{v_1},\overrightarrow{v_2},...,\overrightarrow{v_p}\}$ and is called the subset of $\mathbb{R}^n$ spanned. Essentially, SPAN $\{\overrightarrow{v_1},...\overrightarrow{v_p}\}$ is all vectors that can be written in the form $c_1 \overrightarrow{v_1} + c_2 \overrightarrow{v_2} + ... + c_p \overrightarrow{v_p} = b$ with $c_i$ scalars.

Is $b$ in the plane created by span $\{a_1,a_2\}$ if:

$$
\overrightarrow{a_1} =
\left[\begin{array}{c}
1 \\
-2 \\
3 \\
\end{array}\right],
\overrightarrow{a_2} =
\left[\begin{array}{c}
5 \\
-13 \\
-3 \\
\end{array}\right]
$$

and

$$
\overrightarrow{b} =
\left[\begin{array}{c}
-3 \\
8 \\
1 \\
\end{array}\right]
$$

$$
\left[\begin{array}{cc:c}
1 & 5 & -3 \\
-2 & -13 & 8 \\
3 & -3 & 1 \\
\end{array}\right]
$$

$2R_1 + R_2 \rightarrow R_2$

$-3R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{cc:c}
1 & 5 & -3 \\
0 & -3 & 2 \\
0 & -18 & -8 \\
\end{array}\right]
$$

$-6R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{cc:c}
1 & 5 & -3 \\
0 & -3 & 2 \\
0 & 0 & -2 \\
\end{array}\right]
$$

NO SOLUTION.

## EXERCISE 1

A mining company has two mines. One days operation at mine 1 produces ore that contains 20 metric tons of copper and 550 kg of silver. Mine 2 produces 30 metric tons of copper and 500 kg of silver. How many days should each mine operate to produce 150 tons copper and 2825 kg silver?

$$
x_1
\left[\begin{array}{c}
20 \\
550 \\
\end{array}\right]
+ x_2
\left[\begin{array}{c}
30 \\
500 \\
\end{array}\right]
=
\left[\begin{array}{c}
150 \\
2825 \\
\end{array}\right]
$$

$$
\left[\begin{array}{cc:c}
20 & 30 & 150 \\
550 & 500 & 2825 \\
\end{array}\right]
\sim
\left[\begin{array}{cc:c}
1 & 1.5 & 7.5 \\
550 & 500 & 2825 \\
\end{array}\right]
\sim
\left[\begin{array}{cc:c}
1 & 1.5 & 7.5 \\
0 & -325 & -1300 \\
\end{array}\right]
$$

$$
\sim
\left[\begin{array}{cc:c}
1 & 1.5 & 7.5 \\
0 & 1 & 4 \\
\end{array}\right]
\sim
\left[\begin{array}{cc:c}
1 & 0 & 1.5 \\
0 & 1 & 4 \\
\end{array}\right]
$$

Mine 1: 1.5 days

Mine 2: 4 days

## EXERCISE 2

Let

$$
a_1 =
\left[\begin{array}{c}
1 \\
4 \\
-2 \\
\end{array}\right]
, a_2 =
\left[\begin{array}{c}
-2 \\
-3 \\
7 \\
\end{array}\right]
$$

and

$$
b =
\left[\begin{array}{c}
4 \\
1 \\
h \\
\end{array}\right]
$$

For what values of $h$ is $b$ in the span of $a_1$ and $a_2$?

$$
\left[\begin{array}{cc:c}
1 & -2 & 4 \\
4 & -3 & 1 \\
-2 & 7 & h \\
\end{array}\right]
$$

$-4R_1 + R_2 \rightarrow R_2$

$2R_1 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{cc:c}
1 & -2 & 4 \\
0 & 5 & -15 \\
0 & 3 & h + 8 \\
\end{array}\right]
$$

$\frac{1}{5}R_2 \rightarrow R_2$

$$
\left[\begin{array}{cc:c}
1 & -2 & 4 \\
0 & 1 & -3 \\
0 & 3 & h + 8 \\
\end{array}\right]
$$

$-3R_2 + R_3 \rightarrow R_3$

$$
\left[\begin{array}{cc:c}
1 & -2 & 4 \\
0 & 1 & -3 \\
0 & 0 & h+17 \\
\end{array}\right]
$$

$h = -17$

$h$ must be $-17$ for $b$ to be in the span $\{a_1,a_2\}$

# 1.4.1 - THE MATRIX EQUATION $Ax=b$

If $A$ is a $m \times n$ matrix with columns $a_1, a_2, ..., a_n$ and if $x \in \mathbb{R}^n$ then $Ax$ is the linear combination of the columns of $A$ using the corresponding entires in $x$ as weights:

$$
Ax = [a_1 \ a_2 \ a_3 \ ... \ a_n]
\left[\begin{array}{c}
x_1 \\
x_2 \\
x_3 \\
. \\
x_n \\
\end{array}\right]
= a_1x_1 + a_2x_2 + ... \ a_nx_n
$$

$A$ is $1 \times n$.

The vector is $n \times 1$.

## EXAMPLE 1

Find $Ax$ if:

$$
A =
\left[\begin{array}{ccc}
2 & -1 & 0 \\
3 & 4 & 1 \\
\end{array}\right]
\text{and }
x =
\left[\begin{array}{c}
2 \\
3 \\
-1 \\
\end{array}\right]
$$

$$
Ax = 2
\left[\begin{array}{c}
2 \\
3 \\
\end{array}\right]
+ 3
\left[\begin{array}{c}
-1 \\
4 \\
\end{array}\right]
- 1
\left[\begin{array}{c}
0 \\
1 \\
\end{array}\right]
$$

$$
=
\left[\begin{array}{c}
4 \\
6 \\
\end{array}\right]
+
\left[\begin{array}{c}
-3 \\
12 \\
\end{array}\right]
+
\left[\begin{array}{c}
0 \\
-1 \\
\end{array}\right]
$$

$$
=
\left[\begin{array}{c}
1 \\
17 \\
\end{array}\right]
$$

## EXAMPLE 2

Write the linear combination $2v_1 - 3v_2 + 4v_3$ as a matrix times a vector.

$$
A =
\left[\begin{array}{ccc}
v_1 & v_2 & v_3
\end{array}\right]
\left[\begin{array}{c}
2 \\
-3 \\
4 \\
\end{array}\right]
$$

## REPRESENTATIONS

SYSTEM OF EQUATIONS:

$$
2x_1 + 3x_2 - x_3 = 3 \\
2x_2 + 3x_3 = 4 \\
$$

AUGMENTED MATRIX:

$$
\left[\begin{array}{ccc:c}
2 & 3 & -1 & 3 \\
0 & 2 & 3 & 4 \\
\end{array}\right]
$$

VECTOR EQUATION: $x_1 \overrightarrow{a_1} + x_2 \overrightarrow{a_2} + \ ... \ + x_n \overrightarrow{a_n} = \overrightarrow{b}$

$$
x_1
\left[\begin{array}{c}
2 \\
0 \\
\end{array}\right]+x_2
\left[\begin{array}{c}
3 \\
2 \\
\end{array}\right]+x_3
\left[\begin{array}{c}
-1 \\
3 \\
\end{array}\right]=
\left[\begin{array}{c}
3 \\
4 \\
\end{array}\right]
$$

MATRIX EQUATION: $Ax = b$

$$
\left[\begin{array}{ccc}
2 & 3 & -1 \\
0 & 2 & 3 \\
\end{array}\right]
\left[\begin{array}{c}
x_1 \\
x_2 \\
x_3 \\
\end{array}\right]=
\left[\begin{array}{c}
3 \\
4 \\
\end{array}\right]
$$

## EXISTENCE OF SOLUTIONS

Let $A$ be a $m \times n$ matrix. Then these statements are logically equivalent:

1. For each $b$ in $\mathbb{R}^m$, the equation $Ax = b$ has a solution.
2. Each $b$ in $\mathbb{R}^m$ is a linear combination of the columns of $A$.
3. The columns of $A$ span $\mathbb{R}^m$.
4. $A$ has a pivot position in every row.
   - $A$ must be a coefficient matrix - not augmented.

## EXERCISE 1

$$
\text{Let } A=
\left[\begin{array}{ccc}
1 & 3 & 4 \\
-4 & 2 & -6 \\
-3 & -2 & -7 \\
\end{array}\right]\text{and } b=
\left[\begin{array}{c}
b_1 \\
b_2 \\
b_3 \\
\end{array}\right]
$$

Is the equation $Ax = b$ consistent for all possible $B$?

$$
\left[\begin{array}{ccc:c}
1 & 3 & 4 & b_1 \\
-4 & 2 & -6 & b_2 \\
-3 & -2 & -7 & b_3 \\
\end{array}\right]\sim
\left[\begin{array}{ccc:c}
1 & 3 & 4 & b_1 \\
0 & 14 & 10 & 4b_1 + b_2 \\
0 & 7 & 5 & 3b_1 + b_3 \\
\end{array}\right]\sim
\left[\begin{array}{ccc:c}
1 & 3 & 4 & b_1 \\
0 & 14 & 10 & 4b_1 + b_2 \\
0 & 0 & 0 & b_1 - \frac{1}{2}b_2 + b_3 \\
\end{array}\right]
$$

INCONSISTENT

# 1.4.2 - COMPUTATION OF $Ax$

## ROW-VECTOR RULE FOR COMPUTING $Ax$

If $Ax$ is defined, the $i^{th}$ entry in $Ax$ is the sum of the products of corresponding entires from row $i$ of $a$ and from the vector $x$.

## EXERCISE 1

$$
\text{Given } A=
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right],\overrightarrow{u}=
\left[\begin{array}{c}
-4 \\
2 \\
\end{array}\right],\overrightarrow{v}=
\left[\begin{array}{c}
3 \\
-1 \\
\end{array}\right]
$$

Find:

1. $A(\overrightarrow{u}+ \overrightarrow{v})$

---

$$
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left(\left[\begin{array}{c}
-4 \\
2 \\
\end{array}\right]+
\left[\begin{array}{c}
3 \\
-1 \\
\end{array}\right]\right)=
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left[\begin{array}{c}
-1 \\
1 \\
\end{array}\right]
$$

$$
\left[\begin{array}{c}
2(-1) + 1(1) \\
-4(-1) + 2(1) \\
\end{array}\right]=
\left[\begin{array}{c}
-2 + 1 \\
4 + 2 \\
\end{array}\right]=
\left[\begin{array}{c}
-1 \\
6 \\
\end{array}\right]
$$

2. $A \overrightarrow{u} + A \overrightarrow{v}$

---

$$
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left[\begin{array}{c}
-4 \\
2 \\
\end{array}\right]+
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left[\begin{array}{c}
3 \\
-1 \\
\end{array}\right]
$$

$$
\left[\begin{array}{c}
2(-4) + 1(2) \\
-4(-4) + 2(2) \\
\end{array}\right]+
\left[\begin{array}{c}
2(3) + 1(-1) \\
-4(3) + 2(-1) \\
\end{array}\right]
$$

$$
\left[\begin{array}{c}
-8 + 2 \\
16+4 \\
\end{array}\right]+
\left[\begin{array}{c}
6 -1 \\
-12 -2 \\
\end{array}\right]=
\left[\begin{array}{c}
-6 \\
20 \\
\end{array}\right]
\left[\begin{array}{c}
5 \\
-14 \\
\end{array}\right]=
\left[\begin{array}{c}
-1 \\
6 \\
\end{array}\right]
$$

## EXERCISE 2

$$
\text{Given } A=
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right], \overrightarrow{u}=
\left[\begin{array}{c}
-4 \\
2 \\
\end{array}\right],c=2
$$

Find:

1. $A(c \overrightarrow{u})$

---

$$
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left(
2
\left[\begin{array}{c}
-4 \\
2 \\
\end{array}\right]
\right)
$$

$$
\left[\begin{array}{cc}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left[\begin{array}{c}
-8 \\
4 \\
\end{array}\right]
$$

$$
\left[\begin{array}{c}
2(-8) + 1(4) \\
-4(-8) + 2(4) \\
\end{array}\right]=
\left[\begin{array}{c}
-16 + 4 \\
32 + 8 \\
\end{array}\right]=
\left[\begin{array}{c}
-12 \\
40 \\
\end{array}\right]
$$

2. $c(A \overrightarrow{u})$

---

$$
2
\left(
\left[\begin{array}{c}
2 & 1 \\
-4 & 2 \\
\end{array}\right]
\left[\begin{array}{c}
-4 \\
2 \\
\end{array}\right]
\right)
$$

$$
2
\left[\begin{array}{c}
2(-4) + 1(2) \\
-4(-4) + 2(2) \\
\end{array}\right]=
2
\left[\begin{array}{c}
-8 + 2 \\
16 + 4 \\
\end{array}\right]
$$

$$
2
\left[\begin{array}{c}
-6 \\
20 \\
\end{array}\right]=
\left[\begin{array}{c}
-12 \\
40 \\
\end{array}\right]
$$
