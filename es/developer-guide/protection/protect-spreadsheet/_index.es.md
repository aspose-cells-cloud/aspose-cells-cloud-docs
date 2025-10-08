---
title: Aspose.Cells Cloud Web API - Proteger hoja de cálculo
second_title: Developer Guide for Excel Protectio
ArticleTitle: Protect the Spreadsheet with passwor
linktitle: Proteger la hoja de cálculo
type: docs
url: /es/protect-spreadsheet/
keywords: Aspose.Cells Cloud Web API, password protection, encrypt spreadsheet, modify passwor
description: Este API aplica protección de contraseña de doble capa a las hojas de cálculo Excel, lo que garantiza un acceso y modificación seguros mediante cifrado.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, protección de contraseña de doble capa, cifrar hoja de cálculo, Excel seguro
---
Aplica protección con contraseña a Excel hojas de cálculo, admitiendo tanto contraseñas de apertura como de modificación.

## **Proteger la hoja de cálculo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
|Hoja de cálculo|Archivo|Datos del formulario|Sube el archivo de hoja de cálculo que desea proteger.|
|contraseña|Cadena|Consulta|Contraseña de cifrado para el archivo de hoja de cálculo.|
|modificarContraseña|Cadena|Consulta|Se requiere contraseña para modificar la hoja de cálculo.|
|Ruta de salida|Cadena|Consulta|(Opcional) La ruta de la carpeta donde se almacenará el libro protegido. El valor predeterminado es nulo.|
|nombreAlmacenamientoExterno|Cadena|Consulta|Nombre del almacenamiento para los archivos de salida.|
|región|Cadena|Consulta|Define la configuración regional para la hoja de cálculo.|

## **Respuesta**

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

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar la hoja de cálculo Protect API?

Cuando necesite bloquear una hoja de cálculo con contraseña, puede utilizar esta API.

## ¿Por qué debería utilizar la hoja de cálculo Protect API?

- Bloquee rápidamente hojas de cálculo con contraseña.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## Cómo usar la hoja de cálculo Protect API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet)Proporciona una interfaz de programación detallada para ejecutar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar hojas de cálculo protegidas para celdas con un código mínimo.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
