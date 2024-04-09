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

    Soient $k > 0$ et $n > 0$ des entiers.

    Pour construire une telle décomposition, on utilise l'algorithme glouton: on commence par déterminer le plus grand entier, disons $a_{k}$ tel que $C_{a_{k}}^{k} \leq n$. Puis, on recommence avec $n$ et $k$ remplacés respectivement par $n - C_{q_{k}}^{k}$ et $k-1$. Comme, par construction, on a $n < C_{a_{k}+1}^{k}$ c'est donc que:

    \[n - C_{a_{k}}^{k} < C_{a_{k}+1}^{k} - C_{a_{k}}^{k} = \frac{a_{k}!\left(a_{k}+1 - (a_{k} + 1 - k)\right)}{(a_{k}+1-k)!k!} \implies n - C_{a_{k}}^{k} < \frac{a_{k}!k}{(a_{k} - (k-1))k!}\]

    Donc:

    \[n - C_{a_{k}}^{k} < \frac{a_{k}(k-1)!}{(a_{k}-(k-1))!(k-1)!} = C_{a_{k}}^{k-1}\]

    ce qui assure que la suite $(a_{i})$ est bien strictement décroissante. En effet, on aura:

    \[C_{a_{k-1}}^{k-1} \leq n - C_{a_{k}}^{k} < C_{a_{k}}^{k-1} \implies C_{a_{k-1}}^{k-1} < C_{a_{k}}^{k-1} \implies a_{k-1} < a_{k}\]

    On prouve maintenant l'unicité. Supposons que $n$ possède deux représentations distinctes associées respectivement aux suites $a_{k},...,a_{t}$ et $b_{k},...,b_{r}$, pour $t$ et $r$ des entiers naturels. On considère le plus grand indice pour lequel ces deux suites diffèrent. Quitte à éliminer des termes, on peut supposer que cet indice est $k$ et que $a_{k} > b_{k}$. Mais alors:

    \[n \leq C_{b_{k}}^{k} + C_{b_{k-1}}^{k-1} + ... + C_{b_{r}}^{r} < C_{b_{k}+1}^{k} \leq C_{a_{k}}^{k}\]

    L'inégalité du milieu est due au fait que la suite $(b_{j})_{r \leq j \leq k}$ est strictement décroissante que pour tout $j \in \{r,...,k\}$:

    \[C_{b_{j}+1}^{j} - C_{b_{j}}^{j} = C_{b_{j}}^{j-1}\]

    Donc, en supposant que les notations $k-i$, pour $i=1,...,3$ ont un sens, sinon tronque dans les expressions analytiques ci-dessous les termes qui n'ont pas de sens:

    \[C_{b_{k}+1}^{k} - C_{b_{k}}^{k} - C_{b_{k-1}}^{k-1} - C_{b_{k-2}}^{k-2} - ... - C_{b_{r}}^{r} = (C_{b_{k}+1}^{k} - C_{b_{k}}^{k} - C_{b_{k-1}+1}^{k-1}) + (C_{b_{k-1}+1}^{k-1} - C_{b_{k-1}} - C_{b_{k-2}+1}^{k-2}) + (C_{b_{k-2}+1}^{k-2} - C_{b_{k-2}} - C_{b_{k-3}+1}^{k-3}) + ... + (C_{b_{r}+1}^{r} - C_{b_{r}}^{r})\]

    \[C_{b_{k}+1}^{k} - C_{b_{k}}^{k} - C_{b_{k-1}}^{k-1} - C_{b_{k-2}}^{k-2} - ... - C_{b_{r}}^{r} = (C_{b_{k}}^{k-1} - C_{b_{k-1}+1}^{k-1}) + (C_{b_{k-1}}^{k-2} - C_{b_{k-2}+1}^{k-2}) + (C_{b_{k-2}}^{k-3} - C_{b_{k-3}+1}^{k-3}) + ... + (C_{b_{r}+1}^{r} - C_{b_{r}}^{r}) > 0\]

    Car pour $j \in {r+1, ...,k}$, $C_{b_{j}}^{j-1} - C_{b_{j-1}+1}^{j-1} \geq 0$, puisque $b_{j} \geq b_{j-1} + 1$ et $C_{b_{r}+1}^{r} - C_{b_{r}}^{r} > 0$. Ainsi:

    \[C_{b_{k}+1}^{k} - C_{b_{k}}^{k} - C_{b_{k-1}}^{k-1} - C_{b_{k-2}}^{k-2} - ... - C_{b_{r}}^{r} > 0 \implies C_{b_{k}+1}^{k} > C_{b_{k}}^{k} + C_{b_{k-1}}^{k-1} + C_{b_{k-2}}^{k-2} + ... + C_{b_{r}}^{r}\]

    La relation

    \[n \leq C_{b_{k}}^{k} + C_{b_{k-1}}^{k-1} + ... + C_{b_{r}}^{r} < C_{b_{k}+1}^{k} \leq C_{a_{k}}^{k}\]

    est contradiction. Nous avons ainsi prouvé l'unicité. On peut donc conclure que $n$ peut s'écrire de façon unique sous la forme:

    \[n = C^{k}_{a_{k}} + C^{k-1}_{a_{k-1}} + ... + C^{t}_{a_{t}}\]

    où $a_{k} > a_{k-1} > ... > a_{t} \geq t \geq 1$ sont des entiers.

