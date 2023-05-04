Download Link: https://assignmentchef.com/product/solved-csci316-assignment4
<br>
<ol>

 <li>SUM is a function that is already defined on venus and euclid; if L <em>is any list of numbers</em> then (SUM L)       returns the sum of the elements of L.  [Thus (SUM ( )) returns 0.]  Complete the following definition of a       function MY-SUM <strong><em>without making further calls of</em></strong>  SUM and without calling MY-SUM recursively, in       such a way that if L is any <strong><em>nonempty</em></strong> list of numbers then (MY-SUM L) is equal to (SUM L).</li>

</ol>




(defun my-sum (L)

(let ((X (sum (cdr L))))

__________________________________ ))







<strong>*If you have difficulty with these problems, you are encouraged to see me during my office hours.  Questions about these    problems that are e-mailed to me </strong><strong>will <em>not</em> be answered until <em><u>after</u></em> the due date</strong><strong>. </strong>

<strong> </strong>

<strong><sup>†</sup></strong><strong>This assumes you executed the  </strong><strong>/home/faculty/ykong/316setup</strong><strong>  command on </strong><strong>venus</strong><strong> before you did   </strong><strong> </strong><strong>Lisp Assignment 1 (in accordance with the instructions for Assignment 1). </strong>

<ol>

 <li>NEG-NUMS is a function that is already defined on venus and euclid; if L <em>is any list of real numbers</em> then  (NEG-NUMS  L) returns a new list that consists of the negative elements of L.   For example:</li>

</ol>

(NEG-NUMS ‘(–1 0 –8  2  0 8 –1 –8  2  8  4 –3 0) ) =&gt; (–1 –8 –1 –8 –3).

Complete the following definition of a function MY-NEG-NUMS <strong><em>without making further calls       of</em></strong>  NEG-NUMS and without calling MY-NEG-NUMS recursively, in such a way that if L is          any <strong><em>nonempty</em></strong> list of numbers then (MY-NEG-NUMS L) is equal to (NEG-NUMS L).




(defun my-neg-nums (L)

(let ((X (neg-nums (cdr L))))

______________________________________                ____________ ))

There are two cases: (car L) may or may not be negative.

<strong> </strong>

<ol>

 <li>INC-LIST-2 is a function that is already defined on venus and euclid; if L <em>is any list of numbers</em> and N is a number then (INC-LIST-2 L N) returns a list of the same length as L in which each element       is equal to  (N + the corresponding element of L).   For example,</li>

</ol>

(INC-LIST-2  ( )  5) =&gt; NIL               (INC-LIST-2  ‘(3  2.1  1  7.9)  5) =&gt; (8  7.1  6  12.9)

Complete the following definition of a function MY-INC-LIST-2 <strong><em>without making further calls       of</em></strong>  INC-LIST-2 and without calling MY-INC-LIST-2 recursively, in such a way that if L is         any <strong><em>nonempty</em></strong> list of numbers and N is any number then (MY-INC-LIST-2 L N) is equal to         (INC-LIST-2 L N).

(defun my-inc-list-2 (L N)

(let ((X (inc-list-2 (cdr L) N)))

__________________________________ ))




<ol>

 <li>INSERT is a function that is already defined on venus and euclid; if N <em>is any real number and</em> L <em>is any list of real numbers in ascending order</em> then (INSERT N L) returns a list of numbers in <em> </em>     ascending order obtained by inserting N in an appropriate position in L.   Examples:</li>

</ol>

(INSERT 8 ( )) =&gt; (8)      (INSERT 4 ‘(0 0 1 2 4)) =&gt; (0 0 1 2 4 4)       (INSERT 4 ‘(0 0 1 3 3 7 8 8)) =&gt; (0 0 1 3 3 4 7 8 8)

