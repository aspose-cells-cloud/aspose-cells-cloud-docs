---
title: "Excel Çalışma Sayfasına Satır Ekleme"
second_title: "Belge"
linktitle: "Ekle"
type: docs
url: /rows/add/
keywords: "Aspose.Cells, satır ekleme, Excel API'si, REST, C#, Java, Python, Node.js"
description: "Aspose.Cells Cloud REST API kullanarak tek veya birden fazla satırı bir Excel çalışma sayfasına ekleme adımlı kılavuz ve C#, Java, Python ve Node.js için kod örnekleri."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Sayfasına Satır Ekleme – Adım Adım Kılavuz"
---

## Excel Çalışma Sayfasına Satır Nasıl Eklenir?

Bu makale, Aspose.Cells Cloud REST API kullanarak mevcut bir çalışma sayfasına tek bir boş satır veya birden fazla satır ekleme yöntemini açıklar. İşleme geçmeden önce geçerli bir API anahtarına ve uygun SDK'nın kurulmuş olduğundan emin olun.

**Ön Gereksinimler**  
- [ ] Etkin aboneliğe sahip Aspose.Cells Cloud hesabı.  
- [ ] Aspose Cloud panosundan oluşturulmuş API anahtarı/Erişim belirteci.  
- [ ] Desteklenen SDK'lerden birinin (C#, Java, Python, Node.js) kurulmuş ve yapılandırılmış olması.  

**API Referansı**  
- **HTTP Yöntemi:** `POST`  
- **Uç Nokta:** `https://api.aspose.cloud/v3.0/cells/{dosyaAdı}/worksheets/{sayfaAdı}/rows`  
- **Gerekli Yol Parametreleri:**  
  - `fileName` – Bulutta depolanan Excel dosyasının adı.  
  - `sheetName` – Satırların ekleneceği çalışma sayfasının adı.  
- **Sorgu Parametreleri:**  
  - `startrow` – Ekleme işleminin başlayacağı satırın sıfır tabanlı indeksi.  
  - `totalRows` – Eklenecek satır sayısı.  
  - `folder` – (İsteğe bağlı) Dosyanın bulunduğu bulut klasör yolu.  
  - `storage` – (İsteğe bağlı) Varsayılan olmayan bir depolama alanı kullanılıyorsa depolama adı.  
- **İstek Gövdesi (JSON örneği):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **cURL örneği**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **Başarılı Yanıt (HTTP 200):** Güncellenmiş çalışma sayfası bilgilerini, yeni satır sayısını dahil ederek döndürür.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Hata Yanıt Örneği (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "Geçersiz startrow parametresi. Pozitif bir tam sayı olmalıdır."
  }
  ```

- **Durum Kodları:**  

  | Kod | Anlam                                |
  |-----|--------------------------------------|
  | 200 | Satırlar başarıyla eklendi           |
  | 400 | Geçersiz parametreler veya bozuk JSON |
  | 401 | Kimlik doğrulama başarısız           |
  | 404 | Dosya veya çalışma sayfası bulunamadı |
  | 500 | Sunucu hatası                        |

Aşağıda, satır eklemeyle ilgili ayrıntılı örneklerin hızlı bağlantıları yer almaktadır:

- [Excel çalışma sayfasına boş bir satır ekleme](/cells/rows/add/row/)
- [Excel çalışma sayfasına birden fazla satır ekleme](/cells/rows/add/rows/)
---