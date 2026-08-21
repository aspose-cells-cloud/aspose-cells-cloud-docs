---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /es/cells/flip
aliases: []
keywords: "FlipData, Transformar, Aspose.Cells"
description: "Transpone un rango de datos especificado en un archivo de hoja de cálculo."
weight: 100
---

## FlipData de los servicios web de Aspose.Cells Cloud

Esta API invierte la orientación de una matriz de datos dada. Por ejemplo, un rango de 3x2 (3 filas, 2 columnas) se convertirá en un rango de 2x3 (2 filas, 3 columnas) en la salida. Se utiliza comúnmente para reestructurar datos y cumplir con los requisitos de entrada de distintos gráficos, informes o modelos de datos.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|---------|------------------------------------------|-------------|
| Spreadsheet          | File    | FormData                                 | Archivo de hoja de cálculo subido. |
| worksheet            | String  | Query                                    | Nombre de la hoja de cálculo. |
| cellArea             | String  | Query                                    | Un rango de datos especificado. |
| Horizontal           | Boolean | Query                                    | Invertir horizontalmente / verticalmente. Valor predeterminado: true |
| outPath              | String  | Query                                    | (Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es null. |
| outStorageName       | String  | Query                                    | Nombre del almacenamiento del archivo de salida. |
| region               | String  | Query                                    | Configuración regional / de idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String  | Query                                    | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| --------------------- | ---- | ----------- |
| *Ninguno*             | *N/A* | *No se requiere ningún cuerpo JSON adicional; el archivo se envía como multipart/form-data.* |

### **Respuesta**

```json
{
  "File": "<flujo binario del libro transformado>"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200    | OK          | La operación se completó correctamente y se devuelve el archivo de hoja de cálculo transformado. |
| 400    | Solicitud incorrecta | Falta uno o más parámetros obligatorios o son inválidos. |
| 401    | No autorizado | Falló la autenticación: falta o es inválido el token JWT. |
| 413    | Payload demasiado grande | El archivo subido supera el límite de tamaño permitido. |
| 500    | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo usar FlipData con SDKs

### Especificación de FlipData

La [Especificación de la API FlipData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Hoja1&cellArea=A1:B3&Horizontal=true&outPath=output%2Fcarpeta&outStorageName=MiAlmacenamiento&region=es-ES&password=MiContraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token jwt>" \
  -F "Spreadsheet=@ejemplo.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<flujo binario del libro transformado>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDKs de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracte los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante distintos SDKs:
 `[TBD]`
---