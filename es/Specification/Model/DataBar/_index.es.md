---
title: Base de datos
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/databar/
description: "Aspose.Cells Especificación del modelo de nube: DataBar. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Nube REST API, Barra de datos
weight: 50
---
## **barra de datos**

 Describe la regla de formato condicional de DataBar. Esta regla de formato condicional muestra una barra de datos graduada en el rango de celdas.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Color del eje| Clase:Color| Verdadero| FALSO|| Obtiene el color del eje de las celdas con formato condicional como barras de datos.|
| Posición del eje| Cadena| Verdadero| FALSO|| Obtiene o establece la posición del eje de las barras de datos especificadas por una regla de formato condicional.|
| BarFrontera| Clase:Borde de barra de datos| Verdadero| FALSO|| Obtiene un objeto que especifica el borde de una barra de datos.|
| Tipo de relleno de barra| Cadena| Verdadero| FALSO|| Obtiene o establece cómo se rellena de color una barra de datos.|
| Color| Clase:Color| Verdadero| FALSO|| Obtenga o establezca el color de esta barra de datos.|
| Dirección| Cadena| Verdadero| FALSO||Obtiene o establece la dirección en la que se muestra la barra de datos.|
| MaxCfvo| Clase: Valor de formato condicional| Verdadero| FALSO|| Obtenga o establezca el objeto de valor máximo de esta DataBar. No se puede establecer null o CFValueObject con el tipo FormatConditionValueType.Min.|
| Longitud máxima| Entero| Verdadero| FALSO|| Representa la longitud máxima de la barra de datos.|
| MinCfvo| Clase: Valor de formato condicional| Verdadero| FALSO|| Obtenga o establezca el objeto de valor mínimo de esta DataBar. No se puede establecer null o CFValueObject con el tipo FormatConditionValueType.Max.|
| Longitud mínima| Entero| Verdadero| FALSO|| Representa la longitud mínima de la barra de datos.|
| Formato de barra negativa| Clase: formato de barra negativa| Verdadero| FALSO|| Obtiene el objeto NegativeBarFormat asociado a una regla de formato condicional de la barra de datos.|
| Mostrar valor| Booleano| Verdadero| FALSO|| Obtenga o establezca la bandera que indica si se muestran los valores de las celdas sobre las que se aplica esta barra de datos. El valor predeterminado es verdadero.|

