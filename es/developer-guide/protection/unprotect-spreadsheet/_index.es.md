---
title: "API Web de desprotección de Excel en la nube de Aspose.Cells – Eliminar programáticamente contraseñas de apertura y modificación"
second_title: "Documento"
ArticleTitle: "Eliminar la protección por contraseña de Excel – Desbloquear contraseñas de apertura y modificación al instante"
linktitle: "Desproteger hoja de cálculo"
type: docs
url: /es/unprotect-spreadsheet/
keywords: "desproteger, hoja de cálculo, Aspose.Cells, API, Excel, eliminación de contraseña"
description: "Elimine las contraseñas de apertura y modificación de archivos de Excel mediante programación con la API de desprotección de hojas de cálculo de Aspose.Cells Cloud. Admite .xlsx/.xls, autenticación OAuth2 y procesamiento por lotes."
weight: 100
---

La API de desprotección de hojas de cálculo elimina la protección por contraseña de apertura y modificación de archivos de Excel en una sola llamada. Es ideal para canalizaciones de datos, sistemas de gestión de documentos y flujos de trabajo de migración.

## **API de desprotección de hojas de cálculo**

### **API web**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                 |
|----------------------|--------|-----------|---------------------------------------------------------------------------------------------|
| Spreadsheet          | File   | FormData  | El archivo de Excel que se va a desproteger.                                                |
| password             | String | Query     | La contraseña que protege el archivo contra su apertura.                                    |
| modifyPassword       | String | Query     | La contraseña necesaria para modificar el archivo (opcional si solo está establecida la contraseña de apertura). |
| outPath              | String | Query     | (Opcional) Ruta de carpeta donde se guardará la hoja de cálculo desprotegida.               |
| outStorageName       | String | Query     | (Opcional) Nombre del almacenamiento donde se escribirá el archivo de salida.               |
| region               | String | Query     | (Opcional) Configuración de región de la hoja de cálculo.                                   |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Una respuesta correcta devuelve el archivo desprotegido como un flujo. El archivo puede guardarse en la ubicación especificada por `outPath`/`outStorageName` o recuperarse directamente desde la carga útil de la respuesta.

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                 |
|--------|-------------------------|-------------------------------------------------------------|
| 200    | OK (Correcto)           | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o faltante.                              |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.          |
| 500    | Error interno del servidor | Error inesperado en el servidor.                         |

## ¿Cuándo debería utilizar la API de desprotección de hojas de cálculo?

- **Recuperar el acceso a hojas de cálculo bloqueadas** – Elimine rápidamente contraseñas de apertura o modificación olvidadas sin intervención manual.
- **Automatizar el desbloqueo masivo** – Procese grandes cantidades de archivos en proyectos de migración de datos o archivado.
- **Integrar con flujos de trabajo existentes** – Combine con APIs de almacenamiento o conversión para crear canalizaciones integrales (por ejemplo, subir → desproteger → convertir a PDF).
- **Mantener la seguridad de los datos** – La operación se realiza del lado del servidor, manteniendo los archivos originales seguros mientras la versión desprotegida se almacena en su almacenamiento en la nube.

## Cómo utilizar la API de desprotección de hojas de cálculo con SDKs

### **Especificación OpenAPI**

La [especificación de la API de desprotección de hojas de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) proporciona una interfaz de programación accesible públicamente para facilitar interacciones REST directas desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

### **Utilizar los SDKs de Aspose.Cells Cloud**

El uso de un SDK simplifica la llamada al manejar la autenticación, la construcción de la solicitud y el análisis de la respuesta. Los SDKs están disponibles para muchos lenguajes e incluyen métodos listos para usar para desproteger hojas de cálculo.

Los siguientes ejemplos de código ilustran cómo llamar a la API de desprotección de hojas de cálculo mediante diversos SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}