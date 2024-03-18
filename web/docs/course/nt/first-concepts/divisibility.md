---
comments: true
---

# <span style="color:#074b83"> Divisibilité </span>

## <span style="color:#0a69b7">Divisibilité</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Soient $a$ et $b$ sont deux entiers naturels ou relatifs. On dit que $a$ divise $b$, ou que $b$ est divisible par $a$, s’il existe un entier $q$ tel que:
    
    \[ b = aq .\]

On dit encore que $a$ est un diviseur de $b$, ou que $b$ est un multiple de $a$. On le note $a|b$.

!!! tip "Propriétés"

    Si $a$ et $b$ sont deux entiers avec $b \neq 0$, $b$ divise $a$ si et seulement si la fraction $\frac{a}{b}$ est un entier.
    
    + Tous les entiers divisent $0$, et sont divisibles par $1$.
    + Un entier $n$ est toujours divisible par $1$, $-1$, $n$ et $-n$.
    + Si $a|b$ et $b|c$ alors $a|c$.
    + Si $a|b_{1}, b_{2}, ...,b_{n}$, alors $a|b_{1}c_{1} + b_{2}c_{2} + ... + b_{n}c_{n}$, quels que soient les entiers $c_{1}, c_{2}, ..., c_{n}$.
    + Si $a$ divise $b$ et $b \neq 0$, alors $|a| \leq |b|$.
    + Si $a$ divise $b$ et $b$ divise $a$, alors $a=\pm b$.
    + Si $a$ et $b$ sont deux entiers tels que $a^{n}|b^{n}$ pour un entier $n \geq 1$, alors $a|b$.

Toutes les propriétés listées précédemment sont immédiates, à l’exception de la dernière dont la démonstration n'est pas triviale sans bagage arithmétique. Une preuve possible consiste à utiliser la caractérisation de la divisibilité par les valuations p-adiques.

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice 1"

    Soient $x$ et $y$ des entiers. Montrer que $2x+3y$ est divisible par $7$ si et seulement si $5x+4y$ l'est.

???- success "Solution 1"

    Supposons que $7$ divise $2x+3y$, alors il divise $6(2x+3y)-7(x+2y)=5x+4y$. Réciproquement si $7$ divise $5x+4y$, il divise $6(5x+4y) - 7(4x+3y)=2x+3y$.

!!! question "Exercice 2"

    Pour quels entiers $n$ strictement positifs, le nombre $n^{2}+1$ divise-t-il $n+1$ ?

???- success "Solution 2"

    Si $n^{2} + 1$ divise $n+1$, comme tout est positif, on doit avoir $n^{2}+1 \leq n+1$, ce qui n'est vérifié que pour $n = 1$. On vérifie ensuite que $n=1$ est bien solution.

!!! question "Exercice 3"

    Soient $x$ et $y$ deux entiers. Montrer que $2x+3y$ est divisible par $17$ si et seulement si $9x+5y$ est divisible par $17$.

???- success "Solution 3"

    On a:

    $$ 17 | (2x+3y) \Rightarrow 17|[13(2x+3y)] $$
    
    $$ 17 | (26x+39y) \Rightarrow 17|(26x+39y)-17(x+2y) = 9x + 5y $$ 

    A l'inverse, si $17 | (9x + 5y) \Rightarrow 17|[4(9x+5y)]$, or:

    $$ 17 | (36x + 20y) \Rightarrow 17 | (36x + 20y) - 17(2x+y) = 2x+3y $$

!!! question "Exercice 4"

    Trouver tous les entiers positifs $d$ tels que $d$ divise $n^{2}+1$ et $(n+1)^{2}+1$ pour un certain entier $n$.