!!! example "Exercice $27^{*}$ (Erdös)"

    Soient $a_{1}, ..., a_{n+1}$ des entiers deux à deux distincts dans $\{1, ..., 2n\}$.

    * __a)__ Montrer qu'il existe $i$ et $j$ tels que $a_{i}$ est premier avec $a_{j}$.
    * __b)__ Montrer qu'il existe $i$ et $j$ distincts tels que $a_{i}$ divise $a_{j}$.

???- success "Solution 27"

    * __a)__ D'après le principe des tiroirs parmi les $a_{i}$, il y en a deux consécutifs, qui sont donc premiers entre eux.
    * __b)__ Écrivons pour tout $i$, $a_{i} = 2^{\alpha_{i}}b_{i}$ pour un certain nombre impair $b_{i}$ forcément compris entre $1$ et $2n$. D'après le principe des tiroirs, puisqu'il y a $n$ nombres impairs entre $1$ et $2n$, il existe $i$ et $j$ tels que $b_{i} = b_{j}$. On peut supposer $\alpha_{i} \leq \alpha_{j}$ et dans ce cas $a_{i}$ divise $a_{j}$.

???- warning "Remarque: Principe des tiroirs"

    Si on cherche à ranger $n+1$ chaussettes dans $n$ tiroirs, on sait qu'au moins un tiroir contient au moins deux chaussettes. Ainsi, si on cherche à ranger $n+1$ objets dans $n$ ensembles, au moins un des ensembles contiendra au moins $2$ objets. Plus généralement, si on cherche à ranger au moins $kn+1$ objets dans $n$ ensembles, on sait qu'au moins un des ensembles contient au moins $k+1$ objets.

!!! example "Exercice $28^{*}$ (Australie 96)"

    Si $n$ est un entier, on note $\sigma(n)$ la somme des diviseurs positifs de $n$. Soit $(n_{i})$ une suite strictement croissante d'entiers telle que $\sigma(n_{i}) - n_{i}$ est constante. Montrer que tous les $n_{i}$ sont premiers.

???- success "Solution 28"

    Si $n$ n'est pas premier, il admet un diviseur $d$ différent de $n$ et supérieur à $\sqrt{n}$. Ainsi, $\sigma(n) - n \geq \sqrt{n}$. La suite $\sigma(n_{i})-n_{i}$ est constante, disons égale à $k$. D'autre part, on prouve par récurrence que $n_{i} \geq i$ pour tout $i$. Considérons un $i > k^{2}$. Si $n_{i}$ n'était pas premier, on aurait:

    \[\sigma(n_{i}) - n_{i} \geq \sqrt{n_{i}} \geq \sqrt{i} > k \]

    ce qui est impossible. Ainsi $n_{i}$ est premier (immédiat d'après la démonstration par l'absurde) et $k=1$ (en effet, sinon, on aura $k = \sigma(n_{k^{4}}) - n_{k^{4}} \geq \sqrt{k^{4}} = k^{2} > k$; ce qui serait absurde). 
    
    Nous avons ainsi démontré que tous les $n_{i}$ sont premiers.

