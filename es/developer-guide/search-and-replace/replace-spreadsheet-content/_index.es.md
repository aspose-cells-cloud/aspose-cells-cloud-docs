---
title: "Aspose.Cells Cloud: Reemplazar texto en archivos locales de Excel (API de buscar y reemplazar)"
second title: "Documento"
ArticleTitle: "Reemplazo masivo de texto en archivos locales de Excel – API de buscar y reemplazar"
linktitle: "Reemplazar contenido de hoja de cálculo"
type: docs
url: /replace-spreadsheet-content/
keywords: "reemplazar texto en Excel, Aspose.Cells buscar y reemplazar, API de hoja de cálculo local, reemplazar archivo Excel, API reemplazar contenido"
description: "Reemplace texto en libros locales de Excel sin cargarlos en la nube. Utilice la API de buscar y reemplazar de Aspose.Cells Cloud para actualizar rangos, hojas de cálculo específicas o archivos completos en una única llamada."
weight: 100
---

Reemplace texto específico en archivos locales de hojas de cálculo de Excel sin necesidad de cargarlos en la nube. Actualice el contenido de los libros de forma eficiente mediante la API de buscar y reemplazar de Aspose.Cells Cloud para edición fuera de línea.

## **API para reemplazar contenido de hoja de cálculo**

### **API web**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                                      |
| :------------------- | :----- | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData                                | El archivo local de hoja de cálculo que se procesará. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc.                                                                  |
| searchText           | String | Query                                   | La cadena de texto que se buscará dentro de la hoja de cálculo y el rango de celdas especificados.                                                                             |
| replaceText          | String | Query                                   | La cadena de texto que reemplazará todas las ocurrencias de `searchText` dentro del rango especificado.                                                                         |
| worksheet            | String | Query                                   | _(Opcional)_ El nombre de la hoja de cálculo en la que se realizará la operación de buscar y reemplazar. Si se omite, la operación se aplicará a la primera hoja.              |
| cellArea             | String | Query                                   | _(Opcional)_ El rango específico de celdas (por ejemplo, `"A1:D20"`, `"B5:F15"`) en el que se llevará a cabo la búsqueda y el reemplazo de texto. Si se omite, la operación se aplica a todas las celdas utilizadas de la hoja especificada. |
| region               | String | Query                                   | _(Opcional)_ Establece la configuración regional para el manejo de texto, lo que puede afectar la distinción entre mayúsculas y minúsculas y la codificación de caracteres en las operaciones de búsqueda (por ejemplo, `"en-US"`, `"fr-FR"`). |
| password             | String | Query                                   | _(Opcional)_ Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                                             |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

La respuesta es un flujo binario que contiene el libro actualizado. Guárdelo con la extensión de archivo correspondiente (por ejemplo, `.xlsx`).

### **Códigos de error**

- **400 Bad Request (Solicitud incorrecta)** – URI de la API de Aspose.Cells Cloud inválido o parámetros mal formados.
- **401 Unauthorized (No autorizado)** – Token de acceso inválido o ausente; obtenga un nuevo token.
- **404 Not Found (No encontrado)** – El archivo de hoja de cálculo no es accesible o la hoja especificada no existe.
- **500 Server Error (Error del servidor)** – El archivo de hoja de cálculo ha generado un error interno durante el procesamiento; póngase en contacto con soporte técnico si el problema persiste.

## ¿Dónde debemos utilizar la API de reemplazo de contenido en hojas de cálculo?

- **Procesamiento por lotes de archivos locales de Excel** – Automatice la operación de buscar y reemplazar en múltiples libros almacenados localmente.
- **Bucles de datos en infraestructura local** – Integre la API en trabajos programados que modifiquen informes antes de archivarlos o distribuirlos.
- **Generación local de informes** – Inserte dinámicamente valores en plantillas de libros sin necesidad de subirlos a la nube.

## ¿Por qué debería utilizar la API de reemplazo de contenido en hojas de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con documentación exhaustiva. En comparación con la creación de soluciones personalizadas, esto reduce considerablemente el esfuerzo de desarrollo.
- **Reducción de costos laborales** – Disminuye la necesidad de personal dedicado para realizar tareas manuales de consolidación de documentos.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utilice.
- **Cero costos de mantenimiento** – No hay servidores que mantener, ni actualizaciones de software ni preocupaciones por compatibilidad.
- **Preserva el formato complejo de Excel** – El formato original, fórmulas y gráficos del libro se mantienen intactos tras el reemplazo.

## Cómo utilizar la API de reemplazo de contenido en hojas de cálculo con SDK

### **Especificación OpenAPI**

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) define una interfaz de programación accesible públicamente, lo que permite realizar interacciones REST directamente desde un navegador web.

### **Utilizar los SDK de Aspose.Cells Cloud**

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar operaciones de reemplazo de contenido con un código mínimo. Consulte el repositorio oficial de **Aspose.Cells Cloud SDK en GitHub** para obtener una lista completa de los lenguajes admitidos.

Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}

---