???- success "Solution 4"

    Soit $d | (n^{2} + 1)$ et $d | [(n+1)^{2}+1]$ ou $d | (n^{2} + 2n + 2)$

    Alors:

    \[d | [(n^{2} + 2n + 2) - (n^{2} + 1)]\]

    \[d | (2n+1) \implies d | (4n^{2}+4n+1)\]

    \[d | [4(n^{2} + 2n + 2) - (4n^{2}+4n+1)]\]

    \[d | (4n+7)\]

    Ainsi, 

    \[d | [(4n+7) - 2(2n+1)] \implies d|5\]

    donc $d$ peut être seulement égal à $1$ ou $5$

    En prenant $n=2$, $d = 1$ ou $d = 5$ divisent bien $n^{2} + 1$ et $(n+1)^{2}+1$.

## <span style="color:#0a69b7">Partie entière</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Si $x$ est un réel, on appelle _partie entière_ de x, notée $[x]$, le plus grand entier inférieur ou égal à $x$. Ainsi, on a
    
    \[ [x] \leq x < [x] + 1.\]

!!! warning "Remarque"

    On définit aussi la _partie décimale_ de $x$, comme la différence $x - [x]$. La partie décimale de $x$ est souvent notée $\{x\}$. Cette notion est moins utilisée que la notion de partie entière et les conventions de notations sont différentes suivants les écoles et les livres. Il est convient de préciser, lorsque cela n'est pas fait dans l'énoncé, la signification de ces notations.

    Pour un nombre entier, sa partie entière est égale à ce dernier. Mais pour un nombre décimal:
    
    + S'il est positif, sa partie entière est égale à ce nombre en enlevant la partie après la virgule
    + S'il est négatif, sa partie entière est égale à ce nombre auquel on retranche $1$ puis on enlève la partie après la virgule

!!! example "Exemples"

    $$[4] = 4$$
    
    $$[-3] = -3$$
    
    $$[1.45] = 1$$
    
    $$[-3.14] = -4$$

!!! tip "Quelques propriétés"

    + Pour tout réel $x$, $x = [x] + \{x\}$ 
    + Pour tout réel $x$, on a: $x - 1 < [x] \leq x$
    + Si $x$ est entier, alors $[x] = x$ et $\{x\} = 0$. Réciproquement, si $[x]=x$ ou $\{x\}=0$ alors $x$ est un entier.
    + Pour tout réel $x$, si $x$ est un entier, $[-x] = -[x]$ sinon $[-x] = -[x]-1$
    + Pour tous réels $x$ et $y$, $[x]+[y] \leq [x+y] \leq [x]+[y]+1$
    + Pour tout réel $x$, si $m$ est un nombre entier strictement positif alors il y a exactement $\left[\frac{x}{m}\right]$ multiples de $m$ compris entre $1$ et $x$.

La démonstration de ces résultats repose sur l'utilisation de l'inégalité $[x] \leq x < [x] + 1$, pour tout nombre réel $x$.

### <span style="color:#0c87eb">Exercice</span>

!!! question "Exercice"

    On suppose que $4n+2$ n'est pas le carré d'un nombre entier. Montrer que pour tout $n \geq 0$, on a:

    \[[\sqrt{n} + \sqrt{n+1}] = [\sqrt{4n+2}] \]

???- success "Solution"

    Remarquons tout d'abord que l'inégalité suivante est toujours vraie:

    $$\sqrt{n} + \sqrt{n+1} < \sqrt{4n+2}$$

    En effet, en élevant au carré, on a à comparer $2n + 1 + + 2\sqrt{n^{2}+n}$ et $4n+2$, soit $2\sqrt{n^{2}+n}$ et $2n+1$ et l'inégalité devient évidente après une nouvelle élévation au carré.

    Il reste à prouver qu'il n'existe aucun entier $k$ tel que:

    $$\sqrt{n} + \sqrt{n+1} < k \leq \sqrt{4n+2}$$

    soit, encore en élevant au carré qu'il n'existe aucun entier $k$ tel que:

    $$2n+1+2\sqrt{n^{2} + n} < k^{2} \leq 4n+2$$

    Or $4n+1 < 2n + 1 + 2\sqrt{n^{2}+n}$, ce qui veut dire qu'un tel entier $k$ vérifierait _a fortiori_ $4n+1 < k^{2} \leq 4n+2$. Comme $k$ est un entier, cela impliquerait que $k^{2} = 4n+2$, ce qui contredit l'hypothèse de l'énoncé selon laquelle $4n+2$ n'est pas le carré d'un entier.

