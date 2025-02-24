Download Link : https://programming.engineering/product/ve477-homework-8/

# VE477-Homework-8
VE477 Homework 8

Questions preceded by a * are optional. Although they can be skipped without any deduction, it is important to know and understand the results they contain.

Ex. 1 — Fast multi-point evaluation and interpolation

Let R be a commutative ring, u0, · · · , un−1 be n elements in R, and mi = X − ui , with 0 ≤ i < n, be n degree 1 polynomials in R[X ]. Without loss of generality we assume n to be a power of 2.

Part I — Fast multi-point evaluation

In order to perform fast multi-point evaluation the set of points U = {u0, · · · , un } is recursively split into two halves of equal cardinality.

    1.
    	

    Draw the binary tree resulting from the recursive split of the set U.

    2.
    	

    Denote thei
    	

    depth of the binary tree by k and for all 0 ≤ i ≤ k and 0 ≤ j < 2k −i , define
    	

    Mi ,j = ∏l2=0−1 mj 2i +l . Prove that for each i, j
    			

    (1.1)
    	

    Mi +1,j
    	

    = Mi ,2j Mi ,2j +1
    			
    		

    = mj .
    	
    	

    M0,j
    	

    How do the Mi ,j relate to the binary tree?

    Fast multi-point evaluation.

        Write an algorithm that builds the subproduct tree and returns the polynomials Mi ,j as defined in (1.1).

        Write an recursive algorithm which takes a polynomial P of degree less than n = 2k as input as well as u0, · · · , un−1 and the subproducts Mi ,j . It should go down the subproduct tree and return P(u0), · · · , P(un−1).

    Correctness and complexity.

        By induction on k, prove the correctness of the previous algorithm.

        Show that the complexity of the algorithm is O(M(n) log n) operations in R.

Part II — Fast interpolation

Reusing the notations from part I, let m be the product of all the mi , i.e. m = ∏
	

n 1
	

(X − ui ).

i =0−

* 1. Explain how to perform Lagrange interpolation.

Hint: an element a in R is invertible if there is a b in R such that ab = e, with e a unit in R.

    2. Let si = ∏
    	

    n 1
    	

    m/(x − uj ) and that

    i ̸=j 1/(ui − uj ). Prove that m′, the derivative of m, is m′ = ∑j =0−

m′(ui ) = 1/si .

    Devise a divide and conquer algorithm which proceeds from the leaves to the root of the binary tree from part I question 1, in order to return the interpolation of P at the points u0, · · · , un−1. Hint: use the Mi , j to apply a recursive approach to Lagrange interpolation.

    Correctness and complexity.

* a) By induction on k, prove the correctness of the previous algorithm.

            Prove that computing the si in question 2, amounts to O(M(n) log n) operations in R.

            Conclude that the interpolation problem can be solved in O(M(n) log n) ring operations.

    Discuss the possibility of pre-computing the subproducts Mi , j.

Ex. 2 — Critical thinking

        1. Let G be a group such that for all x, y in G , (xy)2 = (yx)2, and for any x ≠ e, x2 ≠ e, where e is a unit element. Prove that G is abelian.

            After passing ve477 two students, s1 and s2, are asked to determine two integers x and y such that 1 < x < y and x + y < 100. Student s1 is told that x + y , while s2 is given xy. Remembering the importance of critical thinking they start discussing:

S2 : “No idea what those two numbers could be…”

S1 : “I’m not surprised, I knew you couldn’t know!”

S2 : “Uhm…so now I know…”

S1 : “So do I!” What about you?

* Ex. 3 — Beyond ve477

Explain what the Swype keyboard is and propose some hints on how it could be implemented.

    Ex. 4 — Course survey

Complete the course survey and get a +5 bonus on the homework.
