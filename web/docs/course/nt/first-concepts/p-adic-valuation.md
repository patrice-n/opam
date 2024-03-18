---
comments: true
---

# <span style="color:#074b83"> Valuation p-adique </span>

Avec la décomposition en nombre premiers, les valuations sont un moyen d'utiliser toute la puissance de ce théorème.

## <span style="color:#0a69b7">Définitions et exemples</span>

### <span style="color:#0c87eb">Notions</span>

!!! note "Définition"

    Si $p$ est un nombre premier, et $n$ un entier non nul, la _valuation p-adique_ de $n$ est le plus grand entier $k$ tel que $p^{k}$ divise $n$. On la note $v_{p}(n)$.
    Si $n=0$, on convient que $v_{p}(0) = +\infty$ pour tout nombre premier $p$.

!!! tip "Propriétes"

    * Si $n$ non nul se décompose sous la forme $n = p_{1}^{\alpha_{1}}p_{2}^{\alpha_{2}}...p_{k}^{\alpha_{k}}$, alors $v_{p_{i}}(n) = \alpha_{i}$ pour tout $1 \leq i \leq k$, et $v_{p}(n) = 0$ si $p$ est distinct des $p_{i}$. Ainsi, $v_{p}(n) = 0$ sauf pour un nombre fini de nombres $p$ premiers.

    * Si $m$ et $n$ sont deux entiers, $m$ divise $n$ si et seulement si $v_{p}(m) \leq v_{p}(n)$ pour tout nombre premier p.

    * Si $a$ et $b$ sont des entiers non nuls, on a:

        \[v_{p}(PGCD(a,b)) = min(v_{p}(a), v_{p}(b))\]

        \[v_{p}(PPCM(a,b)) = max(v_{p}(a), v_{p}(b))\]

    * Si $m$ et $n$ sont deux entiers, on a, pour tout nombre premier $p$:

        \[v_{p}(ab) = v_{p}(a) + v_{p}(b)\]

        \[v_{p}(a+b) \geq min(v_{p}(a), v_{p}(b))\]

    et la dernière inégalité est une égalité dès que $v_{p}(a) \neq v_{p}(b)$

Ci-dessous, la formule dite de Légendre qui permet de déterminer la valuation $p$-adiques d'une factorielle. On rappelle que

$$ n! = 1 \times 2 \times ... \times n $$

!!! tip "Proposition (Formule de Légendre)"

    Si $p$ est un nombre premier et $n$ est un entier positif, on a:

    $$v_{p}(n!) = \sum_{i=1}^{\infty} \left[\frac{n}{p}\right] = \left[\frac{n}{p}\right] + \left[\frac{n}{p^{2}}\right] + ...$$

!!! warning "Remarque"

    Lorsque $p^{i} > n$, le nombre $\left[\frac{n}{p^{i}}\right] = 0$. Ceci assure qu'il n'y a bien qu'un nombre fini de termes non nuls dans la somme précédente.

???- success "Démonstration"

    Pour un entier positif ou nul $i$, appelons $n_{i}$ le nombre d'entiers compris entre $1$ et $n$ dont la valuation $p$-adique est _exactement_ $i$. On a alors:

    $$v_{p}(n!) = n_{1} + 2n_{2} + 3n_{3} + ...$$

    D'autre part, les entiers dont la valuation excède $i$ sont exactement les multiples de $p^{i}$ et sont au nombre de $\left[\frac{n}{p^{i}}\right]$ entre $1$ et $n$. D'où:

    $$\left[\frac{n}{p^{i}}\right] = n_{i} + n_{i+1} + n_{i+2} ...$$

    En mettant ensemble ces deux formules, on obtient

    $$v_{p}(n!) = \left[\frac{n}{p}\right] + \left[\frac{n}{p^{2}}\right] + ...$$

### <span style="color:#0c87eb">Exercices</span>

!!! question "Exercice"

    Par combien de zéros se termine le nombre $2004!$ ?

???- success "Solution"

    Comme l'entier $10$ n'est pas un nombre premier, on ne peut pas directement appliquer la formule de Legendre. En décomposant $10$ en facteurs premiers, on se rend compte que le plus grand exposant $n$ tel que $10^{n}$ divise $2004!$ est le plus petit des deux nombres $v_{2}(2004!)$ et $v_{5}(2004!)$. En effet, il sera le plus grand exposant $n$ tel que $2^{n}$ divise $2004!$ et $5^{n}$ divise $2004!$. La formule de Legendre prouve directement que c'est $v_{5}(2004!)$. Il vaut:

    $$v_{5}(2004!) = \left[\frac{2004}{5}\right] + \left[\frac{2004}{25}\right] + \left[\frac{2004}{125}\right] + \left[\frac{2004}{625}\right] + \left[\frac{2004}{3125}\right] + ... $$

    \[v_{5}(2004!) = 400 + 80 + 16 + 3 + 0 + ... = 499\]

    Le nombre $2004!$ se termine donc par $499$ zéros.

## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 09/03/2024.