!!! warning "Remarque"

    $4n+2$ n'est jamais le carré d'un entier. En effet, $4n+2$ est pair et s'il est un carré alors il serait divisible par $4$.
    De ce fait, $2$ serait égal à la différence de deux nombres divisibles par $4$ donc $2$ serait divisible par $4$. Cela est absurde.
    Il vient que $4n+2$ n'est jamais le carré d'un entier et donc que pour tout entier naturel $n$, $[\sqrt{n+1}]+[\sqrt{n}] = [\sqrt{4n+2}]$.

!!! tip "Théorème de Beatty"

    Soient $\alpha$ et $\beta$ deux réels strictement positifs. On note $S_{\alpha}$ (respectivement $S_{\beta}$) l'ensemble des entiers strictement positifs qui s'écrivent sous la forme $[n\alpha]$ (respectivement $[n\beta]$) pour un certain entier $n$.

    Les ensembles $S_{\alpha}$ et $S_{\beta}$ forment une partition de $\mathbb{N}^{*}$ si, et seulement si $\alpha$ et $\beta$ sont irrationnels et vérifient 
    
    $$\frac{1}{\alpha}+\frac{1}{\beta} = 1$$ 

!!! info "Démonstration"

    _Supposons que $\alpha$ et $\beta$ sont irrationnels vérifiant $\frac{1}{\alpha} + \frac{1}{\beta} = 1$._ 
    
    Soit $k$ un entier strictement positif. Il est dans l'ensemble $S_{\alpha}$ si et seulement s'il existe un entier $n$ tel que:

    $$n\alpha - 1 < k < n\alpha$$

    L'inégalité de droite étant stricte car $\alpha$ est supposé irrationnel. L'équation se transforme et donne:

    $$\frac{k}{\alpha} < n < \frac{k}{\alpha} + \frac{1}{\alpha}$$

    Autrement dit, $k \in S_{\alpha}$ si et seulement si l'intervalle $\left]\frac{k}{\alpha}, \frac{k}{\alpha} + \frac{1}{\alpha}\right[$ contient un entier. De même $k \in S_{\beta}$ si et seulement si l'intervalle $\left]\frac{k}{\beta}, \frac{k}{\beta} + \frac{1}{\beta}\right[$ contient un entier.

    L'intervalle $\left]\frac{k}{\alpha}, \frac{k}{\alpha} + 1\right[$ est de longueur $1$ et ses bornes sont irrationnelles, donc il contient un et un seul entier $n$. Si $n < \frac{k}{\alpha} + \frac{1}{\alpha}$, alors $k \in S_{\alpha}$. Sinon, on a l'inégalité:

    $$\frac{k}{\alpha} + \frac{1}{\alpha} < n < \frac{k}{\alpha} + 1$$

    L'inégalité de gauche étant stricte car $\frac{k+1}{\alpha}$ est irrationnel et donc ne peut être égal à $n$. Comme $\frac{k}{\alpha} = k - \frac{k}{\beta}$, il vient:

    \[\frac{k}{\beta} < k + 1 - n < \frac{k}{\beta} + \frac{1}{\beta} \]

    et donc $k \in S_{\beta}$. Si $k \in S_{\alpha} \cap S_{\beta}$, c'est-à-dire $k$ à la fois dans $S_{\alpha}$ et $S_{\beta}$, il y aurait un entier dans l'intervalle $\left]\frac{k}{\beta}, \frac{k}{\beta}+ \frac{1}{\beta}\right[$ et donc par le même raisonnement que précédement, il y en aurait deux dans l'intervalle $\left]\frac{k}{\alpha}, \frac{k}{\alpha}+1\right[$, ce qui n'est pas possible.

    Réciproquement, supposons que $S_{\alpha}$ et $S_{\beta}$ forment une partition de $\mathbb{N}^{*}$. Considérons un entier $k$ strictement positif. Il y a $\left[\frac{k}{\alpha}\right]$ entiers dans $\{1,...,k\}$ qui sont dans $S_{\alpha}$. De même, il y a $\left[\frac{k}{\beta}\right]$ entiers dans $\{1, ...,k\}$ qui sont dans $S_{\beta}$. Du fait de la partition, il vient:

    \[\left[\frac{k}{\alpha}\right] + \left[\frac{k}{\beta}\right] = k\]

    pour tout $k$. En faisant tendre $k$ vers l'infini, il vient:

    \[\frac{1}{\alpha} + \frac{1}{\beta} = 1\]

    ce qui démontre la deuxième condition.

    Supposons maintenant par l'absurde que $\alpha$ soit rationnel. Alors, il en est de même de $\beta$ d'après la relation précédente. Écrivons $\alpha = \frac{a}{b}$ et $\beta = \frac{c}{d}$. L'entier $ac$ est élément de $S_{\alpha}$ (en prenant $n=bc$) et également élément de $S_{\beta}$ (en prenant $n=ad$), ce qui est contradictoire.

## <span style="color:#0a69b7">PGCD et PPCM</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Soient $a$ et $b$ deux entiers non tous deux nuls. L'ensemble des diviseurs communs de $a$ et de $b$ est fini et non vide, il possède donc un plus grand élément appelé _plus grand commun diviseur (PGCD)_ de $a$ et $b$ et noté $PGCD(a,b)$.
    
    Lorsque $PGCD(a,b) = 1$, on dit que $a$ et $b$ sont premiers entre eux.

    De même, l'ensemble des multiples communs de $a$ et $b$ (dans le cas où les deux sont positifs), admet donc un plus petit élément qu'on appelle _plus petit commun multiple (PPCM)_ de $a$ et de $b$ et on le note $PPCM(a, b)$

!!! tip "Propriétes"

    * Si $d = PGCD(a,b)$, alors $n$ divise $a$ et $b$ si et seulement si $n$ divise $d$.
    * Si $m = PPCM(a,b)$, alors $n$ est un multiple de $a$ et de $b$ si et seulement si $n$ est un multiple de $m$.
    * Si $a$, $b$ et $n$ sont des entiers non nuls et $n > 0$, alors $PGCD(na,nb)=nPGCD(a,b)$. Si de plus $n$ divise $a$ et $b$ alors $PGCD(\frac{a}{n}, \frac{b}{n}) = \frac{1}{n}PGCD(a,b)$.
    * Si $d = PGCD(a,b)$, on peut écrire $a=da'$ et $b=db'$ pour $a'$ et $b'$ des nombres premiers entre eux.
    * Pour $a$ et $b$ des entiers, l'égalité $PGCD(a,b)=PGCD(a,a+b)$ est toujours vérifiée lorsqu'elle a un sens. En particulier, le $PGCD$ de deux nombres consécutifs est $1$ et plus généralement, le $PGCD$ de $a$ et $a+n$ est un diviseur positif de $n$.
    * Plus généralement, si $x$, $y$, $a$, $b$, $a'$ et $b'$ des entiers, alors:

        $$PGCD(x,y) | PGCD(ax+by, a'x+b'y) | (ab' - ba')PGCD(x,y)$$

        En particulier, si $|ab'-ba'| = 1$, alors $PGCD(x,y) = PGCD(ax + by, a'x + b'y)$

!!! warning "Remarque"

    Pour prouver l'égalité de deux $PGCD$, une méthode efficace est de montrer que chacun divise l'autre.

???- success "Demonstration de $PGCD(x,y) | PGCD(ax+by, a'x+b'y) | (ab' - ba')PGCD(x,y)$"

    Soient $x$, $y$, $a$, $b$, $a'$ et $b'$ des entiers, alors si on écrit $d = PGCD(x,y)$, alors $d | x$ et $d | y$. Ainsi:

    $$d | ax+by \quad \textrm{et} \quad d | a'x+b'y \quad \textrm{cela implique que} \quad d | PGCD(ax+by, a'x+b'y)$$

    Avec $d' = PGCD(ax+by, a'x+b'y)$, on a $d' | ax+by$ et $d' | a'x+b'y \implies d'| b'(ax+by) - b(a'x+b'y) = (ab'-ba')x$ et $d'| a(a'x+b'y) - a'(ax+by) = (ab'-ba')y$, donc:

    $$ d' | PGCD((ab'-ba')x, (ab'-ba')y) = (ab'-ba') PGCD(x,y) $$

    Par conséquent:

    $$PGCD(x,y) | PGCD(ax+by, a'x+b'y) | (ab' - ba')PGCD(x,y)$$

    Et lorsque $|ab'-ba'| = 1$, cela implique que: $PGCD(x,y) | PGCD(ax+by, a'x+b'y) | PGCD(x,y)$ d'où: $PGCD(x,y) = PGCD(ax + by, a'x + b'y)$.

!!! tip "Propriétés classiques"

    * Si $a$ et $b$ sont des entiers non nuls alors $PGCD(a^{n}, b^{n}) = PGCD(a,b)^{n}$ pour tout entier $n \geq 0$
    * Si $a$, $b$ et $c$ sont des entiers non nuls, on a:

        $$ PGCD(a, PPCM(b,c)) = PPCM(PGCD(a,b), PGCD(a,c)) $$

        $$ PPCM(a, PGCD(b,c)) = PGCD(PPCM(a,b), PPCM(a,c)) $$

    * _Théorème de Bézout_: Si $a$ et $b$ sont des entiers premiers entre eux, alors, il existe des entiers $u$ et $v$ tels que

        $$au+bv = 1$$

    * _Lemme de Gauss_: Si des entiers $a, b$ et $c$ sont tels que $a$ divise $bc$ et $a$ est premier avec $b$, alors $a$ divise $c$
    * Si deux entiers premiers entre eux $a$ et $b$ divisent $n$, alors le produit $ab$ divise également $n$.

Ces prorpriétes sont des résultats dont les démonstrations utilisent des notions telles que la décomposition en facteurs premiers d'entiers et des propriétés de la division euclidienne.
Ces notions seront présentées plus tard ainsi que quelques démonstrations de propriétés ci-dessus.

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice 1"

    On définit le $n$-ième _nombre de Fermat_ par la formule $F_{n} = 2^{2^{n}} + 1$. Montrer que les $F_{n}$ sont deux à deux premiers entre eux.

???- success "Solution"

    Avec la relation

    $$F_{n+1} - 2 = 2^{2^{n+1}} - 1 = (2^{2^{n}} - 1)(2^{2^{n}}+1) = (F_{n} - 2)F_{n}$$

    On obtient par récurrence:

    $$F_{n+1} - 2 = F_{n}F_{n-1}...F_{0}$$

    Soit $d$ un diviseur commun de $F_{n}$ et $F_{m}$. Supposons par exemple $n < m$. D'après la formule précédente, étant donné que $d$ divise $F_{n}$, il divise $F_{m} - 2$ et donc $2$.
    La formule des $F_{n}$ montre qu'ils sont tous impairs.

    La seule valeur de $d$ qui correspond est donc $|d| = 1$. Ainsi $F_{n}$ et $F_{m}$ sont premiers entre eux.

!!! question "Exercice 2"

    Soient $a$ et $b$ des nombres premiers entre eux. Montrer que $ab$ et $a + b$ sont aussi premiers entre eux.

???- success "Solution"

    Soit $d$ un diviseur commun de $ab$ et de $a+b$. Alors $d$ divise $a(a+b) - ab = a^{2}$. De même, $d$ divise $b^{2}$. D'après une des propriétés précédentes, les entiers $a^{2}$ et $b^{2}$ sont premiers entre eux (puisque $a$ et $b$ sont premiers entre eux). Ainsi $d = \pm 1$, ce qui permet de conclure la démonstration.

## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 01/03/2024.
