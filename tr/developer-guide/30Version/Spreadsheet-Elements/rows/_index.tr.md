---
---
title: "Excel Satırlarıyla Çalışmak – Aspose.Cells Cloud API"
ArticleTitle: "Excel Satırlarıyla Çalışmak – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Satırlar"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, Excel satırları, REST API, elektronik tablo işleme"
description: "Aspose.Cells Cloud REST API ile Excel dosyalarındaki satırları işleyin. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift’i destekler."
weight: 100
---

## Excel dosyasındaki satırlarla çalışma

**Son güncelleme: Temmuz 2026**

- [Excel çalışma sayfasında satır bilgisi nasıl alınır?](/cells/rows/get/row/)
- [Excel çalışma sayfasına boş bir satır nasıl eklenir?](/cells/rows/add/row/)
- [Excel çalışma sayfasında satırlar nasıl kopyalanır?](/cells/rows/copy/)
- [Excel çalışma sayfasında satırlar nasıl gizlenir?](/cells/rows/hide/)
- [Excel çalışma sayfasında gizli satırlar nasıl gösterilir?](/cells/rows/unhide/)
- [Excel çalışma sayfasında satırlar nasıl gruplanır?](/cells/rows/group/)
- [Excel çalışma sayfasında gruplanan satırlar nasıl ayrılır?](/cells/rows/ungroup/)
- [Çalışma sayfasından bir satır nasıl silinir?](/cells/rows/delete/)

Yaygın satır işlemleri için hızlı API referansı:

| İşlem | HTTP Yöntemi | Uç Nokta                                                               | Ana Parametreler                         |
|-------|--------------|------------------------------------------------------------------------|----------------------------------------|
| [Satırı Al](https://docs.aspose.cloud/cells/rows/get/row/)     | GET          | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Satır Ekle](https://docs.aspose.cloud/cells/rows/add/row/)     | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [Satırları Kopyala](https://docs.aspose.cloud/cells/rows/copy/)      | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Satır Sil](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE       | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Satırları Gizle](https://docs.aspose.cloud/cells/rows/hide/)      | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [Satırları Göster](https://docs.aspose.cloud/cells/rows/unhide/)  | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [Satırları Grupla](https://docs.aspose.cloud/cells/rows/group/)    | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [Satır Grubunu Kaldır](https://docs.aspose.cloud/cells/rows/ungroup/)| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**İstek / Yanıt Ayrıntıları**

- **Satırı Al**  
  *İstek*: Gövde gerekmez.  
  *Yanıt (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Hatalar*: 400 Bad Request (geçersiz dizin), 404 Not Found (dosya veya sayfa eksik).

- **Satır Ekle**  
  *İstek gövdesi (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Yanıt (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Hatalar*: 400 Bad Request (eksik/geçersiz parametreler), 401 Unauthorized.

- **Satırları Kopyala**  
  *İstek gövdesi (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Yanıt (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Hatalar*: 400 Bad Request, 404 Not Found.

- **Satır Sil**  
  *İstek*: Gövde gerekmez.  
  *Yanıt (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Hatalar*: 400 Bad Request, 404 Not Found.

- **Satırları Gizle**  
  *İstek gövdesi (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Yanıt (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Hatalar*: 400 Bad Request.

- **Satırları Göster** – *Satırları Gizle* ile aynı yük; yanıt aynı, durum “Rows unhidden”.

- **Satırları Grupla** – *Satırları Gizle* ile aynı yük; yanıt durumu “Rows grouped”.

- **Satır Grubunu Kaldır** – *Satırları Gizle* ile aynı yük; yanıt durumu “Rows ungrouped”.

Tüm işlemler geçerli bir OAuth 2.0/JWT erişim belirteci ve uygun SDK sürümü gerektirir.  

---