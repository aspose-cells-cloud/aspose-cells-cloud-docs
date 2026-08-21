---
title: "Convertir gráfico a PDF"
ArticleTitle: "Convertir gráfico a PDF – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "ConvertChartToPdf"
type: docs
url: /es/cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, conversión de gráficos"
description: "Convierte un gráfico de una hoja de cálculo en una unidad local a PDF."
weight: 100
---

## La conversión de gráfico a PDF de los servicios web de Aspose.Cells Cloud

Este método lee un gráfico desde un archivo de hoja de cálculo proporcionado mediante una carga local de archivos, lo convierte al formato PDF y devuelve el resultado convertido. Funciona completamente en el servidor en la nube, por lo que no se requiere almacenamiento intermedio. La ruta del archivo de origen y el formato de destino deben ser correctos, y se necesitan permisos adecuados para leer el archivo de origen. Errores como archivos faltantes, problemas de acceso o fallos en la conversión generarán respuestas HTTP de error apropiadas.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|--------|--------------------------------------|-------------|
| Spreadsheet          | Archivo | FormData                             | Cargar archivo de hoja de cálculo. |
| worksheet            | Cadena  | Consulta                             | Nombre de la hoja de cálculo. |
| chartIndex           | Entero  | Consulta                             | Índice del gráfico dentro de la hoja de cálculo. |
| outPath              | Cadena  | Consulta                             | (Opcional) Ruta de la carpeta donde se almacena el libro de trabajo. Por defecto es null. |
| outStorageName       | Cadena  | Consulta                             | Nombre del almacenamiento para el archivo de salida. |
| fontsLocation        | Cadena  | Consulta                             | Utilizar fuentes personalizadas. |
| region               | Cadena  | Consulta                             | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formateo de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | Cadena  | Consulta                             | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo   | Descripción |
|----------------------|--------|-------------|
| Spreadsheet          | Archivo | Cargar archivo de hoja de cálculo. |

### **Respuesta**

```json
{
  "ResponseFile": "flujo binario de archivo PDF"
}
```

**Códigos de estado de respuesta**

| Código | Significado        | Descripción |
|--------|--------------------|-------------|
| 200    | Correcto           | Gráfico convertido correctamente a PDF; se devuelve el archivo PDF binario. |
| 400    | Solicitud incorrecta | Parámetros de solicitud inválidos o URL con formato incorrecto. |
| 401    | No autorizado      | La autenticación ha fallado o no se proporcionaron credenciales. |
| 404    | No encontrado      | Archivo de origen no accesible. |
| 413    | Carga demasiado grande | El archivo cargado excede el límite de tamaño permitido. |
| 500    | Error interno del servidor | Se produjo un error al procesar la conversión. |

## Cómo usar la conversión de gráfico a PDF con SDK

### Especificación de conversión de gráfico a PDF

La [especificación de la API de conversión de gráfico a PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}
{< tab tabNum="1" >}
```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "flujo binario de archivo PDF"
}
```
{< /tab >}
{< /tabs >}

### Utilizar SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando varios SDK:
`[TBD]`
---