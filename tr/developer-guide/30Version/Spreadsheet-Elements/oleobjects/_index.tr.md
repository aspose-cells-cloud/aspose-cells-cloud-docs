---
title: "Excel OLE Nesneleri ile Çalışma"
second_title: "Belge"
linktitle: "OleObjects"
type: docs
url: /oleobjects/
aliases: [/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, Bulut"
description: "Aspose.Cells Cloud REST API’sini kullanarak Excel çalışma sayfalarındaki OLE nesnelerini almak, eklemek, güncellemek, silmek ve dönüştürmek. SDK’lar Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift ve Android için mevcuttur."
weight: 100
ArticleTitle: "Excel OLE Nesneleri ile Çalışma – OLE Nesnelerini Almak, Eklemek, Güncellemek, Silmek ve Dönüştürme Kılavuzu"
---

**Excel çalışma sayfasında OLE nesneleriyle nasıl çalışılır?**

Aspose.Cells Cloud REST API, OLE nesnelerini programatik olarak yönetmek için tam bir işlem seti sağlar. Aşağıda her işlem için HTTP yöntemi, uç nokta şablonu, gerekli parametreler ve kısa bir örnek yanıt verilmiştir.

- [Excel çalışma sayfasından bir OLE nesnesi alma](/cells/oleobjects/get/)
  - **Yöntem:** `GET`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametreler:** `fileName` (string), `sheetName` (string), `oleObjectIndex` (tamsayı)  
  - **Örnek yanıt:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Excel çalışma sayfasına bir OLE nesnesi ekleme](/cells/oleobjects/add/)
  - **Yöntem:** `POST`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parametreler:** `fileName`, `sheetName`, `oleObject` (ikili veya base‑64), `imageFormat` (isteğe bağlı)  
  - **Örnek istek gövdesi:** Dosya akışını içeren multipart/form‑data.  
  - **Örnek yanıt:** Yeni OLE nesnesinin konumunu içeren `201 Created` (Oluşturuldu) ve location başlığı.

- [Excel çalışma sayfasında belirli bir OLE nesnesini güncelleme](/cells/oleobjects/update/)
  - **Yöntem:** `PUT`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametreler:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (güncellenmiş içerik)  
  - **Örnek yanıt:** Güncellenmiş nesne meta verilerini içeren `200 OK` (Tamam).

- [Excel çalışma sayfasındaki bir OLE nesnesini görüntüye dönüştürme](/cells/oleobjects/convert/)
  - **Yöntem:** `GET`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Parametreler:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (örneğin `png`, `jpeg`)  
  - **Örnek yanıt:** Dönüştürülmüş OLE nesnesinin ikili görüntü akışı.

- [Excel çalışma sayfasındaki tüm OLE nesnelerini silme](/cells/oleobjects/clear/)
  - **Yöntem:** `DELETE`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parametreler:** `fileName`, `sheetName`  
  - **Örnek yanıt:** Tüm OLE nesnelerinin kaldırıldığını gösteren `204 No Content` (İçerik Yok).

- [Excel çalışma sayfasında belirli bir OLE nesnesini silme](/cells/oleobjects/delete/)
  - **Yöntem:** `DELETE`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametreler:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Örnek yanıt:** Nesnenin silindiğini onaylayan `204 No Content` (İçerik Yok).