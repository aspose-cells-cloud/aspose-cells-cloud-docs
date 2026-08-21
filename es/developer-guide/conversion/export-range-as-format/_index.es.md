---
title: "Exportar rango de Excel a PDF, PNG, CSV: API de Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Cómo exportar un rango de hoja de cálculo remota a otros formatos: guía paso a paso"
linktitle: "Exportar rango como formato"
type: docs
url: /es/export-range-as-format/
keywords: "Aspose Cells, exportar rango de Excel, PDF, PNG, CSV, API en la nube, conversión de hoja de cálculo"
description: "Aprenda a convertir un rango específico de Excel almacenado en Aspose.Cells Cloud a PDF, PNG, CSV u otros formatos. Incluye detalles del punto de conexión, parámetros, solicitudes de ejemplo, manejo de respuestas e información sobre errores."
weight: 100
---

Exporte un rango de hoja de cálculo/Excel en la nube a un archivo en cierto formato. El archivo de formato puede guardarse en la nube o exportarse al almacenamiento local.

## API de exportación de rango como formato

### API web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                              |
| :------------------- | :----- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | String | Path      | (Obligatorio) Nombre del archivo del libro que se va a recuperar.                                                                                       |
| **worksheet**        | String | Path      | Nombre de la hoja de cálculo.                                                                                                                           |
| **range**            | String | Path      | Rango que se va a convertir (por ejemplo, `A1:C12`).                                                                                                    |
| **format**           | String | Query     | (Obligatorio) Formato de salida deseado (por ejemplo, `pdf`, `png`, `svg`).                                                                             |
| **folder**           | String | Query     | (Opcional) Ruta de la carpeta donde se almacena el libro.                                                                                               |
| **storageName**      | String | Query     | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado.                                                          |
| **outPath**          | String | Query     | (Opcional) Ruta del archivo de salida en el almacenamiento en la nube.                                                                                  |
| **outStorageName**   | String | Query     | (Opcional) Nombre del almacenamiento para el archivo de salida.                                                                                         |
| **fontsLocation**    | String | Query     | (Opcional) Ubicación personalizada de fuentes.                                                                                                          |
| **region**           | String | Query     | (Opcional) Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| **password**         | String | Query     | (Opcional) Contraseña necesaria para abrir el archivo de la hoja de cálculo.                                                                            |

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

| Código | Significado           | Descripción                                                           |
| ------ | --------------------- | --------------------------------------------------------------------- |
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request           | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized          | Token JWT inválido o ausente.                                         |
| 413    | Payload Too Large     | El archivo cargado supera el límite de tamaño.                       |
| 500    | Internal Server Error | Error inesperado del servidor.                                        |

## ¿Dónde debe utilizarse la API de exportación de rango a otro formato?

### Escenarios de exportación y migración de datos

- **Integración con bases de datos** – Exporte rangos específicos de Excel directamente a sistemas de bases de datos.
- **Integración con aplicaciones** – Envíe datos seleccionados de la hoja de cálculo a aplicaciones SaaS.
- **Migración de sistemas** – Transfiera rangos específicos de datos entre sistemas heredados y modernos.
- **Compartición multiplataforma** – Comparta subconjuntos de datos enfocados entre distintas plataformas.

### Informes y análisis

- **Informes específicos** – Exporte secciones concretas de informes a otros formatos para un análisis más dirigido.
- **Alimentación de paneles de control** – Proporcione rangos específicos de datos a herramientas de paneles de control de BI.
- **Métricas de rendimiento** – Extraiga rangos de indicadores clave (KPI) para sistemas de seguimiento de rendimiento.
- **Informes financieros** – Exporte secciones de estados financieros para auditorías externas.

### Desarrollo y pruebas

- **Gestión de datos de prueba** – Exporte rangos específicos de datos para fines de prueba.
- **Entornos de desarrollo** – Comparta rangos de datos de ejemplo con equipos de desarrollo.
- **Pruebas de API** – Genere datos de prueba en formato CSV a partir de secciones específicas de la hoja de cálculo.
- **Desarrollo de prototipos** – Proporcione conjuntos de datos enfocados para prototipos de aplicaciones.

### Operaciones empresariales

- **Compartición selectiva de datos** – Comparta rangos específicos de datos con socios externos.
- **Copia de seguridad parcial de datos** – Realice copias de seguridad de rangos críticos de datos en un formato elegido.
- **Transferencia de datos entre departamentos** – Comparta datos específicos entre departamentos.
- **Informes de cumplimiento** – Exporte rangos de datos regulatorios para presentaciones de cumplimiento.

### Flujos de trabajo automatizados

- **Exportación programada de rangos** – Exporte automáticamente rangos específicos según una programación.
- **Extracción basada en disparadores** – Exporte rangos según eventos o disparadores empresariales.
- **Integración en flujos de trabajo** – Integre exportaciones de rangos en flujos de trabajo de procesos empresariales.
- **Procesamiento por lotes de rangos** – Procese múltiples rangos específicos en operaciones por lotes.

## ¿Por qué debería utilizar la API de exportación de rango a otro formato?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación completa. En comparación con la creación de soluciones personalizadas para renderizar gráficos, esto reduce significativamente la carga de trabajo de desarrollo.
- **Reducción de costos laborales** – Menor necesidad de personal dedicado a la consolidación de documentos.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Sin mantenimiento de servidores** – Sin servidores que mantener, sin actualizaciones de software y sin problemas de compatibilidad.
- **Preserva el formato complejo de Excel** – Los archivos de salida conservan el formato original de la hoja de cálculo.

## ¿Cómo usar la API de exportación de rango de hoja de cálculo como formato con SDK?

### Especificación de la API de exportación de rango como formato

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Especificación de la API de exportación de rango como formato</a> proporciona una interfaz de programación accesible públicamente, lo que permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole exportar un rango de hoja de cálculo a un archivo en cierto formato con un código conciso. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}