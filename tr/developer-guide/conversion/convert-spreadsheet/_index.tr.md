---
title: "Aspose.Cells Cloud Web API - Elektronik Tabloyu Başka Bir Formata Dönüştür - Ücretsiz Çevrimiçi Araç"
secondtitle: "Belge"
articletitle: "Elektronik Tabloyu Başka Bir Formata Nasıl Dönüştürürsünüz: Adım Adım Kılavuz"
linktitle: "Elektronik Tabloyu Dönüştür"
type: docs
url: /tr/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, elektronik tablo dönüştürme, Excel'den PDF'e, Excel API'si, bulut dosya dönüştürme"
description: "Aspose.Cells Cloud API'sini kullanarak bir elektronik tablo dosyasını başka bir formata dönüştürün."
weight: 100
---

Bir yerel elektronik tablo/Excel dosyasını Aspose.Cells Cloud Web API'si ile başka bir formata dönüştürün.

## **Elektronik Tabloyu Dönüştür API'si**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı  | Tür    | Yol/Sorgu Dizisi/HTTPBody | Açıklama                                                                                     |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------- |
| Elektronik Tablo | Dosya | FormData                   | Dönüştürülecek elektronik tablo dosyasını yükleyin.                                           |
| format         | String | Sorgu                      | (Gerekli) İstenen çıktı formatı (örneğin, “XLSX”, “PDF”, “CSV”).                             |
| outPath        | String | Sorgu                      | (İsteğe bağlı) Dönüştürülmüş çalışma kitabının kaydedileceği klasör yolu. Varsayılan değer null'dır. |
| outStorageName | String | Sorgu                      | Çıktı dosyası için bir depo adı belirtin.                                                     |
| fontsLocation  | String | Sorgu                      | Elektronik tablo için özel yazı tiplerini kullanın.                                           |
| region         | String | Sorgu                      | Elektronik tablonun bölgesel ayarını belirtin.                                                |
| password       | String | Sorgu                      | Dosya korumalıysa elektronik tablo dosyasını açmak için şifre.                                |

### **Yanıt**

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

**Başarılı durum kodu**

- **200 OK** – Dönüştürme işlemi başarılı oldu ve yanıt gövdesi dönüştürülen dosya akışını içerir.
- `Content-Type` başlığı, istenen çıktı formatının MIME türünü yansıtır (örneğin, PDF için `application/pdf`).

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400  | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz) | Geçersiz veya eksik JWT belirteci.                                |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklü dosya boyut sınırını aşıyor.                              |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                     |

## Formatlar

