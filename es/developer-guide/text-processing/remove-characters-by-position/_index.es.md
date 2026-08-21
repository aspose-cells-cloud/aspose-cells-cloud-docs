---
title: "Aspose.Cells Cloud Remove Characters by Position Web API – Eliminar texto de ubicaciones específicas en Excel"
second_title: "Documento"
ArticleTitle: "Eliminador de caracteres basado en posición en Excel – Eliminar texto en ubicaciones específicas – Shortcode en línea"
linktitle: "Eliminar caracteres por posición"
type: docs
url: /remove-characters-by-position/
keywords: "Aspose.Cells Cloud, eliminar caracteres por posición, limpieza de texto en Excel, eliminar primeros N caracteres, eliminar últimos N caracteres, eliminar texto antes de un marcador, eliminar texto después de un marcador, eliminación entre valores"
description: "Utilice la API web de Aspose.Cells Cloud para eliminar caracteres de celdas de Excel según su posición: elimine los primeros/últimos N caracteres o el texto antes/después de marcadores específicos con alta precisión."
weight: 100
---

Elimine caracteres de celdas de Excel según su posición: elimine los primeros/últimos N caracteres, o elimine texto antes/después de marcadores especificados. Limpieza precisa de texto con la API web de Aspose.Cells Cloud.


## **Introducción**: Eliminar caracteres no deseados por posición

**Modos de posición**

- `theFirstNCharacters` – eliminar N caracteres desde el inicio
- `theLastNCharacters` – eliminar N caracteres desde el final
- `allCharactersBeforeText` – eliminar todo lo que precede a la primera aparición de la subcadena proporcionada
- `allCharactersAfterText` – eliminar todo lo que sigue a la primera aparición
- `BetweenValues` – eliminar la subcadena (y opcionalmente los propios delimitadores) ubicada entre dos valores definidos por el usuario

**Opciones**

- `caseSensitive` – determina si las búsquedas para `BeforeText`, `AfterText` y `BetweenValues` distinguen entre mayúsculas y minúsculas

## **API RemoveCharactersByPosition**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **RemoveCharactersByPosition**

| Nombre del parámetro    | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                                                                             |
| ----------------------- | ------- | ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | File    | FormData                            | Archivo de hoja de cálculo que se procesará. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc.                                                                  |
| Authorization           | String  | Header                              | Token Bearer para autenticación (obligatorio).                                                                                                                          |
| theFirstNCharacters     | Integer | Query                               | Número de caracteres a eliminar desde el inicio del texto en cada celda seleccionada (por ejemplo, `3` elimina los primeros 3 caracteres).                              |
| theLastNCharacters      | Integer | Query                               | Número de caracteres a eliminar desde el final del texto en cada celda seleccionada (por ejemplo, `2` elimina los últimos 2 caracteres).                                 |
| allCharactersBeforeText | String  | Query                               | Elimina todos los caracteres que aparecen antes de la cadena de texto especificada en cada celda. Si el texto aparece varias veces, la eliminación se basa en la primera ocurrencia. |
| allCharactersAfterText  | String  | Query                               | Elimina todos los caracteres que aparecen después de la cadena de texto especificada en cada celda. Si el texto aparece varias veces, la eliminación se basa en la primera ocurrencia. |
| worksheet               | String  | Query                               | _(Opcional)_ Nombre de la hoja de cálculo donde se aplicará la eliminación de caracteres. Si se omite, la operación se aplica a la primera hoja.                        |
| range                   | String  | Query                               | _(Opcional)_ Rango de celdas donde se aplicará la eliminación de caracteres (por ejemplo, `"A1:C10"`). Si se omite, la operación se aplica a todas las celdas usadas en la hoja especificada. |
| outPath                 | String  | Query                               | _(Opcional)_ Ruta de carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen.            |
| outStorageName          | String  | Query                               | Nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                                            |
| region                  | String  | Query                               | _(Opcional)_ Establece la configuración regional para el manejo de texto, particularmente relevante para posiciones de caracteres y codificación específicas del idioma (por ejemplo, `"en-US"`, `"zh-CN"`). |
| password                | String  | Query                               | _(Opcional)_ Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                                   |

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

- **200 OK**: La solicitud se realizó correctamente y se devuelve el archivo procesado.
- **400 Bad Request**: URI inválido de la API de Aspose.Cells Cloud.
- **401 Unauthorized**: Token de acceso inválido o ID y secreto de cliente inválidos.
- **404 Not Found**: El archivo de hoja de cálculo no es accesible.
- **500 Server Error**: La hoja de cálculo encontró una anomalia al obtener datos de cálculo.

## ¿Dónde debemos utilizar la API Remove Characters by Position?

- **Estandarización de datos**: Limpiar códigos de producto (eliminar ceros iniciales o sufijos), números de teléfono (eliminar códigos de país)
- **Extracción de texto**: Extraer información clave de archivos de registro (eliminar marcas de tiempo o prefijos)
- **Procesamiento de archivos**: Organizar nombres de archivo (eliminar prefijos o sufijos de fecha uniformes)
- **Análisis de datos**: Procesar texto estructurado (extraer contenido entre corchetes o marcadores específicos)
- **Gestión de bases de datos**: Limpiar datos importados (eliminar caracteres de encabezado/cabecera de formato fijo)

## ¿Por qué debería utilizar la API Remove Characters by Position?

- **Precisa y eficiente**: La eliminación posicional directa elimina la necesidad de expresiones regulares complejas.
- **Configuración flexible**: Cinco modos de posicionamiento más una opción de sensibilidad a mayúsculas/minúsculas cubren diversos escenarios.
- **Procesamiento por lotes**: Limpiar columnas completas con una sola llamada, aumentando la eficiencia hasta 10 veces.
- **Análisis inteligente**: Maneje fácilmente la extracción de contenido entre dos delimitadores.
- **Amigable para desarrolladores**: Aspose.Cells Cloud proporciona SDK para múltiples lenguajes, acelerando el desarrollo y ofreciendo documentación exhaustiva. Comparado con la implementación de lógica personalizada de procesamiento de texto, esto reduce significativamente la carga de trabajo de desarrollo.
- **Rentable**: Los caracteres pueden eliminarse sin necesidad de cargar previamente el libro, ahorrando espacio de almacenamiento y reduciendo costos.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar los SDK es la mejor forma de acelerar el desarrollo. El SDK maneja los detalles subyacentes, permitiéndole implementar simplemente la eliminación de caracteres por posición en celdas con un código mínimo.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---