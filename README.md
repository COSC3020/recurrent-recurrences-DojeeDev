# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
```math
 T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
```
Solution to 1:

$T(n) = T(n/13)+5$

$=(T(n/13^2)+5)+5$

...

i = lg n

$=T(n/13^i)+5i$

$=T(1)+5\log n \in \Theta(\log n)$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Solution to 2:

$T(n) = 13T(n/13) +5$

$= 13(13T(n/13^2)+5/13)+5$

$= 13^2T(n/13^2)+10$

...

i = lg n

$= 13^i T(n/13^i) + 5i$

$= nT(1) + 5 \log n \in \Theta(n)$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

Solution to 3:

$T(n) = 13T(n/13) + 2n$

$= 13(13T(n/13^2)+\frac{2n}{13}) + 2n$

$= 13^2 T(n/13^2) +4n$

...

i = log n

$=13^i T(n/13^i) + (2n)i$

$nT(1)+ 2n \log n \in \Theta(n \log n)$



I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
