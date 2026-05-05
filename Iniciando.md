
Para hacer un primer filtro de que features considerar al inicio, porque podriamos tener miles, se rankean en base a una **metrica de utilidad de feature**, como **mutual information**(para todo) y el **test de independencia de chi cuadrado**.(categorico y categorico )



Mutual information is a great general-purpose metric and especially useful at the start of feature development when you might not know what model you'd like to use yet. It is:

- easy to use and interpret,
- computationally efficient,
- theoretically well-founded,
- resistant to overfitting, and,
- able to detect any kind of relationship