---
title: "Importar datos XML a una hoja de cálculo"
ArticleTitle: "Importar datos XML a una hoja de cálculo – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /es/cells/import/data/xml
aliases: []
keywords: "Importar XML, Aspose.Cells, API"
description: "Importar un archivo de datos XML a una hoja de cálculo local mediante Aspose.Cells Cloud."
weight: 1000
---

## Importación de datos XML a una hoja de cálculo mediante los servicios web de Aspose.Cells Cloud

Importa un archivo de datos XML a una hoja de cálculo local. El método analiza el XML, asigna los datos a la estructura de celdas de la hoja de cálculo y guarda el archivo localmente. Los formatos de hoja de cálculo admitidos incluyen .xlsx y .ods.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                            |
|----------------------|---------|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile             | Archivo | FormData                                | Cargar archivo de datos.                                                                                                               |
| Spreadsheet          | Archivo | FormData                                | Cargar archivo de hoja de cálculo.                                                                                                     |
| worksheet            | Cadena  | Query                                   | Hoja de cálculo en la que se debe importar el dato XML.                                                                                |
| startcell            | Cadena  | Query                                   | Posición inicial para la importación de datos                                                                                         |
| insert               | Booleano| Query                                   | Controla el comportamiento de inserción. true: inserta datos; false: sobrescribe los datos existentes. Valor predeterminado: **true** |
| outPath              | Cadena  | Query                                   | (Opcional) Ruta de la carpeta donde se guarda el libro de trabajo. El valor predeterminado es null.                                   |
| outStorageName       | Cadena  | Query                                   | Nombre del almacenamiento de salida del archivo.                                                                                      |
| fontsLocation        | Cadena  | Query                                   | Utilizar fuentes personalizadas.                                                                                                       |
| region               | Cadena  | Query                                   | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | Cadena  | Query                                   | Contraseña para abrir el archivo de hoja de cálculo.                                                                                  |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
|----------------------|------|-------------|
| *Ninguno*            | -    | -           |

### **Respuesta**

```json
{
  "file": "<flujo binario de la hoja de cálculo actualizada>"
}
```

**Códigos de estado de respuesta**

| Código | Significado            | Descripción                                                                                           |
|--------|------------------------|-------------------------------------------------------------------------------------------------------|
| 200    | OK                     | Datos XML importados correctamente y se devuelve el archivo de hoja de cálculo actualizado.         |
| 400    | Solicitud incorrecta   | URL de solicitud inválida o parámetros obligatorios faltantes.                                       |
| 401    | No autorizado          | La autenticación ha fallado o no se proporcionaron credenciales.                                     |
| 404    | No encontrado          | El archivo de origen no es accesible.                                                                |
| 413    | Carga demasiado grande  | El archivo cargado excede el límite de tamaño permitido.                                             |
| 500    | Error interno del servidor | La hoja de cálculo ha encontrado una anomalia al obtener los datos.                                |

## Cómo utilizar la importación de datos XML a una hoja de cálculo con SDK

### Especificación de importación de datos XML a una hoja de cálculo

La [Especificación de la API de importación de datos XML a una hoja de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{NombreDeArchivoDeDatos}" \
  -F "Spreadsheet=@{NombreDeArchivoDeHojaDeCálculo}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<flujo binario de la hoja de cálculo actualizada>"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracto los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose Cells Cloud mediante varios SDK:
`[TBD]`
---