---
comments: true
---

# <span style="color:#074b83">Troisième série d'exercices d'arithmétique</span>

## <span style="color:#074b83">Exercices</span>

!!! example "Exercice $51^{**}$"

    Soient $a$, $b$ et $c$ des entiers strictement positifs, premiers entre eux dans leur ensemble, et tels que:

    \[\frac{1}{a} + \frac{1}{b} = \frac{1}{c}\]

    Prouver que $a+b$ est un carré parfait.

???- success "Solution 51"

    Notons $d = PGCD(a,b)$ et soient $a'$ et $b'$ des entiers tels que $a=da'$ et $b=db'$. L'équation devient:

    \[c(a'+b') = da'b'\]

    d'où on déduit dans un premier temps que $c$ divise $da'b'$. Comme $a, b$ et $c$ sont premiers entre eux dans leur ensemble, $c$ est premier avec $d$ et donc par le lemme de Gauss $c$ divise $a'b'$.

    D'autre part, on déduit également que $a'$ divise $c(a'+b')$, mais comme $a'$ est premier avec $b'$, il est premier avec $a'+b'$ et donc $a'$ divise $c$. De même, on trouve que $b'$ divise $c$. Encore une fois parce que $a'$ et $b'$ sont premiers entre eux, cela implique $a'b'$ divise $c$.

    Les entiers $a'b'$ et $c$ sont positifs et se divisent mutuellement, donc $a'b'=c$ et $a'+b' = d$. En remultipliant par $d$, on trouve finalement $a + b = d^{2}$, ce qui conclut.

!!! example "Exercice $52^{**}$"

    Un nombre $n$ est dit _parfait_ si $\sigma(n) = 2n$ (où $\sigma$ désigne la somme des diviseurs positifs). Montrer que:

    * __a)__ (Euler) l'entier $n$ est parfait pair si et seulement s'il est de la forme $2^{k-1}(2^{k}-1)$ avec $2^{k}-1$ premier;
    * __b)__ (Sylvester) si $n$ est parfait impair, alors il possède au moins trois diviseurs premiers distincts.

???- success "Solution 52"

    __a)__ Supposons que $n$ soit de la forme $2^{k-1}(2^{k}-1)$ avec $2^{k}-1$ premier. On dispose de la décomposition en facteurs premiers de $n$ et donc de l'expression de $\sigma(n)$:

    \[\sigma(n) = \frac{2^{k}-1}{2-1}.\frac{(2^{k} - 1)^{2}-1}{(2^{k}-1)-1} = (2^{k}-1)(2^{k}-1+1) = 2n\]

    Les nombres de cette forme sont donc bien parfaits et pairs (car la condition $2^{k}-1$ premier implique $k \geq 2$).

    Réciproquement, supposons que $n$ soit un nombre parfait pair. Alors $n$ s'écrit $n = 2^{k-1}A$ pour un certain entier $k \geq 2$ et un certain entier positif $A$ impair. Par exemple, en décomposant $A$ en facteurs premiers, on arrive à $\sigma(n) = (2^{k} - 1)\sigma(A)$ ce qui contredit, puisque $n$ est supposé parfait, à:

    \[2^{k}A = (2^{k}-1)\sigma(A)\]

    Comme $2^{k}-1$ est impair (et donc premier avec $2^{k}$), le lemme de Gauss assure que $2^{k} - 1$ divise $A$ et donc que l'on peut écrire $A = a(2^{k}-1)$ pour un certain entier positif $a$. L'égalité du dessus assure $\sigma(A) = A + a$. Puisque $k \geq 2$, les entiers $A$ et $a$ sont distincts et tous deux diviseurs de $A$. Ainsi, comme $1$ est également diviseur de $A$, on doit avoir $a=1$ pour que l'égalité $\sigma(A) = A + a$ soit satisfaite. Cela implique $A = 2^{k}-1$ et $\sigma(A) = A + 1$ et donc $A$ premier. Finalement, $n$ s'écrit bien sous la forme annoncée.

    __b)__ Supposons que $n$ soit impair et ait au plus deux facteurs premiers. Alors on peut écrire $n=p^{a}q^{b}$ pour des nombres premiers impairs distincts $p < q$ et des entiers $a$ et $b$ positifs ou nuls. On a:

    \[\frac{\sigma(n)}{n} = \frac{p^{a+1}-1}{p^{a}(p-1)}\frac{q^{b+1}-1}{q^{b}(q-1)} < \frac{p^{a+1}}{p^{a}(p-1)}\frac{q^{b+1}}{q^{b}(q-1)} = \frac{p}{p-1}\frac{q}{q-1}\]

    D'autre part, on a forcément $p \geq 3$ et $q \geq 5$. Mais alors on obtient $\frac{\sigma(n)}{n} < \frac{3}{2} \times \frac{5}{4} < 2$ et donc $n$ ne peut pas être parfait.

!!! example "Exercice $53^{**}$ (TDV $99$)"

    Montrer que si $a$ et $b$ sont des entiers tels que $PPCM(a, a+5) = PPCM(b, b+5)$ alors $a=b$.

    Existe-t-il des entiers strictement positifs $a$, $b$ et $c$ tels que $PPCM(a,b) = PPCM(a+c, b+c)$ ?

