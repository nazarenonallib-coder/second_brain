El algoritmo LOF funciona comparando la densidad de un punto de datos con la de sus vecinos circundantes. Para ello, mide la distancia entre un punto de datos y sus k vecinos más cercanos. El LOF de un punto de datos se define como la relación entre la densidad promedio de sus k vecinos más cercanos y su propia densidad. Los puntos de datos con un valor LOF bajo se consideran normales, mientras que aquellos con un valor LOF alto se consideran valores atípicos.


**NOTA**: Es susceptible a la maldicion de la dimensionalidad, no super sensible, pero a consideracion.
