Targete encoding es cualquier tipo de encoding que utilice el target.
Una manera facil es usar agregacion por grupo como la media, mismas consideraciones.

Tiene muchos nombres : mean, likelihood encoding, impact encoding, and leave-one-out encoding.

Hay varios problemas al usar esto, categorias raras y desocnocidas, si aparece una desconocida el codigo no va a funcionar y las raras suelen ser poco precisas.

Una solucion es usar suavizado, mezclar la media de la categoria con la media global. Las desconocidas usan la global y las raras tienen poco efecto.

En pseudocode:

```
encoding = weight * in_category + (1 - weight) * overall
```

donde `weight` es un valor entre 0 y 1 calculado de la frequencia.

una manera de calcular weight

```
weight = n / (n + m)
```

donde n es la frcuencia y m es un factor de suavizado, mas alto mas importa la media global.

**casos de uso**
