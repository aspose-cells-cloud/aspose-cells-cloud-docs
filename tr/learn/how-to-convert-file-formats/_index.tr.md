---
title: "Aspose.Cells Cloud ile elektronik tablo dosyası biçimlerini nasıl dönüştüreceğiniz"
linktitle: "Elektronik tablo dosya biçimlerini nasıl dönüştüreceğiniz"
type: docs
url: /tr/how-to-convert-file-formats
description: "Aspose.Cells Cloud ile dosya biçimlerini nasıl dönüştüreceğiniz."
weight: 10
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Aspose.Cells Cloud ile dosya biçimlerini nasıl dönüştüreceğiniz
---

## Giriş

Aspose.Cells Cloud Elektronik Tablo API’si, yerel ve bulut tabanlı elektronik tablo dosyalarını dönüştürmek için çift kanallı bir arayüz seti sunar. Excel (XLS, XLSX), CSV, HTML ve PDF gibi biçimleri destekler; böylece çeşitli ihtiyaçlara kolayca uygun dönüşümler yapmanızı sağlar.

### Üç Dönüşüm Modu · Tek Bir Nesne Modeli · Tüm Biçim Kapsamı

![Dönüşüm Modları](image.png)

## **Temel Dönüşüm Matrisi**

| Dönüşüm Türü          | Nesne Seviyesi    | Tipik API                       | Çıkış Biçimleri                |
|-----------------------|-------------------|---------------------------------|--------------------------------|
| **Yerel Dönüşüm**     | Çalışma Kitabı    | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ biçim  |
|                       | Çalışma Sayfası   | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                   |
|                       |                   | `ConvertWorksheetToPdf`         | PDF                            |
|                       | Tablo             | `ConvertTableToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertTableToPdf`             | PDF                            |
|                       |                   | `ConvertTableToCsv`             | CSV                            |
|                       |                   | `ConvertTableToHtml`            | HTML                           |
|                       |                   | `ConvertTableToJson`            | JSON                           |
|                       | Aralık            | `ConvertRangeToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertRangeToPdf`             | PDF                            |
|                       |                   | `ConvertRangeToCsv`             | CSV                            |
|                       |                   | `ConvertRangeToHtml`            | HTML                           |
|                       |                   | `ConvertRangeToJson`            | JSON                           |
|                       | Grafik            | `ConvertChartToImage`           | PNG/JPEG/SVG/....              |
|                       |                   | `ConvertChartToPdf`             | PDF                            |
| **Bulut Dönüşümü**    | Çalışma Kitabı    | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ biçim  |
|                       | Çalışma Sayfası   | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ biçim  |
|                       | Tablo             | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ biçim  |
|                       | Aralık            | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ biçim  |
|                       | Grafik            | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ biçim  |
| **Bulut Farklı Kaydet**| Çalışma Kitabı    | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ biçim  |

### **Yerel Dosya Dönüşümü**

```csharp
// Cells Cloud API istemcisini alın
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Dosyasını Başka Bir Biçime Dönüştürme**

```c#
// Yerel Excel dosyasını PDF'e dönüştür
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Excel Grafiğini SVG Dosyasına Dönüştürme**

```c#
// Yerel Excel grafiğini SVG'ye dönüştür
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Tabloyu CSV Dosyasına Dönüştürme**

```C#
// Sales çalışma sayfasının SaleLogs tablosunu CSV'ye dönüştür
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Bulut Dosya Dönüşümü**

Aspose Cells Cloud API istemcisini elde etmeniz gerekir.

```csharp
// Cells Cloud API istemcisini alın
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Dosyasını PDF'e Dönüştürme**

```csharp
// Buluttaki Excel dosyasını PDF'e dönüştür ve yerel dosyaya kaydet
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Excel Çalışma Sayfasını PDF'e Dönüştürme**

```csharp
// Buluttaki Excel çalışma sayfasını PDF'e dönüştür ve yerel dosyaya kaydet
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Buluttaki Excel çalışma sayfasını PDF'e dönüştür ve yerel dosyaya kaydet
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Aspose.Cells Cloud SDK’nın Kurulması ve Başlatılması

.NET projenize Aspose.Cells-Cloud NuGet paketini yükleyin; bunu NuGet Paket Yöneticisi Konsolu veya Visual Studio’daki NuGet Paket Yöneticisi aracılığıyla yapabilirsiniz. Paketin Konsol üzerinden nasıl yükleneceği aşağıdadır:

```powershell

Install-Package Aspose.Cells-Cloud

```

Aşağıdaki kod parçasında, `CellsApi` sınıfının yeni bir örneği oluşturulur ve istemci kimliğiniz ile istemci gizli anahtarınızla başlatılır:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Lütfen `YOUR_API_KEY`, `YOUR_APP_SID` ve `YOUR_APP_KEY` alanlarını gerçek API anahtarınız, uygulama SID’niz ve uygulama anahtarınız ile değiştirin.

## **Dosya Biçimi Dönüşümü Kullanım Alanları**

Aspose Cells Cloud API, kritik iş senaryoları için kurumsal düzeyde **elektronik tablo dönüştürme** yetenekleri sunar:

1. **Excel → PDF**  
   Biçimi korunarak yazdırılmaya uygun raporlar oluşturun  
2. **Elektronik Tablolar → HTML**  
   Etkileşimli tabloları web uygulamalarına gömün  
3. **CSV → Excel (XLSX)**  
   Ham verileri analiz edilebilir çalışma kitaplarına dönüştürün  
4. **Özel Biçim Dönüştürme**  
   20+ biçim arasında dönüşüm yapın (XLS, XLSB, ODS, FODS, TSV)  
![Giriş biçimlerinden çıkış biçimlerine dönüşüm](image-1.png)

## **Sonuç: Tek API Çağrısıyla Dönüşümleri Basitleştirin**  

---