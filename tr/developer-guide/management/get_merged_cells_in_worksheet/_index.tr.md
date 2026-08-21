---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Çalışma Sayfasında Birleştirilmiş Hücreleri Al – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /tr/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, birleştirilmiş hücreler, çalışma sayfası, API"
description: "Yerel bir elektronik tablo çalışma sayfasından tüm birleştirilmiş hücre alanlarını alın."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin Çalışma Sayfasında Birleştirilmiş Hücreleri Alma Özelliği

Yerel bir elektronik tablo çalışma sayfasından tüm birleştirilmiş hücre alanlarını alın.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | Dosya | FormData | Elektronik tablo dosyasını yükleyin. |
| worksheet | Dize | Sorgu | Çalışma sayfası adı. |
| region | Dize | Sorgu | Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirmesini, tarih ayrıştırmasını ve yerel ayara özel davranışları etkiler. |
| password | Dize | Sorgu | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| Yok | Yok | Bu işlem JSON gövdesi kabul etmez; elektronik tablo dosyası `multipart/form-data` üzerinden gönderilir. |

### **Yanıt**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|-------|----------|
| 200 | Tamam | Birleştirilmiş hücre alanları başarıyla alındı. |
| 400 | Geçersiz İstek | Bir veya daha fazla istek parametresi geçersiz veya eksik. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız – geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük | Yüklenen elektronik tablo izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Sunucuda beklenmeyen bir hata oluştu. |

## Çalışma Sayfasında Birleştirilmiş Hücreleri Alma'yı SDK’lar ile Nasıl Kullanırız

### Çalışma Sayfasında Birleştirilmiş Hücreleri Alma Spesifikasyonu

[Çalışma Sayfasında Birleştirilmiş Hücreleri Alma API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye istek nasıl yapılır gösterir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=tr-TR&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek atıldığını gösterir:
 `[TBD]`
---