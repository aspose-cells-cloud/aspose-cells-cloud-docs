---
title: "Aspose.Cells Cloud Text Trimming Web API: Eliminar espacios y saltos de línea extra"
second_title: "Documento"
ArticleTitle: "Limpiador de datos de Excel: Recortar caracteres, espacios y saltos de línea automáticamente – En línea, con shortcode"
linktitle: "Recortar caracteres"
type: docs
url: /es/trim-character/
keywords: "Excel, recorte de texto, eliminar espacios, saltos de línea, Aspose.Cells, limpieza de datos, hoja de cálculo, normalizar formato de celda"
description: "Recorte espacios extra, saltos de línea y caracteres no deseados en celdas de Excel mediante la API en la nube de Aspose.Cells. Asegure datos de hojas de cálculo limpios y consistentes."
weight: 100
---

Recorte automáticamente caracteres innecesarios, espacios extra y saltos de línea en celdas de Excel utilizando la API de recorte de caracteres de Aspose.Cells. Limpie entradas de datos y mantenga un formato consistente en sus hojas de cálculo.

## **Descripción general**

- **Recorte de espacios iniciales y finales**
  - Elimine espacios extra al principio y al final del texto
  - Mejore la presentación, orden y legibilidad de los datos
- **Procesamiento de espacios extra entre palabras**
  - Elimine espacios extra entre palabras
  - Solucione la confusión de formato causada por datos procedentes de múltiples fuentes

- **Espacios especiales eliminados**
  - Elimine específicamente los espacios de no separación (non-breaking spaces)
  - Asegure la precisión y consistencia de los datos

- **Gestión de saltos de línea**
  - Elimine saltos de línea extra o todos ellos
  - Mantenga el contenido de las celdas organizado y con aspecto profesional

## **API TrimCharacter**

Antes de llamar a la API, asegúrese de tener una cuenta válida de Aspose Cloud, un `client_id`/`client_secret` y un token de acceso con el ámbito **Cells**.

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **trimCharacter**

| Nombre del parámetro      | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                                                                         |
| :------------------------ | :------ | :----------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet               | File    | FormData                             | Archivo de hoja de cálculo que se procesará. Los formatos compatibles incluyen XLSX, XLS, ODS, CSV, etc.                                                           |
| trimContent               | String  | Query                                | Especifica los caracteres o cadenas concretos que se recortarán del contenido de las celdas. Puede ser un solo carácter, varios caracteres o un patrón personalizado. |
| trimLeading               | Boolean | Query                                | Si es `true`, elimina los caracteres especificados del inicio del contenido de cada celda.                                                                        |
| trimTrailing              | Boolean | Query                                | Si es `true`, elimina los caracteres especificados del final del contenido de cada celda.                                                                         |
| trimSpaceBetweenWordTo1   | Boolean | Query                                | Si es `true`, reduce múltiples espacios consecutivos entre palabras a un único espacio dentro de cada celda.                                                      |
| trimNonBreakingSpaces     | Boolean | Query                                | Si es `true`, elimina los caracteres de espacio de no separación (Unicode U+00A0) del contenido de las celdas.                                                    |
| removeExtraLineBreaks     | Boolean | Query                                | Si es `true`, reduce múltiples saltos de línea consecutivos a un único salto de línea dentro de cada celda.                                                       |
| removeAllLineBreaks       | Boolean | Query                                | Si es `true`, elimina todos los caracteres de salto de línea del contenido de las celdas.                                                                         |
| worksheet                 | String  | Query                                | _(Opcional)_ Nombre de la hoja de cálculo donde se aplicará el recorte de texto. Si se omite, la operación se aplica a la primera hoja.                            |
| range                     | String  | Query                                | _(Opcional)_ Rango de celdas donde se aplicará el recorte de texto (por ejemplo, `"A1:C10"`). Si se omite, la operación se aplica a todas las celdas usadas de la hoja especificada. |
| outPath                   | String  | Query                                | _(Opcional)_ Ruta de carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen.      |
| outStorageName            | String  | Query                                | Nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                                       |
| region                    | String  | Query                                | _(Opcional)_ Establece la configuración regional para el procesamiento de texto, lo que puede afectar el manejo de espacios y saltos de línea según el idioma (por ejemplo, `"es-ES"`, `"ar-SA"`). |
| password                  | String  | Query                                | _(Opcional)_ Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                              |

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

**Ejemplo de éxito (HTTP 200):** La API devuelve un flujo de archivo que contiene el libro recortado.

### Códigos de error

- **400 Bad Request**: URI inválido de la API de Aspose.Cells Cloud.
- **401 Unauthorized**: Token de acceso inválido. O `client id` y `secret` inválidos.
- **404 Not Found**: El archivo de hoja de cálculo no es accesible.
- **500 Server Error**: Se ha producido una anomalia en la obtención de datos de cálculo en la hoja de cálculo.

## ¿Dónde debemos utilizar la API de recorte de caracteres?

- **Normalización de entradas de usuario**: Limpiar datos de tablas introducidos manualmente, eliminando espacios y saltos de línea extra.
- **Mantenimiento de bases de datos de clientes**: Limpiar espacios redundantes y problemas de formato en nombres, direcciones y datos de contacto de clientes.
- **Limpieza automatizada de informes**: Limpia el formato de la fuente de datos antes de generar informes automatizados.
- **Preparación para migración de datos**: Resuelve problemas de formato antes de migrar los datos al nuevo sistema.

## ¿Por qué debería utilizar la API de recorte de caracteres?

- **Reducción de costes laborales**: Elimine los esfuerzos manuales y tediosos de limpieza de datos.
- **Reducción de costes por errores**: Evite errores de análisis causados por problemas de formato.
- **Pago por uso**: Sin cuotas fijas, solo se facturan los datos procesados realmente.
- **Sin inversión en infraestructura**: No es necesario mantener servidores ni software.
- **Soporte multi-formato**: Admite procesamiento de múltiples formatos como XLSX, XLS, CSV, ODS, etc.
- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de documentación completa. En comparación con la creación de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puede eliminar caracteres duplicados sin necesidad de subir primero el libro, lo que ahorra espacio de almacenamiento y reduce costes.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar los SDK es la mejor forma de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar el recorte de caracteres en celdas con muy poco código.
Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}