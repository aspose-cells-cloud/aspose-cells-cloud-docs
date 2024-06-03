---
title: Opción de cálculo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/calculationoptions/
description: "Aspose.Cells Especificación del modelo de nube: Opciones de cálculo. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Cloud REST API, Opciones de cálculo
weight: 50
---
## **Opciones de cálculo**

 Representa opciones de cálculo.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Tamaño de pila de cálculo| Entero| Verdadero| FALSO|| Especifica el tamaño de la pila para calcular celdas de forma recursiva.|
| Ignorar error| Booleano| Verdadero| FALSO|| Indica si se deben ignorar los errores encontrados al calcular las fórmulas. El error puede ser una función no compatible, enlaces externos, etc. El valor predeterminado es verdadero.|
| Estrategia de precisión| Cadena| Verdadero| FALSO|| Especifica la estrategia para procesar la precisión del cálculo.|
| recursivo| Booleano| Verdadero| FALSO|| Indica si calcula las celdas dependientes de forma recursiva al calcular una celda y depende de otras celdas. El valor por defecto es verdadero.|
| Motor personalizado|Clase: motor de cálculo abstracto| Verdadero| FALSO|| El motor de cálculo de fórmulas personalizado para ampliar el motor de cálculo predeterminado de Aspose.Cells.|
| Monitor de cálculo| Clase: Monitor de cálculo abstracto| Verdadero| FALSO|| El monitor para que el usuario realice un seguimiento del progreso del cálculo de la fórmula.|
| Fuentes de datos vinculados|Formación<Class:Workbook> | Verdadero| FALSO|| Especifica las fuentes de datos para enlaces externos utilizados en fórmulas.|

