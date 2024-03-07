---
comments: true
---

# <span style="color:#074b83"> Exercice 4 - OPAM 2023 (arithmétique, combinatoire) </span>

## <span style="color:#0a69b7">L'énoncé (fourni par [KouakouSchool](https://www.youtube.com/@kouakouschool))</span>

!!! question "Énoncé de l'exercice"

    Manzi possède $n$ timbres et un album avec $10$ pages. Il distribue les $n$ timbres dans l'album de sorte que chaque page contienne un nombre distinct de timbres. Il trouve que, peu importe comment il fait cela, il y a toujours un ensemble de $4$ pages tels que le nombre total de timbres dans ces $4$ pages soit au moins $\frac{n}{2}$.

    $$\begin{equation}
    \textrm{Déterminer la valeur maximale possible de} \quad n.
    \label{question-pb-4}
    \end{equation}$$

## <span style="color:#0a69b7">Solutions</span>

### <span style="color:#0c87eb">Solution - Utilisation de la fonction partie entière</span>

!!! warning "Numérotation des pages suivant le nombre de timbres"

    Pour une distribution donnée de timbres effectuée par Manzi, nous numérotons les pages en les rangeant par ordre croissant du nombre de timbres. Notons par $a_{k}$, le nombre de timbres dans la page $k$. Puisque la distribution de timbres dans les pages est telle que deux pages distinctes ont un nombre distinct de pages. La numérotation des pages est donc telle que pour tout $k$ tel que: $2 \leq k \leq 10$, on a:

    \[0 \leq a_{k-1} < a_{k}\]

    Cela implique que:

    $$\begin{equation}
    a_{k} \geq a_{k-1} + 1 \geq 1
    \label{equation-relation-nb-pages}
    \end{equation}$$

__Montrons que la valeur minimale de n est $45$__:

Manzi dispose de $n$ timbres et comme chaque page contient un nombre distinct de timbres, considérons une distribution de timbres effectuée par Manzi. Alors, nous considérons la numérotation telle que:

\[ \forall k, \quad 2 \leq k \leq 10, \quad 0 \leq a_{k-1} < a_{k}\]

_Montrons par récurrence sur $n$ que pour tout $n \in \{1, 2, ..., 10\}$, $a_{n} \geq a_{1} + (n-1)$_

Pour $n = 1$, on a: $a_{n} = a_{1} + (n-1)$.

Supposons que pour un certain $n$, tel que: $n \in \{1, 2, ..., 9\}$, $a_{n} \geq a_{1} + (n-1)$.
Alors, la remarque de la numérotation des pages suivant le nombre de timbres permet de déduire que:

\[a_{n+1} \geq a_{n} + 1 \implies a_{n+1} \geq (a_{1} + (n-1))+ 1\]

D'où:

\[a_{n+1} \geq a_{1} + n\]

Ainsi, nous avons montré par récurrence sur $n$, que:

!!! abstract "Equation relation recurrence nombre de pages"

    $$\begin{equation}
    \forall n \in \{1, 2, ..., 10\}, \quad a_{n} \geq a_{1} + (n-1)
    \label{equation-relation-rec-nb-pgs}
    \end{equation}$$

On a:

\[n = \sum_{k=1}^{10} a_{k} \implies n \geq \sum_{k=1}^{10}(k-1) + \sum_{k=1}^{10}a_{1}\]

!!! abstract "Equation relation nombre pages"

    $$\begin{equation}
    n \geq \frac{9 \times 10}{2} + 10a_{1} \implies n \geq 45 + 10a_{1}
    \label{equation-relation-rec-n-pgs}
    \end{equation}$$

Or, $a_{1} \geq 0$, donc:

$$\begin{equation}
n \geq 45
\label{equation-val-min-n}
\end{equation}$$

Aussi, pour $n = 45$, il existe bien toujours quatre pages pour toute distribution de timbres $(a_{1}, ..., a_{10})$ entre les dix pages telles que le nombre total de timbres est supérieur à $\frac{n}{2}$. En effet, les équations de la relation de recurrence nombre de pages et de la relation nombre pages permettent de dire que:

