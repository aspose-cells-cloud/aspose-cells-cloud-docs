---
title: "Aspose.Cells Cloud Web: almacenamiento en la nube, conversión de hojas de cálculo, fusión, división, protección, procesamiento de datos y más"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: Centro de desarrolladores
type: docs
url: /es/
description: Aspose.Cells Las API web de Cloud admiten Spreadsheet/Excel para crear, convertir, fusionar, dividir, proteger y realizar operaciones de objetos internos, entre otras funciones. Aspose.Cells Cloud proporciona un documento completo, admite interfaces RESTful y ejemplos de código para ayudar a los desarrolladores a integrar rápidamente
weight: 10
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Aspose.Cells Documento en la nube
---
## ¿Qué son las API en la nube Aspose.Cells?

Las API de nube Aspose.Cells son un conjunto de servicios en la nube de hojas de cálculo/Excel: no es necesario instalar Office, no es necesario configurar servidores, solo envíe una solicitud HTTP y podrá realizar todas las operaciones comunes, como crear, editar, convertir formatos, limpiar datos, gráficos, tablas dinámicas, cifrado, división, fusión, marcas de agua, firmas digitales, etc., en cualquier lugar y en cualquier idioma.

## ¿Por qué utilizar las API de la nube Aspose.Cells?

- Creación, edición, conversión y análisis de hojas de cálculo en almacenamiento en la nube basado en servicios Aspose.Cells Cloud Web API.
- Cree, edite, convierta y analice archivos de hojas de cálculo locales basados en los servicios Aspose.Cells Cloud Web API.
- Los formatos de archivo admitidos son 30, como xlsx, csv, ods, xlsb, etc.
- Opere hojas de cálculo directamente a través de la Web en la nube Aspose.Cells API sin necesidad de dependencias Microsoft Excel.
- 150 llamadas gratuitas al mes al API.
- Cobro escalonado, cuanto usan los usuarios, cuanto cobran, cuanto más usan, más descuentos ofrecen.
- **Código corto**:Cosas que se pueden hacer en una frase.
  - **Convertir XLSX a PDF** → Convertir hoja de cálculo a PDF
  - **Eliminar espacios adicionales en todo el archivo** → Recortar contenido de la hoja de cálculo
  - **Combine más de 10 archivos en un solo informe** → Fusionar hojas de cálculo

## **¿Cómo utilizar las API de la nube Aspose.Cells?**

###  Paso 1:**Obtenga las credenciales API**

- **[Registrar cuenta en la nube Aspose](https://dashboard.aspose.cloud/signup)**
- **[Obtener credenciales de cliente](https://dashboard.aspose.cloud/#/applications)**

###  Paso 2:**Llamar a las API web de hojas de cálculo con SDK (recomendado)**

Se recomienda utilizar el SDK oficial para simplificar el proceso de autenticación y solicitud.

#### **[Instalar SDK (usando .NET como ejemplo)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

####  Ejemplo:**Convertir Excel a PDF con SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### Descripción

- **Hoja de cálculo**:El nombre del archivo Excel que debe estar en el almacenamiento local.
- **Formato**:Formato de destino. Por ejemplo, pdf, png, csv, json, etc.
- **Archivo de salida** Se guardará en la ubicación local. El nombre del archivo de salida es "EmployeeSalesSummary.pdf".

## **Funciones principales**

Aspose.Cells Cloud ofrece las siguientes características clave para satisfacer las necesidades de automatización de hojas de cálculo a nivel empresarial:

### **Convertir hoja de cálculo**

- **Convertir hoja de cálculo a archivo PDF**
- **Convertir gráfico de hoja de cálculo a imagen**
- **[Guardar hoja de cálculo como](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **Proceso de datos**

- **[Combinar hojas de cálculo](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **Hojas de cálculo divididas**
- **[Eliminar filas en blanco de una hoja de cálculo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[Eliminar columnas en blanco de una hoja de cálculo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[Reemplazar el contenido de la hoja de cálculo](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## Soporte SDK(**SDK disponibles**)

-  Aspose.Cells Ofertas en la nube[SDK](https://github.com/aspose-cells-cloud)** en varios idiomas, listo para usar:

| Idioma| Método de instalación| Repositorio de GitHub|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Repositorio de GitHub del SDK Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[Repositorio de GitHub del SDK .NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[pepita](https://pypi.org/project/asposecellscloud/) |[Repositorio de GitHub del SDK Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[Node.js](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[Repositorio de GitHub del SDK de Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[Compositor](https://packagist.org/packages/aspose/cells-sdk-php) |[Repositorio de GitHub del SDK PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[GoLang](https://go.dev/) |[Módulos Go](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[Repositorio de GitHub del SDK de GoLang](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[Rubí](https://www.ruby-lang.org/) |[RubyGems](https://rubygems.org/gems/aspose_cells_cloud) |[Repositorio de GitHub del SDK de Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Repositorio de GitHub del SDK Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API Punto final**: [Aspose.Cells Hoja de cálculo en la nube Web API Referencia](https://reference.aspose.cloud/cells/)

## **Ejemplos de código y proyectos de código abierto**

Todos los SDK son de código abierto e incluyen ejemplos completos:

- [Java Ejemplos de SDK en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET Ejemplos de SDK en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python Ejemplos de SDK en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Ejemplos de SDK de Node.js en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP Ejemplos de SDK en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Ejemplos de Go SDK en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Ejemplos de SDK de Ruby en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl Ejemplos de SDK en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
