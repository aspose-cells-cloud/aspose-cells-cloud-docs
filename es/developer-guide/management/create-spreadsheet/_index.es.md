---
title: Aspose.Cells Cloud Web API - Cree una nueva hoja de cálculo con una plantilla de hoja de cálculo
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: Crear hoja de cálculo
type: docs
url: /es/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: El Excel API permite a los usuarios crear una nueva hoja de cálculo con un nombre específico, compatible con plantillas opcionales para contenido o formato predefinidos, lo que mejora la productividad del usuario.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Coincidir con todas las celdas en blanco en una hoja de cálculo Excel, Creación de hojas de cálculo, Soporte de plantillas, Mejora de la productividad
---
Cree una nueva hoja de cálculo, que puede ser una hoja de cálculo en blanco o una hoja de cálculo utilizable creada según la plantilla especificada.

## **Crear hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|---------- ||----------------------- |----- |
|formato| Cadena| Consulta| Especifica el nombre de la nueva hoja de cálculo. Este nombre se usará para identificarla en el sistema.|
| plantilla| Cadena| Consulta| Opcional. Si se proporciona, la nueva hoja de cálculo se creará según la plantilla especificada. Esto puede ser útil para aplicar diseños y estilos predefinidos.|
| Ruta de salida| Cadena| Consulta| (Opcional) La ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
| nombreAlmacenamientoExterno| Cadena| Consulta| Nombre de almacenamiento del archivo de salida.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

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

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar la hoja de cálculo Crear API?

Cuando necesites crear una hoja de cálculo nueva, puedes utilizar este API.

## ¿Por qué debería utilizar la hoja de cálculo Create API?

- No solo puedes crear una hoja de cálculo en blanco, sino que también puedes crear una hoja de cálculo específica basada en una plantilla.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la hoja de cálculo Create API con SDK

### Crear hoja de cálculo API Especificación

 El[Crear hoja de cálculo API Especificación](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) define una interfaz de programación de acceso público y permite interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite crear la hoja de cálculo con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