???- success "Solution 53"

    __a)__ Notons $A = PGCD(a, a+5)$ et $B = PGCD(b, b+5)$. Ce sont des diviseurs de $5$, ils sont donc égaux soit à $1$, soit à $5$.
    Si $A = B$, en vertu de l'égalité $PPCM(x,y).PGCD(x,y) = xy$, l'équation devient $a(a+5) = b(b+5)$, ce qui implique $a = b$ puisque $a$ et $b$ sont positifs.
    Par symétrie, on peut supposer $A=1$ et $B=5$ pour le cas restant. Dans ce cas, $b$ est un multiple de $5$, disons $b=5b'$ et l'équation devient: $a(a+5) = b'(5b'+5) = 5b'(b'+1)$. On en déduit que $5$ divise $a$, ce qui contredit $A=1$.

    __b__) La réponse est non. Supposons, par l'absurde qu'il existe $a, b$ et $c$ solutions. Notons $m=PPCM(a,b) = PPCM(a+c, b+c)$. Soit $p$ un nombre premier diviseur commun de $a$ et $b$. Alors $p$ divise $m$ et donc $p$ divise $a+c$ ou $b+c$. Dans un cas, comme dans l'autre, il divise $c$. En posant $a' = \frac{a}{p}$, $b' = \frac{b}{p}$ et $c'=\frac{c}{p}$, on obtient un nouveau triplet solution. En itérant le procédé, on peut supposer que $a$ et $b$ sont premiers entre eux dès le commencement.

    Dans ces conditions, $m=ab$. Soit $p$ un diviseur premier de $a+c$ et $b+c$. Alors $p$ divise $m$, et donc il divise soit $a$, soit $b$. Il divise donc $c$ et donc $a$ et $b$. Cela est impossible car $a$ et $b$ sont premiers entre eux. Du coup, $a+c$ et $b+c$ sont également premiers entre eux et l'équation devient:

    \[ab = (a+b)(b+c)\]

    qui n'a manifestement pas de solution en entiers strictement positifs.

!!! example "Exercice $54^{**}$"

    Soient $a$, $b$ et $c$ des entiers strictement positifs tels que:

    \[\frac{a}{b} + \frac{b}{c} + \frac{c}{a}\]

    est entier. Montrer que $abc$ est un cube.

???- success "Solution 54"

!!! example "Exercice $55^{**}$"

    Soit $n$ un entier. On suppose que $n = ab = cd$ pour certains entiers positifs $a, b, c$ et $d$. Montrer que $a^{k} + b^{k} + c^{k} + d^{k}$ est un entier composé pour tout entier $k$ positif.

???- success "Solution 55"

!!! example "Exercice $56^{**}$ (OIM 94)"

    Trouver tous les couples $(m,n)$ d'entiers strictement positifs tels que:

    \[\frac{n^{3}+1}{mn-1}\]

    soit entier.

???- success "Solution 56"

!!! example "Exercice $57^{**}$ (SL 99)"

    Montrer que tout rationnel strictement positif peut s'écrire sous la forme:

    \[\frac{a^{3}+b^{3}}{c^{3}+d^{3}}\]

    pour certains entiers $a$, $b$, $c$ et $d$ strictements positifs.

???- success "Solution 57"

!!! example "Exercice $58^{**}$"

    Montrer que tout rationnel compris strictement entre $0$ et $1$ peut s'écrire sous la forme:

    \[\frac{1}{n_{1}} + ... + \frac{1}{n_{k}}\]

    pour certains entiers $n_{i}$ deux à deux distincts.

???- success "Solution 58"

!!! example "Exercice $59^{**}$ (Balkans 96)"

    Soit $p > 5$ un nombre premier. On définit:

    \[S = \{p - n^{2}, n \in \mathbb{N}, n^{2} < p\}\]

    Prouver qu'il existe $a$ et $b$ dans $S$ tels que $1 < a < b$ et $a$ divise $b$.

???- success "Solution 59"

!!! example "Exercice $60^{**}$ (OIM 87)"

    On considère le plan euclidien. Soit $n \geq 3$ un entier. Montrer qu'il existe $n$ points vérifiant:
    
    * (1) trois quelconques de ces points ne sont pas alignés
    * (2) la distance entre deux quelconques de ces points est irrationnelle
    * (3) l'aire du triangle déterminé par trois quelconques de ces points est rationnelle.

???- success "Solution 60"

!!! example "Exercice $61^{**}$ (APMO 98)"

    Trouver le plus grand entier $n$ qui soit divisible par tous les entiers inférieurs ou égaux à $\sqrt[3]{n}$.

???- success "Solution 61"

!!! example "Exercice $62^{**}$ (OIM 92)"

    Trouver tous les entiers $a, b, c$ vérifiant $1 < a < b < c$ et tels que $(a-1)(b-1)(c-1)$ divise $abc - 1$.

???- success "Solution 62"

