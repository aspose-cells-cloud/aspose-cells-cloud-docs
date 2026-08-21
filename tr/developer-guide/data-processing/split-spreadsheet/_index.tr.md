---
title: "Aspose.Cells Cloud Excel Web API’i – Excel Dosyasını Yerel Olarak Birden Fazla Dosyaya Bölün ve 30+ Formata Dışa Aktarın"
second_title: "Belge"
ArticleTitle: "Excel Bölme Aracı – Yerel Elektronik Tabloyu 30+ Formatta Dosyalara Bölün"
linktitle: "Elektronik Tabloyu Böl"
type: docs
url: /tr/split-spreadsheet/
keywords: "böl, excel, aspose cells, elektronik tablo API, pdf dışa aktar, csv, json"
description: "Aspose.Cells Cloud API kullanarak bir Excel çalışma kitabını yerel olarak ayrı dosyalara bölün. Buluta yüklemeye gerek kalmadan PDF, CSV, JSON, XLSX, HTML gibi 30+ forma dışa aktarın."
weight: 100
---

Yerel bir Excel çalışma kitabını tamamen ayrı dosyalara bölün — hiçbir bulut depolama alanı gerekmez. Çıktı, PDF, CSV, JSON, ODS ve XPS dahil olmak üzere 30+ dosya formatını destekler.

## **Elektronik Tabloyu Bölme API’si**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı | Tür      | Yol/Sorgu Dizisi/HTTPBody | Açıklama                                                                                                                                                                                                 |
| :------------ | :------- | :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Dosya    | FormData                  | Bölünmesi istenen yerel elektronik tablo dosyası. Desteklenen formatlar arasında XLSX, XLS, ODS, CSV vb. yer alır. Dosya, bulut depolama gerektirmeksizin tamamen sunucu tarafında işlenir.          |
| from          | Tamsayı  | Sorgu                     | Bölme işlemi için başlatılacak çalışma sayfası aralığının sıfır tabanlı başlangıç indeksi (örneğin ilk çalışma sayfası için `0`).                                                                          |
| to            | Tamsayı  | Sorgu                     | Bölme işlemi için sonlandırılacak çalışma sayfası aralığının sıfır tabanlı bitiş indeksi (örneğin `2`, 0, 1 ve 2 numaralı çalışma sayfalarını böler).                                                      |
| outFormat     | Dize     | Sorgu                     | Bölünmüş dosyaların çıktı formatı. `PDF`, `CSV`, `JSON`, `XLSX`, `HTML` gibi 30+ formatı destekler.                                                                                                      |
| outPath       | Dize     | Sorgu                     | _(İsteğe bağlı)_ Bölünmüş çıktı dosyalarının kaydedileceği yerel klasör yolu. Belirtilmezse, dosyalar varsayılan geçici bir konuma kaydedilir.                                                           |
| outStorageName| Dize     | Sorgu                     | Çıktı dosyalarını düzenlemek için depolama tanımlayıcısı. Yerel işleme modunda bu genellikle oturuma dayalı veya kullanıcı tanımlı bir depolama etiketini ifade eder.                                         |
| fontsLocation | Dize     | Sorgu                     | _(İsteğe bağlı)_ PDF veya görüntü formatlarına dışa aktarma sırasında metin işleme doğruluğunu sağlamak için yerel veya özel bir yazı tipi dizini belirtir.                                                 |
| region        | Dize     | Sorgu                     | _(İsteğe bağlı)_ Çıktı dosyalarındaki sayı, tarih ve para birimi formatlaması için yerel ayarı belirler (örneğin `"en-US"`, `"de-DE"`).                                                                     |
| password      | Dize     | Sorgu                     | _(İsteğe bağlı)_ Yüklenen elektronik tablo parola korumalıysa, dosyayı açıp işlemek için parolayı sağlayın.                                                                                                |

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

Dosya, `outPath` tarafından belirtilen konumdan doğrudan indirilebilir veya oraya kaydedilebilir.

**Başarılı yanıt detayları**

| Durum Kodu | İçerik Türü                | Açıklama                                 |
| ---------- | -------------------------- | ---------------------------------------- |
| 200 OK     | `application/octet-stream` | Birleştirilmiş çalışma kitabının ikili akışı. |

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.      |
| 400 | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                        |

## **Elektronik Tabloyu Bölme API’si Nerede Kullanılmalı?**

- **Bölüm Verisi Dağıtımı**: Birden fazla bölümün verilerini içeren tek bir çalışma kitabını bölüm bazlı ayrı dosyalara bölün.
- **Bölgelere Göre Rapor Dağıtımı**: Ulusal satış raporlarını ayrı bölgeler için rapor dosyalarına bölün.
- **Müşteri Verisi Maskeleme Dağıtımı**: Hassas bilgiler içeren bir çalışma kitabını, müşteri görünümüne uygun bir dosyaya bölün.
- **Periyodik Rapor Bölme**: Özet raporları aylık olarak otomatik olarak haftalık veya günlük raporlara bölün.
- **Çoklu Format Dağıtımı**: Tek bir Excel dosyasını aynı anda PDF, CSV, JSON vb. gibi birden fazla format sürümüne bölün.
- **Şablonlu Bölme**: Veri dosyalarını önceden tanımlanmış şablonlara göre standart çıktı dosyalarına bölün.
- **Veri Kaynağı Ön İşleme**: Veritabanına yüklemeden önce Excel dosyasını standart bir CSV dosyasına bölün.
- **API Verisi Hazırlama**: Büyük veri setlerini API aktarımı için uygun daha küçük parçalara bölün.

## **Elektronik Tabloyu Bölme API’si Neden Kullanılmalı?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; hızlı geliştirme sağlar ve kapsamlı belgeler sağlar. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında, geliştirme iş yükünü önemli ölçüde azaltır.
- **Düşük İş Gücü Maliyeti**: Belge birleştirme için özel görevlendirilmiş pozisyonlara olan ihtiyacı azaltır.
- **Ödeme-her-kullandığınızda**: Ön ödeme gerekmez; yalnızca gerçekten kullanılan API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti**: Sunucuları bakım yapmaya, yazılımları güncellemeye veya uyumluluk sorunlarıyla uğraşmaya gerek yoktur.
- **Karmaşık Excel formatlamasını evrensel olarak erişilebilir PDF formatında korur.**

## **SDK’lar ile Elektronik Tabloyu Bölme API’si Nasıl Kullanılır?**

### Elektronik Tabloyu Bölme API Spesifikasyonu

[Elektronik Tabloyu Bölme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet), doğrudan bir web tarayıcısından REST etkileşimlerini gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tabloyu kısa kodla ayrı dosyalara bölmenizi sağlayan en hızlı geliştirme yöntemidir.  
Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}