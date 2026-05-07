PCA es una tecnica de reduccion de dimensionalidad que usa algebra linear para reducir la cantidad de features pero conservando la mayor cantidad de varianza(datos).

Calcula los autovectores y sus autovalores de la matriz de covarianza, selecciona aquellos con mayor autovalor y proyecta los datos sobre estos para simplificar los datos.

PCA identifica los ejes sobre los cuales los datos se extienden mas:

- ***1st Principal Component (PC1):** Direccion de mayor varianza( mas dispersos ).
- **2nd Principal Component (PC2):** La segunda direccion de mayor varianza, **perpendicular a PC1** y asi.

Estas direcciones vienen de los autovectores de la matriz de covarianza y sus importancia de los respectivos auto 

These directions come from the eigenvectors of the covariance matrix and their importance is measured by eigenvalues. For a square matrix A an eigenvector X (a non-zero vector) and its corresponding eigenvalue λ satisfy:

> AX = \lambda X

This means:

- When __A__ acts on X it only stretches or shrinks X by the scalar λ.
- The direction of X remains unchanged hence eigenvectors define "stable directions" of A.

Eigenvalues help rank these directions by importance.