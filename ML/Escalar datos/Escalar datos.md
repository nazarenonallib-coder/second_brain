Escalar datos es poner los datos continuos en una misma escala de tal manera que estas no afecten en el resto de procesos.

No escalar, o estandarizar datos, hace que la mayoria de modelos y procesos(como SVM o los analisis de varianza) pierdan eficacia o den datos poco veraces.

Como primera opción se pueden usar el **StandardScaler o el MinMaxScaler** de sklearn, que  son las opciones mas simples. 

Sin embargo, el **RobustScaler** es resistente a outliers y puede ser mejor opcion por esto mismo.



**Utilice MinMaxScaler cuando:**

- Sus datos tengan un rango conocido y significativo (p. ej., porcentajes, calificaciones).
- Necesita una salida acotada para redes neuronales con funciones de activación específicas.
- No haya valores atípicos significativos en su conjunto de datos.
- Realice procesamiento de imágenes donde los valores de los píxeles tengan límites naturales.

**Utilice StandardScaler cuando:**

- Sus datos tengan una distribución aproximadamente normal.
- Utilice algoritmos que funcionan bien con datos con media cero y varianza unitaria.
- No haya valores atípicos significativos que afecten los cálculos de la media/desviación estándar.

- Desee una interpretación sencilla (los valores representan desviaciones estándar con respecto a la media).

**Utilice RobustScaler cuando:**

- Sus datos contengan valores atípicos que no pueda o no deba eliminar.
- Sus datos estén sesgados, pero desee preservar la forma de la distribución.

- Se encuentre en fases exploratorias y no esté seguro de la calidad de los datos.

- Trabaje con datos financieros, de análisis web u otros datos complejos del mundo real.