Complete the following definition of a function MY-INSERT <strong><em>without making further calls       of</em></strong>  INSERT and without calling MY-INSERT recursively, in such a way that if N is any real <em> </em>     number and L is any <strong><em>nonempty</em></strong> list of real numbers in ascending order then (MY-INSERT  N  L)              is equal to (INSERT  N  L).

(defun my-insert (N L)

(let ((X (insert N (cdr L))))

__________________________________

__________________________________ ))

[There are two cases: N may or may not be ≤  (car L).  In the former case you do not need to use X,              so if you move that case outside the LET the function will be more efficient.]




<ol>

 <li>ISORT is a function that is already defined on venus and euclid; if L <em>is any list of real numbers</em> then (ISORT L) is a list consisting of the elements of L in ascending order.  Complete the       following definition of a function MY-ISORT <strong><em>without making further calls of</em></strong>  ISORT and          without calling MY-ISORT recursively, in such a way that if L is any <strong><em>nonempty</em></strong> list of real       numbers then (MY-ISORT  L) is equal to (ISORT L).</li>

</ol>




(defun my-isort (L)

(let ((X (isort (cdr L))))

__________________________________ ))

<strong>Hint</strong>: You should not have to call any function other than INSERT and CAR.







<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>IMPORTANT:  If you have not yet done problems 15 – 20 of Lisp Assignment 2, <u>do those six</u>                     <u>problems before you work on the next two problems</u>! </strong>




<ol>

 <li>SPLIT-LIST is a function that is already defined on venus and euclid; if L is any list then (SPLIT-LIST  L) returns a list of two lists, in which the first list consists of the 1<sup>st</sup>, 3<sup>rd</sup>,  5<sup>th</sup>,  …        elements of L, and the second list consists of the 2<sup>nd</sup>, 4<sup>th</sup>, 6<sup>th</sup>,  … elements of L.  Examples:               (SPLIT-LIST ( )) =&gt; (NIL NIL)       (SPLIT-LIST ‘(A B C D 1 2 3 4 5))  =&gt; ((A C 1 3 5) (B D 2 4))</li>

</ol>

(SPLIT-LIST ‘(B C D 1 2 3 4 5)) =&gt;  ((B D 2 4) (C 1 3 5))             (SPLIT-LIST ‘(A)) =&gt; ((A) NIL)

Complete the following definition of a function MY-SPLIT-LIST <strong><em>without making further calls of</em></strong>                SPLIT-LIST and without calling MY-SPLIT-LIST recursively, in such a way that if L is any  <strong>   </strong>  <strong><em>nonempty</em></strong> list then (MY-SPLIT-LIST L) is equal to (SPLIT-LIST L).




(defun my-split-list (L)

(let ((X (split-list (cdr L))))

__________________________________ ))




<ol>

 <li>PARTITION is a function that is already defined on venus and euclid; if L <em>is a list of real numbers and</em> P <em>is a real number</em> then (PARTITION L P) returns a list whose CAR is a list of the       elements of L that are strictly less than P, and whose CADR is a list of the other elements of L.         Each element of L must appear in the CAR or CADR of (PARTITION L P), and should appear       there just as many times as in L. Examples: (PARTITION ‘(7 5 3 2 1 5) 1) =&gt; (NIL (7 5 3 2 1 5))</li>

</ol>

(PARTITION ‘(4 0 5 3 1 2 4 1 4) 4) =&gt; ((0 3 1 2 1) (4 5 4 4))   (PARTITION ( ) 9) =&gt; (NIL NIL)                Complete the following definition of a function MY-PARTITION <strong><em>without making further calls       of</em></strong>  PARTITION and without calling MY-PARTITION recursively, in such a way that if L is any  <strong>    </strong> <strong><em>nonempty</em></strong> list of real numbers and P is a real number then (MY-PARTITION L P) is equal to       (PARTITION L P).

(defun my-partition (L P)

(let ((X (partition (cdr L) P)))

___________________________________________                          ___________________________________________ ))

There are two cases: (car L) may or may not be less than P.




<strong> </strong>

