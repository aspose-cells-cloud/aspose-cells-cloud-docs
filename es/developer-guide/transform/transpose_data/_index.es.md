---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "TransposeData"
type: docs
url: /cells/transpose
aliases: ["/cells/transpose"]
keywords: "TransposeData, Aspose.Cells, API en la nube, hoja de cálculo, transponer"
description: "Intercambia filas y columnas en la hoja de cálculo."
weight: 1000
---

## TransposeData de los servicios web de Aspose.Cells Cloud

Intercambia filas y columnas en la hoja de cálculo.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|------|-----------------------------------------|-------------|
| Spreadsheet            | File | FormData                                | Archivo de hoja de cálculo cargado. |
| worksheet              | String | Query                                   | Nombre de la hoja de cálculo. |
| cellArea               | String | Query                                   | Rango de datos especificado. |
| outPath                | String | Query                                   | (Opcional) Ruta de la carpeta donde se guarda el libro. Por defecto es null. |
| outStorageName         | String | Query                                   | Nombre del almacenamiento para el archivo de salida. |
| region                 | String | Query                                   | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, análisis de fechas y comportamiento específico de la configuración regional. |
| password               | String | Query                                   | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| [TBD]                | [TBD] | [TBD]       |

### **Respuesta**

```json
{
  "file": "flujo binario de la hoja de cálculo transpuesta"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Se devuelve el archivo de hoja de cálculo transpuesta. |
| 400 | Petición incorrecta | Parámetros de entrada inválidos o solicitud mal formada. |
| 401 | No autorizado | La autenticación falló o el token JWT falta o no es válido. |
| 413 | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | Error inesperado en el servidor. |

## Cómo usar TransposeData con SDKs

### Especificación de TransposeData

La [Especificación de la API TransposeData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Hoja1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=es-ES&password=MiContraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token JWT>" \
  -F "Spreadsheet=@ejemplo.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "flujo binario de la hoja de cálculo transpuesta"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDKs de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells Cloud utilizando diversos SDKs:
`[TBD]`
---