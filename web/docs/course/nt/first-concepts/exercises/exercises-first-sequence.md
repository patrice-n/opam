---
comments: true
---

# <span style="color:#074b83">Première série d'exercices d'arithmétique</span>

## <span style="color:#074b83">Exercices</span>

!!! example "Exercice 1"

    On désigne par $d(n)$ le nombre de diviseurs strictement positifs de l'entier $n$.
    Montrer que $d(n)$ est impair si, et seulement si $n$ est un carré.

???- success "Solution 1"

    On sait que si la décomposition en facteurs premiers de $n$ est:

    $$ n = p_{1}^{\alpha_{1}}...p_{k}^{\alpha_{k}} $$

    alors $d(n)$ est donnée par la formule:

    $$ d(n) = (\alpha_{1} + 1)...(\alpha_{\k}+1) $$

    Ainsi ce nombre est impair si et seulement si chacun des facteurs est impair, c'est-à-dire si et seulement si $\alpha_{i}$ est pair pour tout $i$. Ceci est équivalent au fait
    que $n$ soit un carré.

!!! example "Exercice 2 (Saint-Petersbourg 04)"

    Déterminer tous les entiers positifs $n$ tels que $5^{n-1} + 3^{n-1}$ divise $5^{n}+3^{n}$.

???- success "Solution 2"

    On remarque que:

    $$3(5^{n-1}+3^{n-1}) < 5^{n} + 3^{n} < 5 (5^{n-1} + 3^{n-1})$$

    Et donc le quotient $\frac{5^{n} + 3^{n}}{5^{n-1}+3^{n-1}}$ supposé entier ne peut valoir que $4$. On a:

    $$ \frac{5^{n} + 3^{n}}{5^{n-1}+3^{n-1}} = 4 \Leftrightarrow 5^{n} + 3^{n} = 4(5^{n-1} + 3^{n-1}) \Leftrightarrow 5^{n} + 3^{n} = (5 - 1)5^{n-1} + (3 + 1)3^{n-1} $$

    $$ \frac{5^{n} + 3^{n}}{5^{n-1}+3^{n-1}} \quad \textrm{est entier} \Leftrightarrow 5^{n} + 3^{n} = (5^{n} - 5^{n-1}) + (3^{n} + 3^{n-1}) \Leftrightarrow 0 = 3^{n-1} - 5^{n-1}$$

    $$ \frac{5^{n} + 3^{n}}{5^{n-1}+3^{n-1}} \quad \textrm{est entier} \Leftrightarrow 3^{n-1} = 5^{n-1} \Leftrightarrow n = 1$$

!!! example "Exercice 3"

    Montrer que pour tout entier $n$, le nombre $n^{3} - n$ est un multiple de $6$.

???- success "Solution 3"

    Nous allons montrer qu'il est multiple de $2$ et de $3$. Comme $2$ et $3$ sont premiers entre eux, cela conclura. La factorisation:

    $$n^{3} - n = n(n^{2} - 1) = n(n - 1)(n + 1)$$

    nous montre que $n^{3} - n$ s'écrit comme le produit de trois nombres consécutifs. Parmi eux, il y a forcément un multiple de $2$ et un multiple de $3$ (pas forcément distincts bien sûr). Le produit est donc à la fois multiple de $2$ et de $3$ comme on le voulait.

!!! example "Exercice 4 (OIM 59)"

    Montrer que la fraction $\frac{21n+4}{14n+3}$ est toujours irréductible.

???- success "Solution 4"

    Il suffit de remarquer que:

    $$3(14n + 3) - 2(21n + 4) = 1$$

    Le théorème de Bézout assure que $14n + 3$ et $21n + 4$ sont premiers entre eux.
    Comme dans les notions de premiers concepts, ce théorème n'a pas été présenté. Ainsi, nous allons en nous appuyant sur l'égalité au dessus, démontrer que $14n + 3$ et $21n + 4$ sont premiers entre eux. En effet, soit $d = PGCD(14n+3, 21n+4)$, donc $d | 14n+3$ et $d | 21n+4$ ainsi, $d | 3(14n + 3) - 2(21n + 4)$ et donc $d | 1$.

    Par conséquent $d = 1$, d'où $14n + 3$ et $21n + 4$ sont premiers entre eux.

    Pour conclure, la fraction $\frac{21n+4}{14n+3}$ est toujours irréductible.

!!! example "Exercice 5"

    Montrer que $2x+3$ est un multiple de $11$ si, et seulement si $5x+2$ l'est.

