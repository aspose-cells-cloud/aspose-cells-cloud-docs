---
title: "Aspose.Cells Cloud Replace Web API – Actualizar texto en un rango remoto de hoja de cálculo"
second_title: "Documento"
ArticleTitle: "Sustitución masiva de texto en rangos en archivos de Excel en la nube – API de buscar y reemplazar"
linktitle: "Sustituir contenido en rango remoto"
type: docs
url: /es/replace-content-in-remote-range/
keywords: "sustituir texto en rango remoto de Excel, API de Aspose.Cells Cloud, buscar y reemplazar Excel, editar hoja de cálculo en la nube, actualizar archivo de Excel remoto"
description: "Utilice Aspose.Cells Cloud para buscar y sustituir texto en un rango específico de un archivo de Excel remoto. Admite autenticación, manejo de errores y SDK en múltiples lenguajes."
weight: 100
---

Realice sustituciones masivas de texto en archivos de Excel almacenados en la nube. Busque y actualice cadenas de texto específicas dentro de rangos seleccionados de forma eficiente mediante la API de búsqueda y reemplazo de Aspose.Cells Cloud.

## **Sustituir contenido en rango remoto mediante API**

### API web

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                 |
| :------------------- | :----- | :-------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String | Ruta                                    | Nombre del archivo de libro almacenado en el almacenamiento en la nube que se va a modificar (por ejemplo, `"reporte.xlsx"`).                              |
| searchText           | String | Consulta                                | Cadena de texto que se buscará dentro de la hoja de cálculo y el área de celdas especificadas. Admite coincidencia exacta de texto.                       |
| replaceText          | String | Consulta                                | Cadena de texto que reemplazará todas las ocurrencias del `searchText` dentro del rango especificado.                                                      |
| worksheet            | String | Ruta                                    | Nombre de la hoja de cálculo en la que se realizará la operación de buscar y reemplazar.                                                                  |
| cellArea             | String | Ruta                                    | Rango específico de celdas (por ejemplo, `"A1:D20"`) donde se realizará la búsqueda y sustitución del texto.                                              |
| folder               | String | Consulta                                | Ruta de la carpeta en el almacenamiento en la nube donde se encuentra el libro de origen.                                                                 |
| storageName          | String | Consulta                                | _(Opcional)_ Nombre del almacenamiento en la nube donde reside el libro. Si se omite, se utiliza el almacenamiento en la nube predeterminado.             |
| region               | String | Consulta                                | _(Opcional)_ Establece la configuración regional para el procesamiento de texto, lo que puede afectar la distinción entre mayúsculas y minúsculas y la codificación de caracteres en las operaciones de búsqueda (por ejemplo, `"es-ES"`, `"en-US"`). |
| password             | String | Consulta                                | _(Opcional)_ Si el libro está protegido con contraseña, proporcione la contraseña para abrirlo y modificarlo.                                             |

### **Respuesta**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

Una llamada correcta devuelve la siguiente carga JSON concreta:

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### Códigos de error

| Código | Mensaje         | Cuándo ocurre                                           |
| ------ | --------------- | ------------------------------------------------------- |
| 400    | Bad Request     | La URI de la solicitud o sus parámetros están mal formados. |
| 401    | Unauthorized    | Token de autenticación ausente o no válido.             |
| 404    | Not Found       | No se puede encontrar ni acceder al libro especificado. |
| 500    | Server Error    | Error interno del servidor durante el procesamiento del libro. |

## ¿Dónde debemos utilizar la API de sustitución de contenido de rango en hojas de cálculo remotas?

- **Actualización por lotes de archivos en la nube**: Modificar el contenido de múltiples archivos de Excel almacenados en almacenamientos en la nube como AWS S3 y Azure Blob.
- **Población dinámica de plantillas en la nube**: Poblar por lotes datos dinámicos en plantillas de informes almacenadas en la nube.
- **Sincronización de archivos entre regiones**: Sincronizar la coherencia del contenido de archivos de Excel en almacenamiento en la nube entre diferentes regiones geográficas.

## ¿Por qué debería utilizar la API de sustitución de contenido de rango en hojas de cálculo remotas?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con documentación completa. Comparado con la creación de soluciones personalizadas, esto reduce significativamente la carga de desarrollo.
- **Reducción de costos laborales**: Disminuye la necesidad de cargos dedicados para la consolidación de documentos.
- **Pago por uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Costos de mantenimiento cero**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.
- **Preserva el formato complejo de Excel** en un formato PDF de acceso universal.

## Cómo utilizar la API de sustitución de contenido de rango en hojas de cálculo remotas con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor forma de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que le permite implementar simplemente la sustitución de contenido en hojas de cálculo con un mínimo de código. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}