---
title: Opción de copia
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/copyoptions/
description: "Aspose.Cells Especificación del modelo de nube: CopyOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **opciones de copia**

 Representa las opciones de copia.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Ancho de carácter de columna| Booleano| Verdadero| FALSO||Indica si se copia el ancho de columna en unidades de caracteres.|
| Copiar fórmulas no válidas como valores| Booleano| Verdadero| FALSO|| Si la fórmula no es válida para el destino, solo copie los valores.|
| Copiar nombres| Booleano| Verdadero| FALSO|| Indica si se copian los nombres.|
| Extender al rango adyacente| Booleano| Verdadero| FALSO|| Indica si se extienden los rangos al copiar el rango al rango adyacente.|
| Consulte la hoja de destino| Booleano| Verdadero| FALSO|| Al copiar el rango en el mismo archivo y el gráfico hace referencia a la hoja de origen, Falso significa que la fuente de datos del gráfico copiado no se cambiará. Verdadero significa que la fuente de datos del gráfico copiado hace referencia a la hoja de destino.|
| Consulte la hoja con el mismo nombre| Booleano| Verdadero| FALSO||En MS Excel, al copiar fórmulas que hacen referencia a otras hojas de trabajo mientras se copia una hoja de trabajo a otra, las fórmulas copiadas deben hacer referencia al libro de origen. Sin embargo, en algunas situaciones el usuario puede necesitar que las fórmulas copiadas hagan referencia a hojas de trabajo con el mismo nombre en el mismo libro de trabajo, como cuando esas hojas de trabajo se copiaron antes de esta operación de copia, entonces esta propiedad debe mantenerse como verdadera.|