???- success "Solution 5"

    Cela résulte directement des formules:

    $$ 5x + 2 = 8(2x + 3) - 11(x + 2) $$

    $$ 2x + 3 = 7(5x + 2) - 11(3x + 1) $$

    En effet, ces formules étant vérifiée, on a:

    \[ 2x + 3 \quad \textrm{multiple de} \quad 11 \quad \textrm{alors} \quad \exists m \in \mathbb{N}, \quad \textrm{tel que:} \quad 2x+3 = 11m \implies 11m = 7(5x + 2) - 11(3x + 1) \]

    \[ 2x + 3 \quad \textrm{multiple de} \quad 11 \implies 11(m + (3x + 1)) = 7(5x + 2) \implies 11 | 7(5x + 2) \]

    Comme $7$ et $11$ sont premiers entre eux, alors:

    \[ 2x + 3 \quad \textrm{multiple de} \quad 11 \implies 5x+2 \quad \textrm{multiple de} \quad 11 \]

    De même, on a:

    \[ 5x + 2 \quad \textrm{multiple de} \quad 11 \quad \textrm{alors} \quad \exists p \in \mathbb{N}, \quad \textrm{tel que:} \quad 5x+2 = 11p \implies 11p = 8(2x + 3) - 11(x + 2) \]

    Or $7$ et $11$ sont premiers entre eux, ainsi:

    \[ 5x + 2 \quad \textrm{multiple de} \quad 11 \implies 11(p + (x + 2)) = 8(2x + 3) \implies 11 | 7(2x + 3) \]

    Pour conclure:

    \[2x+3 \quad \textrm{est multiple de} \quad 11 \quad \textrm{si et seulement si} \quad 5x+2 \quad \textrm{est multiple de} \quad 11\]

!!! example "Exercice 6"

    Soit $p > 3$ un nombre premier. Montrer que $p^{2}-1$ est un multiple de $12$.

???- success "Solution 6"

    On factorise $p^{2}-1$, ce qui donne:

    $$p^{2} - 1 = (p - 1)(p + 1)$$

    Comme $p$ est un nombre premier différent de $2$ ($p > 3$), il est impair. Ainsi, $p - 1$ et $p + 1$ sont tous les deux pairs et le produit est multiple de $4$.

    De même, $p > 3$ et donc $p$ ne peut être un multiple de $3$. On en déduit que soit $p - 1$, soit $p + 1$ est un multiple de $3$, et donc $p^{2} - 1$ en est également un.

    En conclusion, $p^{2} - 1$ est multiple de $3$ et de $4$, et donc de $12$.

!!! example "Exercice 7"

    Soient $a$ et $b$ des entiers strictement positifs tels que $a^{n}$ divise $b^{n+1}$ pour tout entier $n \geq 1$. Montrer
    que $a$ divise $b$.

???- success "Solution 7"

    Soit $p$ un nombre premier. L'hypothèse nous dit que

    $$ nv_{p}(a) \geq (n+1)v_{p}(b) $$

    Soit encore:

    $$ v_{p}(a) \geq \left(1 + \frac{1}{n}\right)v_{p}(b) $$

    et par passage à la limite (pour $n \rightarrow +\infty$) $v_{p}(a) \geq v_{p}(b)$ pour tout nombre premier $p$. On en déduit que $a$ divise $b$.

!!! example "Exercice 8"

    Soit $n$ un entier strictement positif. On appelle $k$ le nombre de diviseurs premiers de $n$. Prouver que:

    $$ log(n) \geq k log2 $$

???- success "Solution 8"

    La décomposition en facteurs premiers nous donne:

    \[n = p_{1}^{\alpha_{1}}...p_{k}^{\alpha_{k}}\]

    pour certains nombres premiers $p_{i}$ distincts deux à deux et certains exposants $\alpha_{i}$ strictement positifs. On a $p_{i} \geq 2$ et donc _a fortiori_ $p_{i}^{\alpha_{i}} \geq 2$. On en déduit que $n \geq 2^{k}$ et puis l'inégalité proposée en prenant les logarithmes.

!!! example "Exercice 9"

    Soient $p$ un nombre premier et $n$ un entier tels que $p$ divise $n^{k}$. Est-ce qu'alors, forcément, $p$ divise $n$ ?

???- success "Solution 9"

    Comme $p$ divise $n^{k}$, on a: $v_{p}(n^{k}) > 0$ et en particulier

    \[v_{p}(n) = \frac{1}{k}v_{p}(n^{k}) > 0\]

    On en déduit que $p$ divise $n$.

