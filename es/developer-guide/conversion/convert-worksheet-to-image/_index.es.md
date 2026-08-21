---
title: "Conversión de hoja de cálculo – Documentación de la API de Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Cómo convertir datos locales de una hoja de cálculo a un archivo de imagen: guía paso a paso"
linktitle: "Convertir hoja de cálculo a imagen"
type: docs
url: /es/convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, hoja de cálculo a imagen, convertir hoja de cálculo a imagen, Excel a PNG, Excel a SVG, Excel a TIFF, Excel a JPEG, Excel a BMP, API de conversión de imágenes, API REST, exportación de imágenes de hojas de cálculo, ejemplos de SDK"
description: "Guía paso a paso para convertir una hoja de cálculo de Excel a formatos de imagen (PNG, SVG, TIFF, JPEG, BMP, etc.) mediante la API de Aspose.Cells Cloud, incluyendo parámetros de solicitud, detalles de respuesta, códigos de error, escenarios de uso y ejemplos de código SDK."
weight: 100
---

Exporte datos de una hoja de cálculo en un archivo local de Excel a un archivo de [imagen](https://docs.fileformat.com/image/) mediante la API de Aspose.Cells Cloud. Esta operación admite múltiples formatos de imagen y es ideal para generar capturas visuales de los datos de las hojas de cálculo.

**FORMATOS DE IMAGEN SOPORTADOS**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **API para convertir hoja de cálculo a imagen**

### API web

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                          |
| :------------------- | :----- | :---------------------------------- | :----------------------------------------------------------------------------------- |
| Spreadsheet          | Archivo | FormData                            | Cargar el archivo de hoja de cálculo.                                                |
| worksheet            | Cadena  | Consulta                            | Nombre de la hoja de cálculo que se va a convertir.                                 |
| format               | Cadena  | Consulta                            | Formato de imagen deseado (`svg`, `png`, `tiff`, `jpeg`, `bmp`, etc.).              |
| outPath              | Cadena  | Consulta                            | _(Opcional)_ Ruta de la carpeta donde se almacenará la imagen de salida; por defecto es `null`. |
| outStorageName       | Cadena  | Consulta                            | Nombre del lugar de almacenamiento para el archivo de salida.                       |
| fontsLocation        | Cadena  | Consulta                            | Ruta a una carpeta personalizada de fuentes, si necesita utilizar fuentes no disponibles en el servidor. |
| region               | Cadena  | Consulta                            | Configuración regional de la hoja de cálculo (por ejemplo, `es-ES`).                |
| password             | Cadena  | Consulta                            | Contraseña necesaria para abrir un archivo de hoja de cálculo protegido.            |

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

| Código | Significado              | Descripción                                                       |
| ------ | ------------------------ | ----------------------------------------------------------------- |
| 200    | Correcto                 | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT no válido o ausente.                                    |
| 413    | Payload demasiado grande  | El archivo subido supera el límite de tamaño.                    |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                 |

## **¿Dónde debería utilizarse la API para convertir hoja de cálculo a imagen?**

- **Capturas estáticas de informes** – Convierta tablas financieras, cálculos u otros datos en imágenes para incluirlos en informes PDF, diapositivas de PowerPoint o documentos impresos, donde no sea necesario editarlos.
- **Visualización de datos en presentaciones** – Transforme tablas complejas de hojas de cálculo (incluidos formatos condicionales o gráficos simples) en imágenes que se puedan incrustar en presentaciones (PPTX, Google Slides).
- **Documentación y materiales de capacitación** – Capture ejemplos de hojas de cálculo, plantillas o formularios de entrada de datos como imágenes para manuales de usuario, tutoriales o artículos de bases de conocimiento.
- **Vistas previas en miniatura** – Genere pequeñas imágenes de vista previa de secciones clave de la hoja de cálculo para navegadores de archivos, bibliotecas de documentos o resultados de búsqueda.

## **¿Por qué debería utilizar la API para convertir hoja de cálculo a imagen?**

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de una documentación completa. En comparación con construir una solución personalizada de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Rentable** – Puede convertir datos de tablas sin necesidad de almacenar permanentemente el libro de trabajo, lo que ahorra espacio de almacenamiento y reduce costos.
- **Preservación perfecta de píxeles** – Replica fielmente la apariencia de Excel, incluidos el formato de celdas, las fórmulas (como valores mostrados), bordes, colores y formatos condicionales, en la imagen resultante.
- **Compatibilidad universal** – Los formatos de imagen (PNG, JPEG, TIFF, BMP, SVG, etc.) se pueden visualizar en cualquier dispositivo o plataforma sin software especializado, lo que garantiza una accesibilidad máxima.

## **¿Cómo utilizar la API para convertir hoja de cálculo a imagen con SDK?**

### Especificación de la API para convertir hoja de cálculo a imagen

La [Especificación de la API para convertir hoja de cálculo a imagen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) define una interfaz de programación accesible públicamente y permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Hoja1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@miLibro.xlsx" \
  -o convertida.png
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel y permite convertir datos de hojas de cálculo a una imagen con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}