!!! example "Exercice $63^{**}$ (Inde 98)"

    Soit $M$ un entier strictement positif. On note:

    \[S = \{n \in \mathbb{N}, M^{2} \leq n < (M+1)^{2}\}\]

    Montrer que les produits $ab$ pour $a$ et $b$ dans $S$ sont deux à deux distincts.

???- success "Solution 63"

!!! example "Exercice $64^{**}$"

    Pour tout entier $n > 0$, on pose:

    \[H_{n} = 1 + \frac{1}{2} + \frac{1}{3} + ... + \frac{1}{n}\]

    Montrer que $H_{n}$ est entier si, et seulement si $n = 1$. Déterminer les entiers $m$ et $n$ pour lesquels la différence $H_{m+n} - H_{m}$ est entière.

???- success "Solution 64"

!!! example "Exercice $65^{**}$"

    Soient $a < b \leq c < d$ des entiers tels que $ad = bc$ et $\sqrt{d} - \sqrt{a} \leq 1$. Prouver que $a$ est un carré.

???- success "Solution 65"

!!! example "Exercice $66^{**}$ (OIM 83)"

    Soient $a, b$ et $c$ des entiers strictement positifs et premiers entre eux deux à deux. Montrer que $2abc - ab - bc - ca$ est le plus grand entier qui ne peut pas s'écrire sous la forme $xbc + yca + zab$ avec $x, y, z$ entiers positifs ou nuls.

???- success "Solution 66"

!!! example "Exercice $67^{**}$ (Putnam 95)"

    Pour $\alpha$ un réel strictement positif, on note $S(\alpha) = \{[n\alpha], n \in \mathbb{N}^{*}\}$. Montrer que $\mathbb{N}^{*}$ ne peut pas s'écrire comme union disjointe de $S(\alpha)$, $S(\beta)$ et $S(\gamma)$ pour trois réels strictement positifs $\alpha, \beta$ et $\gamma$.

???- success "Solution 67"

!!! example "Exercice $68^{**}$"

    Montrer qu'il n'existe pas de partie $X \subset \mathbb{N}$ infinie telle que pour toute partie finie $I \subset X$, le nombre $\sum_{x \in I} x$ soit un carré parfait.

???- success "Solution 68"

!!! example "Exercice $69^{**}$ (CG 92)"

    Quel est le chiffre des unités du nombre suivant:

    \[\left[\frac{10^{1992}}{10^{83}+7}\right]\]

???- success "Solution 69"

!!! example "Exercice $70^{***}$ (Yakusk 00)"

    Prouver qu'il n'existe pas d'entiers $n > 0$ et $a_{1} < ... < a_{k}$ tels que:

    \[\frac{1}{a_{1}!} + ... + \frac{1}{a_{k}!} = \frac{1}{10^{n}}\]

???- success "Solution 70"

!!! example "Exercice $71^{***}$ (OIM 98)"

    Pour tout entier $n$ strictement positif, $d(n)$ désigne le nombre de diviseurs positifs de $n$ (y compris $1$ et $n$). Trouver tous les entiers strictement positifs $k$ pour lesquels il existe $n$ tel que:

    \[\frac{d(n^{2})}{d(n)} = k\]

???- success "Solution 71"

!!! example "Exercice $72^{***}$ (OIM 84)"

    Soient $a, b, c$ et $d$ des entiers positifs impairs vérifiant $a < b < c < d$, $ad=bc$ et $a + d = 2^{k}$, $b + c = 2^{m}$ pour deux entiers $k$ et $m$. Prouver que $a=1$.

???- success "Solution 72"

!!! example "Exercice $73$"

    Soit $n$ un entier naturel. Montrer que:

    \[\sum_{k=1}^{n} \tau(k) = \sum_{k=1}^{n}\left[\frac{n}{k}\right]\]

???- success "Solution 73"

!!! example "Exercice $74$"

    Soit $n$ un entier naturel. Montrer que

    \[\sum_{d|n} \tau^{3}(d) = \left(\sum_{d|n} \tau(d)\right)^{2}\]

???- success "Solution 74"

!!! example "Exercice $75$ (1984 IMO Short List)"

    Supposons que $a_{1}, a_{2}, ..., a_{2n}$ sont des entiers distincts tels que l'équation

    \[(x-a_{1})(x-a_{2})...(x-a_{2n}) - (-1)^{n}(n!)^{2} = 0\]

    a une solution entière $r$. Montrer que

    \[r = \frac{a_{1}+a_{2}+ ... + a_{2n}}{2n}\]

???- success "Solution 75"

## <span style="color:#074b83">Bibliographie</span>

* Pierre Bornsztein, Xavier Caruso, Pierre Nolin et Mehdi Tibouchi, [Cours d’arithmétique, première partie](http://igor-kortchemski.perso.math.cnrs.fr/olympiades/Cours/Arithmetique/arithm.pdf), Décembre 2004, consulté le 07/05/2024.
* Naoki Sato, [Number Theory](https://artofproblemsolving.com/articles/files/SatoNT.pdf), consulté le 07/05/2024.