!!! example "Exercice $10^{*}$ (Baltique 04)"

    Déterminer tous les ensembles $X$ d'entiers strictement positifs contenant au moins deux éléments et tel que, si $m$ et $n$ sont dans $X$ avec $n > m$ alors il existe un élément $k \in X$ vérifiant $n = mk^{2}$.

???- success "Solution 10"

    Soit $X$ un ensemble d'entiers strictement positifs contenant au moins deux éléments et tel que, si $m$ et $n$ sont dans $X$ avec $n > m$ alors il existe un élément $k \in X$ vérifant $n = mk^{2}$.

    Notons $a$ le plus petit élément de $X$ et $b$ le deuxième plus petit (et donc $b > 1$). D'après l'hypothèse, il existe $k \in X$ tel que $b = ak^{2}$. Il est évident que l'on ne peut pas avoir $k \geq b$, c'est donc que $k = a$ puis $b=a^{3}$. Notons qu'alors $a \neq 1$ puisque $b \neq a$.

    Supposons que $X$ contienne un autre élément $c$ que l'on choisit encore minimal. Encore d'après l'hypothèse, il doit exister $k$ et $k'$ dans $X$ tels que $c = ak^{2}$ et $c = bk'^{2} = a^{3}k'^{2}$. De là, on déduit que $ak^{2} = a^{3}k'^{2}$ puis $(ak')^{2} = k^{2}$ et finalement $ak'= k$.

    Par ailleurs, les entiers $k$ et $k'$ sont deux éléments de $X$ avec $k' < k$, donc en appliquant une nouvelle fois l'hypothèse, il doit exister $k" \in X$ tel que $k = k'k"^{2}$. On en déduit que $a = k"^{2}$ et donc que, puisque $a > 1$, il vient que $k" < a$. Cela contredit la minimalité de $a$.
    
    On déduit que X est réduit à $\{a, a^{3}\}$.

    Réciproquement, les ensembles de la forme $\{a, a^{3}\}$ vérifient l'hypothèse de l'exercice.

!!! example "Exercice $11^{*}$ (Irlande 98)"

    Déterminer les entiers $n$ ayant exactement $16$ diviseurs:
    
    $$ 1 = d_{1} < d_{2} < ... < d_{15} < d_{16} = n $$

    et tels que $d_{6} = 18$ et $d_{9} - d_{8} = 17$.

???- success "Solution 11"

    Comme $n$ est un multiple de $18$, il s'écrit:

    \[ n = 2^{\alpha}3^{\beta} \prod_{i}p_{i}^{\gamma_{i}} \]

    pour certains entiers $\alpha \geq 1$, $\beta \geq 2$ et $\gamma_{i} \geq 0$, et pour certains nombres premiers $p_{i} \geq 5$ deux à deux distincts. D'autre part, on constate que $18$ a exactement $6$ diviseurs (qui sont $1$, $2$, $3$, $6$, $9$ et $18$). Comme un diviseur de $18$ doit être un diviseur de $n$, on a forcément $d_{1} = 1$, $d_{2} = 2$, $d_{3} = 3$, $d_{4} = 6$, $d_{5} = 9$ et $d_{6} = 18$. En particulier, $4$ ne divise pas $n$ et $\alpha = 1$.

    Le nombre de diviseurs de $n$ est donné par la formule:

    \[2(\beta + 1)\prod_{i} (\gamma_{i} + 1)\]

    Ce nombre doit faire $16$ et comme $\beta + 1 \geq 3$, les seules solutions sont $\beta = 3$ (et $\gamma_{1} = 1$) et $\beta = 7$ (et $\gamma_{1} = 0$). Les éventuelles solutions sont donc, soit $2 \times 3^{7}$, soit $2 \times 3^{2} \times p$ pour un nombre premier $p \geq 19$.

    On calcule les diviseurs successifs de $2 \times 3^{7}:$ $d_{7} = 27$, $d_{8} = 54$,$d_{9} = 81$. On a $d_{9} - d_{8} > 17$ et ce nombre n'est donc pas solution.

    De même, on calcule les diviseurs de $2 \times 3^{2} \times p$. 
    
    * Si $19 \leq p < 27$, on a $d_{7} = p$, $d_{8} = 27$, $d_{9} = 2p$, (ayant déjà calculé $d_{1}, ..., d_{6}$) ce qui fournit l'équation $2p - 27 = 17$ et donc $p=22$ qui n'est pas premier. 

    * Si $27 < p < 54$, on a $d_{7} = 27$, $d_{8} = p$, $d_{9} = 54$ et donc $54 - p = 17$ puis $p = 37$, qui convient.

    * Si $p > 54$, on a $d_{7} = 27$, $d_{8} = 54$, $d_{9} = p$ ce qui donne $p = 71$.

    Finalement, il y a deux solutions: 
    
    $$ n = 2 \times 3^{3} \times 37 = 1998 $$

    $$ n = 2 \times 3^{3} \times 71 = 3834 $$

