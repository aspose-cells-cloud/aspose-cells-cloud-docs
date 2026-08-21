---
title: "Aspose.Cells Cloud – Fusionar archivos de Excel en la nube | Combinar hojas de cálculo mediante API"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Fusionar archivos de Excel en la nube | Combinar hojas de cálculo en línea con la API de Aspose.Cells Cloud"
linktitle: "Fusionar hoja de cálculo remota"
type: docs
url: /es/merge-remote-spreadsheet/
keywords: "Aspose.Cells, fusionar Excel, API en la nube, combinar hoja de cálculo"
description: "Fusionar libros de Excel almacenados en el almacenamiento en la nube utilizando la API de Aspose.Cells Cloud. Especifique el formato de salida, la carpeta de destino y el modo de fusión en una única llamada HTTPS."
weight: 100
---

Fusione rápidamente archivos de Excel almacenados en la nube con otras hojas de cálculo mediante la API de Aspose.Cells Cloud, y especifique el formato de los datos de salida y la ubicación del almacenamiento.

## API para fusionar hojas de cálculo remotas

Antes de llamar a esta operación, asegúrese de tener:

- Un **token de acceso JWT** válido (consulte la guía de autenticación).
- El libro de origen y todos los archivos que se van a fusionar cargados en su almacenamiento en la nube.
- Permisos adecuados para leer desde la carpeta de origen y escribir en la carpeta de destino.

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud:

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                              |
| :------------------- | :------ | :-------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String  | Ruta                                    | Nombre del archivo del libro de origen que se va a fusionar.                                                                            |
| mergedSpreadsheet    | String  | Consulta                                | Lista separada por comas de nombres de archivos de hoja de cálculo que se fusionarán en el libro de origen.                              |
| folder               | String  | Consulta                                | Ruta de la carpeta en el almacenamiento en la nube que contiene el libro de origen.                                                     |
| outFormat            | String  | Consulta                                | Formato deseado para el archivo de salida fusionado (por ejemplo, `XLSX`, `PDF`, `CSV`).                                                |
| mergeInOneSheet      | Boolean | Consulta                                | Establezca en `true` para fusionar todos los datos de origen en una sola hoja de cálculo; `false` crea hojas de cálculo separadas por archivo. |
| storageName          | String  | Consulta                                | _(Opcional)_ Nombre del almacenamiento en la nube donde reside el libro de origen. Si se omite, se utiliza el almacenamiento predeterminado. |
| outPath              | String  | Consulta                                | _(Opcional)_ Ruta de la carpeta de destino en el almacenamiento en la nube para guardar el archivo fusionado. Si se omite, el archivo se guarda en la carpeta de origen. |
| outStorageName       | String  | Consulta                                | Nombre del almacenamiento en la nube para guardar el archivo de salida.                                                                  |
| fontsLocation        | String  | Consulta                                | _(Opcional)_ Ruta personalizada de la carpeta para archivos de fuentes utilizados durante la conversión a formatos de imagen/PDF.         |
| region               | String  | Consulta                                | _(Opcional)_ Configuración regional/localización para el formato de fechas, números y monedas en el archivo de salida (por ejemplo, `en-US`, `de-DE`). |
| password             | String  | Consulta                                | _(Opcional)_ Contraseña necesaria para abrir el libro de origen si está protegido.                                                      |

### Respuesta

**Estado:** `200 OK`

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

El archivo se puede descargar directamente o guardarse en la ubicación especificada por `outPath`.

**Detalles de respuesta correcta**

| Código de estado | Tipo de contenido            | Descripción                               |
| ---------------- | ---------------------------- | ----------------------------------------- |
| 200 OK           | `application/octet-stream`   | Flujo binario del archivo del libro fusionado. |

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                     |
| ------ | ----------------------- | --------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido).   |
| 401    | No autorizado           | Token JWT no válido o faltante.                                 |
| 413    | Carga demasiado grande   | El archivo cargado excede el límite de tamaño.                  |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

## ¿Dónde debemos utilizar la API para fusionar hojas de cálculo remotas?

### Integración de datos de nivel empresarial

- **Consolidación de informes multiprofesional** – Consolidar informes de Excel independientes enviados por equipos de ventas, marketing, finanzas y otros departamentos.
- **Resumen de datos por sucursal** – Resumir datos de rendimiento de cada sucursal en todo el mundo.
- **Consolidación de datos de socios** – Fusionar envíos de datos de múltiples socios en un solo libro.

### Flujo de trabajo de procesamiento de documentos en la nube

- Procesamiento de archivos en almacenamiento en la nube: Fusionar directamente archivos de Excel almacenados en AWS S3, Azure Blob o Google Cloud Storage.
- **Consolidación de datos de múltiples orígenes** – Combinar archivos de distintas ubicaciones en la nube en un solo libro.
- **Tuberías automatizadas de datos** – Integrar la API en procesos ETL para automatizar la fusión de archivos.

### Automatización de gestión de documentos

- **Consolidación por control de versiones** – Fusionar distintas versiones de un plan de proyecto o libro de presupuesto.
- **Relleno de datos en plantillas** – Insertar archivos de datos en plantillas estandarizadas de informes.
- **Generación automática de informes periódicos** – Automatizar informes semanales, mensuales y trimestrales.

### Colaboración multiplataforma

- **Colaboración con equipos remotos** – Consolidar el trabajo enviado por miembros del equipo distribuidos.
- **Organización de datos de clientes** – Fusionar datos de pedidos o comentarios de múltiples clientes.
- **Resumen de información de proveedores** – Combinar presupuestos o información de productos de varios proveedores.

## ¿Por qué debería utilizar la API para fusionar hojas de cálculo remotas?

- **Fácil de usar para desarrolladores** – Aspose.Cells Cloud proporciona SDK para muchos lenguajes, acortando el tiempo de desarrollo y ofreciendo documentación completa. Comparado con la construcción de una solución personalizada, reduce drásticamente la carga de trabajo.
- **Reducción de costos laborales** – Disminuye la necesidad de personal dedicado a la consolidación manual de documentos.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Cero costos de mantenimiento** – Sin servidores que mantener, sin actualizaciones de software y sin preocupaciones por compatibilidad.

## Cómo utilizar la API para fusionar hojas de cálculo remotas con SDK

### Especificación de la API para fusionar hojas de cálculo remotas

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">Especificación de la API para fusionar hojas de cálculo remotas</a> describe la interfaz REST que se puede llamar directamente desde cualquier cliente HTTP.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
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

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel y le permite fusionar una hoja de cálculo en otra mediante un fragmento de código breve.  
Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells Cloud utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}