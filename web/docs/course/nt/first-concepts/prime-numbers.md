---
comments: true
---

# <span style="color:#074b83"> Nombres premiers </span>

L'utilité des nombres premiers n'est pas à démontrer de sorte que la plupart des résultats d'arithmétique tournent autour de ces nombres.

## <span style="color:#0a69b7">Définitions et exemples</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Un entier $n > 0$ est dit _premier_ s'il est différent de $1$ et s'il n'admet aucun diviseur positif différent de $1$ et de $n$.
    C'est qu'on appelle _diviseur strict_.

    Un nombre qui n'est pas premier est appelé _nombre composé_.

!!! example "Exemples"

    $1$ n'est pas premier.
    
    Les entiers $2, 3, 5, 7, 11$ et $13$ sont les premiers nombres premiers.
    
    Le nombre $4$ n'est pas par contre premier, puisque $4 = 2*2$ et $2$ est un diviseur strict de $4$

!!! tip "Proposition"

    Soit $n > 1$ un entier. Son plus petit diviseur $d > 1$ est un nombre premier. Si de plus $n$ est composé, alors $d \leq \sqrt{n}$.

???- success "Démonstration"

    Supposons que $d$ ne soit pas premier. Alors par définition, il existe un diviseur strict $d'$ de $d$. Mais alors $d' divise $n$, d' > 1$ et $d' < d$, ce qui contredit la minimalité de $d$.

    Comme $d$ divise $n$, on peut écrire $n = dd'$. On a $d > 1$ et comme $n$ n'est pas premier, $d < n$. Ainsi $d'$ est un diviseur de $n$ strictement supérieur à $1$. Par minimalité de $d$, on obtient $d' \geq d$ et donc $n \geq d^{2}$ puis finalement $d \leq \sqrt{n}$.