!!! example "Exercice $12^{*}$"

    Déterminer tous les entiers $a, b$ et $c$ strictement supérieurs à $1$ tels que $a$ divise $bc-1$, $b$ divise $ca-1$ et $c$ divise $ab-1$.

???- success "Solution 12"

    Un diviseur commun à $a$ et à $b$ doit diviser $bc - 1$ et donc $1$. Ainsi $a$ et $b$ sont premiers entre eux. De même, $a$ et $c$ sont premiers entre eux et $c$ et $c$ sont premiers entre eux. D'où $a$, $b$ et $c$ sont premiers entre eux deux à deux.

    Si $a$ divise $bc - 1$, il divise également $bc + ac + ab - 1$. De même, $b$ et $c$ doivent diviser $bc + ac + ab - 1$. Comme $a$, $b$ et $c$ sont premiers entre eux deux à deux, on en déduit que $abc$ divise $ab + bc + ca - 1$. Le quotient:

    \[\frac{ab + bc + ca - 1}{abc} = \frac{1}{a} + \frac{1}{b} + \frac{1}{c} - \frac{1}{abc}\]

    est inférieur ou égal à $\frac{3}{2}$. Il ne peut donc valoir que $1$.

    On est amené à résoudre:

    \[\frac{1}{a} + \frac{1}{b} + \frac{1}{c} - \frac{1}{abc} = 1\]

    On ne peut pas avoir $a$, $b$ et $c$ supérieurs ou égaux à $3$. Sinon:

    \[\frac{1}{a} + \frac{1}{b} + \frac{1}{c} \leq 1 \implies \frac{1}{a} + \frac{1}{b} + \frac{1}{c} - \frac{1}{abc} < 1 \]

    Ce qui serait contraire à l'équation ci-dessus.    
    
    Ainsi, sans perte de généralité, on peut supposer $a \leq b \leq c$, et donc $a \leq 3$ et donc $a \leq 3$ et donc $a = 2$ ou $a = 3$. Si $a = 2$, l'équation devient:

    \[\frac{1}{b} + \frac{1}{c} - \frac{1}{2bc} = \frac{1}{2}\]

    et comme précédemment $b$ et $c$ ne peuvent pas être simultanément supérieurs ou égaux à $4$. On a donc $b = 2$ ou $b = 3$. Pour $b = 2$, l'équation n'a pas de solution en $c$. Pour $b = 3$, on obtient $c = 5$. On vérifie que le triplet $(2, 3, 5)$ est solution.

    De même, on traite le cas $a = 3$. L'équation devient alors:

    \[ \frac{1}{b} + \frac{1}{c} - \frac{1}{3bc} = \frac{2}{3} \]

    Ici, on ne peut avoir $b$ et $c$ supérieurs ou égaux à $3$ et comme ils sont supposés supérieurs à $a$, il n'y a pas de solution.

    Finalement, les solutions sont le triplet $(2, 3, 5)$ et toutes ses permutations, soit:

   \[(2, 3, 5), (2, 5, 3), (3, 2, 5), (3, 5, 2), (5, 2, 3), (5, 3, 2)\]  

!!! example "Exercice $13^{*}$"

    Pierre et Xavier jouent au jeu suivant. Ils commencent par choisir un nombre entier $n>0$. Puis,
    Pierre choisit en secret un entier $m$ tel que $0 < m < n$. Xavier doit alors découvrir le nombre
    secret. Pour cela, il peut proposer un nombre $k$ quelconque à Pierre qui, en retour, lui indique
    si le nombre $m+k$ est premier ou non. Prouver que Xavier peut déterminer le nombre secret de Pierre
    en moins de $n-1$ questions.

???- success "Solution 13"

    On sait qu'il existe un nombre premier $p$ qui est tel que tous les nombres $p+1, ..., p+n$ soient composés.

    Xavier peut alors tester les entiers de l'ensemble $\{1, ..., n-1\}$ les uns après les autres.
    Pour tester $1$, il propose le nombre $p - 1$: si Pierre répond oui, alors le nombre choisi est $1$, sinon ce n'est pas $1$. Ensuite, il teste $2$ et proposant le nombre $p - 2$, et ainsi de suite.

    Il arrive donc à conclure en moins de $n-1$ questions, puisqu'il est inutile de tester $n-1$: si aucun des nombres $p - k$ n'est premier pour $k \leq n-2$, c'est donc que c'est $m = n-1$.

