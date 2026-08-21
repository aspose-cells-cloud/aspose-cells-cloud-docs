---
title: "Importar datos JSON en hoja de cálculo"
ArticleTitle: "Importar datos JSON en hoja de cálculo – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "docs"
url: /es/cells/import/data/json
aliases: []
keywords: "Importar JSON, Aspose.Cells, Hoja de cálculo, API"
description: "Importar archivo de datos JSON en la hoja de cálculo local."
weight: 1
---

## Importación de datos JSON en hoja de cálculo mediante los servicios web de Aspose.Cells Cloud

Importa un archivo de datos JSON en la hoja de cálculo local. Este método analiza el JSON, asigna los datos a la estructura de celdas de la hoja de cálculo y guarda el archivo localmente. Los formatos de hoja de cálculo admitidos incluyen .xlsx y .ods.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|--------|-----------------------------------------|-------------|
| datafile             | Archivo | FormData                                | Subir archivo de datos. |
| Spreadsheet          | Archivo | FormData                                | Subir archivo de hoja de cálculo. |
| worksheet            | Cadena  | Cadena de consulta                      | Hoja de cálculo en la que se importarán los datos JSON. |
| startcell            | Cadena  | Cadena de consulta                      | Posición inicial para la importación de datos. |
| insert               | Booleano | Cadena de consulta                     | Controla el comportamiento de inserción. `true`: inserta datos; `false`: sobrescribe los datos existentes. (Valor predeterminado: `true`) |
| outPath              | Cadena  | Cadena de consulta                      | (Opcional) Ruta de la carpeta donde se almacena el libro de trabajo. El valor predeterminado es `null`. |
| outStorageName       | Cadena  | Cadena de consulta                      | Nombre del almacenamiento para el archivo de salida. |
| fontsLocation        | Cadena  | Cadena de consulta                      | Utilizar fuentes personalizadas. |
| region               | Cadena  | Cadena de consulta                      | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, análisis de fechas y comportamiento específico de la configuración regional. |
| password             | Cadena  | Cadena de consulta                      | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| --------------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Respuesta**

```json
{
  "file": "flujo binario"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | Archivo generado y devuelto correctamente. |
| 400 | Solicitud incorrecta | URL no válida. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Carga útil demasiado grande | [TBD] |
| 500 | Error interno del servidor | La hoja de cálculo ha encontrado una anomalia al obtener los datos. |

## Cómo utilizar la función de importación de datos JSON en hoja de cálculo con SDK

### Especificación de importación de datos JSON en hoja de cálculo

La [especificación de la API de importación de datos JSON en hoja de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}
{< tab tabNum="1" >}
```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "flujo binario"
}
```
{< /tab >}
{< /tabs >}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells Cloud utilizando diversos SDK:
 `[TBD]`
---