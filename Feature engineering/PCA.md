PCA es una tecnica de reduccion de dimensionalidad que usa algebra linear para reducir la cantidad de features pero conservando la mayor cantidad de varianza(datos).

Calcula los autovectores y sus autovalores de la matriz de covarianza, selecciona aquellos con mayor autovalor y proyecta los datos sobre estos para simplificar los datos.

PCA identifica los ejes sobre los cuales los datos se extienden mas:

- ***1st Principal Component (PC1):** Direccion de mayor varianza( mas dispersos ).
- **2nd Principal Component (PC2):** La segunda direccion de mayor varianza, **perpendicular a PC1** y asi.

Estas direcciones vienen de los autovectores de la matriz de covarianza y sus importancia de los respectivos autovalores. Para una matriz cuadrada A un autovector X( no cero ) y su autovector λ cumplen:

	AX = λX


Significa:
- Cuando A afecta a X solo lo estira o acorta por λ.
- La direccion de X permanece fijo por lo que los autovectores dan direcciones estables para A. 


Los autovalores sirven para ordenarlos por importancia. 


## **Ventajas**

1. **Multicolineridad**: Crea nuevos features sin correlacion por lo que elimina esto.
2. **Reduccion de ruido** Elimina features poco relevantes dejando datos mas claros.
3. **Compresion de datos:*** Acelera todo el proceso y ocupa menos espacio porque tenemos menos features.
4. ***Deteccion de outliers*** Identifica outliers al mostrarlos en el espacio reducido.

## ***Desventajas***

1. **Dificil de explicar** Son mezclas de los datos por lo que es mas dificil de explicar.
2. **Sensibilidad a escala** Es necesario escalar los datos
3. **Perdida de datos** Si reducimos la dimensionalidad de mas podemos perder informacion util.
4. **Asume linearidad** Si los datos son no lineares sufre.
5. **Caro** Es computacionalmente lento y caro.