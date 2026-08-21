---
title: "Buscar texto en hojas de cálculo de Excel remotas – API de Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Buscar texto en hojas de cálculo de Excel remotas – Encontrar datos específicos"
linktitle: "Buscar contenido en hoja de cálculo remota"
type: docs
url: /search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, API de búsqueda de Excel, hoja de cálculo en la nube, búsqueda de texto, REST"
description: "Busque texto, números o fórmulas en archivos de Excel almacenados en almacenamiento en la nube utilizando Aspose.Cells Cloud. Admite consultas que no distinguen mayúsculas, selección de carpetas y libros protegidos con contraseña."
weight: 100
---

### **API para buscar contenido en hojas de cálculo remotas**

Busque texto específico dentro de cualquier hoja de cálculo de Excel programáticamente mediante la API de Aspose.Cells Cloud. Encuentre texto, números o fórmulas en archivos almacenados en almacenamiento en la nube. Esta API REST permite flujos de trabajo automatizados de descubrimiento de datos, análisis de contenido y auditoría de hojas de cálculo.

### **API web**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                 |
| :------------------- | :----- | :-------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String | Ruta                                    | **Obligatorio**. El nombre del archivo del libro de Excel (incluida la extensión) en el que se realizará la búsqueda de texto, por ejemplo, `ventas.xlsx`. |
| searchText           | String | Consulta                                | **Obligatorio**. La cadena exacta, número o contenido parcial que se desea localizar en todo el libro o en las hojas de cálculo.                           |
| ignoringCase         | Boolean| Consulta                                | **Opcional**. Determina si se distingue entre mayúsculas y minúsculas. Establézcalo en `true` para una búsqueda que no distinga mayúsculas (por ejemplo, “Informe” coincide con “INFORME”); el valor predeterminado es `false`. |
| folder               | String | Consulta                                | **Opcional**. La ruta del directorio dentro de su almacenamiento en la nube que contiene el libro objetivo. Si se omite, se asume la carpeta raíz.        |
| storageName          | String | Consulta                                | **Opcional**. El identificador de nombre para un servicio de almacenamiento en la nube configurado personalmente. Si no se especifica, la API usa el almacenamiento predeterminado asociado con la cuenta. |
| region               | String | Consulta                                | **Opcional**. La configuración regional (por ejemplo, `es-ES`) aplicada durante la búsqueda, lo que puede afectar las reglas de normalización o clasificación del texto. |
| password             | String | Consulta                                | **Opcional**. La contraseña de descifrado necesaria para acceder a un archivo de Excel protegido con contraseña. Omita este parámetro si el archivo no está cifrado. |

**Glosario**

- **searchText** – La cadena exacta que se desea localizar; puede ser una coincidencia parcial.
- **ignoringCase** – `true` hace que la búsqueda no distinga mayúsculas; `false` fuerza la distinción entre mayúsculas y minúsculas.
- **folder** – Ruta al directorio que contiene el libro.
- **storageName** – Identificador de una configuración de almacenamiento personalizada.
- **region** – Código regional que influye en las reglas de comparación de texto.
- **password** – Contraseña de descifrado para libros protegidos.

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

La respuesta contiene una lista de celdas (`CellName`) donde se encontró el texto buscado, junto con el nombre de la hoja de cálculo y el texto coincidente. Si no se encuentran coincidencias, la matriz `Cells` está vacía y la solicitud aún devuelve HTTP 200 OK.

### Códigos de error

- **400 Bad Request** – URI inválido para la API de Aspose.Cells Cloud.  
  ```json
  {"code":400,"message":"URI de solicitud no válida"}
  ```
- **401 Unauthorized** – Token de acceso, ID de cliente o secreto de cliente no válidos.  
  ```json
  {"code":401,"message":"Token de acceso no válido"}
  ```
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.  
  ```json
  {"code":404,"message":"Archivo no encontrado"}
  ```
- **500 Server Error** – Una condición inesperada impidió que la API completara la solicitud.  
  ```json
  {"code":500,"message":"Error interno del servidor"}
  ```

## ¿Dónde debemos usar la API para buscar contenido en una hoja de cálculo?

- **Auditoría integral de cumplimiento del libro** – Escanee rápidamente todo el archivo de Excel para identificar todos los términos confidenciales (por ejemplo, “Cláusula Confidencial”, “Datos Internos”) en verificaciones de seguridad y cumplimiento de datos empresariales.
- **Consulta de asociación de datos entre hojas** – Cuando la información del proyecto está dispersa en varias hojas de cálculo, busque un número de proyecto o nombre de cliente específico y localice instantáneamente todos los datos relacionados.
- **Verificación por lotes de contenido de plantillas** – Tras la generación automatizada de informes, escanee varios archivos de Excel en lotes para confirmar que todos los marcadores de posición predefinidos (como `{{Date}}`) se han reemplazado correctamente, garantizando la integridad y precisión del informe.
- **Archivado y extracción de datos históricos** – Analice archivos antiguos, busque códigos de eventos específicos o términos comerciales, y comprenda rápidamente la lógica empresarial histórica para la arqueología de datos.

## ¿Por qué debería usar la API para buscar contenido en una hoja de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación completa. En comparación con la construcción de soluciones personalizadas, esto reduce significativamente el esfuerzo de desarrollo.
- **Reducción de costos laborales** – Automatiza tareas repetitivas de búsqueda, liberando a los desarrolladores del trabajo manual de extracción de datos.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Sin mantenimiento necesario** – Aspose gestiona servidores, actualizaciones y compatibilidad, por lo que puede centrarse en la lógica de su aplicación.
- **Preserva el formato complejo de Excel** – Los resultados se pueden exportar al formato PDF universalmente accesible manteniendo el estilo original.

## Cómo usar la API para buscar enlaces rotos dentro del rango de la hoja de cálculo mediante SDK

### Especificación OpenAPI

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de SDK de Aspose.Cells Cloud

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK maneja los detalles subyacentes, lo que le permite simplemente implementar la búsqueda de contenido en hojas de cálculo con código mínimo. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo invocar los servicios web de Aspose.Cells utilizando varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---