---
title: "API de búsqueda de texto de Aspose.Cells Cloud para Excel: buscar texto en rangos de hojas de cálculo remotas"
second_title: "Document"
ArticleTitle: "Buscar texto en hojas de cálculo de Excel remotas: encontrar datos en rangos específicos"
linktitle: "Buscar contenido en rango remoto"
type: docs
url: /search-content-in-remote-range/
keywords: "Aspose.Cells, API de Excel, buscar texto, rango remoto, hoja de cálculo en la nube, API REST, descubrimiento de datos"
description: "Busque texto, números o fórmulas en un rango específico de un libro de Excel almacenado en Aspose Cloud."
weight: 100
---

## **Buscar contenido en un rango remoto**

Busque mediante programación texto específico dentro de cualquier rango de hojas de cálculo de Excel utilizando la API de Aspose.Cells Cloud. Encuentre texto, números o fórmulas en archivos remotos almacenados en el almacenamiento en la nube. API REST para flujos de trabajo automatizados de descubrimiento de datos, análisis de contenido y auditoría de hojas de cálculo.


### **API web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


**Ejemplo con cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer SU_TOKEN_DE_ACCESO" \
     -H "Content-Type: application/json"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta/Consulta/Cadena/Cuerpo HTTP | Descripción                                                                                                                                         |
| :------------------- | :------ | :------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String  | Ruta                             | **Obligatorio**. Nombre del archivo (incluida la extensión) del libro de Excel que se va a buscar, por ejemplo, `customer_data.xlsx`.             |
| worksheet            | String  | Ruta                             | **Obligatorio**. Nombre exacto de la hoja de cálculo dentro del libro donde buscar, por ejemplo, `Orders_2024`.                                    |
| cellArea             | String  | Ruta                             | **Obligatorio**. Rango de celdas objetivo para la búsqueda, especificado en notación A1 (por ejemplo, `B2:H100`). La búsqueda se limita a esta zona. |
| searchText           | String  | Consulta                         | **Obligatorio**. Cadena de texto, número o contenido parcial específico que buscar dentro del área de celdas definida.                             |
| ignoreCase           | Boolean | Consulta                         | **Opcional**. Si se establece en `true`, la búsqueda ignora las diferencias de mayúsculas y minúsculas (por ejemplo, «Report» coincide con «report»). El valor predeterminado es `false` (distingue mayúsculas y minúsculas). |
| folder               | String  | Consulta                         | **Opcional**. Ruta del directorio en su almacenamiento en la nube donde se encuentra el libro. Si se omite, se utiliza el directorio raíz.         |
| storageName          | String  | Consulta                         | **Opcional**. Identificador de una configuración personalizada de almacenamiento en la nube. Si no se especifica, se utiliza el almacenamiento predeterminado de la cuenta. |
| region               | String  | Consulta                         | **Opcional**. Configuración de cultura/región (por ejemplo, `es-ES`) que podría afectar la interpretación de caracteres o formatos específicos de región durante la búsqueda. |
| password             | String  | Consulta                         | **Opcional**. Contraseña para descifrar y acceder a un archivo de hoja de cálculo protegido por contraseña. Omita si el archivo no está cifrado.    |

### Respuesta

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

### Códigos de error

- **400 Bad Request** – URI inválido de la API de Aspose.Cells Cloud.  
- **401 Unauthorized** – Token de acceso, ID de cliente o secreto de cliente inválido.  
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.  
- **500 Server Error** – Una condición inesperada impidió que el servidor cumpliera la solicitud.

## ¿Dónde debemos utilizar la API de búsqueda de contenido en un rango de hoja de cálculo?

- **Verificación de calidad de datos a gran escala** – Durante la etapa de aceptación del proceso ETL del almacén de datos, busque descripciones de campos faltantes, abreviaturas no definidas o texto de marcador de posición (por ejemplo, `"TBD"` o `"NULL"`) en la tabla de asignación de datos (`DataDictionary!B2:F1000`) para identificar definiciones de datos incompletas.  
- **Generación dinámica de informes y extracción de contenido** – En sistemas de generación automática de informes, busque e extraiga inteligentemente bloques de datos del período actual marcados con identificadores específicos (por ejemplo, `"[KPI]"`) desde hojas de plantilla con datos mixtos (`Monthly_Metrics!C10:G50`) para ensamblar el informe final.  
- **Análisis de contratos y documentos legales** – Al revisar apéndices en hojas de cálculo que contienen muchas cláusulas, localice eficientemente términos legales específicos (por ejemplo, `"liability limit"`), nombres de partes o fechas dentro de un rango definido (`Contract_Terms!A:A`) para acelerar el proceso de revisión.

## ¿Por qué debería utilizar la API de búsqueda de contenido en un rango de hoja de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con documentación exhaustiva, reduciendo significativamente la carga de trabajo de desarrollo en comparación con construir soluciones personalizadas.  
- **Reducción de costos laborales** – Elimina la necesidad de cargos dedicados para la consolidación de documentos.  
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.  
- **Costos de mantenimiento cero** – Sin servidores que mantener, sin actualizaciones de software y sin preocupaciones por compatibilidad.

## Cómo utilizar la API de búsqueda de contenido en un rango de hoja de cálculo con SDK

### Especificación OpenAPI

La [especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Usar el SDK es la mejor forma de acelerar el desarrollo. El SDK maneja los detalles subyacentes, lo que le permite implementar simplemente la búsqueda de contenido en un rango de hojas de cálculo con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---