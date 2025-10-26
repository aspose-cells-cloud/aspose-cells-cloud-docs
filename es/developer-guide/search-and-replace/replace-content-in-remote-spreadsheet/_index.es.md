---
title: Aspose.Cells Cloud Web API - Reemplazar contenido en hoja de cálculo remota
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: Reemplazar el contenido de la hoja de cálculo remota
type: docs
url: /es/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: Reemplace texto de manera eficiente en hojas de cálculo remotas utilizando Excel API
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Reemplazar contenido en Excel, Reemplazo de texto basado en la nube, Modificar texto en una hoja de cálculo remota
---
Reemplace de manera eficiente el texto especificado dentro de un archivo de hoja de cálculo remota.

## **Reemplazar contenido en hoja de cálculo remota API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| nombre| Cadena| Camino| El nombre del archivo del libro de trabajo que se va a modificar.|
| buscarTexto| Cadena| Consulta| El texto a buscar en la hoja de cálculo.|
| reemplazarTexto| Cadena| Consulta| El texto que reemplazará las ocurrencias encontradas.|
| carpeta| Cadena| Consulta| La ruta de la carpeta donde se almacena el libro de trabajo.|
| nombreDeAlmacenamiento| Cadena| Consulta|(Opcional) El nombre del almacenamiento si se usa almacenamiento en la nube personalizado. Si se omite, utilice el almacenamiento predeterminado.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar el contenido Reemplazar en la hoja de cálculo remota API?

Cuando necesite reemplazar contenido en una hoja de cálculo remota, puede usar este API.

## ¿Por qué debería utilizar Reemplazar contenido en la hoja de cálculo remota API?

- Reemplace rápidamente contenido en hojas de cálculo remotas.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar Reemplazar contenido en la hoja de cálculo remota API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente el reemplazo de contenido en las celdas de las hojas de cálculo con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
