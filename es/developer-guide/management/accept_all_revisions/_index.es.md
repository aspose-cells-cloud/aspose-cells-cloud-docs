---
title: "Aceptar todas las revisiones"
ArticleTitle: "Aceptar todas las revisiones – Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Aceptar todas las revisiones"
type: docs
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, hoja de cálculo, revisiones"
description: "Acepta todas las revisiones en un archivo de hoja de cálculo mediante la API de Aspose.Cells Cloud."
weight: 100
---

## El método AcceptAllRevisions de los Servicios Web de Aspose.Cells Cloud

Acepta todas las revisiones en el archivo de hoja de cálculo cargado y devuelve el libro procesado.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|--------|------------------------------------------|-------------|
| Spreadsheet          | Archivo | FormData (Cuerpo HTTP)                  | Carga el archivo de hoja de cálculo. |
| outPath              | Cadena | Cadena de consulta                       | (Opcional) Ruta de la carpeta donde se almacena el libro. Por defecto es null. |
| outStorageName       | Cadena | Cadena de consulta                       | Nombre del almacenamiento para el archivo de salida. |
| fontsLocation        | Cadena | Cadena de consulta                       | Uso de fuentes personalizadas. |
| region               | Cadena | Cadena de consulta                       | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | Cadena | Cadena de consulta                       | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo   | Descripción |
| ---------------------|--------|-------------|
| Spreadsheet          | Archivo | Carga el archivo de hoja de cálculo. |

### **Respuesta**

```json
{
  "File": "Flujo binario de la hoja de cálculo procesada"
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | Las revisiones se aceptaron correctamente y se devuelve el archivo procesado. |
| 400 | Solicitud incorrecta | La solicitud no es válida (por ejemplo, falta el archivo obligatorio o los parámetros son inválidos). |
| 401 | No autorizado | La autenticación falló o el token JWT falta o es inválido. |
| 413 | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo usar AcceptAllRevisions con los SDK

### Especificación de AcceptAllRevisions

La [Especificación de la API AcceptAllRevisions](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=carpetaSalida&outStorageName=MiAlmacenamiento&fontsLocation=/fonts&region=es-ES&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'Spreadsheet=@ejemplo.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "Flujo binario de la hoja de cálculo procesada"
}
```

{< /tab >}

{< /tabs >}

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstrae los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="[TBD]" rel="noopener noreferrer">repositorio de GitHub</a> para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells Cloud mediante diversos SDK:
 `[TBD]`
---