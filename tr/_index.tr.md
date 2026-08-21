---
title: "Aspose.Cells Cloud API – Excel Dosyalarını Dönüştür, Birleştir, Böl ve Korumalı Hale Getir"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud API – Excel Dosyalarını Dönüştür, Birleştir, Böl ve Korumalı Hale Getir"
linktitle: "Geliştirici Merkezi"
type: docs
url: /
description: "Aspose.Cells Cloud REST API, Excel elektronik tablolarının dönüştürülmesini, birleştirilmesini, bölünmesini, korunmasını ve kapsamlı işleme işlemlerini sağlar. Ayda ücretsiz 150 çağrı, 8 dil için SDK."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, elektronik tablo dönüştürme, Excel birleştirme, Excel bölme, Excel koruma, bulut elektronik tablo SDK, REST API, Excel işleme"
---

## Aspose.Cells Cloud API’leri Nedir?

Aspose.Cells Cloud API, buluta dayalı Elektronik Tablo/Excel hizmetlerinin bir koleksiyonudur. Office kurulumuna veya sunucu yapılandırmasına gerek yoktur—basitçe bir HTTP isteği göndererek herhangi bir dilden elektronik tablo oluşturabilir, düzenleyebilir, dönüştürebilir, verileri temizleyebilir, grafik oluşturabilir, pivot tablolar oluşturabilir, şifreleyebilir, bölebilir, birleştirebilir, su damlası ekleyebilir, dijital imza uygulayabilir ve daha fazlasını yapabilirsiniz.

## Aspose.Cells Cloud API’leri Neden Kullanılmalı?

- Aspose.Cells Cloud Web API hizmetlerine dayalı olarak, bulut depolamada elektronik tablolar oluşturma, düzenleme, dönüştürme ve analiz etme.  
- Aspose.Cells Cloud Web API hizmetlerine dayalı olarak, yerel elektronik tablo dosyaları oluşturma, düzenleme, dönüştürme ve analiz etme.  
- Desteklenen dosya formatları 30 adettir: **xlsx**, **csv**, **ods**, **xlsb** vb.  
- Microsoft Excel bağımlılığı olmadan doğrudan Aspose.Cells Cloud Web API üzerinden elektronik tablo işlemleri yapın.  
- Ücretsiz katman, ayda en fazla 150 API çağrısı içerir.  
- Kullanıma dayalı, kullanım-a-öde modeli fiyatlandırma.  
- **Kısa kod**: Bir cümlede yapılabilecek işlemler.  
  - **XLSX’i PDF’e dönüştür** → ConvertSpreadsheetToPdf  
  - **Dosyanın tamamında fazla boşlukları sil** → TrimSpreadsheetContent  
  - **10’dan fazla dosyayı tek bir raporda birleştir** → MergeSpreadsheets  

## **Aspose.Cells Cloud API’leri Nasıl Kullanılır?**

### Adım 1: **API Kimlik Bilgilerini Alın**  

- **[Aspose Cloud Hesabını Kaydedin](https://dashboard.aspose.cloud/signup)**  
- **[İstemci Kimlik Bilgilerini Alın](https://dashboard.aspose.cloud/#/applications)**  

### Adım 2: **Elektronik Tablo Web API’lerini SDK ile Çağırın (önerilir)**  

Kimlik doğrulama ve istek işlemini basitleştirmek için resmi SDK’nın kullanılması önerilir. SDK, erişim belirteçlerini otomatik olarak edinir ve yenilerinden oluşturur.

#### **[.NET SDK’yı Yükleyin (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Örnek: **SDK ile Excel’i PDF’e Dönüştürme**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Açıklama

- **Spreadsheet**: Yerel depolamada bulunan Excel dosyasının adı.  
- **Format**: Hedef format (örn. pdf, png, csv, json).  
- **Çıktı dosyası**: Oluşan dosya, belirtilen adla yerel olarak kaydedilir.  

## **Temel Özellikler**

Aspose.Cells Cloud, kurumsal düzeyde elektronik tablo otomasyonu ihtiyaçlarını karşılamak için aşağıdaki temel özellikleri sunar:

### **Elektronik Tablo Dönüştürme**

- **[Elektronik Tabloyu PDF Dosyasına Dönüştür](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[Elektronik Tablo Grafiğini Görüntüye Dönüştür](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[Elektronik Tabloyu Farklı Kaydet](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Veri İşleme**

- **[Elektronik Tabloları Birleştir](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[Elektronik Tabloları Böl](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[Elektronik Tablo boş satırlarını sil](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[Elektronik Tablo boş sütunlarını sil](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[Elektronik Tablo içeriğini değiştir](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Not:** Her uç nokta için detaylı istek/yanıt şemaları, HTTP yöntemleri, sorgu parametreleri ve örnek yanıtlar aşağıda bağlantısı verilen **Aspose.Cells Cloud Elektronik Tablo Web API Referansında** bulunabilir.

**Hızlı uç nokta referansı**

| İşlem | HTTP Yöntemi | Yol | Gerekli Parametreler | Örnek Yanıt |
|-----------|-------------|------|---------------------|-----------------|
| Elektronik Tabloyu Dönüştür | POST | `/cells/convert` | `Spreadsheet` (dosya), `format` (dize) | İkili dosya (örn. PDF) |
| Elektronik Tabloları Birleştir | POST | `/cells/worksheets/merge` | `files` (dosya listesi) | Birleştirilmiş çalışma kitabını |
| Elektronik Tabloyu Böl | POST | `/cells/worksheets/split` | `Spreadsheet` (dosya), `format` (dize) | Bölünmüş dosyaların arşivi |
| Boş Satırları Sil | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (dosya) | Güncellenmiş çalışma kitabını |
| İçeriği Değiştir | POST | `/cells/replace` | `Spreadsheet` (dosya), `oldValue`, `newValue` | Güncellenmiş çalışma kitabını |

## Desteklenen SDK’lar (**Mevcut SDK’lar**)

- Aspose.Cells Cloud, tüm büyük dillerde hemen kullanıma hazır [SDK’lar](https://github.com/aspose-cells-cloud) sunar—çekin, kodlayın ve dağıtın:

| Dil | Kurulum Yöntemi | GitHub Deposu |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modülleri](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub Deposu](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API Uç Noktası** | [Aspose.Cells Cloud Elektronik Tablo Web API Referansı](https://reference.aspose.cloud/cells/) |  |

## **Kod örnekleri ve açık kaynak projeler**

Tüm SDK’lar açık kaynaktır ve zengin örnekler içerir:

- [Java SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [.NET SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Python SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Node.js SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [PHP SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Go SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Ruby SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Perl SDK Örnekleri Github’da.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---