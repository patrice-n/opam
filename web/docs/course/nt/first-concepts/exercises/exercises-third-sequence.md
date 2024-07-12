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

    Soit $p$ un nombre premier fixé, et $\alpha$, $\beta$, $\gamma$ les valuations $p$-adiques de $a, b$ et $c$. On veut montrer que $\alpha + \beta + \gamma$ est un multiple de $3$. Pour cela, d'après l'hypothèse de l'énoncé, remarquons que:

    \[v_{p}\left(\frac{a}{b} + \frac{b}{c} + \frac{c}{a}\right) \geq 0\]

    et que l'on a la relation:

    \[(\alpha - \beta) + (\beta - \gamma) + (\gamma - \alpha) = 0\]

    Il en résulte que l'un au moins des trois entiers $\alpha - \beta$, $\beta - \gamma$, $\gamma - \alpha$ est négatif. Si aucun n'est strictement négatif, c'est que $\alpha = \beta = \gamma$ et $\alpha + \beta + \gamma$ est bien multiple de $3$. 
    
    Sinon, 
    supposons que le minimum des trois valeurs est atteint exactement une fois donc ce minimum est strictement négatif. Puisque les variables $a$, $b$ et $c$ ont des rôles symétriques, on peut supposer que ce minimum est égal à $\alpha - \beta$, et comme $\alpha - \beta$ est atteint exactement une seule fois, alors $v_{p}\left(\frac{a}{b}\right) \neq v_{p}\left(\frac{b}{c}\right)$ et donc:

    \[v_{p}\left(\frac{a}{b} + \frac{b}{c}\right) = min\left(v_{p}\left(\frac{a}{b}\right), v_{p}\left(\frac{b}{c}\right)\right) = min(\alpha-\beta, \beta-\gamma) = \alpha-\beta\]

    De même, $\alpha-\beta = v_{p}\left(\frac{a}{b} + \frac{b}{c}\right)$ est différent de $\gamma-\alpha = v_{p}\left(\frac{c}{a}\right)$, donc:

    \[v_{p}\left(\frac{a}{b} + \frac{b}{c} + \frac{c}{a}\right) = min\left(v_{p}\left(\frac{a}{b} + \frac{b}{c}\right), v_{p}\left(\frac{c}{a}\right)\right) = \alpha - \beta < 0\]
    
    Ce qui contredit le fait que:

    \[v_{p}\left(\frac{a}{b} + \frac{b}{c} + \frac{c}{a}\right) \geq 0\]

    Ainsi pour que la première relation soit satisfaite, le minimum des trois valeurs doit être atteint au moins deux fois. Par exemple, on a $\alpha - \beta = \beta - \gamma$, ce qui assure que $\alpha + \beta + \gamma = 3\beta$ est encore multiple de $3$.

!!! example "Exercice $55^{**}$"

    Soit $n$ un entier. On suppose que $n = ab = cd$ pour certains entiers positifs $a, b, c$ et $d$. Montrer que $a^{k} + b^{k} + c^{k} + d^{k}$ est un entier composé pour tout entier $k$ positif.

???- success "Solution 55"

    Montrons dans un premier temps qu'il existe des entiers $x$, $y$, $z$ et $t$ tels que $a=xy, b = zt$, $c=xz$ et $d=yt$. Définissons $x = PGCD(a,c)$, $y=\frac{a}{x}$, $z = \frac{c}{x}$ et $t = \frac{b}{z} = \frac{d}{y}$ comme on le vérifie immédiatement. Les quatres égalités voulues sont immédiates, et les nombres $x, y$ et $z$ sont manifestement des entiers. Le seul point qui n'est pas immédiat est de prouver que $t$ est entier. Pour cela, considérons $p$ un nombre premier. On a:

    \[v_{p}(t) = v_{p}(b) - v_{p}(z) = v_{p}(b) - v_{p}(c) + min(v_{p}(a), v_{p}(c))\]

    \[= v_{p}(d)-v_{p}(y) = v_{p}(d) - v_{p}(a) + min(v_{p}(a), v_{p}(c))\]

    Or $min(v_{p}(a), v_{p}(c))$ vaut soit $v_{p}(a)$ et alors la deuxième ligne prouve que $v_{p}(t) \geq 0$, soit $v_{p}(c)$ et c'est alors la première ligne qui permet de conclure.

    Forts de cette remarque, nous pouvons terminer l'exercice. On écrit simplement pour cela:

    \[a^{k} + b^{k} + c^{k} + d^{k} = x^{k}y^{k} + z^{k}t^{k} * x^{k}z^{k} + y^{k}t^{k} = (x^{k} + t^{k})(z^{k} + y^{k})\]

    et les deux facteurs précédents sont supérieurs ou égaux à $2$.