!!! example "Exercice $29^{*}$ (Iran 99)"

    Déterminer tous les entiers $n$ pour lesquels

    \[d_{1}^{2} + d_{2}^{2} + d_{3}^{2} + d_{4}^{2} = n\]

    où $1 = d_{1} < d_{2} < d_{3} < d_{4}$ désignent les quatre plus petits diviseurs de $n$.

???- success "Solution 29"

    Déjà $d_{1} = 1$. Si $n$ était impair, tous ses diviseurs seraient impairs et donc $d_{1}^{2}+d_{2}^{2}+d_{3}^{3}+d_{4}^{2}$ serait pair, or d'après l'énoncé, il est censé être égal à $n$ ce qui n'est pas possible. Donc $n$ est pair et $d_{2}=2$. Si $d_{3}$ et $d_{4}$ étaient de même parité, la somme $d_{1}^{2}+d_{2}^{2}+d_{3}^{2}+d_{4}^{2}$ serait impaire, ce qui n'est pas possible non plus puisque $n$ est pair.

    Supposons que $4$ divise $n$. Les nombres $d_{3}$ et $d_{4}$ sont alors $4$ et un nombre premier $p$ à l'ordre près et on est ramené à l'équation:

    \[21 + p^{2} = n\]

    Or $p$ divise $n$, donc $p$ divise $21$ et ainsi $p$ vaut $3$ ou $7$. On vérifie qu'aucun des deux ne fournit uue solution (car $4$ ne diviserait pas $n$).

    Si $4$ ne divise pas $n$, on a $d_{3}=p$ où $p$ est le plus petit diviseur impair de $n$, et $d_{4} = 2p$ puisque $d_{4}$ doit être pair et le plus petit diviseur de $n$ plus grand que $d_{3}=p$. L'équation:

    \[5 + 5p^{2} = n\]

    Donc $p$ divise $5$ puis $p=5$. Cela conduit à $n=130$ qui convient.

!!! example "Exercice $30^{*}$"

    Soient $(a_{n})$ et $(b_{n})$ deux suites d'entiers. On suppose que les suites $(a_{n} + b_{n})$ et $(a_{n}b_{n})$ sont arithmétiques. Montrer qu'il existe une constante $c$ telle que pour tout $n$, on ait $a_{n} = c$ ou $b_{n} = c$.

???- success "Solution 30"

    Écrivons $a_{n} + b_{n} = \alpha + nr$ et $a_{n}b_{n} = \beta + ns$ pour des entiers $\alpha$, $\beta, r$ et $s$. Pour tout $n$, les nombres $a_{n}$ et $b_{n}$ sont les racines du polynôme (d'après la relation racines d'un polynôme et coefficients de ce dernier):

    \[X^{2} - (\alpha + nr)X + (\beta + ns)\]

    Le discriminant $\Delta_{n} = (\alpha + nr)^{2}-4(\beta + ns)$ est donc un carré parfait pour tout entier $n \geq 0$. On a l'égalité:

    \[r^{2}\Delta_{n} = (nr^{2} + \alpha r -2s)^{2} + d\]

    où $d = -4s^{2} + 4rs\alpha - 4\beta r^{2}$ est indépendant de $n$. Si $r \neq 0$, pour $n$ suffisamment grand on a l'inégalité:

    $$(nr^{2} + \alpha r - 2s - 1)^{2} < r^{2}\Delta_{n} < (nr^{2} + \alpha r -2s + 1)^{2}$$

    Comme $r^{2}\Delta_{n}$ doit être un carré, on doit avoir forcémet avoir $r^{2}\Delta_{n} = (nr^{2} + \alpha r -2s)^{2}$ et donc $d=0$. Mais alors, notre trinôme admet toujours pour racine $c = \frac{s}{r}$. Comme les suites sont deux suites supposées distinctes (sinon il s'agirait d'une seule suite numérique) et qu'elle ont des rôles symmétriques, l'on peut donc prendre la racine $c=\frac{s}{r}$ comme une valeur d'une suite et donc pour tout $n$, on a $a_{n}=c$ ou $b_{n}=c$.

!!! example "Exercice $31^{*}$ (Corée 98)"

    Trouver tous les entiers strictement positifs $l$, $m$, $n$ premiers entre eux deux à deux tels que:

    \[(l + m + n) \left(\frac{1}{l} + \frac{1}{m} + \frac{1}{n}\right)\]

    soit un entier.

