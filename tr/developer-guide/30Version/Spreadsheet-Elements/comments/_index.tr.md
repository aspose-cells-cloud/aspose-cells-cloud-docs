---
title: "Excel Yorumları ile Çalışmak"
second_title: "Belge"
linktitle: "Yorumlar"
type: docs
url: /tr/comments/
aliases: [  /tr/working-with-comments/ ]
keywords: "Aspose.Cells Cloud, Excel yorumları API'si, elektronik tablo yorumları, REST API"
description: "Aspose.Cells Cloud REST API v3.0 ile Excel yorumlarını nasıl ekleyeceğinizi, alacağınızı, güncelleyeceğinizi ve sileceğinizi kod örnekleri, ön koşullar ve hata işleme ile öğrenin."
weight: 100
ArticleTitle: "Excel Yorumları ile Çalışmak – Aspose.Cells Cloud API Kılavuzu"
---

Bir Excel çalışma kitabını oluştururken kullanıcılar çeşitli nedenlerle yorum ekleyebilir. Yaygın bir kullanım örneği, dosyanın başkalarıyla paylaşılacağı durumlarda bir hücredeki formülü açıklamaktır. Yorumlar ayrıca hatırlatıcılar, ortak çalışanlar için notlar veya diğer çalışma kitaplarıyla arasıreferans oluşturmak amacıyla da kullanılabilir. Bir yorum eklendikten sonra, Excel kullanıcıların yorum kutusunu tercih ettikleri stile göre yeniden boyutlandırmalarına, şekillendirmelerine ve biçimlendirmelerine olanak tanır. Yorum yönetimi konusunda uzmanlaşmak, kullanıcıların bu özelliğin tam potansiyelinden faydalanmasını sağlar.

**Ön Koşullar**

- Aktif bir Aspose.Cells Cloud hesabı.  
- OAuth 2.0 ile elde edilmiş geçerli bir **erişim belirteci (access token)**.  
- API sürümü **v3.0** (bu kılavuzda kullanılan uç noktalar bu sürümü hedef alır).  
- İsteğe bağlı: İstek oluşturma işlemini basitleştirmek için tercih ettiğiniz programlama dili için Aspose.Cells SDK’sı.

**Sürüm**

Aşağıdaki örnekler **Aspose.Cells Cloud REST API v3.0** sürümünü hedef alır. Gelecek API sürümleri ek parametreler ekleyebilir veya yanıt yapılarını değiştirebilir; güncel bilgiler için lütfen her zaman en son API referansını kontrol edin.

**Yorum Ekleme**

Bir yorum eklemek için aşağıdaki uç noktaya bir **POST** isteği gönderin:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Yol parametreleri**

| Parametre | Tür    | Zorunlu | Açıklama                                |
|-----------|--------|---------|-----------------------------------------|
| `file`    | string | Evet    | Çalışma kitabı dosyasının adı (uzantısı dahil). |
| `sheet`   | string | Evet    | Yorumun ekleneği çalışma sayfasının adı. |

**İstek gövdesi şeması**

| Alan       | Tür    | Zorunlu | Açıklama                               |
|------------|--------|---------|----------------------------------------|
| `CellName` | string | Evet    | Hücrenin A1 tarzı adresi (örn. **B2**). |
| `Comment`  | string | Evet    | Saklanacak yorumun metni.              |
| `Author`   | string | Hayır   | Yorumu ekleyen kişinin adı.            |

**Örnek istek gövdesi**

```json
{
  "CellName": "B2",
  "Comment": "İnceleme gerekli",
  "Author": "Ahmet Yılmaz"
}
```