!!! example "Exercice $14^{*}$"

    Montrer que les racines cubiques de trois nombres premiers distincts ne peuvent être dans une 
    même progression arithmétique.

???- success "Solution 14"

    Notons $p$, $q$, $l$ trois nombres premiers. Si leurs racines cubiques étaient dans une même progression arithmétique de raison $r$, il existerait des entiers $m$ et $n$ non nuls et distincts tels que:

    \[\sqrt[3]{p} - \sqrt[3]{q} = mr \quad \textrm{et} \quad \sqrt[3]{p} - \sqrt[3]{l} = nr\]

    On a donc:

    \[\sqrt[3]{p} - \sqrt[3]{l} = \frac{n}{m}\left(\sqrt[3]{p} - \sqrt[3]{q}\right)\]

    et donc il existe des rationnels non nuls $\alpha$ et $\beta$ tels que:

    \[ \alpha\sqrt[3]{p} + \beta\sqrt[3]{q} = \sqrt[3]{l} \]

    En élévant au cube, il vient donc:

    $$ l = \alpha^{3}p + \beta^{3}q + 3\alpha\beta(\alpha\sqrt[3]{p} + \beta\sqrt[3]{q})\sqrt[3]{pq} $$
    $$ = \alpha^{3}p + \beta^{3}q + 3\alpha\beta\sqrt[3]{pql}$$

    Il en résulte que $t = \sqrt[3]{pql}$ est rationnel. Mais on doit avoir

    \[v_{p}(t^{3}) = 3v_{p}(t) = 1,\]

    Ce qui est absurde.

!!! example "Exercice $15^{*}$"

    Soit $x$ un réel. Est-il vrai que:
    
    * __a)__ Si $x^{7}$ et $x^{12}$ sont rationnels alors $x$ est rationnel ?
    * __b)__ Si $x^{9}$ et $x^{12}$ sont rationnels alors $x$ est rationnel ? 

???- success "Solution 15"

    * __a)__ Oui. Les entiers $7$ et $12$ sont premiers entre eux, donc d'après le théorème de Bézout, il existe des entiers $u$ et $v$ tels que $7u + 12v = 1$. On a alors:

    $$x = x^{7u+12v} = \left(x^{7}\right)^{u}\times\left(x^{12}\right)^{v}$$

    Ainsi $x$ s'écrit comme un produit de nombres rationnels. Il est donc rationnel.

    __Remarque__: 
    
    Le raisonnement précédent ne permet pas de déduire que si $x^{7}$ et $x^{12}$ sont entiers, alors $x$ est forcément entier: en effet, parmi $u$ et $v$ il y a au moins un nombre négatif et donc le produit $(x^{7})^{u}\times(x^{12})^{v}$ cache en réalité un quotient. Toutefois le résultat est quand même vrai. On vient de prouver que $x$ est rationnel, et on sait que $x^{7}$ est un entier. Un résultat de cours prouve alors que $x$ est entier (On peut utiliser la valuation p-adique de $x$ à l'aide de celle de $x^{7}$ et montrer qu'elle est toujours positive d'où que $x$ est entier).

    De plus, en l'absence de la connaissance du théorème de Bézout à ce stade du cours, il suffit de prendre $u=-5$ et $v=3$ ainsi on a: $7u + 12v = 1$.

    * __b)__ Non. Cette fois-ci les entiers $9$ et $12$ ne sont pas premiers entre eux: leur PGCD est $3$. On choisit $x$ irrationnel tel que $x^{3}$ est rationnel (par exemple $x = \sqrt[3]{3}$). Alors $x^{9} = \left(x^{3}\right)^{3}$ est bien rationnel, ainsi que $x^{12} = \left(x^{3})^{4}$.

!!! example "Exercice $16^{*}$ (d'après Autriche 02)"

    Soit $a \geq 9$ un entier impair. Montrer que l'équation:

    $$x^{[x]} = \frac{a}{2}$$

    n'a pas de solution pour $x \in \mathbb{Q}$.

???- success "Solution 16"

    En écrivant la valuation $2$-adique des deux membres de l'équation, il vient:

    $$[x]v_{2}(x) = -1$$

    ce qui impose $[x] = \pm 1$. 
    
    * Si $[x] = 1$, on a $1 \leq x < 2$ et donc $x^{[x]} < 2$ ce qui est incompatible avec l'équation. 
    
    * Si $[x] = -1$, $x$ est négatif et $x^[x]$ aussi, ce qui est encore incompatible.

    Donc, pour $a \geq 9$ entier impair, l'équation:

    \[x^{[x]} = \frac{a}{2}\]

    n'a pas de solution pour $x \in \mathbb{Q}$.

