---
title: Firma Digital
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/digitalsignature/
description: "Aspose.Cells Especificación del modelo de nube: Firma digital. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Nube REST API, Firma digital
weight: 50
---
## **firma digital**

 Firma en expediente.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Comentarios| Cadena| Verdadero| FALSO|| El propósito de la firma.|
| Hora de firmar| Cadena| Verdadero| FALSO|| La hora en que se firmó el documento.|
| Identificación| Cadena| Verdadero| FALSO|| Especifica un GUID al que se puede hacer referencia cruzada con el GUID de la línea de firma almacenada en el contenido del documento. El valor predeterminado es Guid vacío (todo ceros).|
| Contraseña| Cadena| Verdadero| FALSO|| Especifica el texto de la firma real en la firma digital. El valor predeterminado es Vacío.|
| Imagen|Formación<Byte> | Verdadero| FALSO|| Especifica una imagen para la firma digital. El valor predeterminado es nulo.|
| ID de proveedor| Cadena| Verdadero| FALSO|| Especifica el ID de clase del proveedor de firma. El valor predeterminado es Guid vacío (todo ceros).|
| Es válida| Booleano| Verdadero| FALSO|| Si esta firma digital es válida y el documento no ha sido manipulado, este valor será verdadero.|
| Tipo XAdEST| Cadena| Verdadero| FALSO|| Tipo XAdES. El valor predeterminado es Ninguno (XAdES está desactivado).|

