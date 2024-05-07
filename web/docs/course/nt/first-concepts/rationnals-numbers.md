---
comments: true
---

# <span style="color:#074b83"> Nombres rationnels </span>

## <span style="color:#0a69b7">Définitions et exercices</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Un nombre rationnel est un réel de la forme $\frac{a}{b}$ pour $a$ et $b$ des entiers, $b \neq 0$. On note leur ensemble $\mathbb{Q}$.

!!! warning "Remarque"

    Certaines propriétés restent inchangées sur les rationnels. Précisement, il est possible de parler de décomposition en facteurs premiers, et donc de valuation $p-adique$ pour tout nombre rationnel $r$.

!!! tip "Théorème"

    Soit $r$ un nombre rationnel non nul. Alors $r$ se décompose de façon unique (à permutation des facteurs près) sous la forme:

    $$ r = p_{1}^{\alpha_{1}}...p_{d}^{\alpha_{d}} $$

    où les $p_{i}$ sont des nombres premiers deux à deux distincts et où les $\alpha_{i}$ sont des entiers relatifs.

???- success "Démonstration"

    La démonstration est une conséquence presque directe de la propriété analogue pour les nombres entiers.

    Soit un nombre rationnel $r$ s'écrivant sous la forme $\frac{a}{b}$. A noter que $r$ a une écriture unique telle que $PGCD(a,b)=1$.

    En effet, supposons que l'écriture de $r$ n'est pas unique avec la condition ci-dessus. Alors, il existe $a'$, $b'$ et $a^{(2)}$, $b^{(2)}$ tels que:

    $$ r = \frac{a'}{b'} \quad \textrm{avec} \quad PGCD(a',b')=1 \quad \textrm{et} \quad r = \frac{a^{(2)}}{b^{(2)}} \quad \textrm{avec} \quad PGCD(a^{(2)},b^{(2)})=1 $$

    Ainsi:

    $$ \frac{a'}{b'} = \frac{a^{(2)}}{b^{(2)}} $$

    $$ a'b^{(2)} = a^{(2)}b' $$

    Donc $a' | a^{(2)}$, $b' | b^{(2)}$,  $a^{(2)} | a'$ et $b^{(2)} | b'$, puisque $PGCD(a',b')=1$ et $PGCD(a^{(2)},b^{(2)})=1$. Cela implique que $a' = \pm a^{(2)}$ et $b' = \pm b^{(2)}$.

    Vu que nous considérons des nombres positifs alors $a' = a^{(2)}$ et $b' = b^{(2)}$. Ce qui contredit l'unicité de la décomposition de $r$. 

    Pour conclure $r$ admet une écriture unique $r = \frac{a}{b}$ avec $a$ et $b$ entiers tels que $PGCD(a,b)=1$.

    On utilise à présent les décompositions en facteurs premiers de $a$ et $b$. Soit:

    $$ a = p_{1}^{\alpha_{1}}...p_{k}^{\alpha_{k}} $$
    
    $$ b = q_{1}^{\beta_{1}}...q_{l}^{\beta_{l}} $$   

    Puisque $a$ et $b$ sont premiers entre eux, alors les nombres premiers $p_{i}, i=1,..., k$ et $q_{i}, j=1,..., l$ sont tous distincts. Et on pose:

    $$ p_{i + k} = q_{i},\quad \textrm{et} \quad \alpha_{i + k} = -\beta_{i} \quad \textrm{pour} \quad i=1, ..., l $$

    Donc:

    $$ r = \frac{a}{b} = p_{1}^{\alpha_{1}}...p_{k+l}^{\alpha_{k+l}} $$

    Cette décomposition existe donc bien et l'unicité peut être prouvée en utilisant l'unicité de la décomposition de $r = \frac{a}{b}$ avec $PGCD(a,b) = 1$ ou en utilisant le raisonnement similaire sur l'unicité utilisé pour le théorème fondamental d'arithmétique.

    Nous nous proposons d'utiliser le raisonnement similaire sur l'unicité utilisé pour le théorème fondamental d'arithmétique.
    Si l'on suppose par l'absurde que cette décomposition n'est pas unique, alors on considère $d$, $m$, $m$ et $e$ entiers naturels tels que:

    \[ r = \frac{p'_{1}...p'_{n}}{q'_{1}...q'_{d}} = \frac{p^{(1)}_{1}...p^{(1)}_{m}}{q^{(1)}_{1}...q^{(1)}_{e}} \]

    avec les $p'_{1}, ..., p'_{n}, q'_{1}, ..., q'_{d}, p^{(1)}_{1}, ..., p^{(1)}_{n}, q^{(1)}_{1}, ..., q^{(1)}_{e}$ non tous distincts, et:

    \[min(n+e, m+d) \quad \textrm{est le plus petit possible}\]

    Ce minimum existe bien car l'ensemble $\{min(n+d, m+e), m, n, d, e \in \mathbb{N}\}$ est inclus dans $\mathbb{N}$, un ensemble qui admet un minimum.

    Ainsi, en considérant une des décompositions telle que $min(n+d, m+e)$ est minimale, on obtient donc:

    \[p'_{1}...p'_{n}q^{(1)}_{1}...q^{(e)}_{e} = q'_{1}...q'_{d}p^{(1)}_{1}...p^{(1)_{m}}\]

    Autrement dit, en posant $p'_{i+n} = q^{(1)}_{i}$ pour $i=1, ...,e$ et $q'_{j+d} = p^{(1)}_{j}$ pour $j=1, ...,m$:

    \[ p'_{1}...p'_{n+e} = q'_{1}...q'_{d+m} \]

    $p'_{1}$ divise $q'_{1}...q'_{d+m}$. Comme les nombres $p'_{1},...,p'_{n+e}, q'_{1}, ..., q'_{d+m}$ sont tous premiers alors, il existe $i \in \{1, ..., d+m\}$ tel que $p'_{1} = q'_{i}$. On peut alors simplifier l'égalité:

    \[ p'_{1}...p'_{n+e} = q'_{1}...q'_{d+m} \]

    en divisant par $p'_{1}$, on a:
    
    \[ p'_{2}...p'_{n+e} = \left\{\begin{array}{ccc} q'_{1}...q'_{i-1}q'_{i+1}...q'_{d+m} & si & i \notin \{1,d+m\}\\
    q'_{2}...q'_{d+m} & si & i = 1\\
    q'_{1}...q'_{d+m-1} & si & i = d+m \end{array}\right. \]

    puis en posant:

    \[ \forall l \in \{1, ..., n+e-1\}, \quad p"_{l} = p'_{l+1} \]
    
    \[ \forall l \in \{1, ..., d+m-1\}, \quad q"_{l} = \left\{\begin{array}{ccc} q'_{l} & si & l \leq i-1\\
    q'_{l+1} & si & l \geq i+1 \quad \textrm{et} \quad l < d+m \end{array}\right.\]

    Donc:

    \[ p''_{1}...p''_{n+e-1} = q"_{1}...q"_{d+m-1} \]

    obtenant ainsi un contre-exemple avec $min(n+e-1, d+m-1) = min(n+e, d+m) - 1$ plus petit. C'est contradictoire et l'unicité est donc prouvée.

!!! note "Définition"

    Si $p$ est un nombre premier, on appelle _valuation p-adique_ du rationnel $r \neq 0$, et on note $v_{p}(r)$, l'exposant 
    apparaissant sur le nombre premier $p$ dans la décomposition en facteurs premiers de $r$. Bien sûr, si $p$ n'apparaît pas dans
    cette décomposition, on convient que $v_{p}(r) = 0$.

    Si $r=0$, on convient que $v_{p} = +\infty$ pour tout nombre premier $p$.

!!! tip "Propriétés"

    * Si $r$ est un nombre rationnel non nul, il n'existe qu'un nombre fini de nombres premiers $p$ pour lesquels $v_{p}(r) \neq 0$

    * Si $\frac{a}{b}$ est une fraction représentant le rationnel $r$, alors:

    $$v_{p}(r) = v_{p}(a) - v_{p}(b)$$

    En particulier, la valeur de $v_{p}(a) - v_{p}(b)$ ne dépend pas de la fraction choisie.

    * Soit $r$ un nombre rationnel. Alors $r$ est entier si, et seulement si $v_{p}(r) \geq 0$ pour tout nombre premier $p$.

    * Soient $s$ et $t$ deux nombres rationnels, on a:

    $$v_{p}(st) = v_{p}(s) + v_{p}(t) $$

    $$v_{p}(s+t) \geq min(v_{p}(s), v_{p}(t)) $$

    et la dernière inégalité est une égalité dès que $v_{p}(s) \neq v_{p}(t)$

!!! warning "Remarque"

    Ces propriétés permettent de prouver par exemple l'irrationnalité de $\sqrt{2}$. En effet, si $\sqrt{2}$ était rationnel, on devrait avoir, du fait de l'égalité $(\sqrt{2})^{2} = 2$:

    \[ 2.v_{2}(\sqrt{2}) = 1\]

    soit $v_{2} = \frac{1}{2}$, mais cela n'est pas possible puisque les valuations $p$-adiques sont toujours entières.

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice"

    Montrer que si $n \geq 2$ et $a > 0$ sont des entiers, alors $\sqrt[n]{a}$ est soit un entier, soit un nombre irrationnel.

???- success "Solution"

    Supposons que $\sqrt[n]{a}$ soit un nombre rationnel. On peut alors écrire pour tout nombre premier $p$:

    $$nv_{p} (\sqrt[n]{a}) = v_{p}(a) $$

    et donc $v_{p}(\sqrt[n]{a}) = \frac{1}{n}v_{p}(a) \geq 0$ puisque $a$ est un entier. Cela démontre que $\sqrt[n]{a}$ est un entier.

## <span style="color:#0a69b7">Densité</span>

Une propriété des rationnels souvent utile pour les passages à la limite (et donc finalement assez peu en arithmétique) est donnée par le théorème suivant:

!!! tip "Théorème"

    Soit $\epsilon > 0$ et $x \in \mathbb{R}$. Alors il existe $y \in \mathbb{Q}$ tel que $|x - y| \leq \epsilon$.

On dit, dans cette situation, que $\mathbb{Q}$ est dense dans $\mathbb{R}$.

???- success "Démonstration"

    Soit $q$ un entier strictement supérieur à $\frac{1}{\epsilon}$ et $p = [qx]$. On a l'encadrement $p \leq qx \leq p+1$ et donc en divisant par $q$:

    $$ \frac{p}{q} \leq x \leq \frac{p}{q} + \frac{1}{q} < \frac{p}{q} + \epsilon $$

    Ainsi le rationnel $y = \frac{p}{q}$ convient.

## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 07/05/2024.
