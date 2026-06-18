## Proceso de Machine Learning según Hands-on Machine Learning

Según Aurélien Géron, el proceso típico de un proyecto de ML incluye estos pasos:

### 1. **Definir el Problema (Frame the Problem)**

- Definir el objetivo del negocio
- Determinar el tipo de problema (supervisado/no supervisado, clasificación/regresión, batch/online)
- Seleccionar métricas de rendimiento
- Verificar supuestos

### 2. **Obtener los Datos (Get the Data)**

- Listar fuentes de datos
- Obtener acceso y familiarizarse con el espacio de datos
- Tomar una muestra para exploración si el dataset es muy grande
- Crear un conjunto de prueba y guardarlo aparte

### 3. **Explorar los Datos (Explore the Data - EDA)**

- Crear copias de los datos para experimentación
- Estudiar cada atributo y sus características
- Visualizar los datos
- Estudiar correlaciones
- Identificar transformaciones prometedoras

### 4. **Preparar los Datos (Prepare the Data)**

- Limpiar los datos (valores faltantes, outliers)
- Feature engineering
- Feature selection
- Normalización/estandarización
- Transformaciones

### 5. **Seleccionar y Entrenar Modelos (Select and Train Models)**

- Entrenar varios modelos diferentes
- Usar validación cruzada
- Analizar errores más significativos
- Feature importance

### 6. **Afinar el Modelo (Fine-tune the Model)**

- Grid search o random search para hiperparámetros
- Ensemble methods
- Analizar los mejores modelos y sus errores
- Evaluar el sistema en el test set

### 7. **Presentar la Solución**

- Documentar el proceso
- Crear visualizaciones y presentaciones
- Destacar hallazgos clave

### 8. **Lanzar, Monitorear y Mantener**

- Preparar para producción
- Monitoreo de rendimiento
- Sistemas de alerta
- Reentrenamiento periódico

---

## Proceso de Análisis Exploratorio de Datos (EDA)

### Según Hands-on ML y ISLP

#### **1. Primera Inspección de los Datos**

**Hands-on ML:**

- `data.head()`, `data.info()`, `data.describe()`
- Verificar tipos de datos
- Identificar valores faltantes
- Examinar distribuciones con `value_counts()`

**ISLP:**

- Resúmenes numéricos: media, mediana, varianza, cuartiles
- Identificar la naturaleza de las variables (cuantitativas vs cualitativas)
- Examinar el rango y escala de cada variable

#### **2. Visualización Univariada**

**Histogramas:**

- Distribución de variables continuas
- Identificar sesgos, multimodalidad, outliers

**Gráficos de Barras:**

- Frecuencias de variables categóricas

**Box Plots:**

- Identificar outliers y dispersión
- Comparar distribuciones entre grupos

#### **3. Análisis de Correlaciones**

**Hands-on ML:**

- Matriz de correlación: `data.corr()`
- Heatmaps de correlación
- Scatter plots para pares de variables importantes

**ISLP:**

- Correlación de Pearson para relaciones lineales
- Scatter plot matrix (pairplot) para múltiples variables
- Análisis de colinealidad

#### **4. Visualización Multivariada**

- Scatter plots con color para tercera variable
- Facet grids para comparar distribuciones por categorías
- Parallel coordinates para datasets multidimensionales

#### **5. Detección de Problemas**

- Valores faltantes: patrones y magnitud
- Outliers: estadísticos o gráficos
- Duplicados
- Inconsistencias en los datos

#### **6. Análisis de la Variable Objetivo**

**Para Regresión:**

- Distribución de la variable objetivo
- Transformaciones si es necesario (log, sqrt)

**Para Clasificación:**

- Balance de clases
- Necesidad de técnicas de balanceo

---

## Guía de Comparación de Variables

### **1. Variable Numérica vs Variable Numérica**

#### **Métodos:**

**Correlación de Pearson:**

```
- Rango: -1 a 1
- Mide relación lineal
- r > 0.7: fuerte positiva
- 0.3 < r < 0.7: moderada
- r < 0.3: débil
```

**Scatter Plot:**

- Visualizar relación no lineal
- Identificar clusters o patrones
- Detectar outliers influyentes

**Correlación de Spearman:**

- Para relaciones monótonas no lineales
- Más robusta a outliers

#### **Interpretación:**

- Correlación ≠ causalidad
- Verificar confounders (variables confusoras)
- Buscar relaciones no lineales que Pearson no captura

