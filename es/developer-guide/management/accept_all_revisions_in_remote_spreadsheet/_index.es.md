---
title: "Aceptar Todas las Revisiones en una Hoja de Cálculo Remota"
ArticleTitle: "Aceptar Todas las Revisiones en una Hoja de Cálculo Remota – Aspose.Cells Cloud"
second_title: "Documentos"
linktype: "Aceptar Todas las Revisiones en una Hoja de Cálculo Remota"
type: docs
url: /es/cells/accept-all-revisions
aliases: [  /es/cells/accept-all-revisions ]
keywords: "Aspose.Cells, AcceptAllRevisions, Hoja de cálculo remota"
description: "Acepta todas las revisiones en una hoja de cálculo remota y devuelve el archivo de libro actualizado."
weight: 1000
---

## Aceptar Todas las Revisiones en una Hoja de Cálculo Remota de los Servicios Web de Aspose.Cells Cloud

Acepta todos los cambios rastreados (revisiones) en el libro especificado almacenado en el almacenamiento remoto. La operación puede escribir opcionalmente el libro resultante en una ubicación o almacenamiento diferente y devuelve el archivo actualizado como un flujo binario.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|------|----------------------------------------|-------------|
| name | string | Ruta | El nombre del archivo de libro almacenado en el almacenamiento remoto. |
| folder | string | Consulta | (Opcional) Carpeta en el almacenamiento donde se encuentra el libro. |
| storageName | string | Consulta | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Usa el almacenamiento predeterminado si se omite. |
| outPath | string | Consulta | (Opcional) Ruta de la carpeta donde se debe guardar el libro actualizado. El valor predeterminado es null. |
| outStorageName | string | Consulta | (Opcional) Nombre del almacenamiento de salida para el archivo. |
| fontsLocation | string | Consulta | (Opcional) Ruta a la ubicación personalizada de fuentes. |
| region | string | Consulta | (Opcional) Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | string | Consulta | (Opcional) Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| *Ninguno* | *Ninguno* | Esta operación no requiere cuerpo de solicitud. |

### **Respuesta**

```json
{
  "File": " Flujo binario del libro actualizado (por ejemplo, .xlsx) devuelto como cuerpo de la respuesta."
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Se devuelve el libro con todas las revisiones aceptadas como un flujo binario. |
| 400 | Solicitud incorrecta | Faltan parámetros obligatorios o formato de solicitud inválido. |
| 401 | No autorizado | Token JWT inválido o ausente. |
| 413 | Payload demasiado grande | La solicitud excede los límites de tamaño permitidos. |
| 500 | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo usar Aceptar Todas las Revisiones en una Hoja de Cálculo Remota con SDK

### Especificación de Aceptar Todas las Revisiones en una Hoja de Cálculo Remota

La [Especificación de la API Aceptar Todas las Revisiones en una Hoja de Cálculo Remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Flujo binario del libro actualizado (por ejemplo, .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDK:
 `[TBD]`
---