???- success "Solution 31"

    En réduisant au même dénominateur, la condition est équivalente à $lmn$ divise $(l+m+n)(mn + ln + lm)$.
    
    \[(l+m+n)(mn + ln + lm) = l^{2}(m + n) + m^{2}(l + n) + n^{2}(l+m) + 3lmn \]

    \[(l+m+n)(mn + ln + lm) = l(l(m+n) + m^{2} + n^{2} + 3mn) + mn(m+n) \]

    Comme $lmn$ divise $(l+m+n)(mn + ln + lm)$, cette dernière égalité de dire $l$ divise $mn(m+n)$ et par le lemme d Gauss $l$ divise $m+n$ (comme $m$, $n$ et $l$ sont premiers entre eux).
    
    De même, avec l'égalité:
    
    \[(l+m+n)(mn + ln + lm) = m(m(l+n) + l^{2} + n^{2} + 3ln) + ln(l+n) \]
    
    $m$ divise $ln(l+n)$ et par le lemme de Gauss, $m$ divise $l+n$. 

    Enfin, avec l'égalité:

    \[(l+m+n)(mn + ln + lm) = n(n(l+m) + l^{2} + m^{2} + 3lm) + lm(l+m) \]

    $n$ divise $lm(l+m)$ et par le lemme de Gauss, $n$ divise $l+m$.

    Les rôles des variables étant symétriques, on peut supposer que $n$ est le plus grand des trois. Du coup, $l+m \leq 2n$ et la condition de divisibilité impose $l+m = n$ ou $l + m = 2n$. Dans ce dernier cas, on a forcément $l = m = n$ et cette valeur commune est $1$ car ils sont premiers entre eux. Le triplet $(1, 1, 1)$ est bien solution.

    Sinon, $l + m  = n$, et en remplaçant, le nombre: 

    \[2(l+m)\left(\frac{1}{l} + \frac{1}{m} + \frac{1}{l+m}\right)\]

    doit être entier, ce qui équivaut à:

    \[2(l+m)\left(\frac{1}{l} + \frac{1}{m}\right) = \frac{2(l+m)^{2}}{lm}\]

    est un entier. Comme $l$ et $m$ sont premiers entre eux, on peut supposer $l$ impair. Alors $l$ divise $(l+m)^{2}$ et donc divise $m^{2}$, ce qui n'est possible que si $l = 1$. Alors $m$ divise $2$, et $m=1$ ou $m=2$ (car $m$ divise $(l+m)^{2}$ impliquerait que $m=1$).

    On en déduit de ce qui précède que les solutions sont les triplets $(1, 1, 1)$, $(1, 1, 2)$, $(1, 2, 3)$ et toutes leurs permutations.

!!! example "Exercice $32^{*}$ (Fonction de Moëbius)"

    On définit la _fonction de Moëbius_ par $\mu(1) = 1$, $\mu(n) = 0$ si $n$ est divisible par $p^{2}$ pour un certain nombre premier $p$, et $\mu(p_{1}...p_{r}) = (-1)^{r}$ si les $p_{i}$ sont des nombres premiers deux à deux distincts.

    * __a)__ Montrer que pour tout $n > 1$, on a:

    \[\sum_{d|n}\mu(d) = 0\]

    * __b)__ En déduire que si $f: \mathbb{N}^{*} \rightarrow \mathbb{N}^{*}$ est une fonction et si $g$ est définie par la formule:

    \[g(n) = \sum_{d|n} f(d)\]

    alors on peut retrouver $f$ à partir de $g$ grâce à la formule:

    \[f(n) = \sum_{d|n} \mu\left(\frac{n}{d}\right)g(d)\]

