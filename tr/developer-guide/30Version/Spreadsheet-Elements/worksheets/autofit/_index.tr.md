---
title: "Excel Çalışma Sayfasında Otomatik Uygunluk (Autofit) ile Çalışmak"
second_title: "Belge"
linktitle: "Otomatik Uygunluk"
type: docs
url: /tr/worksheets/autofit/
aliases: [  /tr/autofit-rows-and-columns-of-worksheet/ ]
keywords: "otomatik uygunluk, sütun, satır, Aspose.Cells, Bulut, Excel, API, yeniden boyutlandırma"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki satır ve sütunları otomatik olarak yeniden boyutlandırmayı öğrenin. cURL, .NET, Java ve Python örneklerini içerir."
weight: 20
ArticleTitle: "Excel Çalışma Sayfasında Otomatik Uygunluk (Autofit) ile Çalışmak – Aspose.Cells Cloud API"
---

## Excel Çalışma Sayfasında Otomatik Uygunluk (Autofit) ile Çalışmak

- [Excel çalışma sayfasında bir sütunu otomatik uygun hale getirmenin (autofit) nasıl yapılacağı.](/cells/worksheets/autofit/column/)
- [Excel çalışma sayfasında birden fazla sütunu otomatik uygun hale getirmenin (autofit) nasıl yapılacağı.](/cells/worksheets/autofit/columns/)
- [Excel çalışma sayfasında bir satırı otomatik uygun hale getirmenin (autofit) nasıl yapılacağı.](/cells/worksheets/autofit/row/)
- [Excel çalışma sayfasında birden fazla satırı otomatik uygun hale getirmenin (autofit) nasıl yapılacağı.](/cells/worksheets/autofit/rows/)

**Gereksinimler**  
Otomatik Uygunluk (Autofit) işlemlerini kullanmadan önce şunlara sahip olmanız gerekir:

1. Geçerli bir **Client Id** ve **Client Secret** içeren bir Aspose.Cells Cloud hesabı.  
2. Aspose Cloud depo alanına yüklenmiş bir çalışma kitabına (veya herkese açık bir URL üzerinden erişilebilir bir çalışma kitabına).  
3. Değiştirmek istediğiniz çalışma sayfası adı.

**API Referansı**  

| İşlem | HTTP Yöntemi | Uç Nokta | Gerekli Parametreler | İstek Gövdesi | Örnek Yanıt | Durum Kodları |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| Bir **sütunu** otomatik uygun hale getir | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (yol) <br> `columnIndex` (sorgu) | *yok* | `{ "code": 200, "status": "OK", "message": "Sütun otomatik uygun hale getirildi." }` | 200, 400, 401, 404, 500 |
| **Sütunları** otomatik uygun hale getir | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (yol) <br> `startColumn`, `endColumn` (sorgu) | *yok* | `{ "code": 200, "status": "OK", "message": "Sütunlar otomatik uygun hale getirildi." }` | 200, 400, 401, 404, 500 |
| Bir **satırı** otomatik uygun hale getir | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (yol) <br> `rowIndex` (sorgu) | *yok* | `{ "code": 200, "status": "OK", "message": "Satır otomatik uygun hale getirildi." }` | 200, 400, 401, 404, 500 |
| **Satırları** otomatik uygun hale getir | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (yol) <br> `startRow`, `endRow` (sorgu) | *yok* | `{ "code": 200, "status": "OK", "message": "Satırlar otomatik uygun hale getirildi." }` | 200, 400, 401, 404, 500 |

**Kod Örnekleri**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Kimlik doğrulama
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Sütunları otomatik uygun hale getirme çağrısı
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Satırları otomatik uygun hale getir
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Tek bir sütunu otomatik uygun hale getir
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Bu kod parçacıkları şunları nasıl yapacağınızı gösterir:

1. **Client Id** ve **Client Secret** bilgilerinizle Aspose.Cells Cloud'a kimlik doğrulama.  
2. Sütunlar veya satırlar için uygun Otomatik Uygunluk (Autofit) uç noktasını çağırma.  
3. İşlemin başarıyla tamamlandığını onaylayan yanıtı işleme.

**Sonraki Adımlar**

Otomatik Uygunluk (Autofit) çağrısı tamamlandıktan sonra güncellenmiş çalışma kitabını indirebilirsiniz:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

Belirli aralıkları hedeflemek için `startColumn`, `endColumn`, `startRow` ve `endRow` parametrelerini istediğiniz gibi ayarlamaktan çekinmeyin.
---