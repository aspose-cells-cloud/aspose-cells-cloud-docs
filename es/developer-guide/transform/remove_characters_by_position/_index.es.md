---
title: "Eliminar Caracteres por Posición"
ArticleTitle: "Eliminar Caracteres por Posición – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Eliminar Caracteres por Posición"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Eliminar Caracteres, API"
description: "Elimina caracteres de celdas por posición en una hoja de cálculo."
weight: 100
---

## Eliminación de Caracteres por Posición en los Servicios Web de Aspose.Cells Cloud

Elimina caracteres de todas las celdas del rango objetivo por posición (los primeros/últimos N caracteres, antes/después de una subcadena o entre dos delimitadores), preservando fórmulas, formato y validación de datos.

### Punto de conexión de la API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la Solicitud

| Nombre del Parámetro      | Tipo    | Ruta/Cadena de Consulta/Cuerpo HTTP | Descripción                                                                                                          |
|---------------------------|---------|--------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | File    | FormData                             | Cargar archivo de hoja de cálculo.                                                                                  |
| theFirstNCharacters       | Integer | Query                                | Especificar la eliminación de los primeros n caracteres de las celdas seleccionadas. Opcional.                     |
| theLastNCharacters        | Integer | Query                                | Especificar la eliminación de los últimos n caracteres de las celdas seleccionadas. Opcional.                      |
| allCharactersBeforeText   | String  | Query                                | Eliminar texto ubicado antes de una subcadena especificada. Opcional.                                               |
| allCharactersAfterText    | String  | Query                                | Eliminar texto ubicado después de una subcadena especificada. Opcional.                                             |
| caseSensitive             | Boolean | Query                                | Afecta al modo `Substring` y a `CustomChars` cuando está habilitado. Opcional.                                      |
| worksheet                 | String  | Query                                | Especificar la hoja de cálculo de la hoja de cálculo. Opcional.                                                     |
| range                     | String  | Query                                | Especificar el rango de la hoja de cálculo (por ejemplo, `A1:B10`). Opcional.                                       |
| outPath                   | String  | Query                                | (Opcional) Ruta de la carpeta donde se almacena el libro. Por defecto es null. Opcional.                            |
| outStorageName            | String  | Query                                | Nombre del almacenamiento para el archivo de salida. Opcional.                                                      |
| region                    | String  | Query                                | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Opcional.                      |
| password                  | String  | Query                                | Contraseña para abrir el archivo de hoja de cálculo. Opcional.                                                      |

### Parámetro del Cuerpo de la Solicitud

| Nombre del Parámetro | Tipo | Descripción                 |
| --------------------- | ---- | --------------------------- |
| Spreadsheet           | File | Cargar archivo de hoja de cálculo. |

### **Respuesta**

```json
{
  "status": "OK",
  "message": "Caracteres eliminados correctamente.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Códigos de Estado de Respuesta**

| Código | Significado            | Descripción                                              |
|--------|------------------------|----------------------------------------------------------|
| 200    | OK                     | La operación se completó correctamente y se devuelve el archivo procesado. |
| 400    | Solicitud Incorrecta   | La solicitud tiene un formato incorrecto o contiene parámetros inválidos. |
| 401    | No Autorizado          | La autenticación falló o el token JWT falta o es inválido. |
| 413    | Carga Demasiado Grande | El archivo cargado supera el límite de tamaño permitido. |
| 500    | Error Interno del Servidor | Ocurrió un error inesperado en el lado del servidor. |

## Cómo Usar la Funcionalidad de Eliminar Caracteres por Posición con SDK

### Especificación de la Funcionalidad de Eliminar Caracteres por Posición

La [Especificación de la API Eliminar Caracteres por Posición](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Caracteres eliminados correctamente.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
`[TBD]`
---