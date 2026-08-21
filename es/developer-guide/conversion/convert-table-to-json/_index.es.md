---
title: "Aspose.Cells Cloud Web API: Convertir datos locales de tabla de Excel a un archivo JSON"
second_title: "Documento"
ArticleTitle: "Cómo convertir datos locales de tabla de hoja de cálculo a un archivo JSON: Guía paso a paso"
linktitle: "Convertir tabla a JSON"
type: docs
url: /es/convert-table-to-json/
keywords: "Excel, API, JSON, conversión, nube, archivo, hoja de cálculo"
description: "Use la API web Aspose.Cells Cloud para transformar una tabla local de Excel en un archivo JSON mediante una única solicitud PUT. Incluye ejemplo de cURL, parámetros y fragmentos de SDK para C#, Java, Python y más."
weight: 100
---

Convierta una tabla local de hoja de cálculo/Excel a un archivo **JSON** mediante la API web Aspose.Cells Cloud.

## **API para convertir tabla a JSON**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                         |
|----------------------|--------|-----------|-----------------------------------------------------------------------------------------------------|
| **Spreadsheet**      | Archivo | FormData  | El archivo de Excel que se va a cargar.                                                            |
| **worksheet**        | Cadena  | Query     | Nombre de la hoja de cálculo que contiene la tabla.                                                |
| **tableName**        | Cadena  | Query     | Nombre de la tabla que se va a convertir.                                                          |
| **outPath**          | Cadena  | Query     | (Opcional) Ruta de la carpeta donde se guardará el archivo JSON resultante; por defecto es **null**. |
| **outStorageName**   | Cadena  | Query     | (Opcional) Nombre del almacenamiento donde se colocará el archivo de salida.                       |
| **fontsLocation**    | Cadena  | Query     | (Opcional) Ruta a las fuentes personalizadas utilizadas durante la conversión.                     |
| **region**           | Cadena  | Query     | (Opcional) Configuración regional para el libro de trabajo.                                        |
| **password**         | Cadena  | Query     | (Opcional) Contraseña para abrir un libro de trabajo protegido.                                    |

### Respuesta

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                          |
|--------|-------------------------|----------------------------------------------------------------------|
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o ausente.                                       |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                      |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                    |

## **¿Dónde debería utilizar la API para convertir tabla a JSON?**

- **Paneles en tiempo real** – Convierta datos de Excel en vivo a JSON para bibliotecas de gráficos como Chart.js o D3.js.
- **Hoja de cálculo como servicio** – Exponga tablas de Excel como puntos finales JSON para otros microservicios.
- **Cargas útiles de webhook** – Transforme datos de hojas de cálculo en JSON para notificaciones webhook.
- **Prototipado rápido de datos** – Convierta rápidamente datos de Excel limpiados a JSON para análisis con Python o R.
- **Tuberías de aprendizaje automático** – Preprocese datos de entrenamiento almacenados en hojas de cálculo empresariales.
- **Operaciones de comercio electrónico** – Sincronice catálogos de productos o hojas de precios con sitios web mediante JSON.
- **Automatización de informes** – Genere feeds JSON a partir de modelos financieros para informes automáticos.
- **Configuración de aplicaciones** – Gestione banderas de características, configuraciones o parámetros de pruebas A/B en Excel → JSON.
- **Soporte multilenguaje** – Convierta hojas de cálculo de localización a JSON para bibliotecas i18n.
- **Menús/navegación dinámica** – Almacene estructuras de navegación de sitios web en Excel y despliéguelas como JSON.

## ¿Por qué debería utilizar la API para convertir tabla a JSON?

- **Amigable para desarrolladores** – Aspose.Cells Cloud proporciona SDK para muchos lenguajes, reduciendo el esfuerzo de desarrollo y ofreciendo documentación exhaustiva.
- **Rentable** – Convierta datos de tabla sin cargar primero el libro de trabajo, ahorrando espacio de almacenamiento y reduciendo costos.
- **Compatibilidad moderna con web y dispositivos móviles** – JSON es el lenguaje nativo de datos de la web; la API le permite alimentar datos de hoja de cálculo en vivo directamente en React, Vue, Angular, aplicaciones móviles o aplicaciones de una sola página sin análisis complejos.
- **Amplia compatibilidad con lenguajes** – JSON funciona con prácticamente todos los lenguajes de programación, bases de datos y servicios web.
- **Preservación de datos estructurados**
  - **Detección inteligente de estructura** – Convierte automáticamente datos tabulares en matrices u objetos JSON adecuados.
  - **Asignación de encabezados** – Utiliza la primera fila como claves JSON para estructuras de objetos limpias.
  - **Conservación de tipos de datos** – Mantiene números, fechas y valores booleanos (no solo texto).

_Historial de versiones:_ El punto final Convert Table to JSON se introdujo con la versión de API **v4.0** (2024) y sigue siendo la versión estable actual. Los puntos finales anteriores de la v3.x están obsoletos.

## ¿Cómo utilizar la API para convertir tabla a JSON con SDK?

### Especificación de la API para convertir tabla a JSON

La [Especificación de la API para convertir tabla a JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} proporciona una interfaz de programación accesible públicamente, lo que permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificado en Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nombre de archivo opcional"
}
```

```
{
 "Code": 200,
 "Status": "Correcto"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar SDK de Aspose.Cells Cloud

El uso de un SDK abstracte los detalles de bajo nivel, lo que le permite convertir una tabla de hoja de cálculo en un archivo JSON con un código mínimo. Consulte el repositorio oficial de GitHub para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}