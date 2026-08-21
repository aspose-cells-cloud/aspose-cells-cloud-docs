---
title: "BuscarEnlacesRotosEnHojasDeCálculoRemotas"
ArticleTitle: "Buscar enlaces rotos en hojas de cálculo remotas – API de Aspose.Cells Cloud"
second_title: "Documentos"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, buscar enlaces rotos, hoja de cálculo remota"
description: "Busca enlaces rotos en la hoja de cálculo de una hoja de cálculo almacenada en la nube remota."
weight: 100
---

## Búsqueda de enlaces rotos en hojas de cálculo remotas mediante los servicios web de Aspose.Cells Cloud

Este método busca enlaces rotos dentro de una hoja de cálculo de un archivo de hoja de cálculo almacenado en un almacenamiento en la nube remota. Escanea todas las hojas y celdas para identificar hipervínculos que ya no apuntan a destinos válidos, como URL no válidas o referencias externas faltantes. La operación se realiza de forma remota en el entorno en la nube, sin necesidad de descargar el archivo en la máquina local.

### Punto final de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción |
|----------------------|------|-----------------------------------------|-------------|
| name | string | Ruta | El nombre del archivo del libro que se va a buscar. |
| worksheet | string | Ruta | Especifica la hoja de cálculo en la que realizar la búsqueda. |
| folder | string | Consulta | Ruta de la carpeta donde se almacena el libro. (opcional) |
| storageName | string | Consulta | (Opcional) Nombre del almacenamiento si se utiliza un almacenamiento en la nube personalizado. Se utilizará el almacenamiento predeterminado si se omite. |
| region | string | Consulta | Configuración regional/lingüística de la hoja de cálculo (p. ej., `es-ES`, `fr-FR`). Influye en el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password | string | Consulta | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| — | — | No se requiere cuerpo de solicitud para esta operación. |

### **Respuesta**

```json
{
  "Links": [
    {
      "SheetName": "Hoja1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Lista de enlaces rotos recuperada correctamente. |
| 400 | Solicitud incorrecta | Parámetros de solicitud inválidos o URL con formato incorrecto. |
| 401 | No autorizado | La autenticación ha fallado o no se han proporcionado credenciales. |
| 404 | No encontrado | El archivo de origen no es accesible. |
| 413 | Entidad demasiado grande | La entidad de la solicitud es demasiado grande. |
| 500 | Error interno del servidor | Se ha producido una anomalia en la hoja de cálculo al obtener los datos. |

## Cómo utilizar la función de búsqueda de enlaces rotos en hojas de cálculo remotas con SDK

### Especificación de la búsqueda de enlaces rotos en hojas de cálculo remotas

La [especificación de la API de Búsqueda de enlaces rotos en hojas de cálculo remotas](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}

{< tab tabNum="1" >}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Hoja1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando distintos SDK:
`[TBD]`
---