**MSSubClass**:contar los que tengan la misma cantidad de pisos igual y crear una feature que indique si estan sin terminar. Analizar similitud con HouseStyle.

**MSZoning**: dividir en 2 features, una para las de zona comercial( label encoding ) y otra para el resto.

**LotFrontage y LotArea**: hacer un ratio

Alley y Street: juntar y encodear

**LotShape**:Label encoding

**LandContour**: OHE

LotShape y LandContour: juntar y encodear

**Utilities**: label encoding

**LandSlope**: label encoding

**LandSlope y LandContour:** Analizar en mayor profundidad

**Neighborhood**: OHE o TargetEncoding 

**Condition1 y Condition2**: juntar y encodear.

**BldgType**: OHE

**HouseStyle**: contar los que tengan la misma cantidad de pisos igual y crear una feature que indique si estan sin terminar.Analizar similitud con MSSubClass.

**OverallQual**: label encoding

**OverallCond**: label encoding

OverallCond y OverallQual: junat y encodear.

**YearBuilt**: probar label encoding( el primer ano del que tengamos registro es 0, cualquier dato menor es -1, cualquier dato mayor al mayor dato registrado es  el mayor +1) o Target Encoding 

**YearRemodAdd**: Crear un nuevo feature binario "remodelado", encodear como el anterior

**RoofStyle:** OHE

**RoofMatl**: OHE

**Exterior1 y Exterior2**: juntar y encodear.

Exterior1, Exterior2 y MasVnrType: juntar y encodear

MasVnrType: OHE

**ExterQual**: label encoding

**ExterCond**: label encoding

ExterCond y ExterQual: junat y encodear.

Foundation: OHE

**BsmtQual**: label encoding

**BsmtCond**: label encoding

**BsmtExposure**: label encoding (Unfinished -1)

BsmtCond, BsmtExposure y BsmtQual: junat y encodear.

**BsmtFinType1 y BsmtFinType2**: juntar y encodear.

**BsmtFinType1** y **BsmtFinSF1**: interactuar 

**BsmtFinType2** y **BsmtFinSF2**: interactuar 

BsmtUnfSF, BsmtFinSF1 y BsmtFinSF2: calcular porcentaje para cada uno

**Heating**: OHE

**HeatingQC**: label encoding

Heating y HeatingQC: unir y codear

Heating, HeatingQC y  CentralAir: unir y codear

**Electrical**: OHE

1stFlrSF Y 2ndFlrSF: sumar

LowQualFinSF, 1stFlrSF Y 2ndFlrSF: porcentaje de area de mala calidad

BsmtFullBath y BsmtHalfBath: sumar pesado(Full suma 1 y half suma 0.5)

FullBath y HalfBath: sumar pesado(Full suma 1 y half suma 0.5)




