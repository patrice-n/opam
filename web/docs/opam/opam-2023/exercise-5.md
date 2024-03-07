---
comments: true
---

# <span style="color:#074b83"> Exercice 5 - OPAM 2023 (Arithmétique) </span>

## <span style="color:#0a69b7">L'énoncé (fourni par [KouakouSchool](https://www.youtube.com/@kouakouschool))</span>

!!! question "Énoncé de l'exercice"

    Soient $a$ et $b$ des nombres réels avec $a \neq 0$. Soit:

    $$
    \begin{equation}
    P(x) = ax^4 - 4ax^3 + (5a + b)x^2 - 4bx + b
    \label{equation-pb-5}
    \end{equation}
    $$
    
    Montrer que toutes les racines de $P(x)$ sont réelles et strictement positives si et seulement si $a=b$.

## <span style="color:#0a69b7">Solutions</span>

### <span style="color:#0c87eb">Solution - Utilisation de tableau de variation</span>

__Montrons que si $a$ est négatif cela revient au même que de supposer que $a$ est positif.__

En effet, si $a$ est négatif, posons $a' = -a$ et $b' = -b$, on a: $a'$ est positif, alors d'après l'équation de l'énoncé de l'exercice:

\[P(x) = -a'x^4 + 4a'x^3 - (5a' + b')x^2 + 4b'x - b' \]

\[P(x) = -(a'x^4 - 4a'x^3 + (5a' + b')x^2 - 4b'x + b')\]

Les racines de $P(x)$ sont les mêmes que les racines de $-P(x)$. Aussi, l'expression du polynôme $P$ en fonction de $a$ et $b$ est la même que l'expression du polynôme $-P$ en fonction de $a'$ et $b'$. D'où, l'assertion.

_les racines du polynôme $P(x)$ sont réelles et strictement positives si et seulement si $a = b$_ $\Longleftrightarrow$ _les racines du polynôme $P(x)$ sont réelles et strictement positives si et seulement si $a' = b'$_

Puisque $a \neq 0$, nous pouvons donc montrer l'équivalence:

Les racines du polynôme $P(x)$ sont réelles et strictement positives si et seulement si $a=b$ avec la condition $a > 0$.

__Montrons que les racines du polynôme $P(x)$ sont réelles strictement positives alors $a=b$.__

Soient $a$ et $b$ des nombres réels avec $a \neq 0$. Supposons que les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives.

_Montrons que $a$ et $b$ ont le même signe._

D'après l'hypothèse, nous pouvons écrire le polynôme $P(x)$ sous la forme:

\[P(x) = a(x-\alpha)(x-\beta)(x-\gamma)(x-\mu), \quad \textrm{avec} \quad \alpha, \beta, \gamma, \mu \in \mathbb{R}^{*}_{+}\]

Donc:

\[P(x) = a[x^4 - (\alpha + \beta + \gamma + \mu)x^3 + (\alpha\beta + (\alpha + \beta)(\gamma + \mu) + \gamma\mu)x^2 - ((\alpha + \beta)\mu\gamma + (\gamma + \mu)\alpha\beta)x + \alpha\beta\gamma\mu]\]

D'où, en utilisant l'équation de l'énoncé de l'exercice, nous obtenons:

