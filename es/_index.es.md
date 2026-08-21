---
title: "Aspose.Cells Cloud API: Convertir, fusionar, dividir y proteger archivos de Excel"
second_title: "Documento"
ArticleTitle: "Aspose.Cells Cloud API: Convertir, fusionar, dividir y proteger archivos de Excel"
linktitle: "Centro de desarrolladores"
type: docs
url: /
description: "La API REST de Aspose.Cells Cloud permite la conversión, fusión, división, protección y procesamiento integral de hojas de cálculo de Excel. 150 llamadas gratuitas/mes, SDK para 8 lenguajes."
weight: 10
keywords: "Aspose.Cells Cloud, API de Excel, conversión de hojas de cálculo, fusionar Excel, dividir Excel, proteger Excel, SDK de hojas de cálculo en la nube, API REST, procesamiento de Excel"
---

## ¿Qué son las API de Aspose.Cells Cloud?

Las API de Aspose.Cells Cloud son un conjunto de servicios basados en la nube para hojas de cálculo/Excel. No es necesario instalar Office ni configurar un servidor: simplemente envíe una solicitud HTTP y podrá crear, editar, convertir, limpiar datos, generar gráficos, construir tablas dinámicas, cifrar, dividir, fusionar, agregar marcas de agua, aplicar firmas digitales y mucho más, desde cualquier lenguaje de programación.

## ¿Por qué usar las API de Aspose.Cells Cloud?

- Crear, editar, convertir y analizar hojas de cálculo en almacenamiento en la nube mediante servicios web de Aspose.Cells Cloud.  
- Crear, editar, convertir y analizar archivos de hojas de cálculo locales mediante servicios web de Aspose.Cells Cloud.  
- Los formatos de archivo admitidos incluyen 30 formatos, como **xlsx**, **csv**, **ods**, **xlsb**, etc.  
- Operar hojas de cálculo directamente mediante la API web de Aspose.Cells Cloud, sin depender de Microsoft Excel.  
- El nivel gratuito incluye hasta 150 llamadas a la API por mes.  
- Pago según el uso (modelo de tarificación por consumo).  
- **Código breve**: Operaciones que se pueden expresar en una sola frase.  
  - **Convertir XLSX a PDF** → ConvertSpreadsheetToPdf  
  - **Eliminar espacios extra en todo el archivo** → TrimSpreadsheetContent  
  - **Combinar más de 10 archivos en un solo informe** → MergeSpreadsheets  

## **¿Cómo usar las API de Aspose.Cells Cloud?**

### Paso 1: **Obtener credenciales de la API**  

- **[Registrar una cuenta de Aspose Cloud](https://dashboard.aspose.cloud/signup)**  
- **[Obtener credenciales del cliente](https://dashboard.aspose.cloud/#/applications)**  

### Paso 2: **Llamar a las API web de hojas de cálculo con un SDK (recomendado)**  

Se recomienda utilizar el SDK oficial para simplificar la autenticación y el manejo de solicitudes. El SDK obtiene y actualiza automáticamente los tokens de acceso.

#### **[Instalar SDK para .NET (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Ejemplo: **Convertir Excel a PDF con SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Descripción

- **Spreadsheet**: Nombre del archivo Excel ubicado en el almacenamiento local.  
- **Format**: Formato de destino (por ejemplo, pdf, png, csv, json).  
- **Output file**: El archivo resultante se guardará localmente con el nombre especificado.  

## **Funciones principales**

Aspose.Cells Cloud ofrece las siguientes características clave para satisfacer necesidades de automatización de hojas de cálculo a nivel empresarial:

### **Conversión de hojas de cálculo**

- **[Convertir hoja de cálculo a archivo PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[Convertir gráfico de hoja de cálculo a imagen](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[Guardar hoja de cálculo como](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Procesamiento de datos**

- **[Fusionar hojas de cálculo](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[Dividir hojas de cálculo](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[Eliminar filas en blanco de la hoja de cálculo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[Eliminar columnas en blanco de la hoja de cálculo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[Reemplazar contenido de la hoja de cálculo](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Nota**: Los esquemas detallados de solicitud y respuesta, los métodos HTTP, los parámetros de consulta y las respuestas de ejemplo para cada punto de conexión están disponibles en la **Referencia de la API web de hojas de cálculo de Aspose.Cells Cloud**, enlazada a continuación.

**Referencia rápida de puntos de conexión**

| Operación | Método HTTP | Ruta | Parámetros obligatorios | Respuesta de ejemplo |
|-----------|-------------|------|-------------------------|----------------------|
| Convertir hoja de cálculo | POST | `/cells/convert` | `Spreadsheet` (archivo), `format` (cadena) | Archivo binario (por ejemplo, PDF) |
| Fusionar hojas de cálculo | POST | `/cells/worksheets/merge` | `files` (lista de archivos) | Libro de trabajo fusionado |
| Dividir hoja de cálculo | POST | `/cells/worksheets/split` | `Spreadsheet` (archivo), `format` (cadena) | Archivo comprimido con los archivos divididos |
| Eliminar filas en blanco | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (archivo) | Libro de trabajo actualizado |
| Reemplazar contenido | POST | `/cells/replace` | `Spreadsheet` (archivo), `oldValue`, `newValue` | Libro de trabajo actualizado |

## SDK admitidos (**SDK disponibles**)

- Aspose.Cells Cloud proporciona [SDK listos para usar](https://github.com/aspose-cells-cloud) en todos los lenguajes principales: extraiga, codifique y publique:

| Lenguaje | Método de instalación | Repositorio de GitHub |
|----------|------------------------|------------------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Repositorio GitHub del SDK para Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [Repositorio GitHub del SDK para .NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Repositorio GitHub del SDK para Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Repositorio GitHub del SDK para Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [Repositorio GitHub del SDK para PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Módulos de Go](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [Repositorio GitHub del SDK para GoLang](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Repositorio GitHub del SDK para Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Repositorio GitHub del SDK para Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **Punto de conexión de la API** | [Referencia de la API web de hojas de cálculo de Aspose.Cells Cloud](https://reference.aspose.cloud/cells/) |  |

## **Ejemplos de código y proyectos de código abierto**

Todos los SDK son de código abierto e incluyen numerosos ejemplos:

- [Ejemplos del SDK para Java en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [Ejemplos del SDK para .NET en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Ejemplos del SDK para Python en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Ejemplos del SDK para Node.js en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [Ejemplos del SDK para PHP en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Ejemplos del SDK para Go en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Ejemplos del SDK para Ruby en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Ejemplos del SDK para Perl en Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---