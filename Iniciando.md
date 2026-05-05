
Para hacer un primer filtro de que features considerar al inicio, porque podriamos tener miles, se rankean en base a una **metrica de utilidad de feature**, 

The metric we'll use is called "mutual information". Mutual information is a lot like correlation in that it measures a relationship between two quantities. The advantage of mutual information is that it can detect _any_ kind of relationship, while correlation only detects _linear_ relationships.

Mutual information is a great general-purpose metric and especially useful at the start of feature development when you might not know what model you'd like to use yet. It is:

- easy to use and interpret,
- computationally efficient,
- theoretically well-founded,
- resistant to overfitting, and,
- able to detect any kind of relationship