$$\begin{equation}
n = 45 \implies a_{1} = 0 \quad \textrm{et} \quad \forall n \in \{1, 2, ..., 10\}, \quad a_{n} = a_{1} + (n-1)
\label{equation-min-n-a-k}
\end{equation}$$

Sinon, si nous supposons qu'il existe $l \in \{1, 2, ..., 10\}$, tel que: $a_{l} > a_{1} + (l-1)$. Alors:

\[n = \sum_{k=1, k \neq l}^{10} a_{k} + a_{l} \implies n > \sum_{k=1, k \neq l}^{10}(k-1) + \sum_{k=1, k \neq l}^{10}a_{1} + (l-1) + a_{1}\]

\[n > \sum_{k=1}^{10}(k-1) + \sum_{k=1}^{10}a_{1} \implies n > 45 + 10a_{1} > 45\]

Ce qui est absurde. De même si nous supposons que $a_{1} > 0$, alors:

\[n = \sum_{k=1}^{10} a_{1} + (k-1) \implies n = 45 + 10a_{1} > 45\]

Cela aussi est absurde.

Ainsi, pour $n = 45$, on a: $\forall k \in \{1, 2, ..., 10\}$, $a_{k} = k-1$. Donc: 

\[a_{7} + a_{8} + a_{9} + a_{10} = 6 + 7 + 8 + 9 \implies a_{7} + a_{8} + a_{9} + a_{10} = 30 > \frac{45}{2} \]

Donc pour $n=45$, il existe bien toujours quatre pages pour toute distribution de timbres $(a_{1}, ..., a_{10})$ entre les dix pages telle que le nombre total de timbres est supérieur à $\frac{n}{2}$.

__Montrons que si pour $n$ entier naturel, l'assertion: pour tout arrangement $(a_{1}, ..., a_{10})$, il existe toujours quatre éléments tels que le total est supérieur à $\frac{n}{2}$ est vraie alors $n$ admet une valeur maximale.__

