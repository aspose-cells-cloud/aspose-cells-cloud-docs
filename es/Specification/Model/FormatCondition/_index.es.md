---
title: FormatoCondición
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/formatcondition/
description: "Aspose.Cells Especificación del modelo de nube: FormatCondition. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **formatoCondición**

 

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Prioridad| Entero| Verdadero| FALSO|| La prioridad de esta regla de formato condicional. Este valor se utiliza para determinar qué formato se debe evaluar y representar. Los valores numéricos más bajos tienen mayor prioridad que los valores numéricos más altos, donde '1' es la prioridad más alta.|
| Tipo| Cadena| Verdadero| FALSO|| Obtiene y establece si el formato condicional es Tipo.|
| Detener si es verdadero| Booleano| Verdadero| FALSO|| Es cierto que no se pueden aplicar reglas con menor prioridad que esta regla cuando esta regla se evalúa como verdadera. Sólo aplica para Excel 2007;|
| Por encima del promedio| Clase: superior al promedio| Verdadero| FALSO||Obtenga la instancia "AboveAverage" del formato condicional. La regla de la instancia predeterminada resalta las celdas que están por encima del promedio para todos los valores del rango. Válido sólo para tipo = AboveAverage.|
| Escala de colores| Clase:Escala de colores| Verdadero| FALSO|| Obtenga la instancia "ColorScale" del formato condicional. La instancia predeterminada es un 3ColorScale "verde-amarillo-rojo". Válido sólo para tipo = ColorScale.|
| Barra de datos| Clase: barra de datos| Verdadero| FALSO|| Obtenga la instancia "DataBar" del formato condicional. El color predeterminado de la instancia es azul. Válido sólo para el tipo DataBar.|
| Fórmula 1| Cadena| Verdadero| FALSO|| Obtiene y establece el valor o expresión asociada al formato condicional.|
| Fórmula 2| Cadena| Verdadero| FALSO|| Obtiene y establece el valor o expresión asociada al formato condicional.|
| Conjunto de iconos| Clase:Conjunto de iconos| Verdadero| FALSO||Obtenga la instancia "IconSet" del formato condicional. El IconSetType de la instancia predeterminada es TrafficLights31. Válido sólo para tipo = IconSet.|
| Operador| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de operador de formato condicional.|
| Estilo| Clase:Estilo| Verdadero| FALSO|| Obtiene o establece el estilo de los rangos de celdas con formato condicional.|
| Texto| Cadena| Verdadero| FALSO|| El valor de texto en una regla de formato condicional "el texto contiene". Válido solo para tipo = contieneTexto, noContieneTexto, comienzaCon y terminaCon. El valor predeterminado es nulo.|
| Periodo de tiempo| Cadena| Verdadero| FALSO|| El período de tiempo aplicable en una regla de formato condicional "fecha que ocurrió...". Válido sólo para tipo = timePeriod. El valor predeterminado es TimePeriodType.Today.|
| Top10| Clase:Top10| Verdadero| FALSO||Obtenga la instancia "Top10" del formato condicional. La regla de la instancia predeterminada resalta las celdas cuyos valores se encuentran entre los 10 primeros corchetes. Válido únicamente para el tipo Top10.|
| enlace| Clase: enlace| Verdadero| FALSO|||

**Nombre del padre** : (ElementoEnlace)[elementoEnlace]**Nombre de los niños** : 
	-  [EstiloFormatoCondición](styleformatcondition) 
