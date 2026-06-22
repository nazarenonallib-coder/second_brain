Los outliers son valores atipicos en nuestra distribucion, es decir valores que estan lejos de los otros y son raros. Estos empeoran el rendimiento de la mayoria de modelos e interfieren en la mayoria de metodos de analisis.

En casos de **baja dimensionalidad**:
- Box Plot
- z-score
- Tukey

En casos de **alta dimensionalidad** tenemos que usar un modelo solo para detectarlos:
- Isolation Forest (super eficiente)
- Autoencoders (datos muy complejos)
- Local Outlier Factor (No tan eficiente)

Tambien se puede ***reducir la dimensionalidad*** para reducir coste computacional mediante **PCA**


