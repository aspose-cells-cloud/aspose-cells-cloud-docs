---
title: "Aspose.Cells Cloud Web API: Convertir gráfico de Excel a imagen - Herramienta gratuita en línea"
second_title: "Documento"
ArticleTitle: "Cómo convertir un gráfico de hoja de cálculo en una imagen: Guía paso a paso"
linktitle: "Convertir gráfico a imagen"
type: docs
url: /es/convert-chart-to-image/
keywords: "convertir gráfico a imagen, Aspose.Cells, exportar gráfico de Excel, PNG, SVG, JPEG, BMP, TIFF"
description: "Utilice la API web de Aspose.Cells Cloud para convertir un gráfico de Excel directamente en imágenes PNG, SVG, TIFF, JPEG o BMP a partir de un archivo de hoja de cálculo."
weight: 100
---

Los gráficos de Excel son representaciones visuales de datos que pueden incrustarse dentro de hojas de cálculo. Convertir estos gráficos a formatos de imagen permite su reutilización sencilla en documentos, páginas web e informes sin necesidad de tener Excel instalado.

Convierta un gráfico de una hoja de cálculo local o archivo de Excel en un archivo de imagen. **FORMATOS DE IMAGEN SOPORTADOS:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **Convertir gráfico a imagen (API)**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud:**

| Nombre del parámetro | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                      | Obligatorio |
| :------------------- | :------ | :---------------------------------- | :------------------------------------------------------------------------------- | :---------- |
| Spreadsheet          | Archivo | FormData                            | Cargar el archivo de hoja de cálculo que contiene el gráfico.                   | Sí          |
| worksheet            | Cadena  | Query                               | Especificar el nombre de la hoja de cálculo, si corresponde.                    | No          |
| chartIndex           | Entero  | Query                               | Índice del gráfico que se va a convertir.                                        | Sí          |
| format               | Cadena  | Query                               | (Obligatorio) Tipo de imagen deseado (por ejemplo, svg, png, jpg).              | Sí          |
| outPath              | Cadena  | Query                               | (Opcional) Ruta de la carpeta donde se guardará el archivo de salida; por defecto es null. | No          |
| outStorageName       | Cadena  | Query                               | Nombre del almacenamiento para el archivo de salida.                             | No          |
| fontsLocation        | Cadena  | Query                               | Especificar fuentes personalizadas si es necesario.                              | No          |
| region             | Cadena  | Query                               | Establecer la región de la hoja de cálculo.                                     | No          |
| password             | Cadena  | Query                               | Contraseña para abrir el archivo de hoja de cálculo.                             | No          |

## **Respuesta**

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

| Código | Significado            | Descripción                                                     |
| ------ | ---------------------- | --------------------------------------------------------------- |
| 200    | Correcto               | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta   | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado          | Token JWT inválido o ausente.                                   |
| 413    | Carga demasiado grande  | El archivo cargado supera el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                              |

## ¿Dónde debería utilizar la API Convert Chart to Image?

- **Generación de informes y paneles de control**: Convertir automáticamente gráficos de datos de Excel en imágenes (PNG, JPEG, etc.) para incrustarlos en informes PDF, paneles web o presentaciones de PowerPoint.
- **Aplicaciones web o por correo electrónico**: Servir imágenes de gráficos directamente en páginas web o correos electrónicos sin exigir a los usuarios descargar ni abrir archivos de Excel. Útil para herramientas de informes dinámicos, boletines informativos o notificaciones automatizadas.
- **Flujos de trabajo de procesamiento de documentos**: Integrarlos en canalizaciones automatizadas (por ejemplo, facturación, análisis) donde los gráficos de Excel deben insertarse en otros formatos (Word, PDF, HTML).
- **Aplicaciones móviles o de escritorio**: Mostrar gráficos de Excel en aplicaciones donde renderizar la hoja de cálculo completa no es necesario ni práctico.
- **Archivado y visualización**: Guardar gráficos como imágenes independientes para almacenamiento a largo plazo, miniaturas o vistas previas rápidas sin depender de Excel.

## ¿Por qué debería utilizar la API Convert Chart to Image?

- **Preservación de la fidelidad visual**: Mantiene el formato exacto del gráfico (colores, etiquetas, escala) tal como aparece en Excel, garantizando una salida de calidad profesional.
- **Independencia de plataforma**: No requiere instalación de Excel. Funciona multiplataforma (Windows, Linux, macOS) mediante la API REST, ideal para aplicaciones basadas en la nube o del lado del servidor.
- **Automatización y escalabilidad**: Conversión por lotes de varios gráficos o archivos mediante programación, ahorrando tiempo frente a la exportación manual. Maneja grandes volúmenes de forma eficiente en la nube.
- **Formatos de salida flexibles**: Admite formatos de imagen populares (PNG, JPG, BMP, SVG, etc.), lo que facilita la integración con diversos sistemas y medios.
- **Seguridad y fiabilidad**: Procesa archivos en el entorno en la nube de Aspose sin exponer datos confidenciales a herramientas del lado del cliente. Alta disponibilidad y rendimiento constante.
- **Fácil de usar para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y viene con documentación completa. En comparación con la creación de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puede convertir gráficos sin cargar previamente el libro de trabajo, lo que ahorra espacio de almacenamiento y reduce costos.

## ¿Cómo utilizar la API Convert Chart to Image con SDK?

### Especificación de la API Convert Chart to Image

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">Especificación de la API Convert Chart to Image</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole convertir un gráfico en una imagen con un código breve.  
Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}