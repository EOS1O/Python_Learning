# Assignment2

## Q1.

（a）
$$
\begin{eqnarray*}
&\because& A \ -> DE \\ 
&\therefore& A \ -> D \quad and \quad A \ ->E \\
&\because& E \ -> CD \\ 
&\therefore& A \ -> CD \\
&\therefore& A \ -> C \quad and \quad A \ ->D \\
&\\&
&\because& E \ -> CD \\ 
&\therefore& E \ -> C \quad and \quad E \ ->D \\
&\because& CE \ -> ADH \quad and \quad E \ ->D \\
&\therefore& C \ -> AH \\
&\because& AH \ -> I \\
&\therefore& C \ -> I \\
\\
&\because& A \ -> C \quad and \quad C \ ->I\\
&\therefore& A \ -> I \\
\end{eqnarray*}
$$
(b)
$$
\begin{align*}\label{2}
  & step1 \\
  & let X:= \left\{ A,B,E,C,H,J \right\} \\
  & \\
  & step2 \\
  & try  \quad to \quad remove \quad A \\
  & \left\{ A,B,E,C,H,J \right\}^+=\left\{ A,B,C,D,E,G,H,I \right\} \\
  & Thus \quad X:=\left\{ A,B,E,C,H,J \right\} \\
  & \\
  & step3: \\
  & Try \quad to \quad remove \quad B \\
  & \left\{E,C,H,J \right\}^+=\left\{A,C,D,E,H,I,J \right\} \\
  & B \quad cannot \quad be \quad removed \\
  & \\
  & Then \quad try \quad to \quad remove \quad E \\
  & \left\{B,C,H,J \right\}^+ =\left\{B,C,G,H,I,J \right\} \\
  & E \quad cannot \quad be \quad removed \\
  & \\
  & Then \quad try \quad to \quad remove \quad C \\
  & \left\{B,E,H,J \right\}^+ =\left\{A,B,C,D,E,G,H,I \right\} \\
  & C \quad can \quad be \quad removed \\
  & \\
  & Then \quad try \quad to \quad remove \quad H \\
  & \left\{B,E,J \right\}^+ =\left\{A,B,C,D,E,G,H,I,J \right\} \\
  & H \quad can \quad be \quad removed \\
  & \\
  & Then \quad try \quad to \quad remove \quad J \\
  & \left\{B,E \right\}^+ =\left\{A,B,C,D,E,G,H,I \right\} \\
  & J \quad cannot \quad be \quad removed \\
  & \\
  & A \quad candidate \quad key \quad of \quad R \quad is \quad \left\{B,E,J \right\}
  
\end{align*}
$$


(c)
$$
\begin{eqnarray*}
&\because& B \ -> GI \quad and \quad B \subset \left\{B,E,J \right\} \\ 
&\therefore& R \quad is \quad not \quad 2NF \\
&\because&  The \quad attribute \quad values \quad of \quad R \quad are \quad atomic \\
&\therefore& R \quad is \quad 1NF
\end{eqnarray*}
$$


(d)
$$
\begin{align*}\label{3}
  & step1 \\
  & F^1 = \left\{A->D,A->E,B->G,B->I,E->C,E->D,CE->A,CE->D,CE->H,H->G,AH->I  \right\} \\
  & \\
  & step2 \\
  & CE \quad -> \quad A \\
  & C^+ \quad = \left\{ C \right\};thus \quad CE \quad -> \quad A \quad is \quad not \quad inferred \quad by \quad F^1\\
  & Hence \quad , \quad CE \quad -> \quad A \quad cannot \quad be \quad replaced \quad by \quad C \quad -> \quad A \\
  & E^+ \quad = \left\{ A,C,D  \right\};thus \quad CE \quad -> \quad A \quad is \quad inferred \quad by \quad F^1\\
  & Hence \quad , \quad CE \quad -> \quad A \quad can \quad be \quad replaced \quad by \quad E \quad -> \quad A \\
  & \\
  & Samely \quad CE \quad -> \quad D \quad can \quad be \quad replaced \quad by \quad E \quad -> \quad D \\
  & Samely \quad CE \quad -> \quad H \quad can \quad be \quad replaced \quad by \quad E \quad -> \quad H \\
  & Samely \quad AH \quad -> \quad I \quad can \quad be \quad replaced \quad by \quad A \quad -> \quad I \\
  & F^2 = \left\{A->D,A->E,B->G,B->I,E->C,E->D,E->A,E->D,E->H,H->G,A->I  \right\}
  & \\
  & step3 \\
  & A+|_{F^2-\left\{A->D  \right\} }=\left\{A,B,C,D,E,G,H,I  \right\};Thus \quad A->C \quad is \quad redundant \\
  & A+|_{F^2-\left\{A->E  \right\} }=\left\{A,B,G,I  \right\};Thus \quad A->E \quad is \quad not \quad redundant \\
  & Iteratively \quad we \quad can \quad A->D \quad and \quad B->G \quad and \quad B->I\quad but \quad not \quad the \quad others \\
  & \\
  & F_{min} = \left\{A->E,A->I,E->C,E->D,E->A,E->H,H->G  \right\}
  


  