**Örnek başarılı yanıt** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "Ahmet Yılmaz",
    "HtmlComment": "İnceleme gerekli",
    "Note": "İnceleme gerekli"
  }
}
```

**Yaygın hata kodları**

| Kod | Anlam                                |
|-----|--------------------------------------|
| 400 | Geçersiz hücre adresi veya istek gövdesi |
| 401 | Yetkisiz istek – eksik/geçersiz belirteç |
| 404 | Çalışma kitabı veya çalışma sayfası bulunamadı |

**Yorumları Alma**

Bir çalışma sayfasındaki tüm yorumları almak için:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Yol parametreleri**

| Parametre | Tür    | Zorunlu | Açıklama                |
|-----------|--------|---------|-------------------------|
| `file`    | string | Evet    | Çalışma kitabı dosyasının adı. |
| `sheet`   | string | Evet    | Çalışma sayfasının adı.     |

**Örnek yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Ayşe",
      "HtmlComment": "İlk değer",
      "Note": "İlk değer"
    },
    {
      "CellName": "B2",
      "Author": "Ahmet Yılmaz",
      "HtmlComment": "İnceleme gerekli",
      "Note": "İnceleme gerekli"
    }
  ]
}
```

**Yorum Güncelleme**

Mevcut bir yorumu değiştirmek için bir **PUT** isteği gönderin. Yorum, çalışma sayfasının yorum koleksiyonundaki **indeksine** göre belirlenir (indeksleme 0’dan başlar).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Yol parametreleri**

| Parametre      | Tür    | Zorunlu | Açıklama                             |
|----------------|--------|---------|--------------------------------------|
| `file`         | string | Evet    | Çalışma kitabı dosyasının adı.        |
| `sheet`        | string | Evet    | Çalışma sayfasının adı.              |
| `commentIndex` | int    | Evet    | Güncellenecek yorumun sıfır tabanlı indeksi. |

**İstek gövdesi şeması**

| Alan     | Tür    | Zorunlu | Açıklama                     |
|----------|--------|---------|------------------------------|
| `Comment`| string | Evet    | Yeni yorum metni.            |
| `Author` | string | Hayır   | Güncellenmiş yazar adı (isteğe bağlı). |

**Örnek istek gövdesi**

```json
{
  "Comment": "Güncellenmiş not metni",
  "Author": "Ahmet Yılmaz"
}
```

Yanıt yapısı, **Yorum Ekleme** yanıtının yapısıyla aynıdır.

**Yorum Silme**

Tek bir yorumu indeksine göre silmek için:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Yol parametreleri**

| Parametre      | Tür    | Zorunlu | Açıklama                             |
|----------------|--------|---------|--------------------------------------|
| `file`         | string | Evet    | Çalışma kitabı dosyasının adı.        |
| `sheet`        | string | Evet    | Çalışma sayfasının adı.              |
| `commentIndex` | int    | Evet    | Silinecek yorumun sıfır tabanlı indeksi. |

Başarılı bir silme işlemi şu yanıtı döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Tüm Yorumları Silme**

Bir çalışma sayfasındaki tüm yorumları temizlemek için:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Yol parametreleri**

| Parametre | Tür    | Zorunlu | Açıklama                |
|-----------|--------|---------|-------------------------|
| `file`    | string | Evet    | Çalışma kitabı dosyasının adı. |
| `sheet`   | string | Evet    | Çalışma sayfasının adı.     |

**Hata işleme yönergeleri**

- **404 Bulunamadı** – Çalışma kitabının kimliğini, çalışma sayfası adını ve yorum indeksini kontrol edin.  
- **400 Bad Request** – JSON sözdizimini ve zorunlu alanları (`CellName`, `Comment`) kontrol edin.  
- **429 Çok Fazla İstek** – Üst üste artan bekleme (exponential back-off) uygulayın ve `Retry-After` başlığını dikkate alın.

**Özet**

- Excel yorumları, bir hücreye [not eklemek veya bir formülü açıklamak için](/tr/cells/comments/add/) kullanılır.  
- Excel, kullanıcıların bir çalışma sayfasındaki yorumları [düzenlemek](/tr/cells/comments/update/), [silmek](/tr/cells/comments/delete/), [göstermek](/tr/cells/comments/get/) veya [gizlemek](/tr/cells/comments/update/) için esneklik sunar.  
- Kullanıcılar ayrıca yorum kutusunu [yeniden boyutlandırmak](/tr/cells/comments/update/) ve [taşıyabilir](/tr/cells/comments/update/).  

Diğer elektronik tablo öğeleri ile çalışma konusunda daha fazla bilgi için [hücrelerle çalışma](/tr/cells/working-with-cells/) kılavuzuna bakın.