<strong>SECTION 2 (Main Problems)</strong>




<strong>Your solutions to the following problems will count a total of 2% towards your grade if the grade is computed using rule A.  </strong><strong>Note that a working solution to each of problems 1 – 7 can be obtained  from a solution to the corresponding one of problems A – G by changing the name of the function MY-FUNC to FUNC and adding appropriate base case code, without changing the LET block.</strong><strong>  [The resulting definition of FUNC will be correct because it has the following property: <em>In all non-base cases where</em> <em>FUNC’s recursive call returns the correct result, FUNC returns the same result as  MY-FUNC.</em> Assuming your definition of MY-FUNC is correct, this property implies FUNC returns the correct result whenever FUNC’s recursive call returns the correct result, which in turn implies FUNC never returns an incorrect result if your base case code is correct.] But if you solve a problem this way then </strong><strong>any cases that do not need to use the LET’s local variable should be moved out of the </strong>

<strong>LET</strong><strong>, and </strong><strong>the LET should be eliminated if the value of its local variable is never used more than once</strong><strong>. </strong>

<strong> </strong>

<strong>Note 1:  </strong>On <strong>euclid</strong> and <strong>venus</strong>, when you LOAD a function definition for any of problems 1 – 7, your function will <strong><em>replace</em></strong> the                predefined function that has the same name (and Clisp will issue a WARNING that the predefined function has been                redefined). It follows, for example, that if your definition of SUM for problem 1 is wrong then, after you LOAD your                definition of SUM, your definition of MY-SUM for problem A may stop working even if that definition is correct                because MY-SUM calls SUM.




<strong>Note 2</strong>:  You may use ENDP or NULL to test whether a list is empty. Recall that (ENDP L) returns the same result as (NULL L)                if the value of L is a list. (But evaluation of (ENDP L) produces an error if the value of L is an atom other than NIL.)




<ol>

 <li>Define a recursive function SUM with the properties stated in problem A. Note that whereas NIL is      not a valid argument of MY-SUM,  NIL is a valid argument of SUM.</li>

 <li>Define a recursive function NEG-NUMS with the properties stated in problem B. Note that NIL     is a valid argument of NEG-NUMS.</li>

</ol>




<ol start="3">

 <li>Define a recursive function INC-LIST-2 with the properties stated in problem C. Note that the first     argument of INC-LIST-2 may be NIL.</li>

</ol>




<ol start="4">

 <li>Define a recursive function INSERT with the properties stated in problem D. Note that the second      argument of INSERT may be NIL.</li>

</ol>




<ol start="5">

 <li>Define a recursive function ISORT with the properties stated in problem E. <strong>Hint</strong>: In your definition of</li>

</ol>

ISORT you should not have to call any function other than ISORT itself, INSERT, CAR, CDR, and

ENDP or NULL.   (An IF or COND form is not considered to be a function call, and will be needed.)




<ol start="6">

 <li>Define a recursive function SPLIT-LIST with the properties stated in problem F.</li>

</ol>




<ol start="7">

 <li>Define a recursive function PARTITION with the properties stated in problem G.</li>

</ol>




<ol start="8">

 <li>Without using MEMBER, complete the following definition of a recursive function POS such that if L <em>is a list and</em> E <em>is an element of</em> L then (POS E L) returns the position of the first                 occurrence of E in L, but <em>if </em>L <em>is a list and </em>E<em> is not an element of </em>L<em> then </em>(POS E L)<em> returns</em></li>

</ol>

(DEFUN POS (E L)

(COND ((ENDP L)            … )

((EQUAL E (CAR L))         … )

(T   (LET  ((X  (POS E (CDR L))))




…

))))

Examples:  (POS 5 ‘(1 2 5 3 5 5 1 5)) =&gt; 3    (POS ‘A ‘(3 2 1)) =&gt; 0    (POS ‘(3 B) ‘(3 B)) =&gt; 0     (POS ‘(A B)  ‘((K)  (3 R C)  A  (A B)  (K L L)  (A B)))  =&gt; 4       (POS ‘(3 B) ‘((3 B))) =&gt; 1




