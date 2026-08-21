---
title: "API Web de Protección de Contraseña de Excel en Aspose.Cells Cloud – Automatice la Cifrado de Contraseñas de Apertura y Modificación"
second_title: "Guía para Desarrolladores sobre la Protección de Excel"
ArticleTitle: "Herramienta de Protección de Contraseña de Excel – Configure Contraseñas de Apertura y Modificación – Proteja Sus Hojas de Cálculo"
linktype: "Proteger Hoja de Cálculo"
type: docs
url: /es/protect-spreadsheet/
keywords: "Aspose.Cells, protección de contraseña de Excel, API, contraseña de apertura, contraseña de modificación, almacenamiento en la nube, seguridad de hojas de cálculo"
description: "Proteja programáticamente archivos de Excel con Aspose.Cells Cloud. Establezca tanto contraseñas de apertura como de modificación mediante una única llamada a la API. Compatible con .xlsx, .xls y almacenamiento en la nube. Pruébelo gratis."
weight: 100
---

Automatice la protección de contraseñas de Excel a gran escala con nuestra API para desarrolladores: aplique tanto contraseñas de apertura como de modificación de forma programática. Ideal para flujos de trabajo empresariales y compatible con formatos .xlsx y versiones anteriores. Obtenga documentación y comience su integración gratuita hoy mismo.

## **API de Protección de Hoja de Cálculo**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de la Solicitud:**

| Nombre del Parámetro | Tipo   | Ruta/Cadena de Consulta/Cuerpo HTTP | Descripción                                                                                                                                    |
| :------------------- | :----- | :----------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData                             | El archivo de hoja de cálculo de Excel que se cargará y protegerá mediante cifrado con contraseña.                                           |
| openPassword         | String | Query                                | La contraseña necesaria para abrir (descifrar) la hoja de cálculo protegida.                                                                  |
| modifyPassword       | String | Query                                | La contraseña necesaria para habilitar la edición o modificación del contenido de la hoja de cálculo.                                         |
| outPath              | String | Query                                | (Opcional) Especifica la ruta de la carpeta de salida donde se guardará el libro protegido. Si no se proporciona, el archivo se devuelve en la respuesta. |
| outStorageName       | String | Query                                | El nombre del almacenamiento en la nube utilizado para guardar el archivo protegido de salida.                                               |
| region               | String | Query                                | Especifica la configuración regional/cultural (por ejemplo, formato de fecha, formato numérico) aplicada a la hoja de cálculo durante el procesamiento. |

**Autenticación**  
Todas las llamadas a la API de Protección de Hoja de Cálculo requieren un token de acceso OAuth 2.0 válido. Incluya el token en el encabezado `Authorization`:

```http
Authorization: Bearer {access_token}
```

El token debe obtenerse del punto final de autenticación de Aspose Cloud y debe incluir el ámbito **Cells**.

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

**Códigos de Estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud Incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No Autorizado           | Token JWT inválido o faltante.                                    |
| 413    | Carga de Datos Demasiado Grande | El archivo cargado excede el límite de tamaño.                  |
| 500    | Error Interno del Servidor | Error inesperado del servidor.                                    |

## ¿Dónde debemos usar la API de Protección de Hoja de Cálculo?

- **Proteger Datos Financieros Sensibles** – Proteja archivos de Excel que contengan datos como presupuestos, facturas o información de nómina mediante contraseñas de apertura y modificación para evitar accesos o ediciones no autorizadas.
- **Compartir Informes Confidenciales de forma Segura** – Asegúrese de que solo los destinatarios autorizados puedan ver o modificar informes empresariales, de auditoría o de cumplimiento al distribuirlos interna o externamente.
- **Automatizar la Seguridad de Documentos en Flujos de Trabajo** – Integre la API en sistemas empresariales (por ejemplo, ERP, CRM) para proteger automáticamente con contraseña las hojas de cálculo generadas antes de su almacenamiento o entrega por correo electrónico.
- **Aplicar Acceso de Solo Lectura** – Permita que los usuarios abran informes para su visualización mientras restringe modificaciones mediante una contraseña de modificación independiente; ideal para plantillas o conjuntos de datos finales.
- **Cumplir con Normativas Regulatorias** – Ayude a satisfacer los requisitos de GDPR, HIPAA o SOX mediante el cifrado de datos sensibles en hojas de cálculo, tanto en reposo como en tránsito, mediante protección automatizada.

## ¿Por qué debería usar la API de Protección de Hoja de Cálculo?

- **Amigable para Desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de una documentación completa. Comparado con la construcción de soluciones personalizadas, esto reduce significativamente la carga de desarrollo.
- **Reduce la Necesidad de Personal** – Automatiza la consolidación y seguridad de documentos, reduciendo la necesidad de personal dedicado.
- **Pago por Uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utilice.
- **Cero Costos de Mantenimiento** – Sin servidores que mantener, sin actualizaciones de software y sin preocupaciones por compatibilidad.
- **Preserva Todo el Formato Original de Excel** al aplicar protección con contraseña, asegurando que el libro protegido se vea exactamente igual que el archivo original.

## Cómo Usar la API de Protección de Hoja de Cálculo con SDKs

### Especificación OpenAPI

La [Especificación de la API de Protección de Hoja de Cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) proporciona una interfaz de programación accesible públicamente para facilitar interacciones REST directas desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
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

### Utilizar los SDKs de Aspose.Cells Cloud

Utilizar el SDK es la mejor manera de acelerar el desarrollo. El SDK maneja los detalles subyacentes, permitiéndole simplemente implementar la funcionalidad de protección de hoja de cálculo con un mínimo de código. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}