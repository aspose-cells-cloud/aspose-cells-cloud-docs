---
title: "Despivotar Tabla"
ArticleTitle: "Despivotar Tabla – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Despivotar Tabla"
type: docs
url: /es/cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Despivotar, Transformar"
description: "Intercambiar filas y columnas en la hoja de cálculo."
weight: 1
---

## La función Despivotar Tabla de Aspose.Cells Cloud Web Services

Intercambiar filas y columnas en la hoja de cálculo.

### Punto de acceso de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                            |
|----------------------|---------|-------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | File    | FormData                            | Archivo de hoja de cálculo subido.                                                                                    |
| worksheet            | String  | Query                               | Nombre de la hoja de cálculo.                                                                                          |
| index                | Integer | Query                               | Un rango de datos especificado.                                                                                        |
| skipEmptyValue       | Boolean | Query                               | Omitir valores vacíos (valor predeterminado: true).                                                                   |
| outPath              | String  | Query                               | (Opcional) Ruta de carpeta donde se almacena el libro. El valor predeterminado es null.                               |
| outStorageName       | String  | Query                               | Nombre del almacenamiento para el archivo de salida.                                                                   |
| region               | String  | Query                               | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, análisis de fechas y comportamiento específico de la configuración regional. |
| password             | String  | Query                               | Contraseña para abrir el archivo de hoja de cálculo.                                                                   |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
|----------------------|------|-------------|
| N/A                  | N/A  | No hay parámetros en el cuerpo de la solicitud. |

### **Respuesta**

```json
{
  "File": "flujo binario de la hoja de cálculo despivotada"
}
```

**Códigos de estado de respuesta**

| Código | Significado        | Descripción                                      |
|--------|--------------------|--------------------------------------------------|
| 200    | OK                 | Se devuelve el archivo de hoja de cálculo despivotada. |
| 400    | Bad Request        | Parámetros de solicitud inválidos.              |
| 401    | Unauthorized       | Autenticación fallida o token JWT ausente/inválido. |
| 413    | Payload Too Large  | El archivo subido excede el límite de tamaño permitido. |
| 500    | Internal Server Error | Error inesperado del servidor.                  |

## Cómo usar la función Despivotar Tabla con SDK

### Especificación de Despivotar Tabla

La [Especificación de la API Despivotar Tabla](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "flujo binario de la hoja de cálculo despivotada"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Usar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracte los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
 `[TBD]`
---