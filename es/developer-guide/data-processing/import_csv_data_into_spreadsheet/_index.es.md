---
title: "Importar datos CSV en hoja de cálculo"
ArticleTitle: "Importar datos CSV en hoja de cálculo – Aspose.Cells Cloud API"
second_title: "Documento"
linktype: "docs"
url: /cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, importación CSV, hoja de cálculo, API"
description: "Importar archivo de datos CSV en la hoja de cálculo local mediante la API de Aspose.Cells Cloud."
weight: 100
---

## Importación de datos CSV en hoja de cálculo mediante los servicios web de Aspose.Cells Cloud

Importa un archivo de datos CSV en la hoja de cálculo local. El método analiza el archivo CSV, asigna los datos a la estructura de celdas de la hoja de cálculo y guarda el archivo localmente. Los formatos de hoja de cálculo compatibles incluyen .xlsx y .ods.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro    | Tipo    | Ruta/cadena de consulta/cuerpo HTTP | Descripción                                                                                                                          |
|-------------------------|---------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile                | Archivo | FormData                             | Subir archivo de datos.                                                                                                              |
| Spreadsheet             | Archivo | FormData                             | Subir archivo de hoja de cálculo.                                                                                                    |
| worksheet               | Cadena  | Query                                | Hoja de cálculo en la que se debe importar el datos CSV. (obligatorio)                                                               |
| startcell               | Cadena  | Query                                | Posición inicial para la importación de datos. (obligatorio)                                                                        |
| insert                  | Booleano| Query                                | Controla el comportamiento de inserción: true (insertar datos); false (sobrescribir datos existentes). Valor predeterminado: true (opcional) |
| convertNumericData      | Booleano| Query                                | Indica si las cadenas del archivo de texto se convierten en datos numéricos. Valor predeterminado: true (opcional)                 |
| splitter                | Cadena  | Query                                | Delimitador utilizado para separar los campos CSV. Valor predeterminado: "," (opcional)                                             |
| outPath                 | Cadena  | Query                                | (Opcional) Ruta de carpeta donde se guarda el libro de trabajo. Valor predeterminado: null (opcional)                               |
| outStorageName          | Cadena  | Query                                | Nombre del almacenamiento de salida. (opcional)                                                                                    |
| fontsLocation           | Cadena  | Query                                | Utilizar fuentes personalizadas. (opcional)                                                                                         |
| region                  | Cadena  | Query                                | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, análisis de fechas y comportamiento específico de la configuración regional. (opcional) |
| password                | Cadena  | Query                                | Contraseña para abrir el archivo de hoja de cálculo. (opcional)                                                                     |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| --------------------- | ---- | ----------- |
| [TBD]                | [TBD] | [TBD]      |

### **Respuesta**

```json
{
  "file": "<flujo binario de la hoja de cálculo resultante>"
}
```

**Códigos de estado de respuesta**

| Código | Significado            | Descripción                                                                 |
|--------|------------------------|-----------------------------------------------------------------------------|
| 200    | Correcto               | Datos CSV importados correctamente; se devuelve el archivo de hoja de cálculo resultante. |
| 400    | Solicitud incorrecta   | Parámetros de solicitud inválidos o URL con formato incorrecto.            |
| 401    | No autorizado          | Falló la autenticación o no se proporcionaron credenciales.                |
| 404    | No encontrado          | No se pudo acceder al archivo de origen.                                   |
| 413    | Carga demasiado grande  | Los archivos subidos exceden el límite de tamaño permitido.                |
| 500    | Error interno del servidor | La hoja de cálculo encontró una anomalia al obtener los datos.             |

## Cómo usar la importación de datos CSV en hoja de cálculo con SDK

### Especificación de la importación de datos CSV en hoja de cálculo

La [Especificación de la API de importación de datos CSV en hoja de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flujo binario de la hoja de cálculo resultante>"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDK:
 `[TBD]`
---