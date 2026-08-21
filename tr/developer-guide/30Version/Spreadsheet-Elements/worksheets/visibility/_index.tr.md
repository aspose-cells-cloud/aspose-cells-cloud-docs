---
title: "Excel Çalışma Sayfasında Görünürlük ile Çalışma"
second_title: "Belge"
linktitle: "Görünürlük"
type: docs
url: /tr/worksheets/panes/
keywords: "Aspose.Cells Cloud, çalışma sayfası gizleme API'si, çalışma sayfası gösterme API'si, Excel çalışma sayfası görünürlüğü, REST API Excel, Aspose.Cells v3.0"
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma sayfalarını programlı olarak gizleme veya gösterme konusunda bilgi edinin. İstek URL'leri, cURL ve .NET SDK örnekleri, hata işleme ve sürüm-özel notları içerir."
weight: 20
---

## Excel Çalışma Sayfasında Görünürlük ile Çalışma

*Çalışma sayfası görünürlüğü*, bir sayfanın son kullanıcıya gösterilip gösterilmeyeceğini tanımlar. Aspose.Cells Cloud ile bir çalışma sayfasını basit bir REST çağrısı ile gizleyebilir veya gösterebilirsiniz. Kullanılan API uç noktaları şunlardır:

* **Çalışma sayfasını gizle** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Çalışma sayfasını göster** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Desteklenen API sürümü:** **v3.0** (Mart 2026 itibarıyla)

### Ön Gereksinimler
1. Aktif bir **Aspose.Cells Cloud** hesabı.  
2. Geçerli bir **istemci kimliği** ve **istemci gizli anahtarı** (veya OAuth 2.0 erişim belirteci).  
3. Çalışma kitabının (`{fileName}`) zaten Aspose bulut depolama alanına yüklenmiş olması gerekir.  

---

## Çalışma Sayfasını Gizleme

### İstek
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Yanıt
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Örnek cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Örnek .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Çalışma sayfası gizlendi: {response.Worksheet.Visible}");
```

### Yaygın Hatalar
| HTTP Kodu | Açıklama                                 | Çözüm                                                    |
|----------|------------------------------------------|----------------------------------------------------------|
| 400      | Geçersiz JSON gövdesi veya eksik `Visible` | İstek gövdesinin anahtarı içeren geçerli JSON olduğundan emin olun. |
| 401      | Yetkisiz – belirteç eksik veya süresi dolmuş | OAuth belirtecini yenileyin ve başlıkta dahil edin.       |
| 404      | Çalışma sayfası veya dosya bulunamadı     | `{fileName}` ve `{sheetName}` değerlerinin doğru olduğunu kontrol edin. |
| 409      | Çalışma sayfası zaten gizli              | İsteği göndermeden önce mevcut görünürlük durumunu kontrol edin. |

---

## Çalışma Sayfasını Gösterme

### İstek
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Yanıt
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Örnek cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Örnek .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Çalışma sayfası görünür: {response.Worksheet.Visible}");
```

### Yaygın Hatalar
| HTTP Kodu | Açıklama                                 | Çözüm                                                    |
|----------|------------------------------------------|----------------------------------------------------------|
| 400      | Geçersiz JSON gövdesi veya eksik `Visible` | `"Visible": true` içeren doğru JSON yükünü sağlayın.     |
| 401      | Yetkisiz – belirteç eksik veya süresi dolmuş | Erişim belirtecini yeniden oluşturun ve tekrar deneyin. |
| 404      | Çalışma sayfası veya dosya bulunamadı     | Dosya ve sayfa adlarının depoda mevcut olduğunu doğrulayın. |
| 409      | Çalışma sayfası zaten görünür           | Herhangi bir işlem gerekmez; çalışma sayfası zaten gösteriliyor. |

---

## İlgili İşlemler
> *Bölmeleri Dondur* | *Bölmeleri Böl* | *Yakınlaştır* – ek çalışma sayfası düzen kontrolü için ilgili sayfalara bakın.

---

## Sık Sorulan Sorular

<dl>
  <dt>Aspose.Cells Cloud API ile bir çalışma sayfasını nasıl gizleyebilirim?</dt>
  <dd>`{ "Visible": false }` JSON gövdesi ile `/cells/{fileName}/worksheets/{sheetName}/visibility` uç noktasına bir `PUT` isteği gönderin. Geçerli bir OAuth 2.0 bearer belirteci ekleyin. `200 OK` yanıtı, güncellenmiş çalışma sayfası nesnesini döndürür.</dd>

  <dt>Bir çalışma sayfasını gösterdikten sonra ne tür bir yanıt alırım?</dt>
  <dd>API, `"Visible": true` içeren çalışma sayfası nesnesini içeren `200 OK` yanıtı döndürür. Yanıt, çalışma sayfasının `Name`, `Index` ve `Visible` özelliklerini içerir.</dd>

  <dt>Tek bir çağrıda birden fazla çalışma sayfasını gizleyebilir miyim?</dt>
  <dd>Hayır. Görünürlük uç noktası `{sheetName}` ile tanımlanan tek bir çalışma sayfası üzerinde çalışır. Birden fazla sayfayı gizlemek için istemci kodunuzda her adımda her sayfa adı için yineleme yapın.</dd>
</dl>

---

*Aspose Docs ekibi tarafından yazıldı – Excel iş akışlarını otomatikleştirme konusunda 15 yıldan fazla deneyim.*