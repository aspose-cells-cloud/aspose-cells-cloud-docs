---
title: "Aspose.Cells Cloud'da yerel dosya işlemesi ile bulut dosya işlemesi arasındaki fark nedir?"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud'da yerel dosya işlemesi ile bulut dosya işlemesi arasındaki fark nedir?"
linktitle: "Yerel Dosya İşlemesi vs. Bulut Dosya İşlemesi"
type: docs
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "Aspose.Cells Cloud'da yerel dosya ve bulut dosya işlemlerini karşılaştırın: depolama, maliyet, güvenlik ve tipik senaryolar. İş akışınıza hangi yaklaşımın uygun olduğunu öğrenin."
keywords: "Aspose.Cells Cloud, yerel dosya işlemesi, bulut dosya işlemesi, elektronik tablo dönüştürme, API"
weight: 10
---

Yerel dosya işlemesi ve bulut dosya işlemesi, dosya depolama altyapısı, iş işlemesi, erişim, maliyet yapısı, güvenlik ve uygulanabilir senaryolar açısından önemli farklılıklar barındıran farklı veri yönetimi paradigmalarıdır. İkisi arasındaki temel farklar şunlardır:

**Önkoşullar:** Örnekleri kullanmadan önce geçerli bir Aspose.Cells Cloud hesabınızın, en son SDK sürümünün yüklü olduğundan ve kimlik doğrulama için İstemci Kimliğiniz ve İstemci Sırrınızın hazır olduğundan emin olun.

## 1. Dosya depolama konumu ve altyapı

- Yerel dosya:

  - Dosyalar, bir kişisel bilgisayarın sabit diski, yerel sunucular veya harici sabit diskler gibi kullanıcıya ait veya kullanıcı tarafından yönetilen fiziksel cihazlarda saklanır. **Cells Cloud istemcisini doğrudan yerel depolama cihazında bulunan bir dosyaya gösterebilirsiniz.**
  - Müşteri, donanım üzerinde tam fiziksel kontrole sahiptir.
  - Altyapının satın alınması, bakımı, yükseltilmesi ve kullanım dışı bırakılması, kullanıcının veya kurumun sorumluluğundadır.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# CellsApi'yi başlat
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Yerel Excel dosyasını PDF'e dönüştür
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**API Referansı – Elektronik Tabloyu Dönüştür**

| Yöntem                | HTTP Eylemi | Uç Nokta            | Parametreler (anahtar)                           | Yanıtlar                                          |
|-----------------------|-------------|---------------------|--------------------------------------------------|---------------------------------------------------|
| `convert_spreadsheet` | POST        | `/cells/convert`    | `inputFile` – kaynak dosyanın yolu<br>`format` – hedef format (örneğin, `pdf`) | `200 OK` – dönüştürme başarılı<br>`400 Bad Request` – geçersiz parametreler<br>`401 Unauthorized` – kimlik doğrulama hatası |

- Bulut dosyası:

  - Dosyalar, üçüncü taraf bulut hizmet sağlayıcılarının (Aspose bulut depolama, Dropbox, AWS, Google Cloud, Microsoft Azure) yönettiği uzak veri merkezlerinde saklanır. **AWS, Dropbox, Google Cloud ve Microsoft Azure, Aspose bulut depolamaya bağlanabilir.**
  - Müşteriler, temel donanımın konumundan ve bakımından bağımsız olarak bu dosyalara İnternet üzerinden erişir.
  - Altyapının sorumluluğu bulut hizmet sağlayıcısındadır ve kullanıcılar talep üzerine bunu kullanır.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheetAsRequest,
)

# CellsApi'yi başlat
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Yerel dosyayı bulut depolamaya yükle
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# Buluttaki dosyayı belirli bir forma yerel depolamaya aktar
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# Uzak klasörü tanımla (farklıysa gerçek klasör adınızla değiştirin)
RemoteFolder = "PythonSDK"

# Cells Cloud'daki bir Excel dosyasını, Cells Cloud'da farklı bir forma dönüştür
api.save_spreadsheet_as(
    SaveSpreadsheetAsRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**API Referansı – Bulut Dosya İşlemleri**

| Yöntem                        | HTTP Eylemi | Uç Nokta                         | Parametreler (anahtar)                                                                                 | Yanıtlar                                     |
|-------------------------------|-------------|----------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------|
| `upload_file`                 | PUT         | `/cells/storage/file`            | `localPath` – yerel dosya yolu<br>`remotePath` – bulut depolamadaki hedef konum                       | `200 OK` – yükleme başarılı<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST        | `/cells/{name}/export`           | `name` – bulut dosyası adı<br>`format` – hedef format (örneğin, `pdf`)<br>`folder` – isteğe bağlı klasör | `200 OK` – aktarım başarılı<br>`400 Bad Request` |
| `save_spreadsheet_as`         | POST        | `/cells/{name}/saveas`           | `name` – bulut dosyası adı<br>`format` – hedef format<br>`folder` – hedef klasör                       | `200 OK` – kaydetme başarılı<br>`401 Unauthorized` |

## 2. İşlem işlemesi

Yerel dosya işlemesi veya bulut dosya işlemesi ne olursa olsun, tüm işlem işlemeleri Cells Cloud sunucusunda tamamlanır, **bu nedenle İnternet desteği gerekli**dir.

## 3. Veri Erişimi

- Yerel dosya işlemesi:

  - Erişim genellikle cihazın kendisine sınırlıdır.
  - Çoklu kişi iş birliği zordur.
  - Cihaz veya konum değiştirirken zorluklar vardır.

- Bulut dosya işlemesi:

  - İnternet bağlantısı olduğu sürece, herhangi bir cihazdan (bilgisayar, telefon, tablet) her zaman ve her yerden dosyalara erişim sağlayın.
  - Gerçek zamanlı çoklu kişi iş birliği için doğal destek sunar; birden fazla kullanıcı aynı belgeye aynı anda düzenleyebilir ve sistem otomatik olarak sürüm kontrolünü yönetir.
  - Yüksek taşınabilirlik, esnek ofis desteği ve uzaktan çalışma desteği.

## 4. Maliyet yapısı ve güvenlik

- Yerel dosya:

  - Erken aşamada yüksek sermaye harcaması gerekir. Bu, daha sonra ek operasyonel destek maliyetlerine yol açar.
  - Fiziksel güvenlik ve ağ güvenliği, kullanıcıların kendileri tarafından kontrol edilir.

- Bulut dosyası:

  - Düşük başlangıç yatırımı, esas olarak işlem giderleri, kullanıma göre ödeme.
  - Güvenlik ve bütünlük, bulut hizmet sağlayıcısının sorumluluğundadır.

## 5. Uygulanabilir senaryolar

- Yerel dosya: Dosya işlemleri yalnızca yerel olarak gerçekleştirilebilir.  
- Bulut dosyası: Dosya işlemleri yerel veya bulut ortamında gerçekleştirilebilir.  

**Notlar / Sınırlamalar:** API, bulut işlemesi için en fazla 200 MB boyutundaki dosyaları destekler ve yalnızca belgelerde listelenen formatlar dönüştürülebilir. Büyük elektronik tablolarda işlem süresi, ağ gecikmesinden etkilenabilir.

_Son güncelleme: 30 Temmuz 2026_