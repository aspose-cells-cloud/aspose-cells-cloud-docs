---
title: "Hesap Tablosu İşlemleri"
second_title: "Belge"
type: docs
url: /spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, hesap tablosu işlemleri, otomatik sığdırma, toplu işleme, dosya koruma, dönüştürme, içe aktarma ve dışa aktarma, metin işleme"
description: "Aspose.Cells Cloud REST API’sini kullanarak otomatik sığdırma, toplu dönüştürme, koruma, birleştirme ve bul-değiştir gibi hesap tablosu işlemlerini nasıl gerçekleştireceğinizi öğrenin. Kapsamlı kullanım notları ve kod örneği yönlendirmeleri içerir."
weight: 100
ArticleTitle: "Hesap Tablosu İşlemleri – Aspose.Cells Cloud API Kılavuzu"
---

Hesap Tablosu İşlemleri, **Aspose.Cells Cloud** (v3.0) ile Excel çalışma kitapları üzerinde gerçekleştirebileceğiniz en yaygın işlemlere hızlıca ulaşmanızı sağlayan özet bir rehber sunar. Sütunları otomatik sığdırmak, dosyaları toplu işlemek, çalışma sayfalarını korumak veya metinleri işlemek gibi ihtiyaçlarınız olsun, REST API, Python, C# ve Java gibi dillerde çalışan özel uç noktalar sunar. Aşağıdaki liste, her işlem için detaylı belgelerin bağlantılarını içerir ve hızlıca başlamanıza yardımcı olacak kısa kullanım notları sağlar.

**Önkoşullar**: Bu uç noktaları çağırmak için geçerli bir Aspose.Cells Cloud API anahtarına sahip olmalı ve `Authorization` başlığını (`Bearer <erişim-anahtarı>`) eklemelisiniz. Örnekler API sürümü v3.0 varsayımını temel alır.

- **[Otomatik Sığdırma Seçenekleri](/cells/auto-fitter-options/)** – Sütun genişliklerini ve satır yüksekliklerini otomatik olarak ayarlar. `POST /cells/{dosya}/worksheets/{sayfa}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Excel dosyaları üzerinde toplu işlem: dönüştürme, kilitleme, koruma, bölme ve kilitsiz hale getirme](/cells/batch/)** – Tek bir istekte en fazla 100 dosya üzerinde toplu işlemler (dönüştürme, kilitleme, koruma, bölme, kilitsiz hale getirme) gerçekleştirin. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Excel Dosyalarını Sıkıştırma ve Onarım](/cells/compress-and-repair-excel-files/)** – Dosya boyutunu küçültür ve yapısal sorunları giderir. `POST /cells/{dosya}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {erişim-anahtarı}
  ```
- **[Excel Dosyasını Başka Bir Formata Dönüştürme veya Farklı Kaydetme](/cells/conversion-and-save-as/)** – Excel’i PDF, CSV, HTML vb. formatlara dönüştürün veya çıktı formatını değiştirin. `GET /cells/{dosya}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {erişim-anahtarı}
  ```
- **[Çalışma Kitabını Dönüştürme Seçenekleri](/cells/convert-workbook-options/)** – Sayfa boyutu, oluşturma seçenekleri ve şifre koruması gibi dönüştürme ayarlarını ince ayarla yapın. `POST /cells/{dosya}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Excel Dosyaları Oluşturma ve Excel Raporları Hazırlama](/cells/creating-files-and-reports/)** – Yeni çalışma kitaplarını sıfırdan veya şablonlardan oluşturun. `PUT /cells/{yeniDosya}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[Veriyi Excel Dosyalarına İçe Aktarma ve Excel Dosyalarından Veri Dışa Aktarma](/cells/data-import-and-export/)** – CSV, JSON veya veritabanlarından veri yükleyin ve çalışma sayfası verisini dışa aktarın. `POST /cells/{dosya}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Excel Dosyalarını Şifreleme, Şifresini Çözme ve Dijital İmzalama](/cells/protect/)** – Şifre koruması, şifreleme veya dijital imza uygulayın. `POST /cells/{dosya}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[Dosya Bilgisi](/cells/file-info/)** – Boyut, format ve oluşturma tarihi gibi meta verileri alın. `GET /cells/{dosya}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {erişim-anahtarı}
  ```
- **[Excel Dosyalarını Birleştirme ve Bölme](/cells/merge-and-split/)** – Birden fazla çalışma kitabını tek bir dosyada birleştirin veya bir çalışma kitabını ayrı dosyalara bölün. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Excel Dosyalarındaki Metin İçeriğini Bulma ve Değiştirme](/cells/search-and-replace/)** – Çalışma sayfaları boyunca dizgileri bulun ve değiştirin. `POST /cells/{dosya}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[Excel Metin İşleme: Metin Ekleme, Karakterleri Silme, Metni Kırpma, Kelime Büyük/Küçük Harf Güncelleme ve Daha Fazlası](/cells/text-processing/)** – Hücre değerlerinde gelişmiş metin işlemleri gerçekleştirin. `POST /cells/{dosya}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Excel Dosyalarına Su İmzi Ekleme veya Arka Plan Ayarlama](/cells/watermark-and-background/)** – Resim veya metin su imzeleri ekleyin ve çalışma sayfası arka planlarını ayarlayın. `POST /cells/{dosya}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Excel Dosyaları ile Çalışma: Formül Hesaplama, Otomatik Sığdırma, Nesneleri Temizleme vb.](/cells/workbook/)** – Formülleri hesaplama, nesneleri temizleme ve otomatik sığdırma gibi yaygın çalışma kitabı görevlerini yürütün. `POST /cells/{dosya}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {erişim-anahtarı}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```