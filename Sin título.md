
**MSSubClass**:contar los que tengan la misma cantidad de pisos igual y crear una feature que indique si estan sin terminar. Analizar similitud con HouseStyle.

**MSZoning**: dividir en 2 features, una para las de zona comercial( label encoding ) y otra para el resto.

**LotFrontage y LotArea**: hacer un ratio

**Alley**: Imputar todos los NaN como su propio valor.

**LotShape**:Label encoding

**LandContour**: OHE


**Utilities**: label encoding

**LandSlope**: label encoding

**LandSlope y LandContour:** Analizar en mayor profundidad

**Neighborhood**: OHE o TargetEncoding 

**Condition1 y Condition2**: juntar y encodear.

**BldgType**: OHE

**HouseStyle**: contar los que tengan la misma cantidad de pisos igual y crear una feature que indique si estan sin terminar.Analizar similitud con MSSubClass.

**OverallQual**: label encoding

**OverallCond**: label encoding


**YearBuilt**: Dejar como continuo 

**YearRemodAdd**: Crear un nuevo feature binario "remodelado", encodear como el anterior

**RoofStyle:** OHE

**RoofMatl**: OHE

**Exterior1 y Exterior2**: juntar y encodear.


**MasVnrType**: OHE y codear los NaN como su propio vlaor.

**MasVnrArea**: Imputar basado en MasVnrType.

**ExterQual**: label encoding

**ExterCond**: label encoding


**Foundation**: OHE

**BsmtQual**: label encoding e imputar como su propio valor

**BsmtCond**: label encoding e imputar como su propio valor

**BsmtExposure**: label encoding (Unfinished -1) e imputar como su propio valor y BsmtCond

**BsmtFinType1 y BsmtFinType2**: juntar y encodear. e  imputar como su propio valor y BsmtCond

**BsmtFinType1** y **BsmtFinSF1**: interactuar 

**BsmtFinType2** y **BsmtFinSF2**: interactuar 

**Heating**: OHE

**HeatingQC**: label encoding

Heating, HeatingQC y  CentralAir: unir y codear

**Electrical**: OHE e imputar con moda


**Functional**: label encoding

**FireplacesQual**: imputar como propio valor.


**GarageYrBlt**:probar label encoding( el primer ano del que tengamos registro es 0, cualquier dato menor es -1, cualquier dato mayor al mayor dato registrado es  el mayor +1) o Target Encoding . imputar con 0 para los que no tienen.

**GarageType**: OHE e imputar como propio valor.

**GarageFinish**: LABEL ENCODING

**GarageCars y GarageArea**: analizar redundancia

**GarageQual**: label encoding e imputar como propio valor.

**GarageCond**: label encoding e imputar como propio valor.




**PoolQC** : label encoding e imputar como propio valor.



**Fence**: label encoding e imputar como propio valor.

**MiscFeature**: OHE e imputar como propio valor.

**MoSold**: aplicar cos y sin para representar comportamiento ciclico

**YrSold**: dejar como numerico

**SaleType:** OHE

**SaleCondition**:OHE

