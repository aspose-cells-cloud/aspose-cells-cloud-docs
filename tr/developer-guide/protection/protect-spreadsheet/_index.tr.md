---
title: "Aspose.Cells Cloud Excel Şifre Koruması Web API’si – Şifreleme Açma ve Değiştirme Şifrelerini Otomatikleştirin"
second_title: "Excel Koruması İçin Geliştirici Kılavuzu"
ArticleTitle: "Excel Şifre Koruması Aracı – Açma ve Değiştirme Şifrelerini Ayarlayın – Elektronik Tablo Dosyalarınızı Güven Altına Alın"
linktitle: "Elektronik Tabloyu Korumak"
type: docs
url: /protect-spreadsheet/
keywords: "Aspose.Cells, Excel şifre koruması, API, açma şifresi, değiştirme şifresi, bulut depolama, elektronik tablo güvenliği"
description: "Aspose.Cells Cloud ile Excel dosyalarınızı programatik olarak güven altına alın. Tek bir API çağrısıyla hem açma hem de değiştirme şifrelerini ayarlayın. .xlsx, .xls ve bulut depolamayı destekler. Ücretsiz olarak deneyin."
weight: 100
---

Geliştirici API’mizle Excel şifre korumasını ölçekli bir şekilde otomatikleştirin—açma ve değiştirme şifrelerini programatik olarak uygulayın. Kurumsal iş akışları için idealdir ve .xlsx ile eski formatları destekler. Belgeleri inceleyin ve ücretsiz entegrasyonunuzu bugün başlayın.

## **Elektronik Tabloyu Korumak API’si**

### **Web API’si**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTPBody | Açıklama                                                                                                                                    |
| :------------- | :----- | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya  | FormData                   | Yüklenip şifreleme ile korunacak Excel elektronik tablo dosyası.                                                                              |
| openPassword   | Dize   | Sorgu                      | Korumalı elektronik tabloyu açmak (şifresini çözmek) için gereken şifre.                                                                             |
| modifyPassword | Dize   | Sorgu                      | Elektronik tablo içeriğinin düzenlenmesini veya değiştirilmesini etkinleştirmek için gereken şifre.                                                           |
| outPath        | Dize   | Sorgu                      | (İsteğe bağlı) Korumalı çalışma kitabının kaydedileceği çıktı klasör yolu. Belirtilmezse, dosya yanıtta döndürülür. |
| outStorageName | Dize   | Sorgu                      | Çıktı korumalı dosyasının depolanması için kullanılacak bulut depolama adı.                                                                      |
| region         | Dize   | Sorgu                      | İşlem sırasında elektronik tabloya uygulanacak bölgesel/kültürel ayarları (örn. tarih formatı, sayı formatlaması) belirtir.                  |

**Kimlik Doğrulama**  
Tüm “Elektronik Tabloyu Korumak” API çağrıları, geçerli bir OAuth 2.0 erişim belirteci gerektirir. Belirteci `Authorization` başlığında belirtin:

```http
Authorization: Bearer {access_token}
```

Belirteç, Aspose Cloud kimlik doğrulama uç noktasından alınmalı ve **Cells** kapsamını içermelidir.

## **Yanıt**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP Durum Kodları**

| Kod | Anlamı               | Açıklama                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (Tamam)                    | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)           | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü).      |
| 401  | Unauthorized (Yetkisiz)          | Geçersiz veya eksik JWT belirteci.                                     |
| 413  | Payload Too Large (Çok Büyük Yük)     | Yüklenen dosya boyut sınırını aşıyor.                                 |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                          |

## Elektronik Tabloyu Korumak API’si nerede kullanılmalı?

- ** hassas Finansal Verileri Güvenli Tutma ** – Bütçeler, faturalar veya maaş bilgilerini içeren Excel dosyalarini açma ve değiştirme şifreleriyle koruyarak yetkisiz erişim veya düzenlemeleri önleyin.
- **Gizli Raporları Güvenli Paylaşma ** – Kurum içi veya dış dağıtım sırasında yalnızca yetkili alıcıların iş, denetim veya uyumluluk raporlarını görüntülemesine veya değiştirmesine izin verin.
- **İş Akışlarında Belge Güvenliğini Otomatikleştirme ** – API’yi kurumsal sistemlere (örn. ERP, CRM) entegre ederek, depolamadan veya e-posta iletesinden önce oluşturulan elektronik tablo dosyalarını otomatik olarak şifreyle koruyun.
- **Salt Okunur Erişimi Uygulama ** – Kullanıcıların raporları görüntülemek için açmasına izin verirken, farklı bir değiştirme şifresi kullanarak değişiklikleri kısıtlayın—şablonlar veya nihai veri kümeleri için idealdir.
- **Düzenleyici Uyumluluk Gereksinimlerini Karşılama ** – GDPR, HIPAA veya SOX gereksinimlerini karşılamaya yardımcı olmak için hassas elektronik tablo verilerini, otomatik koruma yoluyla hem depolamada hem de aktarım sırasında şifreleyin.

## Elektronik Tabloyu Korumak API’si neden kullanılmalı?

- **Geliştirici Dostu ** – Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar, hızlı geliştirme sağlar ve kapsamlı belgelerle birlikte gelir. Özel çözümler oluşturmaya kıyasla, bu önemli ölçüde geliştirme iş yükünü azaltır.
- **İşe Alım İhtiyacını Azaltır ** – Belge birleştirme ve güvenliği otomatikleştirerek, özel personel ihtiyacını düşürür.
- **Kullanım Ücretli ** – Ön ödeme gerektirmez; yalnızca gerçek kullanımınız için API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti ** – Bakımı yapılacak sunucu yok, yazılım güncellemesi yok ve uyumluluk sorunu yok.
- **Tüm Orijinal Excel Biçimlendirmesini Korur ** — şifre koruması uygularken, korumalı çalışma kitabının kaynak dosyayla tam olarak aynı görünmesini sağlar.

## SDK’lar ile Elektronik Tabloyu Korumak API’si Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

[Elektronik Tabloyu Korumak API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet), web tarayıcısından doğrudan REST etkileşimlerini kolaylaştırmak için herkese açık bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyModifyPwd" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 ile kodlanmış)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme hızını en çok artıracak yoldur. SDK, temeldeki ayrıntıları yönetir ve size minimum kodla elektronik tabloyu koruma işlevselliğini uygulamanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetleriyle nasıl etkileşime girileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---