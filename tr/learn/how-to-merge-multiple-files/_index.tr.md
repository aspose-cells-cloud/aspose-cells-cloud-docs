---
title: Aspose.Cells Clou ile birden fazla E-Tablo dosyası nasıl birleştirilir
linktitle: Birden fazla E-Tablo dosyası nasıl birleştirilir
type: docs
url: /tr/how-to-merge-multiple-files
description: Aspose.Cells Cloud ile birden fazla E-Tablo dosyası nasıl birleştirilir
weight: 10
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Aspose.Cells Bulut aracılığıyla birden fazla dosya nasıl birleştirilir
---
## giriiş

Aspose.Cells Cloud API, elektronik tablo dosyalarının oluşturulması, düzenlenmesi ve dönüştürülmesi için tasarlanmış güçlü bir bulut tabanlı çözümdür. Bu makalede, tipik kullanım durumları ve örnek kodlar da dahil olmak üzere, Aspose.Cells Cloud API'in dosya biçimi birleştirme için kullanım sürecini adım adım açıklayacağız.

## Genel Bakış

 Aspose.Cells Cloud API, birden fazla elektronik tablo dosyasını çeşitli biçimlerde tek bir dosyada birleştirmek için güçlü API'ler sunar. Desteklenen biçimler şunlardır:**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**ve daha fazlası. Aspose.Cells Cloud API'i kullanarak, birden fazla elektronik tablo dosyasını yaygın olarak kullanılan formatlarda tek bir dosyada zahmetsizce birleştirebilir ve çeşitli gereksinimlerinizi karşılayabilirsiniz.

Dosya birleştirme için çok sayıda API mevcuttur ve genellikle çeşitli çevrimiçi ortamlarla uyumludur. Aşağıda bu API'lerin ayrıntılı bir açıklaması bulunmaktadır:

| İşlev| Tanım| API Referans|
|:------------------------- |:------------------------- |:------------------------- |
|**[E-Tabloları Birleştir](https://docs.aspose.cloud/cells/merge-spreadsheets/)** |Yerel elektronik tablo dosyalarını belirtilen formattaki bir dosyaya birleştirin.|[Birleştirme Tabloları](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[UzakBirleştirmeE-Tablosu](https://docs.aspose.cloud/cells/birleştirme-uzak-birleştirme-e-tablosu/)** | Bulut depolama klasöründeki elektronik tablo dosyalarını belirtilen formattaki dosyaya birleştirin.|[Uzak Elektronik Tabloyu Birleştir](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[Uzak Klasördeki Elektronik Tabloları Birleştirme](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Bulut depolama klasöründeki elektronik tablo dosyalarını belirtilen formattaki dosyaya birleştirin.|[Uzak Klasördeki Elektronik Tabloları Birleştir](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Aspose.Cells Bulut aracılığıyla birden fazla dosya nasıl birleştirilir

 Aspose.Cells Bulut API şunları sağlar:[birden fazla SDK](https://github.com/aspose-cells-cloud) Farklı programlama dilleri için. Tercih ettiğiniz programlama diline uygun SDK'yı seçin ve kurulum ve başlatma için beraberindeki belgeleri izleyin. Alternatif olarak, kendi SDK'nızı aşağıdakilere göre oluşturabilirsiniz:[API referans](https://reference.aspose.cloud/cells/)Bu bölümde, dosya birleştirme işlemini ayrıntılı olarak anlatmak için C# örneğini kullanacağız.

## API Anahtarının Kaydı ve Alınması

Başlamadan önce şunları yapmanız gerekir:[Aspose Bulut hesabını kaydedin](https://id.containerize.com/signup) Ve[kimlik doğrulaması için API anahtarını edinin](https://dashboard.aspose.cloud/applications)Resmi Aspose Cloud web sitesine giriş yaparak ücretsiz hesap oluşturabilir ve kimlik doğrulama amacıyla API anahtarını alabilirsiniz.

 Daha detaylı işlemler için lütfen aşağıdaki belgelere bakınız:[Cells Bulut ile Hızlı Başlangıç](https://docs.aspose.cloud/cells/quickstart/)

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

## API Talebini Oluşturun ve API'i Arayın

### Yerel elektronik tabloları birleştirmek ve konsolide edilmiş dosyaları (yerel çıktılar veya bellek içi akışlar olarak) gereken herhangi bir biçimde sunmak için bulut hizmetlerinden yararlanın

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Bulutta depolanan elektronik tabloları buluta birleştirin ve birleştirilmiş dosyayı yerel olarak veya bulut depolama alanına istediğiniz formatta iletin

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Bulut dizinindeki eşleşen dosyaları otomatik olarak birleştirin, birleştirilmiş sonucu belirtilen biçimde dışa aktarın ve yerel olarak veya bulut depolamasına geri gönderin

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Kullanım Örnekleri

 Birden fazla dosya**birleştirilmiş**Aspose.Cells Cloud API'in bu özelliği çeşitli pratik kullanım durumlarında faydalıdır. İşte bazı yaygın senaryolar:

- **Birden fazla Excel dosyasını bir Excel dosyasında birleştirin** veri analizi ve depolama için.
- **Veri dosyalarını Excel dosyasına birleştir** Veri analizi için.
- **Birden fazla resim dosyasını PDF dosyasında birleştirin** Kolay paylaşım için.
- **Birden fazla dosyayı bir HTML dosyasında birleştirin** web sayfalarında görüntülenmek ve yerleştirilmek üzere.

## Çözüm

Aspose.Cells Cloud API ile birden fazla elektronik tablo dosyasını tek bir dosyada kolayca birleştirebilirsiniz. Basit API aramaları yaparak ve uygun birleştirme seçeneklerini ayarlayarak, çeşitli dosya birleştirme gereksinimlerini verimli bir şekilde karşılayabilirsiniz. Verimliliği artırmak ve geliştirme süresinden tasarruf etmek için Aspose.Cells Cloud API'i uygulamalarınıza entegre edin.

Yukarıdaki örnek kodun yalnızca tanıtım amaçlı olduğunu ve pratikte kullanırken geçerli kimlik doğrulama bilgileri ve dosya yollarıyla değiştirmeniz gerekeceğini lütfen unutmayın. Ayrıca, Aspose.Cells Cloud API, elektronik tablo oluşturma, düzenleme, düzenleme ve veri işleme gibi birçok başka özellik sunar. Ayrıntılı API dokümantasyonu ve örnek kod şu adreste bulunabilir:[resmi Aspose web sitesinin geliştirici kılavuzu](/developer-guide/).

Bu makalenin, Aspose.Cells Cloud API'i dosya birleştirme için nasıl kullanacağınızı anlamanıza yardımcı olmasını umuyoruz. Uygulamanızda bol şans!
