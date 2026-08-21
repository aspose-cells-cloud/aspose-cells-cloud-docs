---
title: "Crear API de hojas de cálculo – Aspose.Cells Cloud (v5.0) | Generar archivos de Excel"
second_title: "Documento"
ArticleTitle: "Cómo crear nuevas hojas de cálculo de Excel: generar archivos vacíos o basados en plantillas"
linktitle: "Crear hoja de cálculo"
type: docs
url: /es/create-spreadsheet/
keywords: "Aspose.Cells, API de hoja de cálculo, crear Excel, nube, XLSX, ODS, CSV, plantilla, SDK, automatización"
description: "Aprenda a crear libros de Excel en blanco o basados en plantillas mediante la API de Aspose.Cells Cloud (v5.0). Incluye endpoint, parámetros, códigos de error, pasos de autenticación y ejemplos de SDK."
weight: 100
---

Cree nuevas hojas de cálculo de Excel mediante programación con la API de Aspose.Cells Cloud. Genere libros vacíos o genere archivos a partir de plantillas personalizadas. La API REST permite la creación automatizada de archivos de Excel, lo que la hace ideal para la generación de informes, la automatización de documentos y los flujos de trabajo de procesamiento de datos.

## **API para crear hojas de cálculo**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                       |
| -------------------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**           | String | Query     | **Obligatorio**. Formato de archivo para la nueva hoja de cálculo (por ejemplo, `XLSX`, `XLS`, `ODS`, `CSV`).                                    |
| **template**         | String | Query     | **Opcional**. Nombre de un archivo de plantilla almacenado en su almacenamiento en la nube (por ejemplo, `invoice_template.xlsx`). Si se omite, se crea un libro en blanco. |
| **outPath**          | String | Query     | **Opcional**. Ruta de la carpeta de destino en el almacenamiento en la nube para el archivo generado. Si es `null` u omite, la hoja de cálculo se guarda en la ubicación predeterminada. |
| **outStorageName**   | String | Query     | **Obligatorio**. Identificador del almacenamiento en la nube configurado (por ejemplo, `MyDrive`).                                               |
| **region**           | String | Query     | **Opcional**. Configuración regional (por ejemplo, `es-ES`) que determina los formatos predeterminados para fechas, números y monedas.           |
| **password**         | String | Query     | **Opcional**. Contraseña para un archivo de plantilla cifrado. Déjelo vacío si la plantilla no está protegida.                                    |

### Respuesta

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

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o ausente.                                    |
| 413    | Payload demasiado grande | El archivo cargado supera el límite de tamaño.                  |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                 |

## ¿Dónde deberíamos usar la API para crear hojas de cálculo?

- **Inicialización del sistema automatizado de generación de informes**: cree un nuevo libro en blanco o genere un archivo de informe a partir de una plantilla estándar al inicio de cada ciclo diario/semanal de automatización.
- **Portal de autoservicio para usuarios**: permita que los clientes seleccionen una plantilla (presupuesto, cronograma de proyecto, etc.) y descarguen instantáneamente un archivo de Excel personalizado.
- **Exportación y distribución por lotes de datos**: genere libros independientes con un formato uniforme para cada conjunto de datos exportado, facilitando la distribución y el procesamiento posteriores.

Para operaciones posteriores, como agregar hojas de cálculo o rellenar celdas, consulte la **API para agregar hoja de cálculo**, la **API para actualizar celda** y la **API para exportar libro**.

## ¿Por qué debería usar la API para crear hojas de cálculo?

- **Amigable para desarrolladores**: ofrece bibliotecas SDK para múltiples lenguajes y documentación amplia, lo que simplifica la integración en comparación con construir soluciones personalizadas.
- **Eficiencia laboral**: permite automatizar la consolidación de documentos, reduciendo el esfuerzo manual.
- **Precios basados en uso**: los cargos se basan en el uso de la API, sin tarifas de licencia previas.
- **Servicio gestionado**: la API está totalmente alojada, eliminando la necesidad de mantenimiento de servidores locales o actualizaciones de software.

## Cómo usar la API para crear hojas de cálculo con SDK

### Especificación de la API para crear hojas de cálculo

La [especificación de la API para crear hojas de cálculo](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) define una interfaz de programación accesible públicamente y permite interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MiAlmacenamiento" \
  -H "Authorization: Bearer {access_token}"
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

### Utilice los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de desarrollar, ya que abstracte los detalles de bajo nivel y le permite crear la hoja de cálculo con código conciso. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}