!!! warning "Remarque"

    On déduit de la propriété précédente que pour tester si un entier $n > 1$ est premier, il suffit de vérifier s'il n'est divisible par aucun nombre entier entre $2$ et $\sqrt{n}$. 
    Si l'on connait la liste des entiers premiers entre $2$ et $\sqrt{n}$, alors il suffira de démontrer qu'aucun d'eux ne divise $n$.

    Une méthode utilisée souvent pour lister les entiers premiers jusqu'à un certain entier $n$ est la méthode appelée _crible d'Érastothène_:

    * On énumere l'ensemble des entiers entre $2$ et $n$
    * Puis, on entoure le premier $2$ et on barre tous ses multiples c'est-à-dire tous les nombres pairs.
    * On entoure ensuite le prochain nombre non barré (en l'occurrence $3$) et on barre tous ses multiples
    * Ainsi si de suite, jusqu'à $\sqrt{n}$
    * On entoure finalement les nombres restant non barrés

    Les nombres entourés sont exactement les nombres premiers entre $1$ et $n$. 

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice"

    Montrer que $131$ est un nombre premier.

???- success "Solution"

    On a $\sqrt{131} < \sqrt{144} = 12$, donc on cherche les entiers entre $2$ et $11$ et plus précisement les entiers premiers entre $2$ et $11$, qui sont $2, 3, 5, 7, 11$.
    Aucun de ces entiers premiers ne divise $131$, ainsi $131$ est un entier premier.

## <span style="color:#0a69b7">Le théorème fondamental de l'arithmétique</span>

Le théorème fondamental est très utile en arithmétique. En effet, il permet de décomposer tout entier en produits de facteurs premiers.

### <span style="color:#0c87eb">Notions</span>

!!! info "Lemme divisibilité de produit par nombre premier"

    Si un nombre premier $p$ divise le produit $a_{1}, ..., a_{n}$, alors il divise l'un des $a_{i}$

La démonstration pourra être présentée plus tard.

!!! tip "Théorème - décomposition en facteurs premiers"

    Tout entier $n \geq 1$ se décompose d'une et d'une seule manière en un produit de nombres premiers. Autrement dit, pour tout entier $n \geq 1$, il existe des nombres premiers deux à deux distincts $p_{1}, ..., p_{k}$ et des entiers strictement positifs $\alpha_{1}, ..., \alpha_{k}$ uniquement déterminés à l'ordre près, tels que:

    $$n = p_{1}^{\alpha_{1}}p_{2}^{\alpha_{2}}...p_{k}^{\alpha_{k}}$$

!!! warning "Remarque"

    Le théorème reste vrai pour $n = 1$: il faut poser $k = 0$, le produit d'aucun entier étant par convention égal à $1$.

???- success "Démonstration"

    Commençons par l'existence de cette décomposition. Nous allons raisonner par récurrence sur $n$. 

    Pour $n = 2$, il s'écrit comme un produit de nombre premiers, $2$ étant lui-même premier.

    Soit $n \geq 3$. Supposons que pour tout entier strictement inférieur à $n$ s'écrive comme il est fait mention dans le théorème et montrons que la conclusion subsiste pour l'entier $n$.
    Il y a deux cas de figure: soit $n$ est premier, soit $n$ est un nombre composé.

    * Si $n$ est premier, alors $n$ s'écrit comme le produit de nombres premiers.
    * Si $n$ est composé, il existe $d$ et $d'$ tels que $2 \leq d < n$ et $2 \leq d' < n$. Les entiers $d$ et $d'$ relèvent de l'hypothèse de récurrence et on peut écrire:

    $$ d = p_{1}p_{2}...p_{k} $$

    $$ d' = p'_{1}p'_{2}...p'_{k} $$

    pour des nombres premiers $p_{i}$ et $p'_{i}$. À noter que cette dernière écriture suppose que les entiers $p_{1}, p_{2}, ..., p_{k}$ et $p'_{1}, p'_{2}, ..., p'_{k}$ ne sont pas tous distincts deux à deux entre eux. Ainsi,

    $$ n = p_{1}p_{2}...p_{k}p'_{1}p'_{2}...p'_{k'} $$

    Ce qui permet de prouver par récurrence l'existence de la décomposition du théorème.

    Passons désormais à l'unicité. Supposons que:

    $$ p_{1}p_{2}...p_{k} = p'_{1}p'_{2}...p'_{k} $$

    pour certains nombres premiers $p_{i}, \quad p'_{i}, \quad i=1, ..., k$ non tous distincts. 
    On souhaite montrer que $k=k'$ et que les $p_{i}$ sont égaux aux $p'_{i}$ à l'ordre près. Raisonnons par l'absurde et supposons que la décomposition n'est pas unique. Alors, nous considérons deux décompositions pour lesquelles $min(k,k')$ est minimale, elles existent puisque $k$ et $k'$ sont des entiers naturels (postifs).
    
    Ainsi, le nombre premier $p_{1}$ divise le produit $p'_{1}p'_{2}...p'_{k'}$, donc d'après le lemme divisibilité de produit par nombre premier, il divise $p'_{i}$ pour un certain entier $i$. Or, les diviseurs de $p'_{i}$ (qui est premier) ne sont que $1$ et $p'_{i}$. Comme $p_{1} \neq 1$, il ne reste plus que la possibilité $p_{1} = p'_{i} = p$. On peut alors simplifier l'égalité:

    $$ p_{1}p_{2}...p_{k} = p'_{1}p'_{2}...p'_{k} $$

    en divisant par p, on a:
    
    $$ p_{2}...p_{k} = p'_{1}...p'_{i-1}p_{i+1}...p'_{k'} $$

    puis en posant:

    $$ \forall l \in \{1, ..., k-1\}, \quad p"_{l} = p_{l+1} $$
    
    $$ \forall l \in \{1, ..., k'-1\}, \quad p^{(3)}_{l} = \left\{\begin{array}{ccc} p'_{l} & si & l \leq i-1\\
    p'_{l+1} & si & l \geq i+1 \quad et \quad l \leq k' \end{array}\right.$$

    Donc:

    $$ p"_{1}...p"_{k-1} = p^{(3)}_{1}...p^{(3)}_{k'-1} $$

    obtenant ainsi un contre-exemple avec $min(k-1, k'-1) = min(k, k') - 1$ plus petit. C'est contradictoire et l'unicité est donc prouvée.

!!! info "Proposition"

    Si la décomposition en facteurs premiers de l'entier $n \geq 1$ est $n = p_{1}^{\alpha_{1}}p_{2}^{\alpha_{2}}...p_{k}^{\alpha_{k}}$, alors les diviseurs positifs de $n$ sont les entiers de la forme $p_{1}^{\beta_{1}}p_{2}^{\beta_{2}}...p_{k}^{\beta_{k}}$, avec $0 \leq \beta_{i} \leq \alpha_{i}$ pour tout $1 \leq i \leq k$.

Cette proposition permet d'obtenir une expression du PGCD et du PPCM de deux entiers lorsqu'on connaît leur décomposition en facteurs premiers. Précisement, si:

$$ a = p_{1}^{\alpha_{1}}p_{2}^{\alpha_{2}}...p_{k}^{\alpha_{k}} $$

$$ b = p_{1}^{\beta_{1}}p_{2}^{\beta_{2}}...p_{k}^{\beta_{k}} $$

Où les $p_{i}$ sont à deux distincts, mais les $\alpha_{i}$ et $\beta_{i}$ sont éventuellement nuls, on a:

\[PGCD(a,b) = p_{1}^{min(\alpha_{1},\beta_{1})}p_{2}^{min(\alpha_{2},\beta_{2})}...p_{k}^{min(\alpha_{k},\beta_{k})}\]

\[PPCM(a,b) = p_{1}^{max(\alpha_{1},\beta_{1})}p_{2}^{max(\alpha_{2},\beta_{2})}...p_{k}^{max(\alpha_{k},\beta_{k})}\]

Si l'on remarque que pour $\alpha$ et $\beta$ des entiers (ou réels), on a toujours $min(\alpha, \beta) + max(\alpha, \beta) = \alpha + \beta$, on déduit directement des deux expressions précédentes la proposition suivante:

!!! info "Proposition"

    Si $a$ et $b$ sont des entiers positifs, on a l'égalité:

    $$ PGCD(a,b).PPCM(a,b) = ab $$

## <span style="color:#0a69b7">Infinité des nombres premiers et raffinements</span>

### <span style="color:#0c87eb">Notions</span>

!!! tip "Proposition"

    Il existe une infinité de nombres premiers.

???- success "Démonstration"

    On raisonne par l'absurde. On suppose qu'il n'existe qu'un nombre fini d'entiers premiers, disons $p_{1}, p_{2}, ..., p_{k}$. On peut alors exhiber un entier qui n'est divisible par aucun de ces nombres premiers, ce qui est contradictoire compte tenu du fait que cet entier possède un diviseur premier. En effet, considérons $N = p_{1}p_{2}...p_{k}+1$: si $p_{i} (1 \leq i \leq k)$ divisait $N$, alors $p_{i}$ diviserait $1$, ce qui est absurde.

Le contenu de cette démonstration permet de démontrer des résultats plus précis à propos de l'infinité des nombres premiers comme nous le verrons en exercice plus tard.

Sur la rarefaction des nombres premiers, la propriété suivante est utile.

!!! tip "Proposition"

    Il existe des suites arbitrairement longues de nombres consécutifs composés. Autrement dit, pour tout $k$, il est possible de trouver un entier $n$ tel que les nombres 
    
    $$n+1, ..., n+k$$

    soient tous composés.

???- success "Démonstration"

    Soit $k$ un entier, on pose $n = (k+1)! + 1.$. Alors, pour $i \in \{1, ..., n+k\}$, on a: 

    $$(i+1) \quad \textrm{divise} \quad n+i \quad \textrm{et} \quad 1 < i+1 < n + i$$

    Donc:

    $$n+1, ..., n+k$$

    sont tous composés.

!!! warning

    L'infinité des nombres premiers permet de définir de la proposition précédente, celle qui suit ci-dessous.

!!! tip "Proposition"

    Pour tout entier $k$, il existe un nombre premier $p$ tel que tous les nombres $p+1, ..., p+k$ soient composés.

???- success "Démonstration"

    Soit $k$ un entier naturel, une idée de démonstration consiste à supposer par absurde que pour tout nombre premier $p$, il existe $i \in \{1, ..., k\}$ tel que $p + i$ soit premier.

Mis à part ces résultats, la repartition des nombres premiers est une question qui a occupé les mathématiciens durant des générations, et plusieurs questions sont ouvertes. Citons ces résultats ci-dessous qu'il est important de connaître même si la démonstration dépasse le cadre de ce cours.

!!! tip "Propriétés"

    * _Postulat de Bertrand_: pour tout entier $n \geq 1$, il existe un nombre premier entre $n$ et $2n$.
    * _Théorème des nombres premiers_: Si on note $\pi(x)$ le nombre d'entiers premiers inférieurs ou égaux à $x$, on a l'estimation $\pi(x) \sim \frac{x}{ln x}$ (au sens où le quotient de deux nombres tend vers $1$ lorsque $x$ tend vers l'infini).
    * _Théorème de Dirichlet_: Si $a \neq 0$ et $b$ sont deux entiers naturels premiers entre eux, la suite $an + b$ ($n$ entier) contient une infinité de nombres premiers.

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice"

    Montrer qu'il existe une infinité de nombres premiers de la forme $4n+3$.

???- success "Solution"

    On raisonne par l'absurde en supposant qu'il n'existe qu'un nombre fini de nombres premiers de cette forme, notés $p_{1}, p_{2}, ..., p_{k}$. On considère alors $N = 4p_{1}p_{2}...p_{k} - 1$. Les diviseurs premiers de $N$ sont distincts de $2$ et des $p_{i}$ $(1 \leq i \leq k)$, et il en existe un qui est de la forme $4n+3$, car sinon on vérifie immédiatemment que $N$ ne pourrait être de la forme $4n + 3$ (un nombre premier qui n'est de la forme $4n + 3$ est de la forme $4n + 1$ et le produit de tels nombres est encore de cette forme).

!!! warning "Remarque"

    De même, on peut prouver qu'il existe une infinité de nombres premiers de la forme $6n+5$. Toutefois, ces cas restent anecdoctiques: par exemple, la démonstration précédente ne s'applique pas pour les nombres premiers de la forme $4n+1$ (qui pourtant forment bien un ensemble infini).

## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 06/03/2024.
* Naoki Sato, [Number Theory](https://artofproblemsolving.com/articles/files/SatoNT.pdf), consulté le 09/03/2024.