\end{align*}
$$


(e)
$$
\begin{align*}
 & R_{1}=(A,E,I) \\
 & R_{2}=(E,C,D,A,H) \\
 & R_{3}=(H,G) \\
 & R_{4}=(B,E,J)
\end{align*}
$$


## Q2.

(a)
$$
\begin{align*}
 & R_{1}(B),R_{4}(A),R_{3}(A),W_{3}(A),W_{4}(A),R_{1}(A),W_{1}(B),R_{2}(B),R_{4}(B),W_{4}(B),W_{1}(A),W_{2}(B) \\
 & (1)R_{1}(B):W_{1}(B),R_{2}(B),R_{4}(B),W_{4}(B),W_{2}(B) \\
 & \quad  \ conflict:W_{4}(B),W_{2}(B) \\
 & (2)R_4{A}:R_{3}(A),W_{3}(A),W_{4}(A),R_{1}(A),W_{1}(A) \\
 & \quad  \ conflict:W_{3}(A),W_{1}(A) \\
 & \\
 & Samely \quad we \quad can \quad find \quad all \quad conflicts: \\
 & \quad  \ R_{3}(A):W_{4}(A),W_{1}(A) \\
 & \quad  \ W_{3}(A):W_{4}(A),R_{1}(A),W_{1}(A) \\
 & \quad  \ W_{4}(A):R_{1}(A),W_{1}(A) \\
 & \quad  \ R_{1}(A):W_{1}(A) \\
 & \quad  \ W_{1}(B):R_{2}(B),R_{4}(B),W_{4}(B),W_{2}(B) \\
 & \quad  \ R_{2}(B):R_{4}(B),W_{4}(B) \\
 & \quad  \ R_{4}(B):W_{2}(B) \\
 & \quad  \ W_{4}(B):W_{2}(B) \\
 
\end{align*}
$$
The direct graph shown as follows:

![未命名文件 (1)](C:\Users\24593\Desktop\未命名文件 (1).png)

Because existing cycle,so the transaction schedule is not conflict serialisable



(b)

| Time | t1   | t2   | t3   | t4   | t5   | t6   | t7   | t8   | t9   | t10  | t11  | t12  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| T1   | R(A) | W(A) | R(B) | W(B) |      |      |      |      |      |      |      |      |
| T2   |      |      |      |      | R(B) | W(B) |      |      |      |      |      |      |
| T3   |      |      |      |      |      |      | R(A) | W(A) |      |      |      |      |
| T4   |      |      |      |      |      |      |      |      | R(A) | W(A) | R(B) | W(B) |



(c)

| T1                                                           | T2                                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| read_lock(B)<br />read(B)<br />unlock(B)<br /><br />read_lock(A)<br />read(A)<br />unlock(A)<br />write_lock(B)<br />read(B)<br />write(B)<br />unlock(B)<br /><br /><br /><br /><br />write_lock(A)<br />read(A)<br />write(A)<br />unlock(A)<br /><br /><br /><br /><br /> | <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />read_lock(B)<br />read(B)<br />unlock(B)<br /><br /><br /><br /><br /><br />write_lock(B)<br />read(B)<br />write(B)<br />unlock(B) |