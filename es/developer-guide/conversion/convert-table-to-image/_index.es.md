---
title: "Aspose.Cells Cloud Web API: Convertir datos locales de tabla de Excel a un archivo de imagen - Herramienta gratuita en línea"
second_title: "Document"
ArticleTitle: "Cómo convertir datos locales de tabla de hoja de cálculo a un archivo de imagen: Guía paso a paso"
linktitle: "Convertir tabla a imagen"
type: docs
url: /es/convert-table-to-image/
keywords: "Aspose.Cells, API en la nube, convertir tabla a imagen, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Convierta rápidamente una tabla de hoja de cálculo local de Excel a un archivo de imagen utilizando la API de Aspose.Cells Cloud. Admite PNG, JPEG, TIFF, BMP, SVG y otros formatos."
weight: 100
---

Exporte los datos de tabla desde un archivo local de Excel a un archivo de [imagen](https://docs.fileformat.com/image/) utilizando la API en la nube.

**FORMATOS DE IMAGEN SOPORTADOS:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API para convertir tabla a imagen**

Antes de utilizar este endpoint, asegúrese de cumplir con los siguientes requisitos previos:

- Un token de acceso JWT válido obtenido mediante la autenticación de Aspose.Cells Cloud.
- Una cuenta de almacenamiento accesible si pretende utilizar los parámetros `outPath` o `outStorageName`.
- El libro de trabajo fuente (archivo local de Excel) debe ser legible y, si está protegido, se debe proporcionar la contraseña correcta.

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                                           |
| :------------------- | :----- | :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet          | File   | FormData                            | Carga el archivo de hoja de cálculo.                                                                                                  |
| worksheet            | String | Query                               | Nombre de la hoja de cálculo del archivo Excel.                                                                                       |
| tableName            | String | Query                               | Nombre de la tabla que se va a convertir.                                                                                             |
| format             | String | Query                               | Formato deseado del archivo de imagen (por ejemplo, png, svg).                                                                       |
| outPath              | String | Query                               | (Opcional) Ruta de carpeta donde se guardará la imagen convertida. Por defecto es null.                                              |
| outStorageName       | String | Query                               | Especifica el nombre del almacenamiento de salida del archivo.                                                                        |
| fontsLocation        | String | Query                               | Utilice fuentes personalizadas si es necesario.                                                                                       |
| region               | String | Query                               | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query                               | Contraseña necesaria para acceder al archivo de hoja de cálculo.                                                                      |

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

**Códigos de estado HTTP**

| Código | Significado            | Descripción                                                       |
| ------ | ---------------------- | ----------------------------------------------------------------- |
| 200    | OK                     | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta   | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado          | Token JWT no válido o ausente.                                    |
| 413    | Payload demasiado grande | El archivo cargado supera el límite de tamaño.                  |
| 500    | Error interno del servidor | Error inesperado del servidor.                                    |

## **¿Dónde debería utilizar la API para convertir tabla a imagen?**

- **Capturas estáticas de informes**: Convierta tablas financieras, resultados de cálculos o cualquier dato formateado en imágenes para incluirlas en informes PDF, diapositivas de PowerPoint o documentos impresos, donde no se requiera edición.
- **Visualización de datos en presentaciones**: Convierta tablas complejas de hojas de cálculo —incluyendo formato condicional o visualizaciones sencillas— en imágenes que se puedan incrustar en presentaciones (PPTX, Google Slides).
- **Documentación y materiales de formación**: Capture ejemplos de hojas de cálculo, plantillas o formularios de entrada de datos como imágenes para manuales de usuario, tutoriales o artículos de bases de conocimiento.
- **Vistas previas en miniatura**: Genere pequeñas imágenes previas de secciones clave de hojas de cálculo para navegadores de archivos, bibliotecas de documentos o resultados de búsqueda.

## ¿Por qué debería utilizar la API para convertir tabla a imagen?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y cuenta con documentación exhaustiva. En comparación con la creación de soluciones personalizadas de renderizado, esto reduce significativamente la carga de trabajo de desarrollo.
- **Rentable**: Puede convertir datos de tablas sin tener que cargar primero todo el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- **Preservación perfecta en píxeles**: Reproduce fielmente la apariencia de Excel —incluyendo formato de celdas, fórmulas (como valores mostrados), bordes, colores y formato condicional— en la imagen de salida.
- **Compatibilidad universal**: Los formatos de imagen (PNG, JPEG, TIFF, BMP, SVG, etc.) se pueden visualizar en cualquier dispositivo o plataforma sin software especializado, garantizando la máxima accesibilidad.

## ¿Cómo utilizar la API para convertir tabla a imagen con SDK?

### Especificación de la API para convertir tabla a imagen

La [especificación de la API para convertir tabla a imagen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) proporciona una interfaz de programación pública accesible para realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificado en Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nombre de archivo opcional"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel, lo que le permite convertir datos de tablas de hojas de cálculo en imágenes con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}