| **Çıktı Formatı**                                                                                      | **Açıklama**                                                                                                                 |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 - 2003 Çalışma Kitabı.                                                                                          |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Office Open XML Elektronik Tablo ML Dosya Formatı.                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel İkili Çalışma Kitabı.                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Excel Makro Etkinleştirilmiş Çalışma Kitabı.                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 - Excel 2003 Şablonu.                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel Şablonu.                                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Excel Makro Etkinleştirilmiş Şablon.                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Excel'e yeni işlevler eklemek için kullanılan Excel Makro Etkinleştirilmiş Eklenti dosyası.                                  |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV (Virgülle Ayrılmış Değer) dosyası.                                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV (Sekme ile Ayrılmış Değerler) dosyası.                                                                                    |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | Ayrımcılı metin dosyası.                                                                                                     |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML formatı.                                                                                                                |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML dosyası.                                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS (OpenDocument Elektronik Tablo).                                                                                         |
| SpreadsheetML                                                                                          | Excel 2003 XML dosyası.                                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Belge, Apple’ın macOS ve iOS için iWork paketinin bir parçası olan “Numbers” uygulaması tarafından oluşturulmuştur.           |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript Nesne Gösterimi.                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Veri Değişim Formatı.                                                                                                        |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | .dbf uzantılı dosya, dBASE veritabanı yönetim sistemi tarafından kullanılan bir veritabanı dosyasıdır.                       |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Taşınabilir Belge Formatı.                                                                                             |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML Kağıt Spesifikasyonu formatı.                                                                                            |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Ölçeklenebilir Vektör Grafikler formatı.                                                                                     |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Etiketli Görüntü Dosyası Formatı.                                                                                            |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Taşınabilir Ağ Grafikleri formatı.                                                                                           |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Bitmap Görüntü formatı.                                                                                                      |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Geliştirilmiş Meta Dosyası formatı.                                                                                          |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG, kayıplı sıkıştırma kullanılarak kaydedilen bir görüntü formatıdır.                                                     |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Grafik Değişim Formatı.                                                                                                      |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Markdown belgesini temsil eder.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | OpenOffice ve StarOffice tarafından kullanılan XML tabanlı bir formattır.                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | Düz XML olarak depolanan bir Open Document formatıdır.                                                                       |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Microsoft Word belgeleri için yaygın kullanılan bir formattır; XML ve ikili dosyaları birleştirir.                            |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | PPTX formatı, Microsoft PowerPoint Open XML sunum dosyası formatına dayanır.                                                 |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Yapılandırılmış Sorgu Dili.                                                                                                  |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML, HTML 4.0’ın yeniden formülleştirilmesini kullanan XML tabanlı bir işaretlemeli metin dosyası formatıdır.             |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | .epub uzantılı dosyalar, yayıncılar ve tüketiciler için standart bir e-kitap formatıdır.                                      |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML, Extensible Markup Language (Genişletilebilir İşaretleme Dili) kısaltmasıdır; HTML benzerdir ancak nesneleri tanımlamak için etiketler kullanır. |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document Şablon Elektronik Tablo (OTS) dosyası.                                                                         |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW, Amazon tarafından Kindle cihazları için geliştirilen bir dijital e-kitap dosya formatıdır. AZW3, diğer adıyla Kindle Format 8 (KF8). |

## Elektronik Tabloyu Dönüştür API'si nerede kullanılmalıdır?

- **Eski Sistem Geçişi**: Modern sistemler için binlerce eski XLS dosyasını XLSX'e dönüştürün.
- **Arşiv Standartlaştırma**: Arşivleme amacıyla çeşitli elektronik tablo formatlarını (XLS, XLSM, ODS, CSV) tek bir formata dönüştürün.
- **Ofis Uygulama Uyumluluğu**: Excel dosyalarını LibreOffice, Google Tablolar veya Apple Numbers ile uyumlu formatlara dönüştürün.
- **Veri Kaynağı Standardizasyonu**: Veritabanı işlemesi için çeşitli elektronik tablo formatlarını CSV veya JSON'a dönüştürün.
- **Web Yayınlama**: Finansal modelleri web gösterimi için HTML’e dönüştürün.

## Elektronik Tabloyu Dönüştür API'si neden kullanılmalıdır?

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı dokümantasyonla birlikte gelir. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında, geliştirme yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önceden yüklemeye gerek kalmadan tablo verilerini dönüştürebilirsiniz; bu da depolama alanını tasarruf eder ve maliyetleri düşürür.
- **Kapsamlı Format Desteği**: 20'den fazla elektronik tablo formatı arasında dönüştürme yapın.
- **Veri Sadeliğini ve Biçimlendirmeyi Korur.**

## Elektronik Tabloyu Dönüştür API'si SDK’lar ile Nasıl Kullanılır?

Aşağıdaki kod örnekleri, Elektronik Tabloyu Dönüştür API'sini çeşitli SDK’larla nasıl kullanacağınızı göstermektedir.

### Elektronik Tabloyu Dönüştür API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">Elektronik Tabloyu Dönüştür API Spesifikasyonu</a>, web tarayıcınızdan doğrudan REST etkileşimlerinde bulunabilmeniz için herkese açık bir programlama arayüzü tanımlar.

Aspose.Cells web servislerine kolayca ulaşmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tablo dosyasını başka bir formata dönüştürmek için kısa kodla hızlı geliştirme yapmanın en hızlı yoludur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Elektronik Tabloyu Dönüştür",
  "description": "Aspose.Cells Cloud kullanarak bir elektronik tablo dosyasını başka bir formata dönüştürün.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Elektronik tabloyu belirtilen formata dönüştürün."
    }
  ]
}
</script>

---