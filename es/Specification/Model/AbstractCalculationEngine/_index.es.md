---
title: ResumenCálculoEngin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/abstractcalculationengine/
description: "Aspose.Cells Especificación del modelo de nube: AbstractCalculationEngine. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Nube REST API, AbstractCalculationEngine
weight: 50
---
## **motor de cálculo abstracto**

Representa el motor de cálculo personalizado del usuario para ampliar el motor de cálculo predeterminado de Aspose.Cells.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralRequired| Booleano| Verdadero| FALSO|| Indica si este motor necesita el texto literal del parámetro mientras realiza el cálculo. El valor predeterminado es falso.|
| IsParamArrayModeRequired| Booleano| Verdadero| FALSO|| Indica si este motor necesita que el parámetro se calcule en modo matriz. El valor predeterminado es falso. Si es necesario al calcular funciones personalizadas, esta propiedad debe establecerse como verdadera.|
| Funciones integradas del proceso| Booleano| Verdadero| FALSO|| Esta implementación debe verificar y procesar las funciones integradas que han sido admitidas por el motor integrado. El valor predeterminado es falso. Si el usuario necesita cambiar la lógica de cálculo de algunas funciones integradas, esta propiedad debe establecerse como verdadera. De lo contrario, deje esta propiedad como falsa para considerar el rendimiento.|

