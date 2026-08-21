---
title: "Aspose.Cells Cloud API ile bir Excel Çalışma Sayfasından Tek Bir Satır Alın"
description: "Aspose Cloud Deposu'nda depolanan bir Excel çalışma sayfasından belirli bir satırı almanın nasıl yapıldığını öğrenin. Aspose.Cells Cloud REST API kullanır. İstek sözdizimi, parametreler, yanıt şeması, örnek cURL ve SDK kodu (C#, Java, Python) içerir."
keywords: "Aspose.Cells Cloud, satır al, Excel API, elektronik tablo REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Bir Excel Çalışma Sayfasından Tek Bir Satır Alın

**Uç Nokta**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Aspose Cloud Deposu'nda depolanan bir çalışma sayfasından bir satır alın. Bu işlem **Read** (Okuma) kapsamlı geçerli bir OAuth 2.0 erişim belirteci gerektirir.

---

## İçindekiler
1. [Ön Gereksinimler](#ön-gereksinimler)  
2. [HTTP İsteği](#http-isteği)  
3. [Parametreler](#parametreler)  
   - [Yol parametreleri](#yol-parametreleri)  
   - [Sorgu parametreleri](#sorgu-parametreleri)  
4. [cURL Örneği](#curl-örneği)  
5. [Yanıt](#yanıt)  
   - [Başarılı şema](#başarılı-şema)  
   - [Durum kodları](#durum-kodları)  
6. [SDK Kod Örnekleri](#sdk-kod-örnekleri)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [İlgili İşlemler](#ilgili-işlemler)  
8. [Notlar ve Sınırlamalar](#notlar-ve-sınırlamalar)  

---

## Ön Gereksinimler
- Aktif aboneliğe sahip **Aspose Cloud hesabı**.  
- **Read** (Okuma) kapsamlı **OAuth 2.0 erişim belirteci**.  
- Hedef çalışma kitabının zaten Aspose Cloud Deposu'nda bulunuyor olması gerekir.  

---

## HTTP İsteği
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*Temel URL*: `https://api.aspose.cloud/v3.0`

---

## Parametreler

### Yol parametreleri
| Ad           | Tür     | Gerekli | Açıklama                                      |
|--------------|---------|---------|-----------------------------------------------|
| `name`       | string  | ✅      | Çalışma kitabı dosyasının adı (örneğin, `MyWorkbook.xlsx`). |
| `sheetName`  | string  | ✅      | Çalışma sayfasının adı (örneğin, `Sheet1`).   |
| `rowIndex`   | integer | ✅      | Alınacak satırın sıfır tabanlı indeksi.       |

### Sorgu parametreleri *(isteğe bağlı)*
| Ad            | Tür     | Gerekli | Açıklama                                         |
|---------------|---------|---------|--------------------------------------------------|
| `folder`      | string  | ❌      | Çalışma kitabının bulunduğu bulut deposundaki klasör yolu. |
| `storageName` | string  | ❌      | Kullanılan depolama hizmetinin adı (özel bir depo kullanıyorsanız). |

---

## cURL Örneği
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Yanıt

### Başarılı şema (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* style nesnesi */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...ek hücreler... */
    ]
  }
}
```

### Durum kodları
| Kod | Anlam |
|-----|-------|
| **200** | Satır başarıyla alındı. |
| **401** | Yetkisiz – eksik veya geçersiz erişim belirteci. |
| **404** | Çalışma kitabı, çalışma sayfası veya satır bulunamadı. |
| **500** | Sunucu iç hatası. |

### Hata örneği (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Erişim belirteci eksik veya geçersiz."
}
```

---

## SDK Kod Örnekleri

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // isteğe bağlı
);

Console.WriteLine($"Satır {response.Row.Index}, {response.Row.Cells.Count} hücre ile alındı.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – isteğe bağlı
);

System.out.println("Satır indeksi: " + response.getRow().getIndex());
System.out.println("Hücre sayısı: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Satır {response.row.index}, {len(response.row.cells)} hücre ile alındı.")
except ApiException as e:
    print("CellsApi->cells_rows_get_worksheet_row çağrısı sırasında istisna:", e)
```

---

## İlgili İşlemler
| İşlem | Açıklama |
|-------|----------|
| **Satır Ekle** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Çalışma sayfasına yeni bir satır ekler. |
| **Satır Sil** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Mevcut bir satırı kaldırır. |
| **Birden Fazla Satır Al** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Birden fazla satırın koleksiyonunu alır. |
| **Satırlara Genel Bakış** | `/cells/rows/` – Satır ile ilgili uç noktalar için genel belgeler. |

---

## Notlar ve Sınırlamalar
- **Oran sınırı**: Hesap başına dakikada 100 istek.  
- **Desteklenen formatlar**: XLS, XLSX, CSV, ODS.  
- Satır indeksi **sıfır tabanlıdır**; ilk satır `0`'dır.  
- Bu uç noktayı çağırmadan önce çalıştırma kitabının belirtilen `folder` klasörüne yüklenmiş olduğundan emin olun.  

---