Soit $n$ fixé un entier naturel, tel que pour toute distribution de timbres parmi les dix pages $(a_{1}, ..., a_{10})$ (suivant l'encadré remarque numérotation des pages suivant le nombre de timbres, il existe toujours quatre éléments tels que le total est supérieur à $\frac{n}{2}$. Prenons la distribution de timbres $(a_{1}, ..., a_{10})$ telle que:

!!! abstract "Equation définition distribution équidistante"

    $$\begin{equation}
    \left\{
        \begin{array}{l}
        a_{i+1} = a_{i} + 1 \quad \textrm{pour tout} \quad i \in \{1, ..., 8\}\\
        a_{1} = \left[\frac{n - 45}{10}\right] \quad \textrm{et} \quad a_{10} = n - 9a_{1} - 36
        \end{array}
    \right.
    \label{equation-def-equidist}
    \end{equation}$$

\[a_{10} = a_{1} + 9 + (n - 45 - 10a_{1})\]

Or:

\[a_{1} \leq \frac{n - 45}{10} \implies n - 45 - 10a_{1} \geq n - 45 - 10\frac{n - 45}{10} = 0 \]

Donc:

\[a_{10} \geq a_{1} + 9 = (a_{1} + 8) + 1 = a_{9} + 1\]

Ainsi, cette distribution est une distribution telle que deux pages distinctes ont un nombre distinct de timbres et on a:

\[a_{i+1} > a_{i} \quad \textrm{pour tout} \quad i \in \{1, ..., 9\} \]

S'il existe quatre pages telles que le nombre total de timbres est supérieur à $\frac{n}{2}$, en notant les quatre indices des pages comme $i, j, k$ et $l$ avec $i < j < k < l$ alors:

\[i < j < k < l \leq 10 \implies i \leq 7,\quad j \leq 8,\quad k \leq 9 \quad \textrm{et} \quad l \leq 10\]

Donc:

\[a_{i} \leq a_{7},\quad a_{j} \leq a_{8},\quad a_{k} \leq a_{9} \quad \textrm{et} \quad a_{l} \leq a_{10}\]

\[a_{7} + a_{8} + a_{9} + a_{10} \geq a_{i} + a_{j} + a_{k} + a_{l} \geq \frac{n}{2} \]

Ainsi:

!!! abstract "Equation inégalité quatre derniers"

    $$\begin{equation}
    a_{7} + a_{8} + a_{9} + a_{10} \geq \frac{n}{2}
    \label{equation-last-four-ndiv2}
    \end{equation}$$

En utilisant l'équation de la définition de distribution équidistante et la définition de $a_{1}$, on a:

\[a_{7} + a_{8} + a_{9} + a_{10} = (a_{1} + 6) + (a_{1} + 7) + (a_{1} + 8) + (n - 9a_{1} - 36) = n - 6a_{1} - 15\]

\[a_{7} + a_{8} + a_{9} + a_{10} \leq n - 6(\frac{n-45}{10} - 1) - 15 \implies a_{7} + a_{8} + a_{9} + a_{10} \leq \frac{4n+6*55-150}{10}\]

\[a_{7} + a_{8} + a_{9} + a_{10} \leq \frac{4n+180}{10}\]

D'où, en utilisant l'équation d'inégalité quatre derniers, on obtient:

\[\frac{4n+180}{10} \geq a_{7} + a_{8} + a_{9} + a_{10} \geq \frac{n}{2} \implies \frac{4n+180}{10} \geq \frac{n}{2}\]

Donc:

\[\frac{n - 180}{10} \leq 0 \implies n \leq 180\]

__Montrons que pour $n$ entier naturel, l'assertion: pour tout arrangement $(a_{1}, ..., a_{10})$, il existe toujours quatre éléments tels que le total est supérieur à $\frac{n}{2}$ est vraie alors la valeur maximale de $n$ est 140.__

Pour tout $n$ entier naturel, nous considérons la distribution de timbres $(a_{1}, a_{2}, ..., a_{10})$ selon la remarque numérotation des pages suivant le nombre de timbres. Pour démontrer le résultat ci-dessus, nous allons effectuer un raisonnement basé sur quelques valeurs possibles de $a_{6}$.

Soit $n \geq 140$,

Si $n = 140$,

Si $a_{6} < 15$, alors:

\[a_{1} + a_{2} + a_{3} + a_{4} + a_{5} + a_{6} \leq a_{6}  + (a_{6} - 1) + (a_{6} - 2) + (a_{6} - 3) + (a_{6} - 4) + (a_{6} - 5)\]

\[a_{1} + a_{2} + a_{3} + a_{4} + a_{5} + a_{6} \leq 6a_{6}  - (1 + 2 + 3 + 4 + 5) \leq 6*14 - 15\]

\[a_{1} + a_{2} + a_{3} + a_{4} + a_{5} + a_{6} \leq 69\]

Donc:

\[a_{7} + a_{8} + a_{9} + a_{10} = n - (a_{1} + a_{2} + a_{3} + a_{4} + a_{5} + a_{6}) \implies a_{7} + a_{8} + a_{9} + a_{10} \geq 140 - 69 \]

\[a_{7} + a_{8} + a_{9} + a_{10} \geq 71 > \frac{140}{2} = \frac{n}{2}\]

Si $a_{6} \geq 15$, alors:

\[a_{7} + a_{8} + a_{9} + a_{10} \geq (a_{6} + 1) + (a_{6} + 2) + (a_{6} + 3) + (a_{6} + 4)  = 4a_{6} + 10\]

\[a_{7} + a_{8} + a_{9} + a_{10} \geq 70 = \frac{140}{2} = \frac{n}{2}\]

Donc, pour $n=140$, pour toute distribution de timbres parmi les dix pages, il existe toujours quatre pages telles que le total de timbres est supérieur à $\frac{n}{2}$.

Si $n > 140$,

Nous raisonnons avec les distributions de timbres sur les $10$ pages suivant la numérotation de la remarque numérotation des pages suivant le nombre de timbres.  Et nous considérons le cas où $a_{6} = \left[\frac{n}{10}\right] + 1$. Cette distribution est possible en posant:

$$\begin{equation}
\left\{
    \begin{array}{l}
    a_{k} = k, \quad \textrm{pour tout} \quad k \in \{1, 2, 3, 4, 5\}\\
    a_{6} = \left[\frac{n}{10}\right] + 1\\
    a_{k} = a_{6} + (k - 6), \quad \textrm{pour tout} \quad k \in \{7, 8, 9\}\\
    a_{10} = n - \sum_{k=1}^{9} a_{k} = n - (1 + 2 + 3 + 4 + 5) - (4a_{6} + (1 + 2 + 3))
    \end{array}
\right.
\label{equation-def-exp-distsup140}
\end{equation}$$

En effet:

\[a_{10} \geq n - 21 - 4*(\frac{n}{10} + 1) \implies a_{10} \geq 6*(\frac{n}{10}) - 25\]

\[a_{10} - (a_{9} + 1) \geq 6*(\frac{n}{10}) - 25 - (a_{9} + 1) \geq 6*(\frac{n}{10}) - 25 - (\left[\frac{n}{10}\right] + 4 + 1) \]

Or,

\[-\left[\frac{n}{10}\right] \geq -\frac{n}{10}\]

Et vu que $n > 140$,

\[a_{10} - (a_{9} + 1) \geq 5*(\frac{n}{10} - 6) > 5*(14 - 6) > 0 \implies a_{10} > a_{9} \]

On obtient une distribution de timbres $\{a_{1}, a_{2}, ..., a_{10}\}$ sur les $10$ pages suivant la numérotation de la remarque numérotation des pages suivant le nombre de timbres.

En écrivant:

$$\begin{equation}
n = 10.(14+a) + b \quad \textrm{avec} \quad a > 0 \quad \textrm{et} \quad 0 < b \leq 9
\label{equation-dec-nsup140}
\end{equation}$$

On obtient:

$$\begin{equation}
a_{6} = 14 + a + 1 = 15 + a \quad \textrm{avec} \quad a > 0
\label{equation-dec-a6}
\end{equation}$$

$$\begin{equation}
n = 10a_{6} + b - 10 \quad \textrm{avec} \quad b > 0
\label{equation-dec-n-a6}
\end{equation}$$

Si $b \leq 5$, on prend:

$$\begin{equation}
\left\{
    \begin{array}{l}
    a_{6} = \left[\frac{n}{10}\right] + 1\\
    a_{1} = a_{6} + b - 10\\
    a_{k} = a_{6} + (k - 6), \quad \textrm{pour tout} \quad k \in \{2, 3, 4, 5, 7, 8, 9, 10\}
    \end{array}
\right.
\label{equation-def-exp-distsup140-binf5}
\end{equation}$$

On a:

\[a_{1} + ... + a_{10} = 6a_{6} + (b - 10) - (1+ 2 + 3 + 4) + 4a_{6} + (1 + 2 + 3 + 4) \]

\[a_{1} + ... + a_{10} = 10a_{6} + b - 10 = n \]

Et:

\[a_{7} + a_{8} + a_{9} + a_{10} = 4a_{6} + 10 = 4(15 + a) + 10 \]

\[a_{7} + a_{8} + a_{9} + a_{10} = 4a + 70\]

\[a_{7} + a_{8} + a_{9} + a_{10} - \frac{n}{2} = 4a + 70 - 5(14 + a) - \frac{b}{2} \]

\[a_{7} + a_{8} + a_{9} + a_{10} - \frac{n}{2} = - a - \frac{b}{2} < 0 \quad \textrm{car} \quad a > 0 \quad \textrm{et} \quad b > 0 \]

\[a_{7} + a_{8} + a_{9} + a_{10} < \frac{n}{2}\]

Donc:

$$\begin{equation}
a_{i} + a_{j} + a_{k} + a_{l} < \frac{n}{2} \quad \forall i, j, k, l \in \{1, ..., 10\}
\label{equation-ineq-sumfour-distsup140-binf5-ndiv2}
\end{equation}$$

Si $b > 5$, on pose:

$$\begin{equation}
\left\{
    \begin{array}{l}
    a_{6} = \left[\frac{n}{10}\right] + 1\\
    a_{k} = a_{6} + (k - 6), \quad \textrm{pour tout} \quad k \in \{1, 2, 3, 4, 5\}\\
    a_{k} = a_{6} + (k - 6) + \delta_{b - 5 > 10 - l}, \quad \textrm{pour tout} \quad k \in \{7, 8, 9, 10\}\\
    \end{array}
\right.
\label{equation-def-exp-distsup140-bsup5}
\end{equation}$$

On a:

\[a_{1} + ... + a_{10} = 6a_{6} - (1+ 2 + 3 + 4 + 5) + 4a_{6} + (1 + 2 + 3 + 4) + (b - 5)\]

\[a_{1} + ... + a_{10} = 10a_{6} + b - 10 = n \]

Et:

\[a_{7} + a_{8} + a_{9} + a_{10} = 4a_{6} + 10 + (b - 5) = 4(15 + a) + 10 + (b - 5) \]

\[a_{7} + a_{8} + a_{9} + a_{10} = 4a + 65 + b\]

\[a_{7} + a_{8} + a_{9} + a_{10} - \frac{n}{2} = 4a + 65 + b - 5(14 + a) - \frac{b}{2} = \frac{b}{2} - 5 - a\]

Donc:

\[a_{7} + a_{8} + a_{9} + a_{10} - \frac{n}{2} \leq \frac{9}{2} - 5 - a = -\frac{1}{2} - a < 0 \quad \textrm{car} \quad a > 0 \quad \textrm{et} \quad b \leq 9\]

\[a_{7} + a_{8} + a_{9} + a_{10} < \frac{n}{2}\]

!!! abstract "Equation inégalité somme quatre (pour b > 5)"

    $$\begin{equation}
    a_{i} + a_{j} + a_{k} + a_{l} < \frac{n}{2} \quad \forall i, j, k, l \in \{1, ..., 10\}
    \label{equation-ineq-sumfour-distsup140-bsup5-ndiv2}
    \end{equation}$$

Ainsi, à l'aide de l'équation inégalité somme quatre (pour b < 5) et de l'équation inégalité somme quatre (pour b > 5), on a:

!!! abstract "Equation inégalité somme quatre distribution supérieure à $140$"

    $$\begin{equation}
    \textrm{Pour} \quad n > 140, \quad \forall i, j, k, l \in \{1, ..., 10\} \quad a_{i} + a_{j} + a_{k} + a_{l} < \frac{n}{2}
    \label{equation-ineq-sumfour-distsup140-ndiv2}
    \end{equation}$$

L'équation d'inégalité somme quatre distribution supérieure à $140$ et le fait que pour $n=140$ et pour toute distribution de timbres parmi les dix pages, il existe toujours quatre pages telles que le total de timbres est supérieur à $\frac{n}{2}$, nous permet de déduire que si l'assertion: pour tout arrangement $(a_{1}, ..., a_{10})$, il existe toujours quatre éléments tels que le total est supérieur à $\frac{n}{2}$ est vraie alors la valeur maximale de $n$ est $140$.

!!! warning "Comment trouver la valeur maximale de $n$"

    Dans les conditions de ce problème, pour déterminer la valeur maximale de $n$, l'on peut se baser sur les deux premiers résultats démontrés ci-dessus, à savoir montrer que:

    \[45 \leq n \leq 180\]

    Puis, en descendant de proche en proche la borne supérieure de la valeur de $n$ et essayant de trouver le cas échéant une distribution des timbres telle que tout ensemble de quatre pages a une somme totale de timbres inférieure strictement à $\frac{n}{2}$.

    Enfin, si l'on connaît la valeur maximale de $n$ d'avance, l'on pourrait se contenter de le démontrer.
