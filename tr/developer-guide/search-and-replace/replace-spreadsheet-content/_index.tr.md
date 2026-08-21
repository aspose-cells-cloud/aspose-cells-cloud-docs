---
title: "Aspose.Cells Cloud – Yerel Excel Dosyalarında Metin Değiştirme (Bul & Değiştir API)"
second_title: "Belge"
ArticleTitle: "Yerel Excel Dosyalarında Toplu Metin Değiştirme – Bul & Değiştir API"
linktitle: "Elektronik Tablo İçeriğini Değiştir"
type: docs
url: /replace-spreadsheet-content/
keywords: "Excel’de metin değiştirme, Aspose.Cells Bul ve Değiştir, yerel elektronik tablo API’si, Excel dosyası değiştirme, içerik değiştirme API’si"
description: "Bulut’a yüklemeden yerel Excel çalışma kitaplarında metin değiştirin. Belirli aralıkları, çalışma sayfalarını veya tüm dosyaları tek bir çağrıda güncellemek için Aspose.Cells Cloud Bul & Değiştir API’sini kullanın."
weight: 100
---

Bulut’a yüklemeden yerel Excel elektronik tablo dosyalarında belirli metni değiştirin. Aspose.Cells Bul & Değiştir API’sini kullanarak ofline düzenleme amacıyla çalışma kitaplarındaki içeriği verimli bir şekilde güncelleyin.

## **Elektronik Tablo İçeriğini Değiştir API’si**

### **Web API’si**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                                                                 |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya  | FormData                   | İşlenecek yerel elektronik tablo dosyası. Desteklenen formatlar şunları içerir: XLSX, XLS, ODS, CSV vb.                                                                                                    |
| searchText     | Metin  | Sorgu                      | Belirtilen çalışma sayfası ve hücre aralığında aranacak metin dizisi.                                                                                                                                     |
| replaceText    | Metin  | Sorgu                      | Belirtilen aralıkta `searchText` metninin tüm geçişlerini değiştirecek metin dizisi.                                                                                                                      |
| worksheet      | Metin  | Sorgu                      | _(İsteğe bağlı)_ Bul ve değiştir işlemisinin yapılacağı çalışma sayfasının adı. Atlanırsa işlem ilk çalışma sayfasına uygulanır.                                                                             |
| cellArea       | Metin  | Sorgu                      | _(İsteğe bağlı)_ Metin aramasının ve değiştirmenin yapılacağı belirli hücre aralığı (örn. `"A1:D20"`, `"B5:F15"`). Atlanırsa işlem belirtilen çalışma sayfasındaki tüm kullanılmış hücrelere uygulanır.          |
| region         | Metin  | Sorgu                      | _(İsteğe bağlı)_ Metin işleme için yerel ayarı ayarlar; bu, arama işlemlerinde büyük/küçük harf duyarlılığını ve karakter kodlamasını etkileyebilir (örn. `"en-US"`, `"fr-FR"`).                           |
| password       | Metin  | Sorgu                      | _(İsteğe bağlı)_ Yüklenecek elektronik tablo dosyası parola korumalıysa, dosyayı açıp işlemek için parolayı belirtin.                                                                                       |

### **Yanıt**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Yanıt, güncellenmiş çalışma kitabını içeren ikili bir akıştır. Uygun dosya uzantısıyla (örn. `.xlsx`) kaydedin.

### **Hata Kodları**

- **400 Bad Request** – Geçersiz Aspose.Cells Cloud API URI’si veya hatalı parametreler.
- **401 Unauthorized** – Geçersiz veya eksik erişim belirteci; yeni bir belirteç alın.
- **404 Not Found** – Elektronik tablo dosyasına erişilemiyor veya belirtilen çalışma sayfası mevcut değil.
- **500 Server Error** – Elektronik tablo işlemesi sırasında iç bir hata oluştu; sorun devam ederse destek ekibiyle iletişime geçin.

## Elektronik Tablo İçeriğini Değiştir API’si nerede kullanılmalı?

- **Yerel Excel dosyalarının toplu işlenmesi** – Yerel olarak depolanan birçok çalışma kitabında otomatik bul ve değiştir işlemi yapın.
- **Yerel veri işlem hatları** – Raporlar arşivlenmeden veya dağıtılmadan önce değiştirilmesi için API’yi zamanlanmış işlere entegre edin.
- **Yerel rapor oluşturma** – Buluta yüklemeden şablon çalışma kitaplarına dinamik olarak değerler ekleyin.

## Elektronik Tablo İçeriğini Değiştir API’si neden kullanılmalı?

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve hızlı geliştirme ile kapsamlı belgeler sağlar. Özel çözümler geliştirmeye kıyasla önemli ölçüde geliştirme çabasını azaltır.
- **Düşük İşgücü Maliyeti** – Elle belge birleştirme yapan özel personel ihtiyacını azaltır.
- **Kullanım Ücretli** – Ön ödeme gerektirmez; yalnızca kullandığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti** – Bakımı yapılacak sunucu yok, yazılım güncellemesi yok, uyumluluk sorunu yok.
- **Karmaşık Excel formatlamasını korur** – Değiştirme işleminden sonra orijinal çalışma kitabının formatı, formülleri ve grafikleri aynen kalır.

## SDK’lar ile Elektronik Tablo İçeriğini Değiştir API’si Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent), web tarayıcısından doğrudan REST etkileşimlerinde bulunabilmeniz için herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, gelişimi hızlandırmanın en hızlı yoludur. SDK, alttaki detayları yönetir; böylece minimum kodla içerik değiştirme işlemlerini gerçekleştirebilirsiniz. Desteklenen dillerin tam listesi için resmi **Aspose.Cells Cloud SDK GitHub** deposuna bakın.

Aşağıdaki kod örnekleri, farklı SDK’larla Aspose.Cells web servislerine nasıl bağlanılacağını gösterir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}