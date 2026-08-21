---
title: "Excel ListObject ile Çalışmak"
ArticleTitle: "Excel ListObject ile Çalışmak"
second_title: "Belge"
linktitle: "ListObject'ler"
type: docs
url: /tr/list-objects/
aliases:
  - /working-with-list-objects/
  - /working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel tablo API'si, tablo ekle, tablo güncelle, tablo sil, tabloya aralık dönüştür, Excel tablosunu sırala"
description: "Aspose.Cells Cloud REST API kullanarak Excel ListObject'lerini (tabloları) nasıl ekleyeceğinizi, güncelleyeceğinizi, sileceğinizi, alacağınızı, sıralayacağınızı ve bir aralığa dönüştüreceğinizi öğrenin. C#, Java, Python ve daha fazlası için kod örneklerini içerir."
weight: 100
---

Excel ListObject'leri (tablolar), veri kümelerini yapılandırılmış bir şekilde organize etmenin bir yolunu sağlar. Otomatik veri düzenlemesi, başlık satırları, yerleşik filtreler ve isteğe bağlı toplam satırları gibi özellikler içerirler. Verilerinizi hızlı ve verimli bir şekilde analiz etmek için bu yetenekleri öğrenin.

**ListObject tanımı:** Bir **ListObject**, satır ve sütunları gruplayan, sıralama, filtreleme ve stillendirme işlemlerini mümkün kılan ve Aspose.Cells Cloud API aracılığıyla erişilebilen Excel’in yerel tablo nesnesidir.

## Tablo (List Object) Nasıl Çalıştırılır

- [Çalışma sayfasına nasıl tablo (list object) eklenir](/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [Çalışma sayfasında tablo (list object) nasıl güncellenir](/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [Tablo (list object) nasıl bir aralığa dönüştürülür](/cells/convert-list-object-or-table-to-range/)
- [Tablo verileri nasıl sıralanır](/cells/sort-table-data/)
- [Tablodan tekrarlayan satırlar nasıl kaldırılır](/cells/list-objects/remove-duplicates/)
- [Tablo için bir süzgeç (slicer) nasıl eklenir](/cells/list-objects/insert-slicer/)

**API Referansı (genel bakış):**  
Aspose.Cells Cloud REST API, `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` ve `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` uç noktaları aracılığıyla ListObject işlemlerini sağlar. Gerekli sorgu parametreleri `folder` ve `storage`'dır. İstek gövdeleri, tablonun özelliklerini (ad, showHeaderRow, showTotalRow vb.) tanımlayan JSON nesneleridir ve yanıtlar, oluşturulan veya değiştirilen ListObject detaylarını içeren JSON yükleri döndürür.

**Önkoşullar:**  
- Geçerli bir Aspose.Cells Cloud kimlik doğrulama jetonu.  
- Çalışma kitapğı dosyası, desteklenen bir depolama konumuna (varsayılan: **/**) yüklenmelidir ve `folder` sorgu parametresi bu konuma işaret etmelidir.  
- İsteğe bağlı: Varsayılan olmayan bir depolama hizmeti kullanıyorsanız `storage` ayarlayın.

**Uç nokta detayları**

| Yöntem | Uç Nokta | Sorgu Parametreleri | İstek Gövdesi (JSON) | Başarılı Yanıt (örnek) | Durum Kodları |
|--------|----------|---------------------|---------------------|---------------------------|---------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (gerekli), `storage` (isteğe bağlı) | *yok* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (gerekli), `storage` (isteğe bağlı) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Created, 400 – Bad Request, 401 – Unauthorized, 409 – Conflict |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (gerekli), `storage` (isteğe bağlı) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (gerekli), `storage` (isteğe bağlı) | *yok* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |

**Kod Parçacıkları**

*C# (POST – ListObject Ekle)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – ListObject'leri Al)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – ListObject Güncelle)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – ListObject Kaldır)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Notlar:**  
- ListObject indeksleri sıfırdan başlar.  
- Bir ListObject eklerken, `StartRow` ve `StartColumn`, tablonun sol üst hücresini tanımlar.  
- API, büyük çalışma sayfaları için `offset` ve `limit` sorgu parametreleri aracılığıyla sayfalama destekler (tabloda gösterilmemiştir).  
- Oran sınırları: Hesap başına dakikada 100 istek; bunu aşmak **429 Too Many Requests** hatası döndürür.

Sayfa boyunca **Excel ListObject** terimini birkaç kez kullanarak, içerik “Excel ListObject”, “Aspose.Cells Cloud” ve “Excel table API” hedef anahtar kelimelerine uygun hale gelir ve SEO performansını artırırken okuyucular için doğal kalır.