---

### **2. Variable Categórica vs Variable Numérica**

#### **Métodos:**

**Box Plots por Categoría:**

- Comparar distribuciones
- Identificar diferencias en medianas
- Detectar outliers por grupo

**Violin Plots:**

- Muestra distribución completa
- Mejor para ver multimodalidad

**Pruebas Estadísticas:**

_Para 2 grupos:_

- **t-test:** si distribuciones son normales
- **Mann-Whitney U:** si no son normales

_Para 3+ grupos:_

- **ANOVA:** si distribuciones son normales y varianzas homogéneas
- **Kruskal-Wallis:** alternativa no paramétrica

**ANOVA (Analysis of Variance):**

```
H0: Las medias de todos los grupos son iguales
p < 0.05: Rechazar H0 (hay diferencias significativas)
```

#### **Interpretación:**

- Verificar supuestos de normalidad (Shapiro-Wilk)
- Verificar homogeneidad de varianzas (Levene)
- Considerar tamaño de efecto, no solo p-values

---

### **3. Variable Categórica vs Variable Categórica**

#### **Métodos:**

**Tabla de Contingencia (Crosstab):**

python

```python
pd.crosstab(df['var1'], df['var2'], margins=True)
```

**Heatmap de Frecuencias:**

- Visualizar patrones de asociación

**Chi-cuadrado (χ²):**

```
H0: Las variables son independientes
p < 0.05: Rechazar H0 (hay asociación)
```

**Cramér's V:**

- Mide fuerza de asociación (0 a 1)
- 0: sin asociación
- 1: asociación perfecta

**Coeficiente de Contingencia:**

- Alternativa a Cramér's V
- Menos intuitivo pero útil para tablas grandes

#### **Interpretación:**

- Chi-cuadrado sensible al tamaño de muestra
- Verificar frecuencias esperadas ≥ 5
- Cramér's V da magnitud del efecto

---

### **4. Comparaciones Avanzadas**

#### **Variable Numérica vs Múltiples Variables**

**Regresión Simple:**

- Cuantificar relación lineal
- R²: proporción de varianza explicada

**Correlación Parcial:**

- Controlar por otras variables
- Aislar efecto de una variable específica

#### **Variable Categórica (Ordinal) vs Variable Numérica**

**Correlación de Spearman:**

- Trata categorías ordinales como rankings

**Prueba de Tendencia:**

- Jonckheere-Terpstra test
- Detecta tendencias monótonas

#### **Análisis Temporal**

**Series de Tiempo:**

- Autocorrelación (ACF)
- Correlación cruzada (CCF)
- Pruebas de estacionariedad

---

### **Tabla Resumen de Métodos**

|Tipo 1|Tipo 2|Visualización|Métrica/Test|Interpretación|
|---|---|---|---|---|
|**Numérica**|**Numérica**|Scatter plot|Pearson r|Relación lineal|
|**Numérica**|**Numérica**|Scatter plot|Spearman ρ|Relación monótona|
|**Categórica**|**Numérica**|Box plot|t-test/ANOVA|Diferencia de medias|
|**Categórica**|**Numérica**|Violin plot|Mann-Whitney/Kruskal|Diferencia de distribuciones|
|**Categórica**|**Categórica**|Heatmap|Chi-cuadrado χ²|Independencia|
|**Categórica**|**Categórica**|Mosaic plot|Cramér's V|Fuerza de asociación|
|**Ordinal**|**Numérica**|Box plot ordenado|Spearman ρ|Tendencia monótona|
|**Múltiples**|**Numérica**|Pair plot|Matriz de correlación|Relaciones múltiples|

---

### **Consideraciones Importantes**

#### **Tamaño de Muestra:**

- n < 30: Usar tests no paramétricos
- n grande: Diferencias pequeñas pueden ser significativas estadísticamente pero no prácticamente

#### **Outliers:**

- Afectan correlación de Pearson y t-tests
- Usar métodos robustos (Spearman, mediana) si hay outliers

#### **Normalidad:**

- Verificar con Shapiro-Wilk o Q-Q plots
- Transformaciones: log, sqrt, Box-Cox

#### **Significancia vs Importancia Práctica:**

- p-value < 0.05 no significa que el efecto sea grande o útil
- Calcular tamaño de efecto (Cohen's d, R², η²)
- Considerar contexto del dominio