<ol start="9">

 <li>Define a recursive function SPLIT-NUMS such that if N <em>is a non-negative integer</em> then</li>

</ol>

(SPLIT-NUMS N)  returns a list of two lists: The first of the two lists consists of the even                     integers between 0 and N in descending order, and the other list consists of the odd integers                  between 0 and N in descending order.   Examples:   (SPLIT-NUMS 0) =&gt; ((0) NIL)                              (SPLIT-NUMS 7) =&gt; ((6 4 2 0) (7 5 3 1))     (SPLIT-NUMS 8) =&gt; ((8 6 4 2 0) (7 5 3 1))







<strong>IMPORTANT: In problems 10 – 13 the term <em><u>set</u></em> is used to mean a proper list of numbers and/or symbols <em><u>in which no atom occurs more than once</u>.  </em>You may use MEMBER but <em>not</em> the functions UNION, NUNION, REMOVE, DELETE, SET-DIFFERENCE, and SET-EXCLUSIVE-OR.   </strong>




<ol start="10">

 <li>Define a recursive function SET-UNION such that if s1 <em>and</em> s2 <em>are <strong><u>sets</u></strong></em> then (SET-UNION s1 s2) is a <strong><em><u>set</u></em></strong> that contains the elements of s1 and the elements of s2, but no other elements.  Thus        (SET-UNION ‘(A B C D) ‘(C E F)) should return a list consisting of the atoms A, B, C, D, E, and F        (in any order) in which no atom occurs more than once.</li>

</ol>




<ol start="11">

 <li>Define a recursive function SET-REMOVE such that if s <em>is a <strong><u>set</u></strong> and</em> x <em>is an atom in</em> s then (SET-REMOVE x s) is a <strong><em><u>set</u></em></strong> that consists of all the elements of s except x, but if s <em>is a <strong><u>set</u></strong> and</em>        x <em>is an atom which is not in</em> s then (SET-REMOVE x s) returns a <strong><em><u>set</u></em></strong> that is equal to s.</li>

</ol>




<strong>In problems 12 and 13 you may use the function SET-REMOVE from problem 11.   </strong>




<ol start="12">

 <li>Define a recursive function SET-EXCL-UNION such that if s1 <em>and </em>s2 <em>are <strong><u>sets</u></strong></em> then</li>

</ol>

(SET-EXCL-UNION s1 s2) is a <strong><em><u>set</u></em></strong> that contains all those atoms that are elements of <em>exactly one</em>        of s1 and s2, but no other atoms. (SET-EXCL-UNION s1 s2) does <em>not</em> contain any atoms that are         neither in s1 nor in s2, and also does <em>not</em> contain the atoms that are in both of s1 and s2.  For        example, (SET-EXCL-UNION ‘(A B C D) ‘(E C F G A)) should return a list consisting of the        atoms B, D, E, F, and G (in any order) in which no atom occurs more than once.







<ol start="13">

 <li>Define a recursive function SINGLETONS such that if e <em>is any list of numbers and/or symbols </em>then (SINGLETONS e) is a <strong><em><u>set</u></em></strong> that consists of all the atoms that occur <em>just once</em> in e.</li>

</ol>

<strong>Examples</strong>:   (SINGLETONS ( )) =&gt; NIL   (SINGLETONS ‘(G A B C B)) =&gt; (G A C)

(SINGLETONS ‘(H G A B C B)) =&gt; (H G A C)     (SINGLETONS ‘(A G A B C B)) =&gt; (G C)                (SINGLETONS ‘(B G A B C B)) =&gt; (G A C)     [<strong>Hint</strong>: When e is nonempty, consider the case in        which (car e) is a member of (cdr e), and the case in which (car e) is not a member of (cdr e).]

<strong> </strong>