!!! example "Exercice $17^{*}$"

    Trouver le plus petit entier $x$ tel que $2|x-1, \quad 3|x-2, \quad ..., \quad 9|x-8$.

???- success "Solution 17"

    La condition est équivalente à $x + 1$ à la fois multiple de $2$, de $3$, ainsi de suite jusqu'à $9$. Elle est donc également équivalente à $x + 1$ multiple de $PPCM(2, 3, 4, 5, 6, 7, 8, 9) = 2520$. La plus petite solution positive est donc:

    $$ x = 2519$$ 

!!! example "Exercice $18^{*}$ (OIM 02)"

    Les diviseurs strictement positifs de l'entier $n > 1$ sont $1 = d_{1} < d_{2} < ... < d_{k} = n$. Soit
    $d = d_{1}d_{2} + d_{2}d_{3} + ... + d_{k-1}d_{k}$. Montrer que $d < n^{2}$ et trouver tous les $n$ pour lesquels d divise $n^{2}$.

???- success "Solution 18"

    On remarque que si $d$ est un diviseur de $n$ alors $\frac{n}{d}$ aussi. L'indexation des diviseurs donne alors $d_{i}d_{k+1-i}=n$. Donc:

    $$d = \sum_{i=1}^{k-1} d_{i}d_{i+1} = n^{2} \sum_{i=1}^{k-1} \frac{1}{d_{i}d_{i+1}} \leq n^{2}\sum_{i=1}^{k-1}\left(\frac{1}{d_{i}} - \frac{1}{d_{i+1}}\right)$$

    La dernière inégalité étant obtenue car $d_{i+1} - d_{i} \geq 1$. On en déduit que:

    \[d \leq n^{2}\left(\frac{1}{d_{1}} - \frac{1}{d_{k}}\right) = n^{2} \left(1 - \frac{1}{n}\right) < n^{2}\]

    Si $n = p$ est un nombre premier, alors $d = p$ qui divise $n^{2}$. Si $n$ est composé, alors $k > 2$. Soit $p$ le plus petit diviseur premier de $n$. On a:

    \[d > d_{k-1}d_{k} = \frac{n^{2}}{p}\]

    et donc:

    \[ 1 < \frac{n^{2}}{d} < p \]

    Mais alors $\frac{n^{2}}{d}$ est un diviseu de $n^{2}$ strictement inférieur à $p$, ce qui n'est pas possible.

    Les seules solutions sont donc les nombres premiers.
    
!!! example "Exercice $19^{*}$ (Nombres de Fermat)"

    Montrer que si $2^{n}+1$ est un nombre premier, alors $n$ est une puissance de $2$. 

???- success "Solution 19"

    Soit $p$ un nombre premier impair divisant $n$. On peut écrire $n = pk$ et:

    \[2^{pk}+1 = (2^{k}+1)(2^{k(p-1)} - 2^{k(p-2)} + ... + 1)\]

    Évidemment $1 < 2^{k} + 1 < 2^{pk} + 1$. On a donc obtenu une factorisation non triviale.

    On en déduit que le seul diviseur premier de $n$ est $2$ et donc que $n$ est une puissance de $2$

    __Commentaire__:

    Les nombres de la forme $F_{n} = 2^{2^{n}} + 1$ s'appelent les _nombres de Fermat_. Fermat avait conjecturé que tous les nombres de cette forme étaient premiers. C'est le cas de $F_{0}$, $F_{1}$, $F_{2}$, $F_{3}$ et $F_{4}$. Malheureusement, Euler démontra en $1732$ que $F_{5}$ est composé. Depuis, on n'a pas trouvé d'autres nombres de Fermat premiers.

!!! example "Exercice $20^{*}$"

    Si $n>1$ est un entier, on note $d(n)$ le nombre de ses diviseurs positifs, $\sigma(n)$ la somme de ses diviseurs positifs ou $\phi(n)$ le nombre de nombre premiers avec $n$ et compris entre $1$ et $n$.

    Trouver tous les entiers $n > 1$ tels que:

    $$\sigma(n) + \phi(n) = n.d(n)$$

