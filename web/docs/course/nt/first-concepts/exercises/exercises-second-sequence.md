---
comments: true
---

# <span style="color:#074b83">Seconde série d'exercices d'arithmétique</span>

## <span style="color:#074b83">Exercices</span>

!!! example "Exercice $26^{*}$ (Iran 96)"

    Soit $k > 0$ un entier. Prouver que tout entier $n > 0$ peut s'écrire de façon unique sous la forme:

    \[n = C^{k}_{a_{k}} + C^{k-1}_{a_{k-1}} + ... + C^{t}_{a_{t}}\]

    où $a_{k} > a_{k-1} > ... > a_{t} \geq t \geq 1$ sont des entiers.

???- success "Solution 26"

!!! example "Exercice $27^{*}$ (Erdös)"

    Soient $a_{1}, ..., a_{n+1}$ des entiers deux à deux distincts dans $\{1, ..., 2n\}$.

    * __a)__ Montrer qu'il existe $i$ et $j$ tels que $a_{i}$ est premier avec $a_{j}$.
    * __b)__ Montrer qu'il existe $i$ et $j$ distincts tels que $a_{i}$ divise $a_{j}$.

???- success "Solution 27"

!!! example "Exercice $28^{*}$ (Australie 96)"

    Si $n$ est un entier, on note $\sigma(n)$ la somme des diviseurs positifs de $n$. Soit $(n_{i})$ une suite strictement croissante
    d'entiers telle que $\sigma(n_{i}) - n_{i}$ est constante. Montrer que tous les $n_{i}$ sont premiers.

???- success "Solution 28"

!!! example "Exercice $29^{*}$ (Iran 99)"

    Déterminer tous les entiers $n$ pour lesquels

    \[d_{1}^{2} + d_{2}^{2} + d_{3}^{2} + d_{4}^{2} = n\]

    où $1 = d_{1} < d_{2} < d_{3} < d_{4}$ désignent les quatre plus petits diviseurs de $n$.

???- success "Solution 29"

!!! example "Exercice $30^{*}$"

    Soient $(a_{n})$ et $(b_{n})$ deux suites d'entiers. On suppose que les suites $(a_{n} + b_{n})$ et $(a_{n}b_{n})$ sont arithmétiques. Montrer qu'il existe telle que pour tout $n$, on ait $a_{n} = c$ ou $b_{n} = c$.

???- success "Solution 30"

!!! example "Exercice $31^{*}$ (Corée 98)"

    Trouver tous les entiers strictement positifs $l$, $m$, $n$ premiers entre eux deux à deux tels que:

    \[(l + m + n) \left(\frac{1}{l} + \frac{1}{m} + \frac{1}{n}\right)\]

    soit un entier.

???- success "Solution 31"

!!! example "Exercice $32^{*}$ (Fonction de Moëbius)"

    On définit la _fonction de Moëbius_ par $\mu(1) = 1$, $\mu(n) = 0$ si $n$ est divisible par $p^{2}$ pour un certain nombre premier $p$, et $\mu(p_{1}...p_{r}) = (-1)^{r}$ si les $p_{i}$ sont des nombres premiers deux à deux distincts.

    * __a)__ Montrer que pour tout $n > 1$, on a:

    \[\sum_{d|n}\mu(d) = 0\]

    * __b)__ En déduire que si $f: \mathbb{N}^{*} \rightarrow \mathbb{N}^{*}$ est une fonction et si $g$ est définie par la formule:

    \[g(n) = \sum_{d|n} f(d)\]

    alors on peut retrouver $f$ à partir de $g$ grâce à la formule:

    \[f(n) = \sum_{d|n} \mu\left(\frac{n}{d}\right)g(d)\]

???- success "Solution 32"

!!! example "Exercice $33^{*}$"

    Prouver que parmi dix entiers consécutifs, il y en a un qui est premier avec chacun des autres.

???- success "Solution 33"

!!! example "Exercice $34^{*}$ (AMM)"

    Si $n$ est un entier, on note $P(n)$ le produit des diviseurs de $n$. Montrer que si $P(n) = P(m)$ alors $n = m$.

???- success "Solution 34"

!!! example "Exercice $35^{*}$"

    Déterminer tous les entiers $n$ et $m$ strictement positifs pour lesquels la somme des entiers de $n$ jusqu'à $n + m$ vaut $1000$.

???- success "Solution 35"

!!! example "Exercice $36^{*}$"

    Déterminer toutes les suites $(a_{n})_{n \geq 1}$ d'entiers strictement positifs telle que $PGCD(a_{i}, a_{j}) = PGCD(i, j)$ pour tous indices $i$ et $j$.

