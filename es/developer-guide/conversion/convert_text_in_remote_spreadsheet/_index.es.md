---
title: "Convertir Texto en una Hoja de Cálculo Remota"
ArticleTitle: "Convertir Texto en una Hoja de Cálculo Remota – Aspose.Cells Cloud"
second_title: "Documentos"
linktype: "Convertir Texto en una Hoja de Cálculo Remota"
type: docs
url: /es/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Conversión de Texto, API"
description: "Convierte texto en un rango especificado de una hoja de cálculo, incluyendo conversión numérica, sustitución de caracteres, manejo de saltos de línea y normalización de caracteres acentuados."
weight: 1000
---

## La función Convertir Texto en una Hoja de Cálculo Remota de los Servicios Web de Aspose.Cells Cloud

Indica la conversión de números almacenados como texto al formato numérico correcto, la sustitución de caracteres no deseados y saltos de línea por caracteres deseados, y la conversión de caracteres acentuados a sus equivalentes sin acentos.

### Punto de acceso de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|------|-------------------------------------|-------------|
| name                 | string | Ruta | (Obligatorio) Nombre del archivo del libro de cálculo que se va a recuperar. |
| worksheet            | string | Ruta | Especifica la hoja de cálculo. |
| range                | string | Ruta | Especifica el rango en la hoja de cálculo. |
| convertTextType      | string | Consulta | Indica el tipo de conversión de texto. (Obligatorio) |
| sourceCharacters     | string | Consulta | Indica los caracteres de origen. (Opcional) |
| targetCharacters     | string | Consulta | Indica los caracteres de destino. (Opcional) |
| folder               | string | Consulta | (Opcional) Ruta de la carpeta donde se almacena el libro de cálculo. El valor predeterminado es null. |
| storageName          | string | Consulta | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Se usa el almacenamiento predeterminado si se omite. |
| region               | string | Consulta | Configuración regional/lingüística de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta al formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. (Opcional) |
| password             | string | Consulta | Contraseña para abrir el archivo de la hoja de cálculo. (Opcional) |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| -                    | -    | -           |

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Conversión de texto completada correctamente.",
  "Data": {
    // Se pueden añadir aquí los detalles del resultado de la conversión, como el número de celdas actualizadas.
  }
}
```

**Códigos de estado de respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200    | OK | La operación de conversión de texto se completó correctamente. |
| 400    | Solicitud incorrecta | La solicitud estaba mal formada o faltaban parámetros obligatorios. |
| 401    | No autorizado | Falló la autenticación o el token JWT es inválido o no se proporcionó. |
| 413    | Carga útil demasiado grande | El cuerpo de la solicitud excede el límite de tamaño permitido. |
| 500    | Error interno del servidor | Se produjo un error inesperado en el servidor. |

## Cómo utilizar la función Convertir Texto en una Hoja de Cálculo Remota con SDK

### Especificación de Convertir Texto en una Hoja de Cálculo Remota

La [Especificación de la API Convertir Texto en una Hoja de Cálculo Remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose Cells Cloud. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Conversión de texto completada correctamente.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Números convertidos, caracteres sustituidos, saltos de línea normalizados."
  }
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
 `[TBD]`
---