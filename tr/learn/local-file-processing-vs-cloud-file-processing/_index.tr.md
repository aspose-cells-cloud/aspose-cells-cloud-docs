---
title: Aspose.Cells Cloud'da yerel dosya işleme ile bulut dosya işleme arasındaki fark nedir?
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: Yerel Dosya İşleme ve Bulut Dosya İşleme
type: docs
url: /tr/learn/local-file-processing-vs-cloud-file-processing/
description: Yerel dosya işleme ile bulut dosya işleme arasındaki fark nedir? Yerel dosya işleme ve bulut dosya işleme, depolama altyapısı, iş süreçleri, erişim, maliyet yapısı, güvenlik ve uygulanabilir senaryolarda önemli farklılıklar gösteren, temelde iki farklı veri yönetimi paradigmasıdır.
weight: 10
kwords: Excel Bulut API, REST, Elektronik Tablo, PDF, CSV, Json, Markdown, Yerel Dosya İşleme ve Bulut Dosya İşleme Karşılaştırması
---
Yerel dosya işleme ve bulut dosya işleme, dosya depolama altyapısı, iş süreçleri, erişim, maliyet yapısı, güvenlik ve uygulanabilir senaryolar açısından önemli farklılıklar gösteren farklı veri yönetimi paradigmalarıdır. İkisi arasındaki temel farklar şunlardır:

## 1. Dosya depolama konumu ve altyapısı

- Yerel dosya:

 Dosyalar, kullanıcının sahip olduğu veya yönettiği fiziksel aygıtlarda (örneğin, kişisel bilgisayarın sabit diski, dahili sunucular veya harici mobil sabit diskler) saklanır. Bu aygıtlara doğrudan Cells Bulut istemcisi tarafından erişilebilir.
 - Müşteri donanım üzerinde tam fiziksel kontrole sahiptir.
 - Altyapının satın alınması, bakımı, yükseltilmesi ve kullanımdan kaldırılması kullanıcının veya kuruluşun sorumluluğundadır.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- Bulut dosyası:

 - Dosyalar, üçüncü taraf bulut servis sağlayıcıları tarafından işletilen uzak veri merkezlerinde saklanır (Aspose bulut depolama, Dropbox, AWS, Google Bulut, Microsoft Azure). AWS, Dropbox, Google Bulut ve Microsoft Azure, kişileri Aspose bulut depolamaya bağlayabilir.
 - Müşteriler, altta yatan donanımın konumu ve bakımı ne olursa olsun, bu dosyalara internet üzerinden erişebilirler.
 - Altyapı bulut servis sağlayıcısının sorumluluğundadır ve kullanıcılar talep ettiklerinde altyapıyı kullanırlar.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. İş süreçleri

Yerel dosya işleme veya bulut dosya işleme fark etmeksizin, tüm iş süreçleri Cells Bulut sunucusunda tamamlanır.**bu nedenle İnternet desteği gereklidir**.

## 3. Veri Erişimi

- Yerel dosya işleme:

 - Erişim genellikle cihazın kendisiyle sınırlıdır.
 - Çok sayıda kişinin bir arada çalışması zordur.
 - Ekipman veya yer değiştirmede zorluk yaşanması.

- Bulut dosya işleme:

 - İnternet bağlantınız olduğu sürece, istediğiniz zaman, istediğiniz yerden, istediğiniz cihazdan (bilgisayar, telefon, tablet) dosyalara erişin.
 - Çok kişili gerçek zamanlı işbirliğine doğal destek, birden fazla kullanıcı aynı anda aynı belgeyi düzenleyebilir, sistem otomatik olarak sürüm kontrolünü gerçekleştirir.
 - Güçlü hareket kabiliyeti, esnek office desteği ve uzaktan çalışma.
  
## 4. Maliyet yapısı ve güvenlik

- Yerel dosya:
  
 - Erken aşamada yüksek sermaye harcaması, sonraki aşamada operasyonel destek için belirli maliyetler gerektirir.
 Fiziksel güvenlik ve ağ güvenliği kullanıcılar tarafından kontrol edilir.

- Bulut dosyası:

 - Düşük ön yatırım, çoğunlukla işletme giderleri, talep üzerine ödeme.
 - Güvenlik ve bütünlük bulut servis sağlayıcısının sorumluluğundadır.

## 5. Uygulanabilir senaryolar

- Yerel dosya: Dosya işlemleri yalnızca yerel olarak gerçekleştirilebilir.
- Bulut dosyası: Dosya işlemleri yerel olarak veya bulutta gerçekleştirilebilir.
