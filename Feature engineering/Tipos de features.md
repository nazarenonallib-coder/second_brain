**Consideraciones clave para pensar features:**
- Entender tus features, referirte a la documentación si la tenes.
- Hace investigación del dominio del problema. Wikipedia esta bien pero consulta con expertos y lee artículos .
- Estudia trabajos similares para sacar insight
- Visualiza la data, te va a aclarar o permitir ver cosas.

**Transformaciones matemáticas**
Crear ratios, usar logaritmos con distribuciones sesgadas y aplicar formulas aprendidas de la investigación.
Sumas, diferencias, productos, etc.

**Cuentas**
Las features qeu muestran la presencia o ausencia de cosas suelen venir en grupos, para tratar con estos grupos podes juntar estas features usando una **Cuenta**.
Estos features van a ser binarios o booleanos.

	**Ejemplo:**
	features: ['isFat', 'isOld', 'isChild'...]
	count: 'factores de riesgo'


**Construir y romper features**
podes romper en partes mas chicas cosas que sigan un patrón y tengan partes claramente diferenciadas, también podes unir cosas que crees que tienen una relación.

Se pueden separar fechas en días, meses y años.
O se pueden unir coordenadas longitudinales y latitudinales para crear posiciones.

**Transformaciones de grupo**
Estas juntan informacion entre distintas filas agrupadas por una categoria. Se pueden crear cosas como "Sueldo promedio por estado" o "Proporcion hombre mujer en distintos paises.".
Si descubriste una interaccion por categoria es buena investigar una interaccion de grupo.

Usando una funcion de agregacion, una transformacion de grupo combina una feature categorica(  por la que agrupamos ) y otra( la que agrupamos ). En el caso de "Sueldo promedio por estado", 'Estado' es la agrupadora, la media es la funcion de agregacion y 'Sueldo' la agregada.

Con esto se debe tener mucho cuidado de no hacer data leakeage. 
- **La feature se calcula solo en el train pero se aplica a todo**
- **La feature no usa datos de la fila para la que esta calculando** ( la feature se calcula para cada fila pero sin incluirla misma )