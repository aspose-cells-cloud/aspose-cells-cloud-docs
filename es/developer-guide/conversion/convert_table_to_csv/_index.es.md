---
title: "Convertir Tabla a CSV"
ArticleTitle: "Convertir Tabla a CSV – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convertir Tabla a CSV"
type: docs
url: /cells/convert/table/csv
aliases: []
keywords: "Convertir Tabla CSV, Aspose.Cells, Cloud API"
description: "Convierte una tabla de una hoja de cálculo en una unidad local a un archivo CSV."
weight: 1
---

## Convertir Tabla a CSV con los Servicios Web de Aspose.Cells Cloud

Este método lee un archivo de hoja de cálculo desde el sistema de archivos local, convierte su tabla especificada a un archivo CSV y devuelve el resultado convertido. Opera completamente en el servidor en la nube, por lo que no es necesario cargar previamente el archivo a un almacenamiento en la nube. La ruta del archivo fuente y el formato de destino deben especificarse correctamente, y se requieren permisos adecuados para leer el archivo fuente. Errores como archivos faltantes, rutas inaccesibles o fallos en la conversión generarán las excepciones correspondientes.

### Punto de conexión de la API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|--------|-------------------------------------|-------------|
| Spreadsheet          | File   | FormData                            | Archivo de hoja de cálculo a subir. |
| worksheet            | String | Query                               | Nombre de la hoja de cálculo. |
| tableName            | String | Query                               | Nombre de la tabla. |
| outPath              | String | Query                               | (Opcional) Ruta de la carpeta donde se guardará el libro. Por defecto es null. |
| outStorageName       | String | Query                               | Nombre del almacenamiento para el archivo de salida. |
| fontsLocation        | String | Query                               | Fuentes personalizadas. |
| AutoRowsFit          | Boolean| Query                               | (Opcional) Ajusta automáticamente todas las filas en las hojas de cálculo. |
| AutoColumnsFit       | Boolean| Query                               | (Opcional) Ajusta automáticamente todas las columnas en las hojas de cálculo. |
| region               | String | Query                               | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, análisis de fechas y comportamiento específico de la configuración regional. |
| password             | String | Query                               | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| *None*               | *None* | *No se requiere cuerpo de solicitud; el archivo se envía como multipart/form-data.* |

### **Respuesta**

```json
{
  "file": "flujo binario del archivo CSV generado"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | La tabla se convirtió correctamente y se devuelve el archivo CSV. |
| 400 | Solicitud incorrecta | Parámetros inválidos o URL con formato incorrecto. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 404 | No encontrado | El archivo fuente no es accesible o no existe. |
| 413 | Carga demasiado grande | El archivo subido excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | La hoja de cálculo encontró una anomalia durante la conversión. |

## Cómo usar Convertir Tabla a CSV con SDKs

### Especificación de Convertir Tabla a CSV

La [Especificación de la API Convertir Tabla a CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "flujo binario del archivo CSV generado"
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells Cloud utilizando diversos SDK:
`[TBD]`
---