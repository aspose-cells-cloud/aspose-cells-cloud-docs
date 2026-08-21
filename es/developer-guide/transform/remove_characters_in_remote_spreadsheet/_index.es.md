---
title: "Eliminar Caracteres en una Hoja de Cálculo Remota"
ArticleTitle: "Eliminar Caracteres en una Hoja de Cálculo Remota – API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Eliminar Caracteres en una Hoja de Cálculo Remota"
type: docs
url: /es/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, Eliminar Caracteres, Procesamiento de Texto"
description: "Elimina caracteres definidos por el usuario, conjuntos predefinidos de símbolos o cualquier subcadena de cada celda en el rango seleccionado, preservando fórmulas, formato y validación de datos para una hoja de cálculo remota."
weight: 100
---

## El método Eliminar Caracteres en una Hoja de Cálculo Remota de los Servicios Web de Aspose.Cells Cloud

Elimina caracteres definidos por el usuario, conjuntos predefinidos de símbolos o cualquier subcadena de cada celda en el rango seleccionado, preservando fórmulas, formato y validación de datos para una hoja de cálculo remota.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                                       |
|----------------------|---------|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                 | string  | Ruta                                    | (Obligatorio) Nombre del archivo del libro que se va a recuperar.                                                                                                                 |
| worksheet            | string  | Ruta                                    | Especifica la hoja de cálculo.                                                                                                                                                    |
| range                | string  | Ruta                                    | Especifica el rango de la hoja de cálculo.                                                                                                                                        |
| removeTextMethod     | string  | Consulta                                | Especifica el tipo de método para eliminar texto.                                                                                                                                |
| characterSets        | string  | Consulta                                | Especifica los conjuntos de caracteres.                                                                                                                                          |
| removeCustomValue    | string  | Consulta                                | Especifica el valor personalizado a eliminar.                                                                                                                                    |
| caseSensitive        | boolean | Consulta                                | Afecta al modo `Substring` y a `CustomChars` cuando está habilitado.                                                                                                             |
| folder               | string  | Consulta                                | (Opcional) Ruta de la carpeta donde se almacena el libro. El valor predeterminado es null.                                                                                       |
| storageName          | string  | Consulta                                | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Se utiliza el almacenamiento predeterminado si se omite.                          |
| region               | string  | Consulta                                | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | string  | Consulta                                | Contraseña para abrir el archivo de la hoja de cálculo.                                                                                                                           |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| *Ninguno*            | *Ninguno* | Esta operación no requiere cuerpo de solicitud. |

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Caracteres eliminados correctamente.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**Códigos de estado de respuesta**

| Código | Significado       | Descripción                                                                 |
|--------|-------------------|-----------------------------------------------------------------------------|
| 200    | OK                | Los caracteres se eliminaron correctamente y el libro se actualizó.       |
| 400    | Solicitud incorrecta | Uno o más parámetros faltan o son inválidos.                              |
| 401    | No autorizado     | Falló la autenticación: token JWT ausente o inválido.                      |
| 413    | Payload demasiado grande | El tamaño de la solicitud excede el límite permitido.                   |
| 500    | Error interno del servidor | Se produjo un error inesperado en el lado del servidor.              |

## Cómo usar Eliminar Caracteres en una Hoja de Cálculo Remota con SDK

### Especificación de Eliminar Caracteres en una Hoja de Cálculo Remota

La [Especificación de la API Eliminar Caracteres en una Hoja de Cálculo Remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Usar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "Caracteres eliminados correctamente.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Ejemplo.xlsx",
      "Path": "/documents/Ejemplo.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose Cells Cloud utilizando diversos SDK:
`[TBD]`
---