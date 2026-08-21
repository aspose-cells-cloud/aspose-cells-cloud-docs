---
title: Sütun Detaylarını Al – Aspose.Cells Cloud API Referansı (v4.0)
description: Aspose.Cells Cloud REST API kullanarak bir çalışma sayfası sütunuyla ilgili detaylı bilgiyi (indeks, genişlik, stil, gizli durumu) alın.
keywords: Aspose.Cells, Bulut API, Excel sütunu, Sütun al, REST API, JWT, çalışma sayfası
date: 2026-07-30
---

# Sütun Detaylarını Al  

Aspose Cloud’da depolanan bir Excel çalışma kitabından belirli bir çalışma sayfası sütunuyla (indeks, genişlik, stil, gizli durumu) ilgili detaylı bilgi alın.

## İçindekiler
1. [Önkoşullar](#önkoşullar)  
2. [Kimlik Doğrulama](#kimlik-doğrulama)  
3. [Uç Nokta](#uç-nokta)  
4. [İstek Parametreleri](#istek-parametreleri)  
5. [cURL Örneği](#curl-örneği)  
6. [Yanıt Örneği](#yanıt-örneği)  
7. [Yanıt Şeması](#yanıt-şeması)  
8. [Olası Hatalar](#olası-hatalar)  
9. [SDK Örnekleri](#sdk-örnekleri)  
10. [Ek Kaynaklar](#ek-kaynaklar)  

---

## Önkoşullar
- Aspose Cloud kimlik doğrulama yoluyla elde edilmiş geçerli bir **JWT erişim jetonu**.  
- Çalışma kitabının dosyası, Aspose Cloud Depolama Alanı (veya başka desteklenen bir depolama) içinde depolanmış olmalı ve gerekliyse klasör yolu bilinmelidir.  

---

## Kimlik Doğrulama
Tüm Aspose.Cells Cloud API’leri, **JWT jeton tabanlı kimlik doğrulama** kullanır. Jetonu `Authorization` başlığına ekleyin:

```http
Authorization: Bearer <access_token>
```

Jeton alma ile ilgili ayrıntılar için [kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakın.

---

## Uç Nokta
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – Çalışma kitabının dosya adı (örn. `test.xlsx`).  
- **{sheetName}** – Çalışma sayfasının adı (örn. `Sheet1`).  
- **{columnIndex}** – Alınacak sütunun sıfır tabanlı indeksi.  

---

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

## Istek Parametreleri

| Ad               | Konum | Tür     | Gerekli | Açıklama |
|------------------|-------|---------|---------|----------|
| **name**         | path  | string  | Evet    | Çalışma kitabının dosya adı. |
| **sheetName**    | path  | string  | Evet    | Sütunu içeren çalışma sayfası. |
| **columnIndex**  | path  | integer | Evet    | Alınacak sütunun sıfır tabanlı indeksi. |
| **folder**       | query | string  | Hayır   | Çalışma kitabının bulunduğu depolama klasörü. |
| **storageName**  | query | string  | Hayır   | Depolama hizmetinin adı (örn. Aspose Cloud Depolama Alanı). |

---

## cURL Örneği
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Yanıt Örneği
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Yanıt Şeması
| Alan                 | Tür     | Açıklama |
|----------------------|---------|----------|
| `Column.GroupLevel`  | integer | Sütunun özet düzeyi (gruplama için kullanılır). |
| `Column.Index`       | integer | Sütunun sıfır tabanlı indeksi. |
| `Column.IsHidden`    | boolean | Sütun gizliyse `true`, aksi halde `false`. |
| `Column.Width`       | number  | Sütunun genişliği karakter cinsinden. |
| `Column.Style`       | object  | Sütunun stil kaynağına bir `link` içerir. |
| `Column.link`        | object  | Sütun kaynağına yönelik kendi bağlantısı (self-link). |
| `Code`               | integer | Yanıtın HTTP durum kodu. |
| `Status`             | string  | Durumun metinsel açıklaması (örn. **OK**). |

---

## Olası Hatalar
| HTTP Durumu | Kod | Mesaj                   | Ne zaman oluşur |
|-------------|-----|-------------------------|-----------------|
| 400         | 400 | Bad Request (Geçersiz İstek) | Gerekli parametreler eksik veya hatalı. |
| 401         | 401 | Unauthorized (Yetkisiz)      | Eksik veya geçersiz `Authorization` başlığı. |
| 404         | 404 | Not Found (Bulunamadı)       | Çalışma kitabı, çalışma sayfası veya sütun mevcut değil. |
| 500         | 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu tarafı sorunu. |

### Örnek – 404 Bulunamadı
```json
{
  "Code": 404,
  "Message": "Sütun indeksi aralık dışı."
}
```

### Örnek – 401 Yetkisiz
```json
{
  "Code": 401,
  "Message": "Geçersiz veya eksik kimlik doğrulama jetonu."
}
```

---

## SDK Örnekleri
Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK’larını kullanarak **Get Worksheet Columns** (Çalışma Sayfası Sütunlarını Al) işlemini çağırma yöntemini göstermektedir. Bir Gist kullanılamaz hale gelirse, örnek kod burada doğrudan verilmiştir.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// API istemcisini yapılandır
var apiInstance = new CellsApi("client_id", "client_secret");

// Gerekli parametreleri ayarla
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // isteğe bağlı
string storageName = "MyStorage";    // isteğe bağlı

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Sütun İndeksi: " + response.Column.Index);
    Console.WriteLine("Genişlik: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("CellsApi.GetWorksheetColumns çağrısında özel durum: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // isteğe bağlı
        String storageName = "MyStorage";    // isteğe bağlı

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Sütun indeksi: " + result.getColumn().getIndex());
            System.out.println("Genişlik: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("CellsApi#getWorksheetColumns çağrısında özel durum");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # isteğe bağlı
storage_name = "MyStorage"  # isteğe bağlı

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Sütun indeksi:", response.column.index)
    print("Genişlik:", response.column.width)
except Exception as e:
    print("CellsApi->get_worksheet_columns çağrısında özel durum:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // isteğe bağlı
const storageName = "MyStorage"; // isteğe bağlı

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Sütun indeksi:", result.column?.index);
        console.log("Genişlik:", result.column?.width);
    })
    .catch((error) => {
        console.error("getWorksheetColumns çağrısında hata:", error);
    });
```

</details>

> **Not:** Tüm SDK’lar, `client_id` ve `client_secret` sağladığınızda otomatik olarak `Authorization` başlığını işlemektedir.

---

## Ek Kaynaklar
- **OpenAPI Spesifikasyonu:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Kimlik Doğrulama Kılavuzu:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **GitHub Deposu (SDK’lar ve Örnekler):** <https://github.com/aspose-cells-cloud>  

--- 

*Belge son güncelleme tarihi: 2026-07-30.*