!!! example "Exercice $56^{**}$ (OIM 94)"

    Trouver tous les couples $(m,n)$ d'entiers strictement positifs tels que:

    \[\frac{n^{3}+1}{mn-1}\]

    soit entier.

???- success "Solution 56"

    Supposons que le couple $(m, n)$ soit solution. Alors le quotient $\frac{n^{3}+1}{mn-1}$ est entier, et donc il en est de même de:

    \[m^{3}\frac{n^{3}+1}{mn-1} = \frac{(mn)^{3}-1}{mn-1} + \frac{m^{3}+1}{mn-1}\]

    \[=(mn)^{2} + (mn) + 1 + \frac{m^{3}+1}{mn-1}\]

    On en déduit que $(n, m)$ est également solution. Les rôles des deux variables sont donc symétriques et on peut ne chercher que les solutions pour lesquelles $m \geq n$.
    Soit $K = \frac{n^{3}+1}{mn-1} \geq 1$. On a $n^{3}+1 = K(mn-1)$ et donc $n$ divise $K+1$, puis $K = nx-1$ pour un certain entier $x \geq 1$. Mais alors pour $n > 1$:

    \[nx - 1 = K \leq \frac{n^{3}+1}{n^{2}-1} = n + \frac{1}{n-1}\]

    Si de plus $n \geq 3$, il vient $n(x-1) < 2$ et donc $n(x-1) = 0$ (puisque c'est un multiple de $n$) puis $x=1$. L'équation devient:

    \[n-1 = \frac{n^{3}+1}{mn-1}\]

    d'où:

    \[m = n + 1 + \frac{2}{n-1}\]

    ce qui implique que $n-1$ divise $2$. Comme $n \geq 3$, la seule possibilité est $n-1 = 2$, soit $n=3$. Dans ce cas, $m=5$ donne une solution.

    Reste à regarder les cas $n=1$ et $n=2$. Pour $n=1$, on doit avoir $m-1$ divise $2$ et donc $m=2$ ou $m=3$. Pour $n=2$, il vient $2m-1$ divise $9$, puis $m=2$ et $m=5$ (car on suppose toujours $m \geq n =2$).

    Finalement, les solutions sont $(2,1), (3,1), (2,2), (5,2), (5,3), (1,2), (1,3), (2,5)$ et $(3,5)$.

!!! example "Exercice $57^{**}$ (SL 99)"

    Montrer que tout rationnel strictement positif peut s'écrire sous la forme:

    \[\frac{a^{3}+b^{3}}{c^{3}+d^{3}}\]

    pour certains entiers $a$, $b$, $c$ et $d$ strictements positifs.

???- success "Solution 57"

    Soit $r$ un nombre rationnel compris strictement entre $\frac{1}{2}$ et $2$. Posons $r = \frac{m}{n}$. On remarque alors que $a = 2m - n, b = m + n, c = 2n - m$ et $d = m + n$ sont des entiers strictement positifs qui conviennent. En effet, on a:

    \[\frac{a^{3}+b^{3}}{c^{3}+d^{3}} = \frac{(2m-n)^{3}+(m+n)^{3}}{(2n-m)^{3}+(m+n)^{3}}\]

    \[= \frac{8m^{3}-12m^{2}n+6mn^{2}-n^{3} + m^{3} + 3m^{2}n + 3mn^{2} + n^{3}}{8n^{3} - 12n^{2}m + 6nm^{2} - m^{3} + m^{3} + 3m^{2}n + 3mn^{2} + n^{3}}\]

    \[= \frac{9m^{3} - 9m^{2}n + 9mn^{2}}{9n^{3} - 9n^{2}m + 9nm^{2}} = \frac{9m(m^{2} - mn + n^{2})}{9n(n^{2} - nm + m^{2})} = \frac{m}{n} = r\]

    Pour le cas général, quitte à considérer l'inverse, on peut supposer $r \geq 1$. Il existe alors $n \geq 0$ tel que:

    \[\frac{1}{2}\left(\frac{3}{2}\right)^{3n} < r \leq \frac{1}{2}\left(\frac{3}{2}\right)^{3n+3}\]

    En effet, $n = \left[\frac{ln(2r)}{3ln(\frac{3}{2})}\right]$ convient. Ainsi, $r\left(\frac{2}{3}\right)^{3n}$ est un rationnel strictement compris entre $\frac{1}{2}$ et $2$. On utilise le résultat précédent:

    \[r\left(\frac{2}{3}\right)^{3n} = \frac{a^{3}+b^{3}}{c^{3}+d^{3}}\]

    pour certains entiers strictement positifs $a, b, c$ et $d$. On en déduit:

    \[r = \frac{(3^{n}a)^{3}+(3^{n}b)^{3}}{(2^{n}c)^{3}+(2^{n}d)^{3}}\]

    ce qui assure la conclusion.

!!! example "Exercice $58^{**}$"

    Montrer que tout rationnel compris strictement entre $0$ et $1$ peut s'écrire sous la forme:

    \[\frac{1}{n_{1}} + ... + \frac{1}{n_{k}}\]

    pour certains entiers $n_{i}$ deux à deux distincts.

???- success "Solution 58"

    Soit $r = \frac{p_{1}}{q_{1}}$ le rationnel que l'on veut écrire comme somme d'inverses d'entiers. On va voir que « l'algorithme glouton » consistant à soustraire à $r$ la plus grande fraction $1/n$ possible fournit bien une solution au problème, et se termine en au plus $p_{1}$ étapes.

    Plus précisément, construisons par récurrence les suites $(p_{k}), (q_{k})$ et $(n_{k})$ de la façon suivante: en supposant $p_{k} > 0$ et $q_{k}$ construits, on note $n_{k}$ le plus petit entier (nécessairement supérieur ou égal à $2$) tel que $1/n_{k} \leq p_{k}/q_{k}$, et $p_{k+1}$ et $q_{k+1}$ sont le numérateur et le dénominateur de la fraction:

    \[\frac{p_{k}}{q_{k}} - \frac{1}{n_{k}}\]

    écrite sous forme irréductible. En particulier, $p_{k+1}$ est un diviseur de $p_{k}n_{k}-q_{k}$. Or on a:

    \[\frac{1}{n_{k}} \leq \frac{p_{k}}{q_{k}} < \frac{1}{n_{k}-1}\]

    ce qui donne $0 \leq p_{k}n_{k} - q_{k} < p_{k}$. Il en résulte que $0 \leq p_{k+1} < p_{k}$, et la suite $(p_{k})$ est donc strictement décroissante, et atteint en particulier la valeur $0$ (car sinon l'algorithme continue).

    Lorsque $p_{k+1}=0$, la construction s'arrête, et l'on a:

    \[r = \frac{1}{n_{1}} + \frac{1}{n_{2}} + ... + \frac{1}{n_{k}}\]

    Reste à voir que les $n_{i}$ sont tous distincts. En fait, $n_{i+1} > n_{i}$. En effet, si l'on avait $n_{i+1} \leq n_{i}$, on aurait $\frac{2}{n_{i}} \leq \frac{p_{i}}{q_{i}}$ (car pour $i \geq 2$, si cela a un sens, on a: $\frac{p_{i}}{q_{i}} = r - \left(\frac{1}{n_{1}} + ... + \frac{1}{n_{i-1}}\right) \geq \frac{1}{n_{i}} + \frac{1}{n_{i+1}}$ et donc avec $n_{i+1} \leq n_{i}$, on a: $\frac{p_{i}}{q_{i}} \geq \frac{1}{n_{i}} + \frac{1}{n_{i+1}} \geq \frac{2}{n_{i}}$). Mais $\frac{1}{(n_{i}-1)} \leq \frac{2}{n_{i}}$, et donc $n_{i} - 1$ aurait dû être choisi à la place de $n_{i}$.

    _Remarque_.

    La décomposition précédente n'est pas unique par exemple grâce à l'égalité:

    \[\frac{1}{n} = \frac{1}{n+1} + \frac{1}{n(n+1)}\]

!!! example "Exercice $59^{**}$ (Balkans 96)"

    Soit $p > 5$ un nombre premier. On définit:

    \[S = \{p - n^{2}, n \in \mathbb{N}, n^{2} < p\}\]

    Prouver qu'il existe $a$ et $b$ dans $S$ tels que $1 < a < b$ et $a$ divise $b$.

???- success "Solution 59"

    Traitons d'abord le cas où $1 \in S$. Alors il existe un entier $n$ tel que $p = n^{2}+1$. Cela implique $n > 2$ et $n$ pair. On pose $a = p - (n-1)^{2} = 2n$ et $b = p - 1 = n^{2}$ qui conviennent.

    Maintenant si $1 \notin S$. Alors il existe $n > 2$ tel que:

    \[n^{2}+1 < p < (n+1)^{2} - 1 = n(n+2)\]

    En effet, en prenant le plus grand entier naturel $n$ tel que $n^{2}+1 < p$, on aura $p \leq (n+1)^{2}+1$. La dernière inégalité implique que $p = (n+1)^{2} + 1$ ou $p < (n+1)^{2}-1$ car $p$ est premier. Or $1 \notin S$, donc on ne peut avoir $p = (n+1)^{2} + 1$, ainsi pour ce $n$, on a bien $n^{2} + 1 < p < (n+1)^{2} - 1 = n(n+2)$. On pose $a = p-n^{2} \in S$. On a $a - n = p - n(n+1)$ qui est non nul puisque $p$ est premier et $a$ est strictement inférieur à $n$ en valeur absolue du fait de l'inégalité ci-dessus. On pose $b = p - (a-n)^{2} \in S$. On vérifie que $b = a(1 + 2n - a)$. On a $a < 2n$ et donc $1 + 2n - a > 1$ puis $a < b$. Le couple $(a,b)$ convient.

!!! example "Exercice $60^{**}$ (OIM 87)"

    On considère le plan euclidien. Soit $n \geq 3$ un entier. Montrer qu'il existe $n$ points vérifiant:
    
    * (1) trois quelconques de ces points ne sont pas alignés
    * (2) la distance entre deux quelconques de ces points est irrationnelle
    * (3) l'aire du triangle déterminé par trois quelconques de ces points est rationnelle.

???- success "Solution 60"

    Pour $n \geq 0$, on considère le point $A_{n}$ de coordonnées $(n, n^{2})$. La distance entre $A_{n}$ et $A_{m}$ est donnée par la formule:

    \[\sqrt{(n-m)^{2} + (n^{2} - m^{2})^{2}} = |n-m|\sqrt{(n+m)^{2}+1}\]

    Si $n \neq m$, on a $|n-m| \neq 0$, et $n + m \geq 1$ ce qui implique que $(n+m)^{2}+1$ ne peut pas être un carré. La racine carrée écrite précédemment n'est pas un entier, c'est donc forcément un nombre irrationnel: en effet, s'il existe $x \in \mathbb{Q}$ tel que $x^{2}=n$ pour un certain entier $n$ fixé, on a $2v_{p}(x)=v_{p}(n) \geq 0$ pour tout nombre premier $p$ et donc $x$ est entier.

    Il reste à voir que si $n, m$ et $p$ sont trois entiers distincts, alors l'aire du triangle dont les sommets sont $A_{n}$, $A_{m}$ et $A_{p}$ est rationnelle et non nulle. L'aire d'un tel triangle se calcule via:

    \[\frac{1}{2}det\left(overline{A_{n}A_{m}}, \overline{A_{n}A_{p}}\right) = \frac{1}{2}[(m^{2}-n^{2})(p-n)-(p^{2}-n^{2})(p-n)]\]

    \[=\frac{1}{2}(m-n)(p-n)(m-p)\]

    qui est bien non nul et rationnel.

!!! example "Exercice $61^{**}$ (APMO 98)"

    Trouver le plus grand entier $n$ qui soit divisible par tous les entiers inférieurs ou égaux à $\sqrt[3]{n}$.

???- success "Solution 61"

    Soit $n$ un entier. Notons $m = [\sqrt[3]{n}]$. Dire que $n$ est divisible par tous les entiers inférieurs à $\sqrt[3]{n}$ revient à dire que $n$ est divisible par $PPCM(1,2,...,m)$.

    Deux nombres consécutifs sont forcément premiers entre eux. Ainsi le $PPCM(m,m-1) = m(m-1)$ et $PPCM(m-2,m-3)=(m-2)(m-3)$. Un nombre premier $p \geq 5$ ne peut diviser chacun de ces deux produits. Il en est de même de $4$ et de $9$. Ainsi le $PGCD$ de $m(m-1)$ et de $(m-2)(m-3)$ est un diviseur de $6$. On en déduit que:

    \[PPCM(m, m-1, m-2, m-3) = PPCM(m(m-1), (m-2)(m-3))\]

    est un multiple de:

    \[\frac{m(m-1)(m-2)(m-3)}{6}\]

    Ainsi $n$ doit également en être un, et on obtient une inégalité:

    \[(m+1)^{3} \geq n \geq \frac{m(m-1)(m-2)(m-3)}{6}\]

    que l'on peut réécrire:

    \[m \leq 6\left(1 + \frac{2}{m-1}\right)\left(1 + \frac{3}{m-2}\right)\left(1 + \frac{4}{m-3}\right)\]

    ce qui n'est plus vérifié pour $m \geq 13$. En effet, en faisant l'étude de la fonction

    \[f(x) = 6\left(1 + \frac{2}{x-1}\right)\left(1 + \frac{3}{x-2}\right)\left(1 + \frac{4}{x-3}\right) - x\]

    on prouve que cette fonction est strictement décroissante et négative en $x = 13$. Nous avons donc un nombre fini de vérification à faire.

    Même si cela a été montrer, en réalité $m$ ne peut valoir $13$: on calculte $PGCD(1, ..., 13) = 360 360$

!!! example "Exercice $62^{**}$ (OIM 92)"

    Trouver tous les entiers $a, b, c$ vérifiant $1 < a < b < c$ et tels que $(a-1)(b-1)(c-1)$ divise $abc - 1$.

???- success "Solution 62"

    Tout d'abord, il est clair que le quotient:

    \[q = \frac{abc-1}{(a-1)(b-1)(c-1)}\]

    ne peut valoir $1$. Comme c'est un entier, il est au moins égal à $2$.

    Remarquons ensuite que pour tout réel $x \geq 5$, on a $x - 1 \geq \frac{x}{\sqrt[3]{2}}$ (l'on peut élever chaque membre de l'inégalité au cube). Ainsi pour $a \geq 5$, on a:

    \[2(a-1)(b-1)(c-1) \geq abc > abc - 1\]

    et donc $abc-1$ ne peut être divisible par $(a-1)(b-1)(c-1)$. On a donc prouvé que $2 \leq a \leq 4$.

    Supposons $q = 2$. Alors $abc$ est impair et d'après ce qui précède, $a$ qui doit être impair ne peut valoir que $3$. L'équation se réécrit $4(b-1)(c-1)=3bc-1$, soit $bc + 5 = 4b + 4c$, qui se réecrit $(b-4)(c-4)=11$ qui conduit directement à la solution $b-4 = 1$, $c-4=11$, soit $b=5$ et $c=15$.

    Supposons maintenant $q \geq 3$. 
    
    Si $a = 2$, il vient $q(bc - b - c + 1) = 2bc - 1$, soit $(q-2)bc + (q+1) = qb + qc$ qui se factorise en:

    \[[(q-2)b-q][(q-2)c-q] = q + 2\]

    On a $b \geq 3$, et si $c \geq 4$, on a $(q-2)b-q \geq 2q-6$ et $(q-2)c-q \geq 3q - 8$. Ainsi le produit $[(q-2)b-q][(q-2)c-q] \geq (2q-6)(3q-8)$ et ce dernier minorant est strictement supérieur à $q+2$ dès que $q \geq 4$. Il ne reste plus que la possibilité $q=3$. Dans ce cas, il vient $(b-3)(c-3)=5$ qui conduit à $b=4$ et $c=8$.

    Si $a=3$, on a $2q(bc-b-c+1) = 3bc - 1$, soit $(2q-3)bc + (2q+1) = 2qb + 2qc$. Comme $b \geq 4$, on a $(2q-3)bc \geq (8q - 12)c \geq 4qc > 2qc + 2qb$, il n'y a pas de solution.

    Si $a=4$, on écrit $(3q-4)bc + (3q+1) = 3qb + 3qc$. Mais $b \geq 4$, et donc $(3q-4)bc \geq (12q-16)c > 6qc > 3qb + 3qc$, et il n'y a pas non plus de solution.

    En conclusion, les seules solutions sont $a=2$, $b=4$, $c=8$ et $a=3$, $b=5$, $c=15$.

!!! example "Exercice $63^{**}$ (Inde 98)"

    Soit $M$ un entier strictement positif. On note:

    \[S = \{n \in \mathbb{N}, M^{2} \leq n < (M+1)^{2}\}\]

    Montrer que les produits $ab$ pour $a$ et $b$ dans $S$ sont deux à deux distincts.

???- success "Solution 63"

    Soit $A = M^{2} + M$, et $a$, $b$, $c$, $d$ quatre éléments de $S$ tels que $ab=cd$. On pose $a=A+x$, $b=A+y$, $c=A+z$ et $d=A+t$ de sorte que $x$, $y$, $z$ et $t$ sont en valeur absole inférieurs ou égaux à $M$. L'égalité imposée s'écrit alors:

    \[(x+y)A + xy = (z+t)A + zt\]

    Si l'on a $x+y = z +t$, il vient $xy = zt$ et donc les paires $\{x, y\}$ et $\{z,t\}$ sont égales, et c'est terminé. Sinon, on écrit:

    \[2M^{2} \geq |xy - zt| = |(x+y)-(z+t)|.|A| > |(x+y)-(z+t)|.M^{2}\]

    ce qui impose que les sommes $x+y$ et $z+t$ diffèrent de $1$ exactement, par exemple $x+y = z+t+1$, et par suite $xy = zt - A$. Alors $x$ et $y$ sont racines du trinôme:

    \[X^{2} - (z+t+1)X + (zt-A)\]

    Les racines sont:

    \[\frac{z+t+1\pm\sqrt{\Delta}}{2}\]``

    avec:

    \[\Delta = (z+t+1)^{2} - 4zt + 4A = (z - t + 1)^{2} + 4A + 4t = (z - t + 1)^{2} + 4d \geq 4M^{2}\]

    En fait, il ne peut avoir égalité sinon $d = M^{2}$ et $z-t+1=0$, ce qui implique $t=-M$ et $z=-M-1$, ce qui est absurde. Ainsi $\Delta > 4M^{2}$.

    Donc si $z+t+1 \geq 0$, la racine correspondant à $+\sqrt{\Delta}$ est strictement supérieure à $M$, et si $z+t+1 \leq 0$, la racine correspondant à $-\sqrt{\Delta}$ est strictement inférieure à $-M$. Dans tous les cas, on obtient que $x$ ou $y$ dépasse $M$ en valeur absolue, ce qui est absurde. D'où le résultat.

!!! example "Exercice $64^{**}$"

    Pour tout entier $n > 0$, on pose:

    \[H_{n} = 1 + \frac{1}{2} + \frac{1}{3} + ... + \frac{1}{n}\]

    Montrer que $H_{n}$ est entier si, et seulement si $n = 1$. Déterminer les entiers $m$ et $n$ pour lesquels la différence $H_{m+n} - H_{m}$ est entière.

???- success "Solution 64"

    Soit $r$ le plus grand entier naturel tel que $2^{r} \leq n$. Alors pour tout $k$ compris entre $1$ et $n$, $v_{2}(k) \leq r$. On en déduit que:

    \[v_{2}(H_{n}) = v_{2}\left(1 + \frac{1}{2} + ... + \frac{1}{n}\right) = -r\]

    et donc $H_{n}$ n'est pas entier si $r \geq 1$, ce qui se produit dès que $n \geq 2$.

    L'entier $m \geq 1$ étant fixé, notons d'autre part $u_{n} = H_{m+n} - H_{m}$. Notons $a_{n} = v_{2}(u_{n})$. Nous allons montrer par récurrence que l'on a:

    \[a_{n} = - max_{1 \leq k \leq n} v_{2}(m+k)\]

    C'est vrai pour $a_{1}=v_{2}(\frac{1}{m+1})$. Supposons alors le résultat au rang $n$. Soit $v=v_{2}(m+n+1)$.

    Si $v \neq -a_{n}$, on a $a_{n+1} = inf(a_{n}, -v)$ et le résultat s'ensuit. Sinon, cela signifierait qu'il existe un entier $k$ compris entre $m+1$ et $m+n$ et de valuation $v$. Mais alors $2^{v}$ divise $k$ et $m + n + 1$, et donc $m+n+1 \geq k + 2^{v}$. Mais $v_{2}(k+2^{v}) \geq v + 1$ (car $k$ est de la forme $2^{v}(2k'+1)$), ce qui contredit le fait que $a_{n}=-v$.

    Finalement, on a montré que la différence $H_{m+n}-H_{m}$ n'était entière que pour $m=0$ et $n=1$.

!!! example "Exercice $65^{**}$"

    Soient $a < b \leq c < d$ des entiers tels que $ad = bc$ et $\sqrt{d} - \sqrt{a} \leq 1$. Prouver que $a$ est un carré.

???- success "Solution 65"

    On a $d - a > c-b$ d'où en élevant au carré $a^{2}-2ad+d^{2} > c^{2}-2bc+b^{2}$. En ajoutant $4ad = 4bc$ des deux côtes de l'inégalité, on obtient $(a+d)^{2} > (b+c)^{2}$, soit encore:

    \[a+d \geq b + c + 1\]

    Si $\sqrt{d} - \sqrt{a} < 1$, on obtiendrait:

    \[a + d < 1 + 2\sqrt{ad} = 1 + 2\sqrt{bc} \leq 1 + b + c \leq a + d\]

    ce qui est absurde. On a donc forcément $\sqrt{d} - \sqrt{a} = 1$. On a alors:

    \[a + d = 1 + 2\sqrt{ad} = 1 + \sqrt{bc} \leq 1 + b + c \leq a + d\]

    et donc toutes les inégalités précédentes sont des égalités. Ainsi $b = c$ et donc $ad=b^{2}$. Notons $p$ un diviseur premier commun à $a$ et à $d$. Forcément $p$ divise $b$ et $p$ divise $a+d = 2b + 1$, ce qui est impossible. Ainsi $a$ et $d$ sont premiers entre eux. Comme leur produit est un carré, $a$ est également un carré.

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
