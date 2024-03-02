---
comments: true
---

# <span style="color:#074b83"> Exercice 3 - OPAM 2023 (Arithmétique) </span>

## <span style="color:#0a69b7">L'énoncé (fourni par [KouakouSchool](https://www.youtube.com/@kouakouschool))</span>

!!! question "Énoncé de l'exercice"

    On considère la suite de nombres réels définie par:

    $$
    \begin{equation}
    \left\{
        \begin{array}{l}
        x_1 = c \\
        x_{n+1} = cx_{n} + \sqrt{c^2 - 1}\sqrt{x_{n}^2 - 1}  \quad \textrm{pour tout} \quad n \geq 1.
        \end{array}
    \right.
    \label{equation-pb-3}
    \end{equation}
    $$

    Montrer que si $c$ est un nombre entier naturel non nul, alors $x_{n}$ est un entier pour tout $n \geq 1$.

## <span style="color:#0a69b7">Solutions</span>

### <span style="color:#0c87eb">Solution 1 - Changement de variable</span>

Définissons la suite numérique $a_n$ telle que pour tout entier naturel $n$,

\[x_n = cosh(a_n)\]

Cette suite est bien définie car la fonction $cosh$ est bijective sur $\mathbb{R^{+}}$.
En effet, la fonction cosinus hyperbolique est strictement croissante sur $\mathbb{R^{+}}$ (car sa dérivée est la fonction sinus hyperbolique qui est strictement positive sur $\mathbb{R^{+}}$), elle est donc bijective sur $\mathbb{R^{+}}$.

Ainsi, l'équation de l'énoncé devient:

!!! abstract "Equation problème cosinus hyperbolique"

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        x_n = cosh(a_n) \quad \textrm{pour tout} \quad n \geq 1\\
        cosh(a_{n+1}) = cosh(a_1)cosh(a_{n}) + \sqrt{cosh(a_1)^2 - 1}\sqrt{cosh(a_{n})^2 - 1}  \quad \textrm{pour tout} \quad n \geq 1.
        \end{array}
    \right.
    \label{equation-pb-3-sol-cosh}
    \end{equation}$$

Nous avons les identités remarquables suivantes pour les fonctions $cosh$ (cosinus hyperbolique) et $sinh$ (sinus hyperbolique):

!!! abstract "Equation relations cosinus/sinus hyperpolique"

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        cosh(x)^2 + sinh(x)^2 = 1 \quad \textrm{pour tout} \quad x \quad \textrm{et} \quad y \quad \textrm{nombres réels}\\
        cosh(x+y) = cosh(x)cosh(y) +  sinh(x)sinh(y) \quad \textrm{pour tout} \quad x \quad \textrm{et} \quad y \quad \textrm{nombres réels}\\
        cosh(x) > 0 \quad \textrm{et} \quad sinh(x) > 0 \quad \textrm{pour tout} \quad x \quad \textrm{et} \quad y \quad \textrm{nombres réels strictement positifs}
        \end{array}
    \right.
    \label{equation-pb-3-relation-cosh}
    \end{equation}$$

Ainsi, en utilisant la seconde relation de l'équation avant celle-ci, on peut écrire:

\[cosh(a_{n+1}) = cosh(a_1)cosh(a_{n}) + sinh(a_1)sinh(a_{n}) \]

Cela implique que:

!!! abstract "Equations reduites du problème"

    $$\begin{equation}
    cosh(a_{n+1}) = cosh(a_1 + a_n)
    \label{equation-pb-3-relation-cosh-an}
    \end{equation}$$

    La fonction cosinus hyperbolique est bijective. Ainsi:

    $$\begin{equation}
    a_{n+1} = a_1 + a_n
    \label{equation-pb-3-relation-an}
    \end{equation}$$

Par récurrence sur $n$, nous montrons que $a_{n} = n*a_{1}$ pour tout $n \geq 1$. En effet, pour $n=1$, cela est vrai car $a_{1} = 1*a_{1}$. Supposons que pour un certain $n \geq 1$, $\forall k \leq n$, $a_{k} = k*a_{1}$. Alors, on a:

\[a_{n+1} = a_{n} + a_{1} \implies a_{n+1} = n*a_{1} + a_{1}\]

Donc:

\[a_{n+1} = (n+1)a_{1} \]

Ainsi, par récurrence:

!!! abstract "Equation de recurrence suite reduite"

    $$\begin{equation}
    a_{n} = n*a_{1} \quad \textrm{pour tout} \quad n \geq 1 \quad \textrm{entier naturel}.
    \label{equation-pb-3-reccur-an}
    \end{equation}$$

Donc:

!!! abstract "Equation recurrence suite problème"

    $$\begin{equation}
    \left\{
        \begin{array}{l}
    cosh(a_{1}) = c\\
    x_{n} = cosh(na_{1}) \quad \textrm{pour tout} \quad n \geq 1 \quad \textrm{entier naturel}.
    \end{array}
    \right.
    \label{equation-pb-3-reccur-xn}
    \end{equation}$$

__Montrons que si $cosh(x)$ est un entier alors pour tout entier naturel $n$, $cosh(nx)$ est un entier naturel__:

Pour tous nombres réels $a$ et $b$ et tout entier naturel $n$, on a:

\[(a + b)^n = \sum_{k=0}^{n} c_{k}^{n} a^{k}b^{n-k}\]

Car lorsqu'on choisit $a$ dans $k$ termes $a + b$, l'on choisira automatiquement $b$, $n-k$ fois pour former un terme de $(a+b)^n$. De plus, nous pouvons calculer la valeur de $c_{k}^{n}$ comme étant le nombre de manière de choisir $k$ éléments parmi $n$ éléments sans tenir compte de l'ordre, c'est à dire:

\[c_{k}^{n} = \binom{n}{k} \]

Or

\[\binom{n}{n-k} = \binom{n}{k} \implies c_{k}^{n} = c_{n-k}^{n}\]

D'où:

!!! abstract "Equation développement exposant de somme"

    $$\begin{equation}
    (a + b)^n  = \sum_{k=0}^{\left[\frac{n}{2}\right]} c_{k}^{n} (a^{k}b^{n-k} + a^{n-k}b^{k}) - \delta_{\left[\frac{n}{2}\right], \frac{n}{2}} c_{\left[\frac{n}{2}\right]}^{n} a^{\frac{n}{2}}b^{\frac{n}{2}}
    \label{equation-pb-3-sumabpown-2}
    \end{equation}$$

Où la notation $\left[x\right]$ signifie, la partie entière de $x$ et $\delta_{a,b}$ est telle que:

\[\delta_{a, b} = \left\{
    \begin{array}{l}
    1 \quad \textrm{si} \quad a = b\\
    0 \quad \textrm{si} \quad a \neq b
    \end{array}
\right.\]

Ainsi, pour $a = e^{x}$ et $b = e^{-x}$, on a: $2^{n}cosh(x)^{n} = (a + b)^{n}$. Ce qui donne donc:

\[
2^{n}cosh(x)^{n} = \sum_{k=0}^{\left[\frac{n}{2}\right]} c_{k}^{n} (e^{(n-2k)x} + e^{-(n-2k)x}) - \delta_{(\left[\frac{n}{2}\right], \frac{n}{2})} c_{\frac{n}{2}}^{n}
\]

Donc:

\[
2^{n}cosh(x)^{n} = \sum_{k=0}^{\left[\frac{n}{2}\right]} c_{k}^{n} 2cosh((n-2k)x) - \delta_{(\left[\frac{n}{2}\right], \frac{n}{2})} c_{\frac{n}{2}}^{n}
\]

\[
2c_{0}^{n} cosh(nx) = 2^{n}cosh(x)^{n} - \sum_{k=1}^{\left[\frac{n}{2}\right]} 2c_{k}^{n}cosh((n-2k)x) + \delta_{(\left[\frac{n}{2}\right], \frac{n}{2})} c_{\frac{n}{2}}^{n}
\]

Or $c_{0}^{n} = \binom{n}{0} = 1$, donc:

!!! abstract "Equation décomposition cosinus hyperbolique"

    $$\begin{equation}
    cosh(nx) = 2^{n-1}cosh(x)^{n} - \sum_{k=1}^{\left[\frac{n}{2}\right]} c_{k}^{n} cosh((n-2k)x) + \delta_{(\left[\frac{n}{2}\right], \frac{n}{2})} \frac{c_{\frac{n}{2}}^{n}}{2}
    \label{equation-pb-3-coshnx-decomp}
    \end{equation}$$

Soit $x$ tel que $cosh(x)$ est un entier naturel.
Par récurrence, montrons que pour tout entier naturel $n$, $cosh(nx)$ est un entier naturel.
Pour $n = 1$, on a $cosh(nx)=cosh(x)$ est un entier naturel.

!!! abstract "Equation hypothèse de récurrence"

    $$\begin{equation}
    \textrm{Soit} \quad n, \quad \textrm{tel que pour tout} \quad k \leq n, \quad cosh(kx) \quad \textrm{est un entier naturel.}
    \label{equation-pb-3-coshnx-hypothese}
    \end{equation}$$

Donc:

!!! abstract "Identité sur cosinus hyperbolique"

    $$\begin{equation}
    \forall k \leq \left[\frac{n+1}{2}\right], \quad c_{k}^{n+1} cosh((n+1-2k)x) \quad \textrm{est un entier naturel}
    \label{equation-pb-3-forall-coshlx}
    \end{equation}$$

Car $\forall k \quad \textrm{tel que,} \quad 1 \leq k \leq \left[\frac{n+1}{2}\right]$, $0 \leq n+1-2k \leq n$, l'hypothèse est applicable pour $l=n+1-2k$ et $c_{k}^{n+1} = \binom{n + 1}{k}$ est un entier.

Aussi,

\[\delta_{(\left[\frac{n+1}{2}\right], \frac{n+1}{2})} \frac{c_{\frac{n+1}{2}}^{n+1}}{2} = \left\{
    \begin{array}{l}
    \frac{c_{\frac{n+1}{2}}^{n+1}}{2} \quad \textrm{si} \quad n+1 \quad \textrm{est pair}\\
    0 \quad \textrm{si} \quad n+1 \quad \textrm{est impair}
    \end{array}
\right.\]

Si $n+1$ est pair,

\[c_{\frac{n+1}{2}}^{n+1} = \binom{n+1}{\frac{n+1}{2}} \implies c_{\frac{n+1}{2}}^{n+1} = \frac{(n+1)!}{(\frac{n+1}{2})!(\frac{n+1}{2})!}  \implies c_{\frac{n+1}{2}}^{n+1} = 2 \frac{n!}{(\frac{n-1}{2})!(\frac{n+1}{2})!} \]

\[c_{\frac{n+1}{2}}^{n+1} = 2\binom{n}{\frac{n+1}{2}} \implies c_{\frac{n+1}{2}}^{n+1} = 2c_{\frac{n+1}{2}}^{n} \implies \frac{c_{\frac{n+1}{2}}^{n+1}}{2} = c_{\frac{n+1}{2}}^{n} \]

Donc:

!!! abstract "Equation valeur delta"

    $$\begin{equation}
    \delta_{(\left[\frac{n+1}{2}\right], \frac{n+1}{2})} \frac{c_{\frac{n+1}{2}}^{n+1}}{2} = \left\{
        \begin{array}{l}
        c_{\frac{n+1}{2}}^{n} \quad \textrm{si} \quad n+1 \quad \textrm{est pair}\\
        0 \quad \textrm{si} \quad n+1 \quad \textrm{est impair}
        \end{array}
    \right.
    \label{equation-pb-3-cfloor-half-nplusone}
    \end{equation}$$

D'après l'équation de la décomposition de $cosh(nx)$,

\[cosh((n+1)x) = 2^{n}cosh(x)^{n+1} - \sum_{k=1}^{\left[\frac{n+1}{2}\right]} c_{k}^{n+1} cosh((n+1-2k)x) + \delta_{(\left[\frac{n+1}{2}\right], \frac{n+1}{2})} \frac{c_{\frac{n+1}{2}}}{2}\]

et

\[cosh((n+1)x) > 0 \quad \textrm{pour tout} \quad x \quad \textrm{nombres réel strictement positifs}\]

En utilisant les remarques $c_{k}^{n+1} cosh((n+1-2k)x) \quad \textrm{est un entier naturel}$, l'expression de $\delta_{(\left[\frac{n+1}{2}\right], \frac{n+1}{2})} \frac{c_{\frac{n+1}{2}}^{n+1}}{2}$ et le fait que $cosh(x)$ est un entier naturel alors $cosh((n+1)x)$ est un entier.

Ainsi, si $x$ est un nombre réel tel que $cosh(x)$ est un entier naturel alors pour tout entier naturel $n$, $cosh(nx)$ est un entier naturel.

Pour conclure, en utilisant l'expression de $x_{n}$ en fonction de $a_{1}$ et l'implication précédente, nous pouvons déduire que:

Si $c$ est un nombre entier naturel non nul, alors $x_{n}$ est un entier pour tout $n \geq 1$.

### <span style="color:#0c87eb">Solution 2 - A partir d'une relation de récurrence de la suite</span>

__Montrons par récurrence que pour tout entier naturel $n \geq 2$, $x_{n+1} = 2cx_{n} - x_{n-1}$__:

Pour $n = 1, 2$ et $3$, on a:

\[x_{1} = c \]

\[x_{2} = c^2 + \sqrt{c^2 - 1}\sqrt{c^2 - 1} \implies x_{2} = 2c^2 - 1 \]

\[x_{3} = c(2c^2 - 1) + \sqrt{c^2 - 1}\sqrt{(2c^2 -  1)^2 - 1} \implies x_{3} = 2c^3 - c + \sqrt{c^2 - 1}\sqrt{4c^2(c^2 - 1)} \]

\[x_{3} = 2c^3 - c + (c^2 - 1)(2c) \implies x_{3} = 4c^3 - 3c \implies x_{3} = 2c(2c^2 - 1) - c \]

!!! abstract "Equations valeurs initiales"

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        x_{1} = c\\
        x_{2} = 2c^2 - 1\\
        x_{3} = 2c(2c^2 - 1) - c
        \end{array}
    \right.
    \label{equation-pb-3-sol-2-x1x2x3}
    \end{equation}$$

    D'où:

    $$\begin{equation}
    x_{3} = 2cx_{2} - x_{1}
    \label{equation-pb-3-sol-2-x3fctx1x2}
    \end{equation}$$

Donc pour $n=2$, on a: $x_{n+1} = 2cx_{n} - x_{n-1}$.

Supposons que pour un certain $n \geq 2$, on a: $\forall k, 2 \leq k \leq n, x_{k+1} = 2cx_{k} - x_{k-1}$. Alors, on a d'après la définition de la suite $x_{n}$,

$$\begin{equation}
x_{n+2} = cx_{n+1} + \sqrt{c^2 - 1}\sqrt{x_{n+1}^2 - 1}
\label{equation-pb-3-sol-2-xnplustwofctxnplusone}
\end{equation}$$

D'après l'hypothèse, on a:

\[x_{n+1}^2 = (2cx_{n} - x_{n-1})^2 \implies x_{n+1}^2 = 4c^{2}x_{n}^{2} - 4cx_{n}x_{n-1} + x_{n-1}^{2} \]

\[x_{n+1}^2 - 1 = (4c^{2}x_{n}^{2} - 4cx_{n}x_{n-1}) + (x_{n-1}^{2} - 1) \]

\[(c^2 - 1)(x_{n+1}^2 - 1) = (c^{2} - 1)(4c^{2}x_{n}^{2} - 4cx_{n}x_{n-1}) + (c^{2} - 1)(x_{n-1}^{2} - 1) \]

Or, d'après la définition de la suite $x_{n}$ selon l'équation de l'énoncé de l'exercice:

\[(c^{2} - 1)(x_{n-1}^{2} - 1) = (x_{n} - cx_{n-1})^{2} \]

Donc:

\[(c^2 - 1)(x_{n+1}^2 - 1) = (c^{2} - 1)(4c^{2}x_{n}^{2} - 4cx_{n}x_{n-1}) + (x_{n}^{2} - 2c x_{n}x_{n-1} + c^{2}x_{n-1}^{2}) \]

\[(c^2 - 1)(x_{n+1}^2 - 1) = (4c^{4} - 4c^{2} + 1)x_{n}^{2} - 2c(2c^{2} - 1)x_{n-1}x_{n} + c^{2}x_{n-1}^{2} \]

Aussi:

\[(cx_{n+1} - x_{n})^{2} = c^{2}x_{n+1}^{2} - 2cx_{n+1}x_{n} + x_{n}^{2} \]

D'après l'hypothèse de la récurrence, pour $k=n$:

\[x_{n+1} = 2cx_{n} - x_{n-1} \quad \textrm{et} \quad x_{n+1}^2 = 4c^{2}x_{n}^{2} - 4cx_{n}x_{n-1} + x_{n-1}^{2} \]

Donc:

\[(cx_{n+1} - x_{n})^{2} = c^{2}(4c^{2}x_{n}^{2} - 4cx_{n}x_{n-1} + x_{n-1}^{2}) - 2c(2cx_{n} - x_{n-1})x_{n} + x_{n}^{2} \]

\[(cx_{n+1} - x_{n})^{2} = (4c^{4} - 4c^{2} + 1)x_{n}^{2} - 2c(2c^{2} - 1)x_{n-1}x_{n} + c^{2}x_{n-1}^{2} \]

D'où:

\[(c^2 - 1)(x_{n+1}^2 - 1) = (cx_{n+1} - x_{n})^{2}\]

L'équation de l'énoncé de l'exercice donne:

\[x_{n+2} = cx_{n+1} + (cx_{n+1} - x_{n}) \quad \textrm{car} \quad cx_{n+1} \geq c^{2}x_{n} \geq x_{n} \quad (\textrm{car} \quad c \geq 1)\]

\[x_{n+2} = 2cx_{n+1} - x_{n}\]

Ainsi, par récurrence, pour tout $n \geq 2$:

!!! abstract "Equation relation de recurrence simplifiée suite"

    $$\begin{equation}
    x_{n+1} = 2cx_{n} - x_{n-1}
    \label{equation-pb-3-sol-2-xnplusonefct-xn-xnminusone}
    \end{equation}$$

__Montrons par récurrence sur $n$ que si $c$ est un entier naturel alors pour tout $n \geq 1, x_{n}$ est un entier naturel__:

Supposons que $c$ est un entier naturel non nul.

Pour $n = 1$, $x_{1} = c$ est un entier naturel non nul. Pour $n=2$, l'expression de $x_{2}$ donnée par l'équation des valeurs initiales est: $x_{2}=2c^{2} - 1$. Donc $x_{2}$ est un entier naturel non nul.

Supposons que pour un certain $n \geq 2$, $\forall k, 1 \leq k \leq n, x_{k}$ est un entier naturel non nul. 

L'équation de la relation de recurrence simplifiée de la suite implique que $x_{n+1} = 2cx_{n} - x_{n-1}$. Or d'après l'hypothèse de récurrence $x_{n}$ et $x_{n-1}$ sont des entiers naturels non nuls. Donc, $x_{n+1}$ est un entier relatif. Aussi, $x_{n+1} \geq 1$ car les termes de l'expression de $x_{n+1} = cx_{n} + \sqrt{c^2 - 1}\sqrt{x_{n}^2 - 1}$ selon l'équation de l'énoncé de l'exercice sont tels que $cx_{n} \geq 1$ et $\sqrt{c^2 - 1}\sqrt{x_{n}^2 - 1} \geq 0$ car $c \geq 1$ et $x_{n} \geq 1$. D'où, $x_{n+1}$ est un entier naturel non nul.

Ainsi par récurrence, $\forall n \geq 1$, $x_{n}$ est un entier naturel non nul.

Pour conclure, si $c$ est un nombre entier naturel non nul, alors $x_{n}$ est un entier naturel pour tout $n \geq 1$.

!!! warning "Polynôme de Chebyshev"

    Le problème posé est équivalent à une suite de polynômes de Chebyshev de premier type noté $T_{n}$, tel que:

    \[T_{n}(cos\theta) = cos(n\theta)\]

    Pour démontrer que nous sommes face à un polynôme de Chebyshev, nous pouvons calculer les premiers termes de la suite et vérifier qu'ils sont égaux à la suite de polynômes de Chebyshev.

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        T_{0}(x) = 1\\
        T_{1}(x) = x\\
        T_{2}(x) = 2x^2 - 1\\
        T_{3}(x) = 4x^{3} - 3x\\
        T_{4}(x) = 8x^{4} - 8x^{2} + 1\\
        T_{5}(x) = 16x^{5} - 20x^{3} + 5x\\
        T_{6}(x) = 32x^{6} - 48x^{4} + 18x^{2} - 1
        \end{array}
    \right.
    \label{equation-termes-chebyshev}
    \end{equation}$$

    La relation de la solution 2, découle de la propriété suivante de la suite du polynôme de Chebyshev.

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        T_{0}(x) = 1\\
        T_{1}(x) = x\\
        T_{n+1}(x) = 2xT_{n}(x) - T_{n-1}(x) \quad \forall n \geq 1
        \end{array}
    \right.
    \label{equation-relation-chebyshev}
    \end{equation}$$

    Pour plus de détails sur les propriétés du polynôme de Chebychev, se reférer à la page wikipédia suivante [Chebyshev Polynomials](https://en.wikipedia.org/wiki/Chebyshev_polynomials).

## <span style="color:#0a69b7">Bibliographie</span>

* Wikipedia, Chebyshev Polynomials, [https://en.wikipedia.org/wiki/Chebyshev_polynomials](https://en.wikipedia.org/wiki/Chebyshev_polynomials), consulté le 02/03/2024.