???- success "Solution 20"

    Soit $n > 1$ un entier. On constate que les entiers $1$ et $n$ sont toujours des diviseurs distincts de $n$ et que tous les autres diviseurs de $n$ sont strictement plus petits que $n$. On en déduit l'inégalité:

    \[\sigma(n) \leq 1 + n + (d(n) - 2)n \]

    et cette égalité est stricte dès que $n$ admet plus de deux diviseurs, c'est-à-dire dès que $n$ est composé.

    D'autre part, il ne peut y avoir plus de $n-1$ entiers premiers avec $n$ dans l'intervalle $[1,n]$ (en effet, $n$ n'est pas premier avec lui-même). On en déduit que $\phi(n) \leq n-1$. En combinant avec l'inégalité obtenue précédemment, on arrive à:

    \[\sigma(n) + \phi(n) \leq n.d(n) \]

    et cette inégalité est stricte si $n$ est composé.

    On en déduit que les seuls $n$ susceptibles de répondre à la question sont les nombres premiers. On vérifie par ailleurs que si $p$ est premier, $d(p) = 2$, $\sigma(p)=p+1$ et $\phi(p) = p-1$, et donc que l'on a bien l'égalité:

    \[\sigma(p) + \phi(p) = p.d(p) \]

    Les solutions sont donc exactement les nombres premiers.

!!! example "Exercice $21^{*}$ (OIM 68)"

    Le symbôle $[x]$ désignant la partie entière de $x$. Calculer:

    $$\left[\frac{n+1}{2}\right] + \left[\frac{n+2}{4}\right] + \left[\frac{n+4}{8}\right] + ... + \left[\frac{n+2^{k}}{2^{k+1}}\right] + ...$$

???- success "Solution 21"

    Il est clair que cette somme ne possède qu'un nombre fini de termes non nuls, $\left[\frac{n+2^{k}}{2^{k+1}}\right]$ est non nul dès que $2^{k+1} > n+2^{k}$, donc $2^{k} > n$. Cet énoncé se résout facilement si l'on connaît le lemme:

    "Pour tout réel $x$, $[2x] = [x] + [x + \frac{1}{2}]$"

    Qui se vérifie immédiatement: si $n \leq x \leq n + \frac{1}{2}$, $[x]=n=[x+\frac{1}{2}]$ et $[2x] = 2n$, et si $n + \frac{1}{2} \leq x < n+1$, $[x] = n$, $[x + \frac{1}{2}] = n+1$, et $[2x] = 2n+1$. Il en résulte que:

    \[\left[\frac{n+2^{k}}{2^{k+1}}\right] = \left[\frac{n}{2^{k+1}} + \frac{1}{2}\right] = \left[\frac{n}{2^{k}}\right] - left[\frac{n}{2^{k+1}}\right]\]

    La somme s'écrit donc:

    \[\left([n] - \left[\frac{n}{2}\right]\right) + \left(\left[\frac{n}{2}\right] - \left[\frac{n}{4}\right]\right) + \left(\left[\frac{n}{2}\right] - \left[\frac{n}{4}\right]\right) + ...\]

    et par "simplification téléscopique", elle vaut $[n]$, soit $n$ si $n$ est un entier.

!!! example "Exercice $22^{*}$"

    On note $p_{n}$ le $n$-ième nombre premier. En utilisant le théorème des nombres premiers, montrer que $p_{n} \sim nlog(n)$.

???- success "Solution 22"

    Par définition $\pi(p_{n}) = n$. Ainsi:

    \[nlog(n) = \pi(p_{n})log(\pi(p_{n}))\]

    D'après le théorème des nombres premiers, le quotient $\pi(p_{n}).\frac{log p_{n}}{p_{n}}$ tend vers 1 quand $n$ tend vers l'infini (car $p_{n}$ tend vers l'infini) et donc en passant au logarithme, il vient:

    \[log(\pi(p_{n})) - log p_{n} + log(log p_{n}) \rightarrow 0\]

    puis en divisant tout par $log p_{n}$, il vient:

    \[log(\pi(p_{n})) \sim log p_{n} \]

    En appliquant une nouvelle fois le théorème des nombres premiers, on a:

    \[nlogn = \pi(p_{n})log(\pi(p_{n})) \implies nlog n \sim \frac{p_{n}}{log p_{n}}.log p_{n} = p_{n}\]

!!! example "Exercice $23^{*}$ (APMO 04)"

    Déterminer toutes les parties $E$ non vides de $\mathbb{N}^{*}$ telles que pour tous $a$ et $b$ dans $E$, le nombre $\frac{a+b}{PGCD(a,b)}$ est aussi dans $E$.

???- success "Solution 23"

    Soit $E$ un tel ensemble, et $a \in E$ quelconque. Alors d'après l'hypothèse, $(a+a)/a = 2 \in E$. On peut remarquer que le singleton $\{2\}$ est en fait une solution du problème. On suppose dorénavant que $E$ contient au moins un autre élément que $2$.

    * Si $1$ est dans $E$, alors pour tout $a \in E$, $(a+1)/1 = a+1 \in E$, donc une récurrence immédiate montre que $E = \mathbb{N}^{*}$, qui est bien une solution.

    Dans le cas contraire, soit $m$ le plus petit élément de $E$ autre que $2$. 
    
    * Si $m$ était pair, disons $m=2k$ avec $k \geq 2$, on aurait $\frac{2k+2}{2} = k+1 \in E$. Or $2 < k+1 < 2k$, ce qui contredirait la minimalité de $m$. 
    
    Donc $m$ est impair, et $m+2$ (car $m+2 = \frac{m+2}{PGCD(m,2)}$ et $\frac{m+2}{PGCD(m,2)} \in E$) est aussi dans $E$, et de même pour $m+2p$ (par récurrence) pour tout $p \geq 0$. Tous les nombres impairs à partir de $m$ sont donc dans $E$, et en particulier $km$ pour tout $k \geq 1$ impair. Ainsi, $\frac{km+m}{m} = k+1 \in E$, ce qui montre que $E$ contient tous les entiers pairs, et en particulier $4$. La minimalité de $m$ assure alors que $m=3$ et donc que $E$ contient tous les entiers au moins égaux à $2$, ce qui réciproquement fournit bien une solution au problème.

    \[\textrm{Finalement, il y a trois solutions, qui sont:} \quad \{2\}, \quad \mathbb{N}^{*} \quad \textrm{et} \quad \mathbb{N}^{*}\backslash \{1\}. \]

!!! example "Exercice $24^{*}$"

    Trouver tous les entiers $n$ strictement positifs pour lesquels $2^{n}$ divise $3^{n}-1$.

???- success "Solution 24"

    On a la factorisation:

    \[3^{n} - 1 = 2(3^{n-1} + 3^{n-2} + ... + 1)\]

    Si $n$ est impair le facteur entre parenthèses est une somme de $n$ termes impairs et donc est impair. On en déduit que $3^{n} - 1$ ne peut être un multiple de $4$ et donc _a fortiori_ de $2^{n}$ pour $n>1$. Le cas $n=1$ convient comme on le vérifie à part.

    Supposons $n$ pair et posons donc $n=2k$. La condition se réécrit $2^{2k}$ divise $3^{2k} - 1 = (3^{k} - 1)(3^{k} + 1)$. Les deux nombres $3^{k} - 1$ et $3^{k} + 1$ sont distants de $2$ et dons leur $PGCD$ est un diviseur de $2$. D'autre part, ces nombres sont toujours pairs et donc $PGCD(3^{k}-1, 3^{k} + 1) = 2$. On en déduit que soit $3^{k}-1$, soit $3^{k}+1$ est divisible par $2^{2k - 1}$. Cela implique en toutes circonstances $3^{k}+1 \geq 2^{2k - 1}$ ce qui n'est plus vrai pour $k \geq 3$. On vérifie à la main que $k=0$, $k=1$ et $k=2$ sont solutions.

    \[\textrm{Finalement les seules solutions sont:} \quad n=1, \quad n=2 \quad \textrm{et} \quad n=4.\]

!!! example "Exercice $25^{*}$ (USA 72)"

    Soient $a, b$ et $c$ des entiers strictement positifs. Montrer que:

    $$\frac{PGCD(a,b,c)^{2}}{PGCD(a,b)PGCD(b,c)PGCD(a,c)} = \frac{PPCM(a,b,c)^{2}}{PPCM(a,b)PPCM(b,c)PPCM(a,c)}$$

???- success "Solution 25"

    Soit $p$ un nombre premier. On va prouver que les valuations $p$-adiques des deux membres de l'égalité à prouver sont toujours égales. Notons $\alpha = v_{p}(a)$, $\beta = v_{p}(b)$ et $\gamma = v_{p}(c)$. Il s'agit de montrer que:

    \[2inf(\alpha, \beta, \gamma) - inf(\alpha, \beta) - inf(\beta, \gamma) - inf(\alpha, \gamma) = 2sup(\alpha, \beta, \gamma) - sup(\alpha, \beta) - sup(\beta, \gamma) - sup(\alpha, \gamma)\]

    Où $inf$ désigne le plus petit élément et $sup$, le plus grand élément. Comme les rôles de $\alpha$, $\beta$ et $\gamma$ sont similaires, on peut supposer $\alpha \leq \beta \leq \gamma$ et donc dans ce cas, les deux membres de l'égalité précédente sont égaux à $-\beta$. Ce qui conclut.

## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 24/03/2024.
