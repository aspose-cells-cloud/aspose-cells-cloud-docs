---
title: "Aspose.Cells Cloud Web API: Convertir texto en números en Excel y limpiar caracteres especiales"
second_title: "Documento"
ArticleTitle: "Limpieza de datos de Excel - Convertir texto en números y eliminar caracteres no deseados"
linktitle: "Convertir texto"
type: docs
url: /convert-text/
keywords: "Aspose.Cells convertir texto, texto de Excel a números, eliminar caracteres especiales en Excel, reemplazar saltos de línea en Excel, normalizar caracteres acentuados, API de limpieza de datos de Excel"
description: "Convierta números con formato de texto en valores numéricos, reemplace caracteres y saltos de línea no deseados, y normalice caracteres acentuados en archivos de Excel mediante la API de Aspose.Cells Cloud."
weight: 100
---

Limpiamos los datos de Excel convirtiendo números con formato de texto en valores numéricos, reemplazando caracteres y saltos de línea no deseados, y normalizando caracteres acentuados a letras estándar mediante la API de Aspose.Cells.

## Descripción general

**Convierta números almacenados como texto, elimine datos basura y sustituya caracteres acentuados con una sola llamada, sin fórmulas.**

- **Convertir números almacenados como texto en números**: Transforme datos numéricos almacenados como texto en números verdaderos, garantizando cálculos precisos y una representación correcta de los datos.
- **Reemplazar caracteres específicos**: Reemplace todas las ocurrencias de caracteres especificados en las celdas seleccionadas de una sola vez para estandarizar sus datos.
- **Convertir saltos de línea en espacio, coma o punto y coma**: Mejore la legibilidad convirtiendo saltos de línea en espacios, comas o puntos y comas, generando una presentación más organizada y visualmente atractiva.
- **Reemplazar caracteres acentuados**: Si sus datos están en distintos idiomas, puede sustituir caracteres acentuados como “é” o “ü” por sus equivalentes sin acento, mejorando la coherencia y claridad.

## **API ConvertText**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **convertText**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                  |
|----------------------|--------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | Archivo | FormData                                | Archivo de hoja de cálculo que se procesará. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc.                                                       |
| convertTextType      | Cadena  | Consulta                                | Especifica el tipo de conversión de texto que se aplicará, como convertir números con formato de texto en valores numéricos o convertir caracteres acentuados en sus equivalentes sin acento. |
| sourceCharacters     | Cadena  | Consulta                                | Especifica los caracteres, cadenas o patrones que se reemplazarán o eliminarán del texto (por ejemplo, `"é,è,ê"`, `"#N/A"`, `"\\n"` para saltos de línea). |
| targetCharacters     | Cadena  | Consulta                                | Especifica los caracteres o cadenas de reemplazo que sustituirán a los caracteres de origen (por ejemplo, `"e"` para letras acentuadas, `""` para eliminar, `" "` para saltos de línea). |
| worksheet            | Cadena  | Consulta                                | *(Opcional)* Nombre de la hoja de cálculo donde se aplicará la conversión de texto. Si se omite, la operación se aplica a la primera hoja.                   |
| range                | Cadena  | Consulta                                | *(Opcional)* Rango de celdas donde se aplicará la conversión de texto (por ejemplo, `"A1:C10"`). Si se omite, la operación se aplica a todas las celdas usadas en la hoja especificada. |
| outPath              | Cadena  | Consulta                                | *(Opcional)* Ruta de la carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen. |
| outStorageName       | Cadena  | Consulta                                | Nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                                 |
| region               | Cadena  | Consulta                                | *(Opcional)* Establece la configuración regional para las reglas de conversión de texto, especialmente relevante para la manipulación de caracteres específicos del idioma (por ejemplo, `"en-US"`, `"fr-FR"`). |
| password             | Cadena  | Consulta                                | *(Opcional)* Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                         |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Códigos de error

- **400 Bad Request (Solicitud incorrecta)**: URI inválido de la API de Aspose.Cells Cloud.
- **401 Unauthorized (No autorizado)**: Token de acceso inválido o ID de cliente y secreto inválidos.
- **404 Not Found (No encontrado)**: El archivo de hoja de cálculo no es accesible.
- **500 Server Error (Error del servidor)**: La hoja de cálculo encontró una anomalia al obtener datos de cálculo.

## ¿Dónde debemos usar la API Convert Text?

- **Corrección de formato numérico**: Convertir números almacenados como texto (por ejemplo, “123.45”) en un formato numérico adecuado para cálculos.
- **Limpieza de caracteres especiales**: Eliminar símbolos innecesarios, espacios extra o caracteres invisibles de los datos.
- **Manejo de saltos de línea**: Reemplazar saltos de línea en celdas por espacios u otros delimitadores.
- **Normalización de caracteres acentuados**: Convertir letras acentuadas (por ejemplo, “é”, “ñ”) en letras estándar (“e”, “n”).
- **Preprocesamiento de archivos CSV**: Estandarizar el formato de texto antes de importar archivos CSV a Excel.

## ¿Por qué deberíamos usar la API Convert Text?

- **Conversión automática de formato**: Convertir números con formato de texto en valores calculables en lote con una sola solicitud.
- **Estandarización de caracteres**: Manejar de forma uniforme caracteres especiales, diacríticos y problemas de codificación.
- **Consistencia de datos**: Asegurar que el formato de texto sea completamente uniforme en todo el conjunto de datos.
- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, permitiendo un desarrollo rápido y ofreciendo una documentación completa. Comparado con la creación de soluciones personalizadas de procesamiento de texto, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puede convertir texto sin cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Usar los SDK es la mejor forma de acelerar el desarrollo. El SDK maneja los detalles subyacentes, permitiéndole implementar simplemente Convert Text para celdas con un código mínimo.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---