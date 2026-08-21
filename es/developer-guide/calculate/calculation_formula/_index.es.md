---
title: "Calcular Fórmula"
ArticleTitle: "Calcular Fórmula – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Calcular Fórmula"
type: docs
url: /es/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, calcular fórmula, hoja de cálculo, API"
description: "Calcular fórmula en una hoja de cálculo usando la API de Aspose.Cells Cloud."
weight: 100
---

## La función Calcular Fórmula de los servicios web Aspose.Cells Cloud

Calcula una fórmula especificada en una hoja de cálculo dada de un archivo de hoja de cálculo cargado y devuelve la hoja de cálculo resultante como un flujo de archivos. Esta operación admite el procesamiento según la configuración regional mediante el parámetro **region** y puede abrir archivos protegidos con contraseña.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|--------|-------------------------------------|-------------|
| Spreadsheet          | Archivo | FormData                            | Archivo de hoja de cálculo cargado. |
| worksheet            | Cadena  | Consulta                            | Nombre de la hoja de cálculo que contiene la fórmula. |
| formula              | Cadena  | Consulta                            | Fórmula que se va a calcular (por ejemplo, `=SUM(A1:B2)`). |
| region               | Cadena  | Consulta                            | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato numérico, el análisis de fechas y el comportamiento específico de la región. |
| password             | Cadena  | Consulta                            | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| --------------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Respuesta**

```json
{
  "File": "<flujo binario de la hoja de cálculo resultante>"
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | El cálculo se realizó correctamente; se devuelve el archivo de hoja de cálculo resultante. |
| 400 | Solicitud incorrecta | Uno o más parámetros de solicitud faltan o no son válidos. |
| 401 | No autorizado | Falló la autenticación o el token JWT falta o no es válido. |
| 413 | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño permitido. |
| 500 | Error interno del servidor | Ocurrió un error inesperado en el servidor. |

## Cómo usar Calcular Fórmula con SDK

### Especificación de Calcular Fórmula

La [Especificación de la API Calcular Fórmula](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=es-ES&password=MiContraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token jwt>" \
  -F "Spreadsheet=@ejemplo.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "<flujo binario de la hoja de cálculo resultante>"
}
```

{< /tab >}

{< /tabs >}

### Uso de los SDK de Aspose Cells Cloud

Usar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstrae los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
 `[TBD]`
---