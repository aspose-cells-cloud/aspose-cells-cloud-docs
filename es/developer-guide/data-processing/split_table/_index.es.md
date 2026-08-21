---
title: "Dividir Tabla"
ArticleTitle: "Dividir Tabla – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Dividir Tabla"
type: docs
url: /es/cells/split/table
aliases: []
keywords: "Aspose.Cells, Dividir Tabla, API"
description: "API para dividir una tabla en una hoja de cálculo según los valores de una columna."
weight: 1
---

## El método SplitTable de los servicios web de Aspose.Cells Cloud

Este método realiza una operación de división sobre la tabla de origen agrupando las filas según los valores distintos de la columna especificada. Cada grupo de datos (para cada valor único de división) se procesa luego como una unidad de datos independiente. El destino de exportación se controla mediante dos parámetros booleanos clave:
- Determina la estructura del libro. Si es `true`, cada unidad dividida se guarda en un archivo de libro independiente. Si es `false`, cada unidad se convierte en una nueva hoja dentro del libro actual.
- Determina el empaquetado de salida. Cuando se establece en `true` y se combina con `toNewWorkbook` = `true`, el método genera varios archivos individuales y los devuelve como un archivo ZIP. Cuando es `false`, todos los datos se consolidan en un único archivo (ya sea un libro multihoja o un solo archivo según otras configuraciones).

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                                                                                   |
|----------------------|---------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | Archivo | FormData                            | Archivo de hoja de cálculo a cargar.                                                                                                                                          |
| worksheet            | Cadena  | Query                               | Hoja de cálculo que contiene la tabla.                                                                                                                                        |
| tableName            | Cadena  | Query                               | Tabla de datos que debe dividirse.                                                                                                                                            |
| splitColumnName      | Cadena  | Query                               | Nombre de la columna según la cual dividir.                                                                                                                                   |
| saveSplitColumn      | Boolean | Query                               | Si se debe conservar la columna utilizada para dividir.                                                                                                                       |
| splitRowNumber       | Entero  | Query                               | [TBD]                                                                                                                                                                          |
| toNewWorkbook        | Boolean | Query                               | Control del destino de exportación: `true` – Crea nuevos archivos de libro que contienen los datos divididos; `false` – Añade una nueva hoja al libro actual.                 |
| toMultipleFiles      | Boolean | Query                               | `true` – Exporta los datos de la tabla como **varios archivos independientes** (devueltos como archivo ZIP); `false` – Almacena todos los datos en un **único archivo** con varias hojas. Valor predeterminado: `false`. |
| outPath              | Cadena  | Query                               | (Opcional) Ruta de la carpeta donde se almacenará el libro. Por defecto es `null`.                                                                                            |
| outStorageName       | Cadena  | Query                               | Nombre del almacenamiento para el archivo de salida.                                                                                                                          |
| fontsLocation        | Cadena  | Query                               | Uso de fuentes personalizadas.                                                                                                                                                 |
| region               | Cadena  | Query                               | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | Cadena  | Query                               | Contraseña para abrir el archivo de hoja de cálculo.                                                                                                                           |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo   | Descripción                     |
|----------------------|--------|---------------------------------|
| Spreadsheet          | Archivo | Archivo de hoja de cálculo a cargar. |

### **Respuesta**

```json
{
  "file": "secuencia binaria (archivo ZIP o libro, según los parámetros)"
}
```

**Códigos de estado de respuesta**

| Código | Significado            | Descripción                                                                 |
|--------|------------------------|-----------------------------------------------------------------------------|
| 200    | Correcto               | La operación de división se completó correctamente. La respuesta contiene el archivo generado (archivo ZIP o libro). |
| 400    | Solicitud incorrecta   | URL o parámetros de solicitud inválidos.                                    |
| 401    | No autorizado          | La autenticación ha fallado o no se han proporcionado credenciales.         |
| 404    | No encontrado          | El archivo de origen no es accesible.                                       |
| 413    | Carga de solicitud demasiado grande | El tamaño del cuerpo de la solicitud excede el límite permitido. |
| 500    | Error interno del servidor | La hoja de cálculo ha encontrado una anomalia al obtener los datos.    |

## Cómo usar SplitTable con SDK

### Especificación de SplitTable

La [Especificación de la API SplitTable](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "secuencia binaria (archivo ZIP o libro, según los parámetros)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando varios SDK:
`[TBD]`