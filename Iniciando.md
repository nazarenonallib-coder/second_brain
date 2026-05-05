
Para hacer un primer filtro de que features considerar al inicio, porque podriamos tener miles, se rankean en base a una **metrica de utilidad de feature**, como **mutual information**(para todo) y el **test de independencia de chi cuadrado**.(categorico y categorico )

**Mutual Information** es el crack para empezar:
- Facil y rapido de usar.
- Eficiente.
- Bien fundado.
- Detecta cualquier tipo de relacion

Los valores de **MI** van desde 0.0 a infinito, aunque mayor a 2.0 es raro, 0 es independecia total.

Para chi cuadrado:
Si el _valor-p_ es mayor a 0.05 se considera una asociación significativa. Valores altos indican mayor desviación de la independencia. 