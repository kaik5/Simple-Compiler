# Simple-Compiler
A Simple Compiler that  will read the program and make sure that its syntax and semantics are correct. If the syntaxor semantics are not correct, the compiler will output an error message with the line number. If input programhas correct syntax and semantics, the compiler should evaluate the polynomial expressions in the START section of the program and the output of the compiler is the sequence of values resulting from the evaluationsof the polynomials in the START section.

# Simple input and output
POLY F = x^2 + 1;
POLY G = x + 1;STARTF(4);
G(2);1 2 3 18 19
The output of the program will be 17 3

POLY A(M, N, O) = M^7 - 6 N M O^4 + 9 M^8 N^3 O^2 - 5 N M^5 O + 23 M^2 N O;
POLY B = x^4 + x^3 + x^2 + x^1 + x^0;
POLY C(P, Q) = P - P + Q - Q;
START
INPUT X;
INPUT Y;
C(X, Y);
C1(X);
D(1);
B(D(1));
98 34 92 12 3 4
Output: 3: Error Code 3: 8 9 10 

POLY A(M, N, O) = M^7 - 6 N M O^4 + 9 M^8 N^3 O^2 - 5 N M^5 O + 23 M^2 N O;
POLY B = x^4 + x^3 + x^2 + x^1 + x^0;
POLY C(P, Q) = P - P + Q - Q;
START
INPUT X;
INPUT Y;
INPUT Z;
C(X, Y, Z);
A(X);
B(1);
B(B(1));
98 34 92 12 3 4
Error Code 4: 8 9 


1: POLY F = x^2 + 1;
2: POLY G(X,Y) = X Y^2 + X Z;
3: START
4: INPUT Z;
5: INPUT W;
6: F(Z);
7: G(Z,W);
8: 1 2 3 18 19
The polynomial G is declared with twovariables X and Y but its equation (calledpolynomial_bodyin the grammar) has Z which is differentfrom X and Y. The output captures this error: Error Code 2: 2

POLY A(M, N, O) = M^7 - 6 N M O^4 + 9 M^8 N^3 O^2 - 5 N M^5 O + 23 M^2 N O;
POLY B = x^4 + x^3 + x^2 + x^1 + x^0;
POLY C(P, Q) = P - P + Q - Q;
START
INPUT X;
INPUT Y;
INPUT Z;
C(A, B);
A(X, F, E);
B(1);
B(B(1));
98 34 92 12 3 4
Error Code 5: 8 8 9 9 

POLY T(X, Y) = X + Y;
POLY (R, Y, U, W) = R^2 + Y^2 + W^44 + U;
POLY Y = x + 5555;
START
INPUT A;
INPUT B;
INPUT C;
Y(A);
1 2 3 4 5
SYNTAX ERROR !&%!
