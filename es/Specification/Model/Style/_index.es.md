---
title: estilo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/style/
description: "Aspose.Cells Especificación del modelo de nube: Estilo. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Cloud REST API, Estilo
weight: 50
---
## **estilo**

 Representa el estilo de visualización del documento de Excel, como fuente, color, alineación, borde, etc. El objeto Estilo contiene todos los atributos de estilo (fuente, formato de número, alineación, etc.) como propiedades.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Fuente| Clase:Fuente| Verdadero| FALSO|| Obtiene un objeto.|
| Nombre| Cadena| Verdadero| FALSO|| Obtiene o establece el nombre del estilo.|
| CulturaPersonalizado| Cadena| Verdadero| FALSO|| Obtiene y establece la cadena de patrón dependiente de la referencia cultural para el formato numérico. Si no se ha establecido ningún formato de número para este objeto, se devolverá nulo. Si el formato de número está integrado, se devolverá la cadena de patrón correspondiente al número integrado.|
| Costumbre| Cadena| Verdadero| FALSO|| Representa la cadena de formato de número personalizado de este objeto de estilo. Si el formato de número personalizado no está configurado (por ejemplo, el formato de número está integrado), se devolverá "".|
| Color de fondo| Clase:Color| Verdadero| FALSO|| Obtiene o establece el color de fondo de un estilo.|
| Color de primer plano| Clase:Color| Verdadero| FALSO|| Obtiene o establece el color de primer plano de un estilo.|
| EstáFórmulaHidden| Booleano| Verdadero| FALSO||Representa si la fórmula estará oculta cuando la hoja de cálculo esté protegida.|
| EsFechaHora| Booleano| Verdadero| FALSO|| Indica si el formato de número es un formato de fecha.|
| Está envuelto en texto| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si el texto dentro de una celda está ajustado.|
| EsGradiente| Booleano| Verdadero| FALSO|| Indica si el sombreado de celda es un patrón de degradado.|
| Está bloqueado| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si una celda se puede modificar o no.|
| es por ciento| Booleano| Verdadero| FALSO|| Indica si el formato numérico es un formato de porcentaje.|
| Reducir para ajustar| Booleano| Verdadero| FALSO|| Representa si el texto se reduce automáticamente para ajustarse al ancho de columna disponible.|
| Nivel de sangría| Entero| Verdadero| FALSO|| Representa el nivel de sangría de la celda o rango. Sólo puede ser un número entero de 0 a 250.|
| Número| Entero| Verdadero| FALSO|| Obtiene o establece el formato de visualización de números y fechas. Los patrones de formato son diferentes para diferentes regiones.|
| Ángulo de rotación| Entero| Verdadero| FALSO|| Representa el ángulo de rotación del texto.|
| Patrón| Cadena| Verdadero| FALSO|| Obtiene o establece el tipo de patrón de fondo de la celda.|
| Dirección del texto| Cadena| Verdadero| FALSO|| Representa el orden de lectura del texto.|
| Alineamiento vertical| Cadena| Verdadero| FALSO||Obtiene o establece el tipo de alineación vertical del texto de una celda.|
| Alineación horizontal| Cadena| Verdadero| FALSO|| Obtiene o establece el tipo de alineación horizontal del texto de una celda.|
| Colección Frontera| Envase| Verdadero| FALSO|||
| FondoTemaColor| Clase:TemaColor| Verdadero| FALSO|| Obtiene y establece el color del tema de fondo.|
| Primer PlanoTemaColor| Clase:TemaColor| Verdadero| FALSO|| Obtiene y establece el color del tema de primer plano.|

