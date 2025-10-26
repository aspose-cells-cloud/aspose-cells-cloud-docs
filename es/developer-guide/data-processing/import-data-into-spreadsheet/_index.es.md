---
title: Aspose.Cells Cloud Web API - Importar datos CSV, JSON o XML a un archivo de hoja de cálculo
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Importar datos a una hoja de cálculo
type: docs
url: /es/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Importe datos de manera eficiente a una hoja de cálculo desde formatos compatibles como CSV, JSON y XML utilizando Aspose.Cells Cloud Web API
weight: 100
kwords: Aspose.Cells Cloud Web API, Importar datos, Office Cloud, REST, Hoja de cálculo, CSV, JSON, XM
---
 Importar datos a una hoja de cálculo. El formato admitido del archivo de datos importado es[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) o[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **Importar datos a una hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| archivo de datos| Archivo| Datos del formulario| Sube el archivo de datos que deseas importar.|
| Hoja de cálculo| Archivo| Datos del formulario| Sube el archivo de hoja de cálculo de destino.|
| hoja de trabajo| Cadena| Consulta| Especifique la hoja de trabajo para importar datos.|
| celda de inicio| Cadena| Consulta|Especifique la posición inicial para importar datos.|
| insertar| Booleano| Consulta| Indica si se deben insertar o sobrescribir los datos de importación especificados.|
| convertirDatosNumericos| Booleano| Consulta| Especifique si desea convertir datos numéricos durante la importación.|
| disidente| Cadena| Consulta| Especifique el delimitador para el formato CSV.|
| Ruta de salida| Cadena| Consulta| (Opcional) La ruta de la carpeta donde se almacena el libro. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno| Cadena| Consulta| Especifique el nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Define fuentes personalizadas que se utilizarán.|
| regresar| Cadena| Consulta| Establecer la configuración de la región de la hoja de cálculo.|
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

## ¿Dónde debemos utilizar la importación de datos en la hoja de cálculo API?

- Importar grandes cantidades de datos a una hoja de cálculo.
-  El formato del archivo de datos importados es[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) y[CSV](https://docs.fileformat.com/spreadsheet/csv/).

## ¿Por qué debería utilizar la función Importar datos en la hoja de cálculo API?

- Importar grandes cantidades de datos a hojas de cálculo.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo utilizar la función Importar datos en una hoja de cálculo API con SDK

### Importar datos a una hoja de cálculo API Especificación

 El[Importar datos a una hoja de cálculo API Especificación](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) Proporciona una interfaz de programación de acceso público, que permite interacciones REST directamente desde su navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite importar datos a una hoja de cálculo con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo invocar los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