???- success "Solution 36"

!!! example "Exercice $37^{*}$ (Nombres de Mersenne)"

    Montrer que si $2^{n}-1$ est un nombre premier, alors $n$ est également premier.

???- success "Solution 37"

!!! example "Exercice $38^{*}$ (URSS 61)"

    Prouver que parmi $39$ entiers consécutifs, on peut toujours en trouver un dont la somme des chiffres (écriture décimale) est divisible par $11$.

    Est-ce encore vrai pour $38$ entiers consécutifs ?

???- success "Solution 38"

!!! example "Exercice $39^{**}$ (Putnam 83)"

    Déterminer un nombre réel $x > 0$ tel que, pour tout entier $n > 0$, le nombre $[x^{n}]$ a la même parité que $n$.

???- success "Solution 39"

!!! example "Exercice $40^{**}$ (SL 96)"

    Construire une fonction $f: \mathbb{N} \rightarrow \mathbb{N}$ bijective et vérifiant:

    \[f(3mn + m + n) = 4f(m)f(n) + f(m) + f(n) \]

    pour tous entiers $m$ et $n$.

???- success "Solution 40"

!!! example "Exercice $41^{**}$"

    En utilisant le théorème de répartition des nombres premiers, montrer que l'ensemble:

    \[\{\frac{p}{q}, p \quad \textrm{et} \quad q \quad \textrm{premiers}\}\]

    est dense dans $\mathbb{R}^{+}$.

???- success "Solution 41"

!!! example "Exercice $42^{*}$ (Moscou 95)"

    Montrer qu'il existe une infinité d'entiers composés $n$ pour lesquels:
    
    \[n \quad \textrm{divise} \quad 3^{n-1} - 2^{n-1}.\]

???- success "Solution 42"

!!! example "Exercice $43^{**}$ (Théorème de Miller)"

    Montrer qu'il existe un réel $x$ tel que la suite définie par:

    \[\left\{\begin{array}{cc} x_{0} = 0 & \\
    x_{n+1} = 2^{x_{n}} & n \leq 0\end{array}\right.\]

    et telle que pour tout $n$, $[x_{n}]$ est un nombre premier. (On pourra utiliser le postulat de Bertrand).

???- success "Solution 43"

!!! example "Exercice $44^{*}$ (OIM 75)"

    Peut-on placer $1975$ points sur le cercle unité dont les distances deux à deux sont toutes rationnelles ?

???- success "Solution 44"

!!! example "Exercice $45^{**}$"

    On note $\sigma(n)$ la somme des diviseurs positifs de l'entier $n$. Pour tout entier $p > 0$, on pose:
    
    \[f(m) = max\{n \in \mathbb{N}^{*}| \sigma(n) \leq m\}\]

    Montrer que, pour tout entier $k > 0$, l'équation

    \[m - f(m) = k\]

    a une infinité de solutions.

???- success "Solution 45"

!!! example "Exercice $46^{**}$ (Chine 88)"

    Déterminer le plus petit $n > 3$ pour lequel pour toute écriture 
    
    \[\{3, ..., n\} = A \cup B\]

    l'équation

    \[xy = z\]

    a une solution pour $x$, $y$ et $z$ non nécessairement distincts, et tous les trois dans $A$ ou tous les trois dans $B$.

???- success "Solution 46"

!!! example "Exercice $47^{**}$"

    Soit $p \geq 5$ un nombre premier. Calculer:

    \[\sum_{k=1}^{p-1} \left[\frac{k^{3}}{p}\right] \quad \textrm{et} \quad \sum_{k=1}^{(p-1)(p-2)}\left[\sqrt[3]{kp}\right]\]

???- success "Solution 47"

!!! example "Exercice $48^{**}$ (Italie 04)"

    * __a)__ Montrer qu'il existe $2004$ puissances parfaites distinctes en progression arithmétique.

    * __b)__ Est-il possible de trouver une suite arithmétique infinie formée exclusivement de puissances parfaites ?

???- success "Solution 48"

!!! example "Exercice $49^{**}$"

    Soit $n > 0$ un entier. Montrer qu'il n'existe pas de rationnels $x$ et $y$ tels que:

    \[x + y + \frac{1}{x} + \frac{1}{y} = 3n \]

???- success "Solution 49"

!!! example "Exercice $50^{**}$ (Moldavie 96)"

    Soit $n = 2^{13} \times 3^{11} \times 5^{7}$. Déterminer le nombre de diviseurs de $n^{2}$ inférieurs à $n$ et ne divisant pas $n$.

???- success "Solution 50"


## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 24/03/2024.