???- success "Solution 32"

    __a)__ Décomposons $n > 1$ en facteurs premiers:

    \[n = p_{1}^{\alpha_{1}}p_{2}^{\alpha_{2}}...p_{d}^{\alpha_{d}}\]

    Les diviseurs $d$ de $n$ pour lesquels $\mu(d) \neq 0$ s'écrivent $d = \prod_{i\in I}p_{i}$ pour $I$ un certain sous-ensemble de $\{1, ...,d\}$. La valeur de $\mu(d)$ est alors $(-1)^{Card I}$.

    Pour conclure, il faut donc juste voir que l'ensemble $\{1, ..., d\}$ possède autant de sous-ensembles de cardinal pair que de sous-ensembles de cardinal impair. Mais à chaque ensemble de cardinal pair, on peut associer un ensemble cardinal impair en lui ajoutant $1$ s'il n'appartient pas à l'ensemble de départ ou en lui otant s'il appartient. Cette association est bijective: il y a donc autant de sous-ensembles de cardinal pair que de cardinal impair, et la formule de sommation est prouvée.

    __b)__ La somme proposée se réecrit:

    \[\sum_{d|n}\sum_{d'|d}\mu\left(\frac{n}{d}\right)f(d')\]

    Dans la somme précédente le terme $f(d')$ apparaît pour tout entier $d$ tel que $d'|d|n$. Ainsi le coefficient qui restera au final de $f(d')$ est:

    \[\sum_{d'|d|n}\mu\left(\frac{n}{d}\right)\]

    En écrivant $d = d'x$, cette somme s'écrit encore:

    \[sum_{x|\frac{n}{d'}} \mu\left(\frac{n}{d'x}\right) = \sum_{x|\frac{n}{d'}} \mu(x)\]

    la dernière égalité provenant du changement de variable $x \mapsto \frac{n}{d'x}$. D'après $a)$, cette somme fait toujours $0$ sauf si $\frac{n}{d'} = 1$ (i.e. $n = d'$) auquel cas elle fait $1$. On trouve ainsi bien la formule annoncée.

!!! example "Exercice $33^{*}$"

    Prouver que parmi dix entiers consécutifs, il y en a un qui est premier avec chacun des autres.

???- success "Solution 33"

    Parmi ces $10$ entiers, il y en a $5$ impairs. Parmi ces $5$ impairs, il y en a au plus $2$ qui sont divisibles par $3$ (noter que les multiples de $3$ sont alternativement pairs et impairs). Parmi ces mêmes $5$, il y en a au plus $1$ qui est multiple de $5$ et plus $1$ qui est multiple de $7$.

    Donc, il y a au moins un des dix entiers qui n'est pas divisible ni par $2$, ni par $3$, ni par $5$, ni par $7$. Appelons-le $n$. Le PGCD de $n$ et $n+k$ est un diviseur de $k$, donc si $k$ est non nul et est compris entre $-9$ et $9$, $PGCD(n, n+k)$ doit être divisible par un nombre premier strictement inférieur à $10$. Mais par construction $n$ n'est divisible par aucun tel nombre premier. L'entier $n$ convient donc.

!!! example "Exercice $34^{*}$ (AMM)"

    Si $n$ est un entier, on note $P(n)$ le produit des diviseurs de $n$. Montrer que si $P(n) = P(m)$ alors $n = m$.

???- success "Solution 34"

    Écrivons:

    \[n = p_{1}^{\alpha_{1}}...p_{d}^{\alpha_{d}}\]

    \[m = p_{1}^{\beta_{1}}...p_{d}^{\beta_{d}}\]

    où les $p_{i}$ sont des nombres premiers deux à deux et les exposants $\alpha_{i}$ et $\beta_{i}$ sont des entiers positifs ou nuls.

    On a vu dans le cours que le produit des diviseurs de $n$ s'écrit:

    \[p_{1}^{\gamma_{1}}...p_{d}^{\gamma_{d}}\]

    pour:

    \[\gamma_{i} = \frac{1}{2}\alpha_{i}(\alpha_{1}+1)...(\alpha_{d} + 1)\]

    L'hypothèse de l'énoncé assure que pour tout $i$:

    \[\alpha_{i}(\alpha_{i}+1)...(\alpha_{d}+1) = \beta_{i}(\beta_{1}+1)...(\beta_{d}+1)\]

    et donc il existe un rationnel $q$, indépendant de $i$, telle que $\alpha_{i} = q\beta_{i}$. Quitte à intervertir $m$ et $n$, on peut supposer $q \geq 1$. L'hypothèse se réécrit alors:

    \[q(q\beta_{1}+1)...(q\beta_{d}+1) = (\beta_{1}+1)...(\beta_{d}+1)\]

    et on voit directement que si $q > 1$, le membre de gauche est strictement supérieur à celui de droite. On a donc $q=1$ et $m=n$.

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
