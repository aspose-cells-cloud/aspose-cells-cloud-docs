---
title: "Aspose.Cells Cloud – Elektronik Tablo Verilerini Birleştir, Böl ve İçe Aktar"
second_title: "Belge"
ArticleTitle: "Elektronik Tablo Verisi İşleme – Birleştir, Böl ve İçe Aktar"
linktitle: "Veri İşleme"
type: docs
url: /tr/data-processing/
keywords: "Aspose.Cells Cloud, elektronik tablo verisi işleme, Excel birleştirme, Excel bölme, CSV içe aktarma, JSON içe aktarma, API"
description: "Aspose.Cells Cloud REST API kullanarak CSV/JSON verilerini içe aktarma, uzaktaki Excel çalışma kitaplarını birleştirme ve büyük elektronik tabloları bölme konusunda detaylı kılavuz; istek/yanıt örnekleri de dahil."
weight: 30
---

**Aspose.Cells Cloud** – Excel dosyalarını bulutta programlı olarak işlemeyi sağlayan bir RESTful hizmettir. Birden fazla formattan veri içe aktarmayı, çalışma kitaplarını birleştirmeyi ve büyük elektronik tabloları bölmeyi destekler.

**Aspose.Cells Cloud API**’nin **Veri İşleme** bölümü, elektronik tablo verilerini programlı olarak içe aktarmanıza, birleştirmenize ve bölmenize olanak tanır. Aşağıdaki uç noktaları kullanarak CSV/JSON içe aktarmalarını yönetebilir, çalışma kitaplarını birleştirebilir veya büyük dosyaları yönetilebilir parçalara bölebilirsiniz.

## Veri İçe Aktarma ve Yönetimi

- **[CSV, JSON, XML verilerini Excel dosyalarına içe aktarın](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

İçe aktarma işlemi CSV, JSON veya XML yüklerini kabul eder ve hedef çalışma kitabında yeni bir çalışma sayfası oluşturur (veya mevcut birini günceller).

**Uç nokta ayrıntıları**

| HTTP Yöntemi | Uç Nokta | İstek Gövdesi | Başarılı Yanıt |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{dosyaAdı}/import` | `application/json` veya `text/csv` (biçime göre) | JSON içeren `200 OK`; güncellenmiş çalışma kitabı meta verileri |
| GET | `https://api.aspose.cloud/v3.0/cells/{dosyaAdı}?format=excel` | *hiçbiri* | İşlenmiş çalışma kitabı dosyasını döndürür |

**Örnek cURL isteği (CSV içe aktarma)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {erişim_belirteci}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Örnek JSON yanıtı**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Önkoşullar**: OAuth2 erişim belirteci gereklidir. Kaynak dosya, Aspose Cloud depolama alanına yerleştirilmeli veya çok parçalı yükleme yoluyla sağlanmalıdır.

## Dosya Birleştirme İşlemi

- **[Uzaktaki Excel Dosyalarını Belirtilen Çalışma Kitabına Birleştirin](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Birden Fazla Excel Dosyasını Tek Bir Çalışma Kitabına Birleştirin](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Uzaktaki Bir Klasördeki Eşleşen Excel Dosyalarını Birleştirin](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

Birleştirme, iki veya daha fazla çalışma kitabını tek bir hedef çalışma kitabında birleştirir. API, açık dosya listelerini ve depo klasöründeki desen tabanlı birleştirmeleri destekler.

**Uç nokta ayrıntıları**

| HTTP Yöntemi | Uç Nokta | Parametreler | Başarılı Yanıt |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (dosya adları dizisi), `target` (isteğe bağlı hedef çalışma kitabı adı) | `200 OK` ile birleştirilmiş çalışma kitabını açıklayan JSON |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` ile birleştirilmiş çalışma kitabı meta verileri |

**Örnek cURL isteği (açık liste birleştirme)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {erişim_belirteci}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Örnek JSON yanıtı**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Önkoşullar**: Tüm kaynak çalışma kitapları aynı bulut depolama konumunda bulunmalı ve istekte bulunan kişinin okuma/yazma izinleri olmalıdır.

## Dosya Bölme İşlemi

- **[Bir Excel Dosyasını Çalışma Sayfalarına Göre Birden Fazla Dosyaya Bölün](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Excel Dosyasını Özel Kurallara Göre Bölün](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

Bölme, bireysel çalışma sayfalarını veya satır/sütun gruplarını ayrı çalışma kitabları dosyalarına çıkarır.

**Uç nokta ayrıntıları**

| HTTP Yöntemi | Uç Nokta | Parametreler | Başarılı Yanıt |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{dosyaAdı}/split` | `splitBy` (örneğin, `worksheet`), `outputFolder` | `200 OK` ile oluşturulmuş dosya URL’lerinin listesi |
| POST | `https://api.aspose.cloud/v3.0/cells/{dosyaAdı}/split/custom` | Özel kural JSON’u (sayfa boyutu, satır aralığı vb.) | `200 OK` ile bölünmüş dosyaların ayrıntıları |

**Örnek cURL isteği (çalışma sayfasına göre bölme)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {erişim_belirteci}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Örnek JSON yanıtı**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Önkoşullar**: Kaynak çalışma kitabının Aspose Cloud depolama alanında erişilebilir olması ve istekte bulunan kişinin hedef klasör için yazma izni olması gerekir.