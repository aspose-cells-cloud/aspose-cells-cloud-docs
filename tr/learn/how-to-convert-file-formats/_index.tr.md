---
title: Aspose.Cells Clou ile elektronik tablo dosya biçimleri nasıl dönüştürülür
linktitle: E-tablo dosya biçimi nasıl dönüştürülür
type: docs
url: /tr/how-to-convert-file-formats
description: Aspose.Cells Cloud ile dosya formatları nasıl dönüştürülür?
weight: 10
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Aspose.Cells Bulut aracılığıyla dosya formatlarını nasıl dönüştürebilirim?
---
## giriiş

Aspose.Cells Bulut E-Tablosu API, yerel ve bulut tabanlı e-tablo dosyalarını dönüştürmek için bir dizi çift kanallı arayüz sağlar. Excel (XLS, XLSX), CSV, HTML ve PDF gibi formatları destekleyerek, çeşitli ihtiyaçları karşılamak için dönüştürmeyi zahmetsiz hale getirir.

### Üç Dönüştürme Modu · Birleşik Nesne Modeli · Tam Biçim Kapsamı

![Dönüşüm Modları](image.png)

## **Çekirdek Dönüşüm Matrisi**

| Dönüşüm Türü| Nesne Düzeyi| Tipik API| Çıktı Biçimleri|
|-----------------|-------------|---------------------------|--------------------------|
|**Yerel Dönüşüm**  | Çalışma kitabı|`ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30+ format|
|| Çalışma sayfası|`ConvertWorksheetToImage`       |PNG/JPEG/SVG                   |
|||`ConvertWorksheetToPdf`         | PDF|
|| Masa|`ConvertTableToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertTableToPdf`             | PDF|
|||`ConvertTableToCsv`             | CSV|
|||`ConvertTableToHtml`            | HTML|
|||`ConvertTableToJson`            | HTML|
|| Menzil|`ConvertRangeToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertRangeToPdf`             | PDF|
|||`ConvertRangeToCsv`             | CSV|
|||`ConvertRangeToHtml`            | HTML|
|||`ConvertRangeToJson`            | JSON|
||Çizelge|`ConvertChartToImage`           |PNG/JPEG/SVG/....              |
|||`ConvertChartToPdf`             |PDF                            |
|**Bulut Dönüşümü**  | Çalışma kitabı|`ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30+ format|
|| Çalışma sayfası|`ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30+ format|
|| Masa|`ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30+ format|
|| Menzil|`ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30+ format|
||Çizelge|`ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30+ format|
|**Bulut Farklı Kaydet**     | Çalışma kitabı|`SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30+ format|

### **Yerel Dosya Dönüştürme**

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel Dosya Dönüştürme**

```c#
// Convert local Excel to PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Excel Tablosunu SVG dosyasına dönüştürün**

```c#
// Convert local Excel Chart to Svg
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **Tabloyu CSV dosyasına dönüştür**

```C#
# Convert the sale logs table of the Sales worksheet to csv
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **Bulut Dosya Dönüştürme**

Ayrıca Aspose Cells Cloud API istemcisini de edinmeniz gerekiyor.

```csharp
// Get Cells Cloud API client
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel'i PDF'e dönüştürün**

```csharp
// Convert cloud Excel to PDF, Save to local file
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Excel çalışma sayfasını PDF'ye dönüştürün**

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// Convert cloud Excel worksheet to PDF, Save to local file
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Aspose.Cells Cloud SDK'sını Yükleme ve Başlatma

.NET projenize Aspose.Cells-Cloud NuGet paketini kurun, NuGet Paket Yöneticisi Konsolunu veya Visual Studio'deki NuGet Paket Yöneticisini kullanabilirsiniz.
Paketi Paket Yöneticisi Konsolu'nu kullanarak nasıl kurabileceğiniz aşağıda açıklanmıştır:

```Powershell

Install-Package Aspose.Cells-Cloud

```

CellsApi sınıfının yeni bir örneğini oluşturur ve istemci kimliğiniz ve istemci sırrınızla başlatır. Yukarıda belirtilen kod parçacığının ayrıntıları aşağıdadır:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

KENDİ'nizi değiştirdiğinizden emin olun_API_ANAHTAR, SENİN_UYGULAMA_SID ve SİZİN_UYGULAMA_Gerçek API anahtarınız, uygulama SID'niz ve uygulama anahtarınızla KEY.

## **Dosya Biçimi Dönüştürme Kullanım Örnekleri**

 Aspose Cells Bulut API kurumsal düzeyde hizmet sunar**elektronik tablo dönüşümü** Kritik iş senaryoları için yetenekler:

1. **Excel → PDF**  
 Korunmuş biçimlendirmeyle baskıya hazır raporlar oluşturun
2. **Elektronik Tablolar → HTML**  
 Etkileşimli tabloları web uygulamalarına yerleştirin
3. **CSV → Excel (XLSX)**  
 Ham verileri analiz edilebilir çalışma kitaplarına dönüştürün
4. **Özel Format Kod Dönüştürme**  
 20'den fazla format arasında dönüştürme yapın (XLS, XLSB, ODS, FODS, TSV)
![Giriş formatlarından çıktı formatlarına dönüştürme](image-1.png)

## **Sonuç: Tek Bir API Çağrısıyla Dönüşümleri Kolaylaştırın**
