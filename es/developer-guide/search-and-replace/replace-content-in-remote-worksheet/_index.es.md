---
title: "Aspose.Cells Cloud Replace Web API – Actualizar texto en hoja de cálculo remota"
second_title: "Documentación"
ArticleTitle: "Buscar y reemplazar texto en hoja de cálculo remota con Aspose.Cells Cloud API"
linktitle: "Reemplazar contenido en hoja de cálculo remota"
type: docs
url: /es/replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, reemplazar texto, hoja de cálculo remota, API de Excel, hoja de cálculo en la nube, buscar y reemplazar, API REST"
description: "Reemplazar texto en una hoja de cálculo específica de un archivo de Excel almacenado en Aspose Cloud. Admite libros protegidos con contraseña, búsqueda sensible a la región y actualizaciones masivas."
weight: 100
---

Reemplace texto específico dentro de una hoja de cálculo determinada de archivos de Excel remotos. Actualice el contenido en hojas de cálculo específicas de forma eficiente utilizando la API de búsqueda y reemplazo de Aspose.Cells Cloud para una edición precisa de hojas de cálculo.

## **Reemplazar contenido en la API de hoja de cálculo remota**

### **API web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                                  |
| :------------------- | :----- | :-------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String | Ruta                                    | Nombre del archivo de libro almacenado en el almacenamiento en la nube que se va a modificar (por ejemplo, `"sales_report.xlsx"`, `"budget_2024.xls"`).                     |
| worksheet            | String | Ruta                                    | Nombre de la hoja de cálculo específica en la que se realizará la operación de buscar y reemplazar (por ejemplo, `"Q1_Sales"`, `"Sheet1"`).                                  |
| searchText           | String | Consulta                                | Cadena de texto que se buscará dentro de la hoja de cálculo especificada. La búsqueda se aplica a todas las celdas de la hoja, salvo que se restrinja adicionalmente.         |
| replaceText          | String | Consulta                                | Cadena de texto que reemplazará todas las ocurrencias de `searchText` encontradas dentro de la hoja de cálculo especificada.                                                 |
| folder               | String | Consulta                                | Ruta de la carpeta en el almacenamiento en la nube donde se encuentra el libro de origen (por ejemplo, `"/reports/monthly/"`, `"/finance/"`).                               |
| storageName          | String | Consulta                                | _(Opcional)_ Nombre del almacenamiento en la nube personalizado (por ejemplo, `"CorporateS3"`, `"AzureArchive"`). Si se omite, se utiliza el almacenamiento en la nube predeterminado de su cuenta. |
| region               | String | Consulta                                | _(Opcional)_ Establece la configuración regional para el manejo de texto, lo que puede afectar la codificación de caracteres y el comportamiento de la búsqueda específica del idioma dentro de la hoja de cálculo (por ejemplo, `"en-GB"`, `"es-ES"`). |
| password             | String | Consulta                                | _(Opcional)_ Si el libro está protegido con contraseña, proporcione la contraseña para abrir y modificar el archivo.                                                        |

**Ejemplo de solicitud (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **Códigos de error**

| Código | Descripción                              | Cuándo ocurre                                                    |
|--------|------------------------------------------|------------------------------------------------------------------|
| 400    | Solicitud incorrecta                     | La URI de la solicitud está mal formada o faltan parámetros obligatorios. |
| 401    | No autorizado                            | Falta el token de acceso, es inválido o las credenciales del cliente son incorrectas. |
| 404    | No encontrado                            | No se puede encontrar el libro ni la hoja de cálculo especificados. |
| 500    | Error interno del servidor               | Se produjo un error inesperado al procesar la solicitud.        |

## ¿Dónde debemos utilizar la API de reemplazo de contenido de hoja de cálculo en hojas de cálculo remotas?

- **Actualización por lotes de archivos en la nube**: Modificar el contenido de múltiples archivos de Excel almacenados en almacenamientos en la nube como AWS S3 y Azure Blob.
- **Población dinámica de plantillas en la nube**: Rellenar por lotes datos dinámicos en plantillas de informes almacenadas en la nube.
- **Sincronización de archivos entre regiones**: Sincronizar la consistencia del contenido de archivos de Excel en el almacenamiento en la nube entre distintas regiones geográficas.

## ¿Por qué debería utilizar la API de reemplazo de contenido de hoja de cálculo en hojas de cálculo remotas?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de una documentación completa. En comparación con la creación de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de trabajo de desarrollo.
- **Reducción de costos laborales**: Disminuye la necesidad de personal dedicado a la consolidación de documentos.
- **Pago por uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Costos de mantenimiento cero**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.

## Cómo utilizar la API de reemplazo de contenido de hoja de cálculo en hojas de cálculo remotas mediante SDK

### **Especificación OpenAPI**

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### **Utilizar los SDK de Aspose.Cells Cloud**

Utilizar los SDK es la mejor manera de acelerar el desarrollo. Los SDK gestionan los detalles subyacentes, lo que le permite simplemente implementar el reemplazo de contenido de hoja de cálculo en hojas de cálculo con un código mínimo.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK: