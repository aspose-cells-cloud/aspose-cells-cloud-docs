---
title: "Eliminar subcadenas duplicadas en una hoja de cálculo remota"
ArticleTitle: "Eliminar subcadenas duplicadas en una hoja de cálculo remota – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Eliminar subcadenas duplicadas en una hoja de cálculo remota"
type: docs
url: /es/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, Eliminar subcadenas duplicadas, API"
description: "API para encontrar y eliminar subcadenas repetidas dentro de celdas de un rango especificado en un libro de cálculo."
weight: 1
---

## Eliminar subcadenas duplicadas en una hoja de cálculo remota de Aspose.Cells Cloud Web Services

Encuentra y elimina subcadenas repetidas dentro de cada celda del rango seleccionado, utilizando delimitadores definidos por el usuario o predefinidos, preservando al mismo tiempo fórmulas, formato y validación de datos.

**Cómo se detectan los duplicados**  
1. El valor de cada celda se divide en subcadenas mediante los delimitadores elegidos.  
2. La herramienta compara subcadenas **dentro de la misma celda** y conserva únicamente la **primera aparición** de cada subcadena duplicada.  
3. Las subcadenas limpias se vuelven a unir mediante los mismos delimitadores y se escriben de nuevo en la celda.  

**Opciones de delimitadores**  
- Lista predefinida: coma, punto y coma, espacio, tabulador, salto de línea  
- `Custom` (personalizado): introduzca cualquier carácter o caracteres; varios caracteres se tratan como un único delimitador compuesto  
- `TreatConsecutiveDelimitersAsOne` (tratar delimitadores consecutivos como uno solo): colapsa los delimitadores adyacentes en un único separador  

Solo se procesan celdas de tipo cadena; los números, valores booleanos y fórmulas se convierten a cadena antes de dividirlos (las fórmulas se descartan). Devuelve la cantidad de celdas limpiadas y el flujo del libro de cálculo actualizado.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|------|-----------------------------------------|-------------|
| name | string | Ruta | (Obligatorio) Nombre del archivo del libro de cálculo que se va a recuperar. |
| worksheet | string | Ruta | Especifica la hoja de cálculo. |
| range | string | Ruta | Especifica el rango en la hoja de cálculo. |
| delimiters | string | Consulta | Delimitadores utilizados para dividir los valores de celda (por ejemplo, coma, punto y coma, espacio, tabulador, salto de línea). Obligatorio. |
| treatConsecutiveDelimitersAsOne | boolean | Consulta | Colapsa los delimitadores adyacentes en un único separador. Valor predeterminado: true. Opcional. |
| caseSensitive | boolean | Consulta | Realiza una comparación sensible a mayúsculas y minúsculas al detectar duplicados. Opcional. |
| folder | string | Consulta | (Opcional) Ruta de la carpeta donde se almacena el libro de cálculo. Valor predeterminado: null. |
| storageName | string | Consulta | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. |
| region | string | Consulta | Configuración regional / de idioma de la hoja de cálculo (por ejemplo, `es-ES`, `en-US`). Opcional. |
| password | string | Consulta | Contraseña para abrir el archivo de hoja de cálculo. Opcional. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| - | - | No se requiere cuerpo de solicitud para esta operación. |

### **Respuesta**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "flujo de libro de cálculo codificado en base64"
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Operación realizada con éxito; devuelve la cantidad de celdas limpiadas y el flujo del libro de cálculo actualizado. |
| 400 | Solicitud incorrecta | Uno o más parámetros de solicitud faltan o no son válidos. |
| 401 | No autorizado | La autenticación falló o el token JWT falta o no es válido. |
| 413 | Carga útil demasiado grande | La solicitud supera los límites de tamaño permitidos. |
| 500 | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo usar la función Eliminar subcadenas duplicadas en una hoja de cálculo remota con SDK

### Especificación de Eliminar subcadenas duplicadas en una hoja de cálculo remota

La [Especificación de la API Eliminar subcadenas duplicadas en una hoja de cálculo remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}
{< tab tabNum="1" >}
```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "flujo de libro de cálculo codificado en base64"
}
```
{< /tab >}
{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
`[TBD]`