!!! abstract "Équation relation racines coefficients"

    $$
    \begin{equation}
    \left\{
        \begin{array}{l}
        \frac{b}{a} = \alpha\beta\gamma\mu\\
        4\frac{b}{a} = (\alpha + \beta)\mu\gamma + (\gamma + \mu)\alpha\beta\\
        5+\frac{b}{a} = \alpha\beta + (\alpha + \beta)(\gamma + \mu) + \gamma\mu\\
        4 = \alpha + \beta + \gamma + \mu
        \end{array}
    \right.
    \label{equation-rel-racines-coef}
    \end{equation}
    $$

Puisque $\alpha > 0$, $\beta > 0$, $\gamma > 0$ et $\mu > 0$ alors:

\[\alpha\beta\gamma\mu > 0 \implies \quad \textrm{d'après la première ligne de la relation racines coefficients, on obtient:}  \quad \frac{b}{a} > 0\]

Ainsi, $a$ et $b$ ont le même signe.

La dérivée première et la dérivée seconde du polynôme $P$ sont données par les relations:

$$\begin{equation}
P'(x) = 2[2ax^3 - 6ax^2+(5a+b)x-2b]
\label{equation-pb-5-pderpre}
\end{equation}$$

$$\begin{equation}
P"(x) = 12a\left[(x-1)^2 - \frac{a-b}{6a}\right]
\label{equation-pb-5-pdersec}
\end{equation}$$

Supposons que $a \neq b$, alors il y a deux possibilités:

\[a > b \quad \textrm{ou} \quad a < b\]

_Possibilité 1 - supposons que $a > b$ avec $a > 0$._

Comme $a$ et $b$ ont le même signe d'après la démonstration précédente, alors $a > 0$, $b > 0$ et $a > b$. Ainsi le polynôme $P"$ admet des racines réelles qui sont:

\[r_{1} = 1 - r \quad \textrm{,} \quad r_{2} = 1 + r \quad \textrm{avec} \quad r = \sqrt{\frac{a-b}{6a}}\]

\[P"(r_{1}) = 0 \quad \textrm{et} \quad P"(r_{2}) = 0\]

\[P'(1 + r) =  2[2a(1+ r)^3 - 6a(1+ r)^2+(5a+b)(1+ r)-2b] \]

\[P'(1 + r) = 2[2ar^3 + (b-a)r + (a-b)]\]

\[\textrm{Or,} \quad r^2 = \frac{a-b}{6a} \implies P'(1+ r) = 2(a-b)\frac{3 - 2r}{3}\]

De même, en remplaçant $r$ par $-r$, on a:

\[P'(1- r) = 2(a-b)\frac{3 + 2r}{3}\]

Donc:

\[P'(r_{1}) = 2(a-b)\frac{3 + 2r}{3} \quad \textrm{et} \quad P'(r_{2}) = 2(a-b)\frac{3 - 2r}{3}\]

De plus,

\[0 < r^2 = \frac{a-b}{6a} <  \frac{a}{6a} = \frac{1}{6} \implies 4r^2 < \frac{4}{6} = \frac{2}{3} < 1 \implies 2r < 1\]

Donc:

\[a-b > 0 \quad \textrm{et} \quad r>0 \implies 2(a-b)\frac{3 + 2r}{3} > 0 \implies P'(r_{1}) > 0\]

\[\frac{3 - 2r}{3} > 0 \implies 2(a-b)\frac{3 - 2r}{3} > 0 \implies P'(r_{2}) > 0\]

Aussi,

$$\begin{equation}
P'(0) = -4b \quad \textrm{et} \quad P'(1) = 2(a-b)
\label{equation-pb-5-pderpremval}
\end{equation}$$

$$\begin{equation}
P(0) = b \quad \textrm{et} \quad P(1) = 2(a-b)
\label{equation-pb-5-pval}
\end{equation}$$

Nous obtenons ainsi le tableau de variation de la fonction polynômiale $P(x)$:

![file](../../diagrams/out/opam-2023/exercice-5-tab-variation-first.png "Premier tableau de variation de P(x)")

D'après le tableau de variation de la fonction polynômiale $P(x)$, il existe $r' \in ]0,1[$, tel que $P'(r') = 0$.
Aussi, selon le signe de $P(r')$, le polynôme $P$ admet soit deux racines réelles distinctes, une racine réelle ou aucune racine réelle. En effet, 

!!! abstract "Equations conditions de signe du polynôme $P(x)$"

    $$\begin{equation}
    \textrm{Si} \quad P(r') > 0 \implies P(x) > 0, \quad \forall x \in \mathbb{R} \quad \textrm{alors} \quad P \quad \textrm{n'admet aucune racine réelle}
    \label{equation-sig-pder-rppos}
    \end{equation}$$

    $$\begin{equation}
    \textrm{Si} \quad P(r') = 0 \implies \textrm{le polynôme} \quad P \quad \textrm{admet une seule racine réelle} \quad r' \in ]0,1[
    \label{equation-sig-pder-rpnul}
    \end{equation}$$

    $$\begin{equation}
    \textrm{Si} \quad P(r') < 0 \implies \textrm{le polynôme} \quad P \quad \textrm{admet deux racines réelles} \quad r_{(1)} \quad \textrm{et} \quad r_{(2)} \in ]0,1[
    \label{equation-sig-pder-rpneg}
    \end{equation}$$

Rappelons l'hypothèse de départ, qui spitule que $P$ admet des racines réelles strictement positives.

La dernière implication de la relation sur les conditions de signes du polynôme $P(x)$ est absurde par rapport à l'hypothèse de départ.

D'après l'hypothèse, les racines de $P$ sont réelles et strictement positives. D'après la deuxième relation sur les conditions de signes du polynôme $P(x)$, $P$ admet une seule racine réelle $r' \in ]0,1[$. Ainsi, il s'agit d'une racine de multiplicité $4$. La dernière équation de la relation racines coefficients implique donc que: $4r'=4 \implies r'=1$. Ce qui est absurde car  $0 < r' < 1$.

Enfin, selon la dernière relation sur les conditions de signes du polynôme $P(x)$, $P$ admet deux racines réelles $r_{(1)} \in ]0,1[$ et $r_{(2)} \in ]0,1[$. Ainsi, il s'agit de racines de multiplicités combinées $m_{(1)}$ et $m_{(2)}$ égale à $4$, c'est-à-dire $m_{(1)} + m_{(2)} = 4$. La dernière équation des relations acines coefficients implique donc que: $m_{(1)}r_{(1)} + m_{(2)}r_{(2)} =4$. Or:

\[0 < r_{(1)} < 1 \quad \textrm{et} \quad 0 < r_{(2)} < 1 \implies 0 < m_{(1)}r_{(1)} + m_{(2)}r_{(2)} < m_{(1)} + m_{(2)} = 4 \]

Ce qui contredit  $m_{(1)}r_{(1)} + m_{(2)}r_{(2)} =4$. C'est donc absurde.

Ainsi, nous avons montré par absurde que $a$ n'est pas strictement supérieur à $b$ si les racines de $P$ sont réelles strictement positives.

_Possibilité 2 - supposons que $a < b$ avec $a > 0$_

Comme $a$ et $b$ ont le même signe, alors $a > 0$, $b > 0$ et $a < b$. Cela implique que $-\frac{a-b}{6a} > 0$. Ainsi le polynôme $P"$ est strictement positif. Nous avons ainsi le tableau de variation suivant pour la fonction polynômiale $P(x)$.

![file](../../diagrams/out/opam-2023/exercice-5-tab-variation-sec.png "Second tableau de variation de P(x)")

Le tableau de variation ci-dessus est celui de la fonction polynômiale $P(x)$ lorsque $a < b$. Puisque $b > 0$, $2(a-b) < 0$ alors à l'aide du tableau de variation de $P(x)$, nous pouvons dire que la fonction polynômiale $P(x)$ a exactement deux racines réelles $r_{(1')}$ et $r_{(2')}$ avec $0 < r_{(1')} < 1$ et $1 < r_{(2')}$. D'après l'hypothèse, ce sont donc des racines de multiplicités combinées $m_{(1')}$ et $m_{(2')}$ égale à $4$, c'est-à-dire $m_{(1')} + m_{(2')} = 4$. La dernière équation des relations racines coefficients implique donc que: $m_{(1')}r_{(1')} + m_{(2')}r_{(2')} =4$. D'où:

!!! abstract "Équation relation racines polynôme"

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        0 < r_{(1')} < 1\\
        1 < r_{(2')}\\
        m_{(1')} + m_{(2')} = 4\\
        m_{(1')}r_{(1')} + m_{(2')}r_{(2')} = 4\\
        r_{(1')}^{m_{(1')}}r_{(2')}^{m_{(2')}} = \frac{b}{a}
        \end{array}
    \right.
    \label{equation-rel-racine-pol}
    \end{equation}$$

Ainsi, nous avons:

\[r_{(2')} = \frac{4 - m_{(1')}r_{(1')}}{4 - m_{(1')}} \implies^{\textrm{d'après les relations des racines du polynôme}} \quad r_{(1')}^{m_{(1')}}\left(\frac{4 - m_{(1')}r_{(1')}}{4 - m_{(1')}}\right)^{4 - m_{(1')}} = \frac{b}{a}\]

Donc:

!!! abstract "Equation valeur polynôme racine"

    $$\begin{equation}
    r_{(1')}^{m_{(1')}}(4 - m_{(1')}r_{(1')})^{4 - m_{(1')}} - \frac{b}{a}(4 - m_{(1')})^{4 - m_{(1')}} = 0
    \label{equation-val-fct-rac-posleq1}
    \end{equation}$$

Posons:

\[f(r) = r^{m_{(1')}}(4 - m_{(1')}r)^{4 - m_{(1')}} - \frac{b}{a}(4 - m_{(1')})^{4 - m_{(1')}}\]

\[f'(r) = 4m_{(1')}(1 - r)r^{m_{(1')} - 1}(4 - m_{(1')}r)^{3 - m_{(1')}}\]

Puisque $1 \leq m_{(1')} \leq 3$, on a:

\[\forall r, \quad 0 < r < 1, \quad f'(r) > 0\]

Ainsi, la fonction $f$ est strictement croissante sur $[0,1]$, or:

\[
\left\{
    \begin{array}{l}
    f(0) = -\left(\frac{b}{a}\right)(4 - m_{(1')})^{4 - m_{(1')}} < 0,\\
    f(1) = (1 - \left(\frac{b}{a}\right))(4 - m_{(1')})^{4 - m_{(1')}} < 0 \quad \textrm{car} \quad \frac{b}{a} > 1
    \end{array}
\right.
\]

Donc $f$ est strictement négative sur $[0,1]$, donc:

\[\forall r \in [0,1], \quad f(r) < 0 \Longleftrightarrow \forall r \in [0,1], \quad r^{m_{(1')}}(4 - m_{(1')}r)^{4 - m_{(1')}} < \frac{b}{a}(4 - m_{(1')})^{4 - m_{(1')}}\]

Ce qui contredit l'équation valeur polynôme racine, absurde.

Ainsi, nous avons montré par absurde que l'assertion $a < b$ n'est pas vraie.

Par conséquent, si $a$ et $b$ sont des nombres réels avec $a \neq 0$, tels que les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives alors $a = b$.

__Montrons que si $a = b$ alors les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives.__

Supposons que $a = b$, alors:

\[P(x) = a(x^4 - 4x^3 + 6x^2 - 4x + 1) \implies P(x) = a(x - 1)^4\]

Ainsi, $1$ est la seule racine du polynôme $P$ de multiplicité $4$. D'où les racines du polynôme $P$ sont réelles strictement positives.

Pour conclure:

Les racines du polynôme $P$ définit dans l'équation de l'énoncé de l'exercice sont réelles et strictement positives si et seulement si $a=b$.

### <span style="color:#0c87eb">Solution - Utilisation de l'inégalité AGH et/ou de Muirhead (Proposée)</span>

Dans cette solution, nous allons montrer que si les racines de $P(x)$ sont réelles strictement positives alors $a=b$. La réciproque étant démontrée par la dernière partie de la solution précédente dans laquelle la résolution utilisée est simple et indépendante de l'intitulé de la méthode de la solution 1.

__Montrons que si les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives alors $a=b$.__

Soient $a$ et $b$ des nombres réels avec $a \neq 0$. Supposons que les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives. Ainsi, d'après la relation racines polynôme, on obtient ces relations:

\[
\left\{
    \begin{array}{l}
    \frac{b}{a} = \alpha\beta\gamma\mu\\
    4\frac{b}{a} = (\alpha + \beta)\mu\gamma + (\gamma + \mu)\alpha\beta\\
    5+\frac{b}{a} = \alpha\beta + (\alpha + \beta)(\gamma + \mu) + \gamma\mu\\
    4 = \alpha + \beta + \gamma + \mu
    \end{array}
\right.
\]

_Montrons que $a \leq b$._

Puisque les racines du polynôme $P$ ($\alpha$, $\beta$, $\gamma$ et $\mu$) sont strictement positives alors, leur moyenne harmonique est plus petite que leur moyenne géométrique. D'où:

$$\begin{equation}
\frac{4}{\frac{1}{\alpha} + \frac{1}{\beta} + \frac{1}{\gamma} + \frac{1}{\mu}} \leq (\alpha \beta \gamma \mu)^{\frac{1}{4}}
\label{equation-ihg}
\end{equation}$$

Aussi, en divisant la deuxième équation de la relation racines coefficients par la première équation, on obtient:

\[4 = \frac{1}{\alpha} + \frac{1}{\beta} + \frac{1}{\gamma} + \frac{1}{\mu} \implies \frac{4}{\frac{1}{\alpha} + \frac{1}{\beta} + \frac{1}{\gamma} + \frac{1}{\mu}} = 1\]

La moyenne harmonique est égale à $1$ et en utilisant la première équation de la relation racines coefficients, la moyenne géométrique est égale à $\left(\frac{b}{a}\right)^{\frac{1}{4}}$. Ainsi:

\[1 \leq \left(\frac{b}{a}\right)^{\frac{1}{4}} \implies a \leq b\]

_Montrons que $a \geq b$._

_Première approche - l'inégalité arithmétique géométrique (IAG)_

Comme $\alpha$, $\beta$, $\gamma$ et $\mu$ sont strictement positives alors, leur moyenne géométrique est plus petite que leur moyenne arithmétique. D'où:

$$\begin{equation}
\frac{\alpha + \beta + \gamma + \mu}{4} \geq (\alpha \beta \gamma \mu)^{\frac{1}{4}}
\label{equation-iag}
\end{equation}$$

Aussi, d'après la dernière équation de la relation racines coefficients, la moyenne arithmétique est égale à $1$. Or, la moyenne géométrique est égale à $\left(\frac{b}{a}\right)^{\frac{1}{4}}$. Ainsi:

\[1 \geq \left(\frac{b}{a}\right)^{\frac{1}{4}} \implies a \geq b\]

_Deuxième approche - Inégalités de Muirhead_

Notons:

\[c = (2, 0, 0, 0) \quad \textrm{,} \quad d = (1, 1, 0, 0)\]

Et avec, $\Omega$ l'ensemble des permutations de $\{1, 2, 3, 4\}$ et $x_{1}, x_{2}, x_{3}$ et $x_{4}$ des nombres réels positifs,

\[\left[c\right] = \frac{1}{4!}\sum_{\sigma \in \Omega} x_{\sigma_{1}}^{2}x_{\sigma_{2}}^{0}x_{\sigma_{3}}^{0}x_{\sigma_{4}}^{0} \quad \textrm{,} \quad \left[d\right] = \frac{1}{4!}\sum_{\sigma \in \Omega} x_{\sigma_{1}}^{1}x_{\sigma_{2}}^{1}x_{\sigma_{3}}^{0}x_{\sigma_{4}}^{0}\]

Donc:

\[\left[c\right] = \frac{3!}{4!}\sum_{\sigma \in \Omega} x_{\sigma_{1}}^{2} =  \frac{1}{4}\sum_{\sigma \in \Omega} x_{\sigma_{1}}^{2} \quad \textrm{,} \quad \left[d\right] = \frac{2!*2!}{4!}\sum_{\sigma \in \Omega} x_{\sigma_{1}}^{1}x_{\sigma_{2}}^{1} = \frac{1}{6}\sum_{\sigma \in \Omega} x_{\sigma_{1}}x_{\sigma_{2}}\]

On a:

\[c \geq d\]

Car, si nous écrivons $c = (c_{1}, c_{2}, c_{3}, c_{4})$ et $d = (d_{1}, d_{2}, d_{3}, d_{4})$, alors:

\[\forall k \in \{1, 2, 3, 4\},  c_{1} + ... + c_{k} \geq d_{1} + ... + d_{k} \quad \textrm{et} \quad c_{1} + ... + c_{4} = d_{1} + ... + d_{4}\]

D'après l'inégalité de Muirhead (voir la remarque de l'inégalité de Muirhead et des moyennes arithmétique géométrique), on obtient:

\[\left[c\right] \geq \left[d\right]\]

Ce qui implique en posant:

\[x_{1} = \alpha, \quad x_{2} = \beta, \quad x_{3} = \gamma \quad \textrm{et} \quad x_{4} = \mu \quad \text{où, } \alpha, \beta, \gamma, \mu \quad \textrm{sont les racines de $P$} \]

\[\frac{1}{4}(\alpha^2 + \beta^2 + \gamma^2 + \mu^2) \geq \frac{1}{6}(\alpha\beta + \alpha\gamma + \beta\gamma + \alpha\mu + \beta\mu + \gamma\mu) \]

Or

\[\alpha^2 + \beta^2 + \gamma^2 + \mu^2 = (\alpha + \beta + \gamma + \mu)^2 - 2(\alpha\beta + \alpha\gamma + \beta\gamma + \alpha\mu + \beta\mu + \gamma\mu)\]

Et d'après les deux dernières équations de la relation racines coefficients:

\[\alpha\beta + \alpha\gamma + \beta\gamma + \alpha\mu + \beta\mu + \gamma\mu = 5 + \frac{b}{a}\]

\[\alpha + \beta + \gamma + \mu = 4\]

Ainsi:

\[\frac{1}{4}(16 - 2(5 + \frac{b}{a})) \geq \frac{1}{6}(5 + \frac{b}{a}) \implies 3(6 - 2\frac{b}{a}) \geq 2(5 + \frac{b}{a})\]

\[18 - 6\frac{b}{a} \geq 10 + 2\frac{b}{a} \implies -8\frac{b}{a} \geq -8 \implies \frac{b}{a} \leq 1\]

D'où:

\[a \geq b\]

Pour conclure, si les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives alors $a=b$.

Cette dernière implication ainsi que la démonstration de la réciproque effectuée à la fin de la solution 2 de ce problème, nous permet de dire que les racines du polynôme $P(x)$ de l'équation de l'énoncé de l'exercice sont réelles strictement positives si et seulement si $a=b$.

!!! warning "Inégalité de Muirhead et des moyennes arithmétique géométrique"

    Soit $c = (c_{1}, ..., c_{n})$ une suite de nombres réels. Pour toute suite $x_{1}, ..., x_{n}$ de nombres réels positifs, on définit la $c$-moyenne, notée $\left[c\right]$, de $x_{1}, ..., x_{n}$ par:

    \[\left[c\right] = \frac{1}{n!}\sum_{\sigma} x_{\sigma_{1}}^{c_{1}} ... x_{\sigma_{n}}^{c_{n}}\]

    où la somme est étendue à toutes les permutations $\sigma$ de $\{1, ..., n\}$.

    En notant $d = (d_{1}, ..., d_{n})$, une autre suite de nombres réels, alors:

    Si les suites $c$ et $d$ sont décroissantes, on a $\left[c\right] \leq \left[d\right]$ pour toute suite $x_{1}, ..., x_{n}$ si et seulement si $\forall k \in \{1, ..., n\},  c_{1} + ... + c_{k} \leq d_{1} + ... + d_{k} \quad \textrm{et} \quad c_{1} + ... + c_{n} = d_{1} + ... + d_{n}$

    L'IAG (inégalité de la moyenne arithmétique géométrique) peut être déduite de l'inégalité de Muirhead. En effet, l'on peut prendre 

    \[c = \left(\frac{1}{n}, ...,\frac{1}{n}\right)\quad \textrm{} \quad d = (1, 0, 0, ...,0)\]

    Pour plus de détails sur l'inégalité de Muirhead, se reférer à la page wikipédia suivante [Inégalité de muirhead](https://fr.wikipedia.org/wiki/Inégalité_de_Muirhead).

!!! warning "Relation entre les coefficients et les racines d'un polynôme dite 'de Viète'"

    Les formules de Viète permettent d'écrire une relation entre les racines d'un polynôme et ses coefficients. Un énoncé est le suivant:

    Soit $P$, un polynôme de dégré $n$ s'écrivant sous la forme:

    \[P(x) = a_{n}x^n + a_{n - 1}x^{n - 1} + ...  + a_{1}x + a_0 \]

    avec les coefficients $a_{k}$ pouvant être des nombres réels ou des nombres complexes et $a_{n} \neq 0$. Le polynôme $P$ a $n$ racines complexes non nécéssairement distinctes $r_{1}, r_{2}, ..., r_{n}$ d'après le théorème fondamental de l'algèbre. Les formules de Viète s'écrivent:

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        r_{1} + r_{2} + ... + r_{n-1} + r_{n} = -\frac{a_{n-1}}{a_{n}}\\
        (r_{1} r_{2} + r_{1} r_{3} + ... + r_{1} r_{n}) + ... + (r_{2} r_{3} + ... + r_{2} r_{n}) + ... + r_{n-1} r_{n} = \frac{a_{n-2}}{a_{n}}\\
        .\\
        .\\
        .\\
        r_{1} r_{2} ... r_{n} = (-1)^{n}\frac{a_{0}}{a_{n}}
        \end{array}
    \right.
    \label{equation-viete}
    \end{equation}$$

    Ou de manière synthétique:

    $$\begin{equation}
    \forall k \in \{1, 2, ..., n\}, \quad \sum_{1 \leq i_{1} < i_{2} < ... < i_{k} \leq n} \left(\prod_{j=1}^{k}r_{i_{j}}\right) = (-1)^{k}\frac{a_{n-k}}{a_n}
    \label{equation-viete-synth}
    \end{equation}$$

    Les indices $i_{k}$ sont ordonnés dans un ordre croissant pour s'assurer que chaque produit de $k$ racines est utilisé exactement une fois.

    Pour plus de détails sur les relations entre les racines de polynôme et les coefficients de celui-ci, se reférer à la page wikipédia suivante [Relation de Viète](https://en.wikipedia.org/wiki/Vieta%27s_formulas).

    Pour plus de détails sur le théorème fondamental de l'algèbre, se reférer à la page wikipédia suivante [Théorème fondamental d'algèbre](https://en.wikipedia.org/wiki/Fundamental_theorem_of_algebra).

## <span style="color:#0a69b7">Bibliographie</span>

* Wikipedia, Fundamental Theorem of Algebra, [https://en.wikipedia.org/wiki/Fundamental_theorem_of_algebra](https://en.wikipedia.org/wiki/Fundamental_theorem_of_algebra), consulté le 07/03/2024.
* Wikipedia, Vieta Formula, [https://en.wikipedia.org/wiki/Vieta%27s_formulas](https://en.wikipedia.org/wiki/Vieta%27s_formulas), consulté le 07/03/2024.
* Wikipedia, Inégalité de Muirhead, [https://fr.wikipedia.org/wiki/Inégalité_de_Muirhead](https://fr.wikipedia.org/wiki/Inégalité_de_Muirhead), consulté le 07/03/2024.
