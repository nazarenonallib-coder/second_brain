Podemos usar modelos no supervisados, normalmente k-neighbours,  para representar la estructura de los datos agrupando.

Sirve para crear grupos similares basando en features espaciales o cercanas.

**K-means**
A pesar de que hay muchos modelos de clustering, difieren en como miden distancias, k-means usa la distancia euclidiana.
Crea k centroides ( ¨centro¨ de un cluster) y asigna cada punto de datos al centroide mas cercanos, creando asi los clusters.
Una vez determinado el lugar de los centroides se crea un hiperplano que divide el espacio de cada cluster ( Teselación de Voronoi) del de los otros y es lo que se usa para calcular futuros datos.

El proceso de entrenamiento es asi:
- inicializamos aletoriamente k centroides.
- Asignas los puntos al centroide mas cercano
- Moves los centroides para minimizar la distancia a sus puntos.
- Repetís para reducir varianza.

**K se suele calcular con cross validation**