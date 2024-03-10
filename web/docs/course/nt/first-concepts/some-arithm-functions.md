---
comments: true
---

# <span style="color:#074b83"> Quelques fonctions arithmétiques </span>

Nous comprenons par fonctions arithmétiques, les fonctions qui permettent d'effectuer des opérations arithmétiques.

## <span style="color:#0a69b7">Définitions et exemples</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Les principales fonctions arithmétiques sont les suivantes:

    * La fonction $d$ qui à $n$ associe le nombre de diviseurs positifs de $n$;

    * La fonction $\sigma$ qui à $n$ associe la somme des diviseurs positifs de $n$;

    * plus généralement, la fonction $\sigma_{s}$ qui à $n$ associe les sommes des diviseurs positifs de $n$ élévés à la puissance $s$ (les deux cas précédents correspondent à $s=0$ et $s=1$);

    * la fonction $P$ qui à $n$ associe le produit des diviseurs positifs de $n$

!!! warning "Remarque"

    Les notations introduites précédemment sont traditionnelles mais ne sont pas universelles. Elles seront normalement reprécisées à chaque nouvelle apparition (ou utilisation). De même, si nous sommes amenés à utiliser ces fonctions, il est souhaitable de redonner rapidement la définition avant pour fixer les notations.

En utilisant la décomposition en facteurs premiers des entiers naturels, les fonctions arithmétiques ont les expressions suivantes:

!!! tip "Proposition"

    Si la décomposition en facteurs premiers de $n$ est $n = p_{1}^{\alpha_{1}}...p_{k}^{\alpha_{k}}$, alors on a les expressions suivantes:

    $$ d(n) = (\alpha_{1}+1)(\alpha_{2}+1)...(\alpha_{k}+1) $$

    $$ \sigma_{s}(n) = \frac{p_{1}^{s(\alpha_{1}+1)}-1}{p_{1}^{s}-1}.\frac{p_{2}^{s(\alpha_{2}+1)}-1}{p_{2}^{s}-1}...\frac{p_{k}^{s(\alpha_{k}+1)}-1}{p_{k}^{s}-1}$$

    $$ P(n) = n^{\frac{d(n)}{2}}$$

!!! success "Démonstration"

    On ne démontre que l'expression de $P$ qui est la plus difficile, les autres se traitant de façon analogue.

    Un diviseur positif de $n$ s'écrit $p_{1}^{\beta_{1}}...p_{k}^{\beta_{k}}$ où $0 \leq \beta_{i} \leq \alpha_{i}$. Le produit de tous ces nombres est de la forme:

    $$ p_{1}^{\gamma_{1}}...p_{k}^{\gamma_{k}}$$

    Il suffit donc de calculer les exposants $\gamma_{i}$. Fixons un entier $v \in \{0, 1, ..., \alpha_{1}\}$. Il y a exactement $(\alpha_{2}+1)...(\alpha_{k}+1)$ diviseurs de $n$ pour lesquels $\beta_{1} = v$. Lorsque l'on multiplie tous ces diviseurs, on aura donc:

    $$\gamma_{1} = (\alpha_{2}+1)...(\alpha_{k}+1)\sum_{v=0}^{\alpha_{1}}v = \frac{1}{2}\alpha_{1}(\alpha_{1}+1)...(\alpha_{k}+1) = \alpha_{1}.\frac{d(n)}{2}$$

    On a de même pour les autres $i \in \{1,...,k\}$, $\gamma_{i} = \alpha_{i}.\frac{d(n)}{2}$

    Ainsi:

    $$ P(n) = p_{1}^{\gamma_{1}}...p_{k}^{\gamma_{k}} = p_{1}^{\alpha{1}.\frac{d(n)}{2}}...p_{k}^{\alpha_{k}.\frac{d(n)}{2}}$$

    $$ P(n) = (p_{1}^{\alpha_{1}}...p_{k}^{\alpha_{k}})^{\frac{d(n)}{2}} $$

    $$ P(n) = n^{\frac{d(n)}{2}} $$

    Pour calculer $\sigma_{s}(n)$, on peut écrire que:

    $$\sigma_{s} = \sum_{0 \leq \beta_{1} \leq \alpha_{1}, ..., 0 \leq \beta_{k} \leq \alpha_{k}} p_{1}^{s\beta_{1}}...p_{k}^{s\beta_{k}}$$

    $$\sigma_{s} = (1 + ... + p_{1}^{s\alpha_{1}})...(1 + ... + p_{k}^{s\alpha_{k}})$$

    $$\sigma_{s} = \frac{p_{1}^{s(\alpha_{1}+1)}-1}{p_{1}^{s}-1}...\frac{p_{k}^{s(\alpha_{k}+1)}-1}{p_{k}^{s}-1}$$

    La démonstration de l'expression de $d(n)$ est un peu rapide, vu que le nombre de diviseurs positifs de $n$ peut s'obtenir en faisant varier pour tout $i$, $\beta_{i}$ de $0$ à $\alpha_{i}$, d'où:

    $$ d(n) = (\alpha_{1}+1)...(\alpha_{k}+1) $$

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice 1"

    L'entier $n > 0$ étant fixé, déterminer le nombre de couples $(x,y)$ d'entiers strictement positifs vérifiant 
    
    $$ \frac{1}{x} + \frac{1}{y} = \frac{1}{n} $$

!!! success "Solution 1"

    L'équation se réécrit sous la forme:

    $$(x-n)(y-n) = n^{2}$$

    Il y a donc autant de solutions que de diviseurs positifs de $n^{2}$ en remarquant que puisque $\frac{1}{x} + \frac{1}{y} = \frac{1}{n}$, on a forcément $x > n$ et $y > n$.

    Le nombre de solution est donc $d(n^{2})$.

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 10/03/2024.
