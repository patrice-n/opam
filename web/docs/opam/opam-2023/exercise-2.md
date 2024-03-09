---
comments: true
---

# <span style="color:#074b83"> Exercice 2 - OPAM 2023 (arithmétique) </span>

## <span style="color:#0a69b7">L'énoncé (fourni par [KouakouSchool](https://www.youtube.com/@kouakouschool))</span>

!!! question "Enoncé de l'exercice"

	Trouver tous les nombres entiers naturels non nuls $m$ et $n$ qui n'ont pas de diviseur commun plus grand que $1$ tels que:

	$$m^3 + n^3 \quad \textrm{divise} \quad m^2 + 20mn + n^2.$$

## <span style="color:#0a69b7">Une solution (Utilisation d'une identité remarquable)</span>

Trouvons tous les nombres entiers naturels non nuls $m$ et $n$ qui n'ont pas de diviseur commun plus grand que $1$ tels que:

$$
m^3 + n^3 \quad \textrm{divise} \quad m^2 + 20mn + n^2.
$$

On a l'identité suivante pour tous entiers naturels $m$ et $n$:

$$
m^3 + n^3 = (m+n)(m^2-mn+n^2)
$$

Nous allons noter le symbole $|$ comme représentant la division, c'est-à-dire $a|b$ veut dire $a$ divise $b$.
Ainsi, $m^3 + n^3$ divise $m^2+20mn+n^2$ implique que $m+n$ divise $m^2+20mn+n^2$ et $m^2-mn+n^2$ divise $m^2+20mn+n^2$. D'où l'équation:

\[\left\{
	\begin{array}{l}
	m+n | m^2+20mn+n^2 \\
	m^2-mn+n^2 | m^2+20mn+n^2
	\end{array}
\right.\]

Donc:

\[\left\{
	\begin{array}{l}
	m+n | (m+n)^2 + 18mn \\
	m^2-mn+n^2 | m^2+20mn+n^2
	\end{array}
\right.\]

Comme $m^2+20mn+n^2 - (m^2-mn+n^2) = 21mn$, en utilisant la deuxième relation, on a:

$$ m^2-mn+n^2 | 21mn $$

En utilisant la première relation et sachant que $m + n | (m + n)^2$, nous obtenons $m+n | ((m+n)^2 + 18mn) - (m+n)^2$. Cela implique:

$$ m+n | 18mn $$

Nous notons le symbole $\land$ comme étant la notation du plus grand diviseur commun, c'est-à-dire $a \land b$ est le plus grand diviseur commun de $a$ et $b$. Tout diviseur de $mn$ et $m+n$ est diviseur de toute combinaison linéaire. Ainsi, le plus grand diviseur commun de deux entiers naturels divise toute combinaison linéaire de ces deux entiers naturels. En l'occurence:

\[mn \land (m + n)  | mn \land (mn - m*(m + n)) \implies mn \land (m + n)  | mn \land - m*m\]

Or, $mn \land - m*m = m(n \land - m)$ donc:

\[mn \land (m + n)  | m(n \land - m)\]

Donc:

$$
mn \land (m + n)  | m(n \land m)
$$

D'après l'énoncé, $m$ et $n$ n'ont pas de diviseur commun plus grand que 1. Cela est équivalent à $m \land n = 1$.

$$
m \land n = 1
$$

Ainsi:

$$
mn \land (m + n)  | m
$$

On a:

\[mn \land (m + n)  | m + n \]

Donc:

\[mn \land (m + n)  | (m + n) \land m \]

\[(m + n) \land m | ((m + n) - m) \land m \implies (m + n) \land m | n \land m\]

Ainsi,

$$
mn \land (m + n)  = 1
$$

Or $m+n | 18mn$. Cela implique donc que:

$$
m+n | 18
$$

D'où $m + n \in \{2, 3, 6, 9, 18\}$ car $m$ et $n$ étant des entiers naturels non nuls, $m + n \geq 2$. Afin de déterminer $m$ et $n$, nous considérons le cas où $m \geq n$ car $m$ et $n$ sont interchangeables. Ainsi, pour chaque valeur de $m+n$, nous déterminons les valeurs de $m$ et $n$ tels que $m \land n = 1$.
Cela donne:

\[m + n = 2 \implies (m, n) = (1, 1)\]

\[m + n = 3 \implies (m, n) = (2, 1)\]

\[m + n = 6 \implies (m, n) = (5, 1)\]

\[m + n = 9 \implies (m, n) \in \{(8, 1), (7, 2), (5, 4)\}\]

\[m + n = 18 \implies (m, n) \in \{(17, 1), (13, 5), (11, 7)\}\]

Donc, avec $m \geq n$, on a:

\[(m, n) \in \{(1,1), (2, 1), (5, 1), (8, 1), (7, 2), (5, 4), (17, 1), (13, 5), (11, 7)\} \]

Pour chaque valeur de $(m, n)$, nous vérifions si $m^2 - mn + n^2 | 21mn$. Ainsi, le tableau suivant permet de voir les résultats.

!!! abstract "Tableau de divibilité $m^2 - mn + n^2 | 21mn$"

	$$
	\begin{array}{|c|c|c|c|c|c|}
	\hline
	m + n & m & n & m^2 - mn + n^2 & 21mn & m^2 - mn + n^2 | 21mn\\ \hline
	2 & 1 & 1 & 1 &  21 & vrai \\
	3 & 2 & 1 & 3 &  21*2 & vrai \\
	6 & 5 & 1 & 21 &  21*5 & vrai \\
	9 & 8 & 1 & 57=3*19 &  21*8*1 & faux \\
	9 & 7 & 2 & 39=3*13 &  21*7*2 & faux \\
	9 & 5 & 4 & 21=7*3 &  21*5*4 & vrai \\
	18 & 17 & 1 & 273=3*7*13 &  21*17 & faux \\
	18 & 13 & 5 & 129=3*43 &  21*13*5 & faux \\
	18 & 11 & 7 & 93=3*31 &  21*11*7 & faux \\
	\hline
	\end{array}
	$$

Donc:

$$
(m, n) \in \{(1,1), (2, 1), (1, 2), (5, 1), (1, 5), (5, 4), (4, 5) \}
$$

Réciproquement, $(m,n) \in \{(1,1), (2, 1), (1, 2), (5, 1), (1, 5)\}$ est tel que $m^3+n^3$ divise $m^2+20mn+n^2$. Cependant,
si $(m,n) \in \{(5, 4), (4, 5)\}$ alors $m^3+n^3$ ne divise pas $m^2+20mn+n^2$. Cela se voit d'après le tableau suivant:

!!! abstract "Tableau de divibilité  $m^3+n^3 | m^2 + 20mn + n^2$"

	$$
	\begin{array}{|c|c|c|c|c|}
	\hline
	m & n & m^3 + n^3 & m^2 + 20mn + n^2 & m^3+n^3 | m^2 + 20mn + n^2\\ \hline
	1 & 1 & 2 & 22 & vrai \\
	2 & 1 & 9 & 45 & vrai \\
	5 & 1 & 126 & 126 & vrai \\
	5 & 4 & 189=9*3*7 & 441=9*7*7 & faux \\
	\hline
	\end{array}
	$$

Ainsi, nous pouvons conclure que les valeurs des entiers naturels non nuls $m$ et $n$ qui n'ont pas de diviseur commun plus grand que $1$ tels que: $m^3 + n^3$ divise $m^2+20mn+n^2$ sont:

!!! abstract "Valeurs solutions au problème"

	$$ (1,1), (2, 1), (1, 2), (5, 1), (1, 5) $$
