---
title: "Aspose.Cells Cloud – API de detección de enlaces rotos en Excel – Escaneo y validación de enlaces en hojas de cálculo remotas"
second_title: "Documento"
ArticleTitle: "Buscar y corregir enlaces rotos en Excel remoto: verificador de enlaces en hojas de cálculo en la nube"
linktype: "Buscar enlaces rotos en hojas de cálculo remotas"
type: docs
url: /es/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, enlaces rotos, API, nube, hoja de cálculo, validación, Aspose.Cells"
description: "Utilice la API de Aspose.Cells Cloud para escanear libros de Excel remotos en busca de enlaces externos rotos, fórmulas inválidas y fuentes de datos ausentes."
weight: 100
---

## **Búsqueda de enlaces rotos en hojas de cálculo remotas mediante API**

Detecte automáticamente enlaces rotos en archivos de Excel almacenados en almacenamiento en la nube. Nuestra API escanea rangos especificados en busca de referencias externas rotas, fórmulas inválidas y fuentes de datos ausentes. Soporta auditoría de hojas de cálculo remotas, comprobaciones automáticas de calidad e integración con proveedores de almacenamiento en la nube. Utilice la API RESTful para automatizar flujos de trabajo empresariales.

### **API web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                               |
| :------------------- | :----- | :-------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String | Ruta                                    | **Obligatorio.** El nombre del archivo del libro de Excel que se va a escanear en busca de enlaces rotos (por ejemplo, `Quarterly_Report.xlsx`).         |
| worksheet            | String | Consulta                                | **Obligatorio.** El nombre de la hoja de cálculo donde se realizará la operación de búsqueda. Especifique el nombre exacto de la hoja tal como aparece en el libro. |
| cellArea             | String | Consulta                                | **Obligatorio.** El rango de celdas que se va a analizar en busca de enlaces rotos, expresado en notación A1 (por ejemplo, `C5:J50`). La API solo busca dentro de esta área. |
| folder               | String | Consulta                                | **Opcional.** La ruta al directorio que contiene el libro en su almacenamiento en la nube. Si se omite, se asume el directorio raíz.                        |
| storageName          | String | Consulta                                | **Opcional.** El nombre de su configuración personalizada de almacenamiento en la nube. Si se omite, se utiliza el almacenamiento predeterminado del sistema. |
| region               | String | Consulta                                | **Opcional.** Configuración regional aplicada durante el procesamiento (por ejemplo, `es-ES`). Puede afectar la interpretación de la sintaxis o referencias específicas de la región en fórmulas. |
| password             | String | Consulta                                | **Opcional.** Contraseña necesaria para abrir una hoja de cálculo cifrada. Omita si el archivo no está protegido con contraseña.                             |

**Ejemplo de solicitud cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Respuesta**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
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

**Ejemplo de respuesta JSON**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "File not found"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "External reference not supported in cloud mode"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Códigos de error

- **400 Bad Request** – URI inválido de la API de Aspose.Cells Cloud.  
- **401 Unauthorized** – Token de acceso, cliente ID o cliente secret inválidos.  
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.  
- **500 Server Error** – Se produjo una anomalia al obtener los datos de cálculo.

## ¿Dónde deberíamos utilizar la API de búsqueda de enlaces rotos en la hoja de cálculo?

- **Auditoría regular de grandes modelos financieros** – Antes de publicar informes mensuales o trimestrales, escanee automáticamente áreas clave de cálculo (por ejemplo, `Dashboard!B5:K50`) que contienen muchas referencias a datos externos, para garantizar que todos los enlaces apunten a archivos de origen válidos.  
- **Integración de datos en fusiones y adquisiciones** – Al fusionar varias hojas de cálculo que representan unidades empresariales, escanee la hoja "Overview" tras la integración para identificar enlaces que se hayan vuelto inválidos debido a cambios en las rutas de archivo o problemas de permisos.  
- **Preparación de paquetes de datos para inversores** – Antes de finalizar materiales de presentación que contengan gráficos y tablas enlazados a bases de datos externas o fuentes de datos de mercado, verifique la validez de todos los enlaces.

## ¿Por qué debería utilizar la API de búsqueda de enlaces rotos en la hoja de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud proporciona bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación exhaustiva. En comparación con la creación de una solución personalizada, esto reduce significativamente el esfuerzo de desarrollo.  
- **Reducción de costos laborales** – Automatiza la validación de enlaces, eliminando la necesidad de personal dedicado para consolidar documentos manualmente.  
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.  
- **Costos de mantenimiento cero** – Sin servidores que mantener, sin actualizaciones de software ni preocupaciones por compatibilidad.

## Cómo utilizar la API de búsqueda de enlaces rotos en la hoja de cálculo con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más eficiente de acelerar el desarrollo. El SDK abstracte los detalles HTTP subyacentes, permitiéndole implementar la detección de enlaces rotos con un mínimo de código. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo interactuar con los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}