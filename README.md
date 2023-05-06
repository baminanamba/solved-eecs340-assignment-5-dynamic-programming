Download Link: https://assignmentchef.com/product/solved-eecs340-assignment-5-dynamic-programming
<br>
Problem 1

Provide a dynamic programming solution to each problem by following the described steps:

<strong>Steps:</strong>

(i) Identify the “last” question you need to answer in developing a solution.

*(ii)* Define and prove optimal substructure.

(iii) Define subproblems, express the solution to the overall problem in terms of the subproblems. (iv) Formulate a recursive solution to the subproblems. Do not forget to specify the base case(s).

(v) Characterize the runtime of the resulting procedure assuming that you would implement your solution using a bottom-up procedure.

*(vi)* Provide the pseudo code of the bottom-up procedure you use to compute the value of the optimal solution, as well as the procedure for reconstructing the optimal solution.

<strong>* </strong>Note that, you only need to apply items (ii) and (vi) on <u>one </u>of the problems (of your own choice, you can choose a different problem for each item). Clearly express which problems you choose.

<strong>Problems:</strong>

<ul>

 <li>We are given an arithmetic expression <em>x</em><sub>1</sub><em>o</em><sub>1</sub><em>x</em><sub>2</sub><em>o</em><sub>2</sub><em>…x<sub>n</sub></em><sub>−1</sub><em>o<sub>n</sub></em><sub>−1</sub><em>x<sub>n </sub></em>such that <em>x<sub>i </sub></em>for 1 ≤ <em>i </em>≤ <em>n </em>are positive numbers and <em>o<sub>i </sub></em>∈{+<em>,</em>×} for 1 ≤ <em>i </em>≤ <em>n </em>− 1 are arithmetic operations (summation or multiplication). We would like to parenthesize the expression in a such a way that the value of the expression is <u>maximized</u>. For example, if the expression is 3+4×2+6×0<em>.</em>5, then the optimal parenthesization is (3 + 4) × (2 + (6 × 0<em>.</em>5)), with a value of 35.</li>

 <li>We are given <em>n </em>types of coin denominations with integer values <em>v</em><sub>1</sub>, <em>v</em><sub>2</sub>, …, <em>v<sub>n</sub></em>. Given an integer <em>t</em>, we would like to compute the <u>minimum </u>number of coins to make change for <em>t </em>(i.e., we would like to compute the minimum number of coins that add up to <em>t</em>, where repetitions are allowed). We know that one of the coins has value 1, so we can always make change for any amount of money <em>t</em>. For example, if we have coin denominations of 1, 2, and 5, then the optimal solution for <em>t </em>= 9 is 5, 2, 2.</li>

 <li>Given two strings <em>X </em>=<em>&lt; x</em><sub>1</sub><em>,x</em><sub>2</sub><em>,…,x<sub>m </sub>&gt; </em>and <em>Y </em>=<em>&lt; y</em><sub>1</sub><em>,y</em><sub>2</sub><em>,…,y<sub>n </sub>&gt;</em>, the edit distance between <em>X </em>and <em>Y </em>is defined as the <u>minimum </u>number of edit operations (<em>replacement</em>, <em>insertion</em>, or <em>deletion </em>of a character) required to convert <em>X </em>to <em>Y </em>. For example, the edit distance between <em>X </em>= <em>esteban </em>and <em>Y </em>= <em>stephen </em>is 4, comprising of 1 deletion (<em>e</em>), 1 insertion (<em>h</em>), and 2 replacements (<em>b </em>→ <em>p </em>and <em>a </em>→ <em>e</em>). We would like to compute the edit distance between two given strings.</li>

</ul>

<h1>Problem 2</h1>

We are given <em>n </em>currencies and an exchange rate <em>r<sub>ij </sub></em>for any pair of currencies <em>i </em>an <em>j</em>. Namely, if we exchange 1 unit of currency <em>i </em>with currency <em>j</em>, we receive <em>r<sub>ij </sub></em>units of currency <em>j</em>. If we are given a source currency <em>s </em>and a target currency <em>t</em>, then we can go through a path of different currencies to reach <em>t </em>from <em>s </em>so as to maximize our profit. The markets can also charge an exchange fee depending on the number of exchanges we make. For example if the exchange fee is <em>f</em>(<em>k</em>) for making <em>k </em>exchanges and we start with 1 unit of currency <em>s</em>, then the path of exchanges <em>s </em>→ <em>t </em>will yield <em>r<sub>st </sub></em>− <em>f</em>(1) units of currency <em>t</em>, whereas the path of exchanges <em>s </em>→ <em>i </em>→ <em>j </em>→ <em>t </em>will yield <em>r<sub>si </sub></em>×<em>r<sub>ij </sub></em>×<em>r<sub>jt </sub></em>−<em>f</em>(3) units of currency <em>t</em>. The problem is to find the sequence of exchanges that will maximize the amount of target currency <em>t </em>we can obtain for a given source currency <em>s</em>.

<ul>

 <li>Define and prove the optimal substructure for this problem when there is no exchange fee (<em>f</em>(<em>k</em>) = 0 for all <em>k</em>).</li>

 <li>Prove that it is possible to find an exchange fee schedule <em>f</em>(<em>k</em>) so that the optimal substructure you defined above will not hold anymore.</li>

</ul>