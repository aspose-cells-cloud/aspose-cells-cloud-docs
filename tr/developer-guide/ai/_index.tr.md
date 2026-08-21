---
---
title: "Aspose.Cells Cloud AI – Görev Ayrıştırma, Elektronik Tablo ve Metin Çevirisi"
second_title: "Belge"
ArticleTitle: "Yapay Zeka Becerilerinizi Geliştirin: Excel Çevirisi, Görev Ayrıştırma ve Daha Fazlasını Öğrenin"
linktype: "AI"
type: docs
url: /ai/
keywords: "Aspose.Cells, Bulut AI, Excel çevirisi, görev ayrıştırma, REST API"
description: "Aspose.Cells Cloud AI ile görevleri ayrıştırın, Excel çalışma kitaplarını ve metin dosyalarını çevirin. REST uç noktalarını, örnek kodu ve en iyi uygulamaları içerir."
weight: 20
---

Aspose.Cells Cloud AI, Excel ve metin verileriyle çalışmayı kolaylaştıran üç güçlü yapay zeka tabanlı hizmet sunar: **Kullanıcı Görevini Ayrıştır**, **Elektronik Tabloyu Çevir** ve **Metin Dosyasını Çevir**. Bu API’ler, geliştiricilerin karmaşık kullanıcı hedeflerini uygulanabilir adımlara bölmelerine, tüm çalışma kitaplarını veya düz metin dosyalarını çevirmelerine ve sonuçları özel uygulamalara entegre etmelerine olanak tanır. Hızlı başlamak için aşağıdaki uç noktaları kullanın ve her hizmet için sağlanan ayrıntılı istek/yanıt spesifikasyonlarına başvurun.

- **[Kullanıcı Görevini Ayrıştır](https://docs.aspose.cloud/cells/decompose-user-task/)** – Aspose.Cells Cloud AI ile kullanıcı hedeflerini sıralı eylem planlarına dönüştürün.  
  - **İstek Yöntemi:** `POST`  
  - **Uç Nokta URL’si:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **Başlıklar:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **İstek Gövdesi (JSON):**  
    ```json
    {
      "task": "Grafikler ve pivot tablolar içeren üç aylık satış raporu oluştur"
    }
    ```  
  - **Yanıt:** Görev listesini içeren elektronik tablo dosyasını indirilebilir bir dosya olarak döndürür.  
  - **Durum Kodları:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **Ön Koşullar:** **CellsAI** kapsamına sahip geçerli bir erişim belirteci.  
  - **Örnek Yanıt (JSON parçası):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **Notlar:** Oluşturulan çalışma kitabında, sıralı adımları içeren **TaskList** adlı bir çalışma sayfası bulunur. Hız limiti: dakikada 100 istek.

- **[Elektronik Tabloyu Çevir](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Aspose.Cells Cloud AI ile tüm elektronik tabloyu çevirin.  
  - **İstek Yöntemi:** `POST`  
  - **Uç Nokta URL’si:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **Başlıklar:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **İstek Parametreleri:**  
    - `file` – Çevrilecek Excel dosyası (ikili).  
    - `targetLanguage` – ISO dil kodu (örn. `fr`, `de`).  
  - **Yanıt:** Çevrilmiş çalışma kitabını indirilebilir bir dosya olarak döndürür.  
  - **Durum Kodları:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Ön Koşullar:** **CellsAI** kapsamına sahip erişim belirteci ve yeterli depolama kotası.  
  - **Örnek Yanıt (JSON parçası):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **Notlar:** Tüm hücre değerleri, yorumlar ve sayfa adları çevrilir. Hız limiti: dakikada 100 istek.

- **[Metin Dosyasını Çevir](https://docs.aspose.cloud/cells/translate-text-file/)** – Aspose.Cells Cloud AI ile tüm metin dosyasını çevirin.  
  - **İstek Yöntemi:** `POST`  
  - **Uç Nokta URL’si:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **Başlıklar:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **İstek Parametreleri:**  
    - `file` – Çevrilecek metin dosyası (ikili).  
    - `targetLanguage` – ISO dil kodu (örn. `es`, `ja`).  
  - **Yanıt:** Çevrilmiş metin dosyasını döndürür.  
  - **Durum Kodları:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Ön Koşullar:** **CellsAI** kapsamına sahip geçerli bir erişim belirteci.  
  - **Örnek Yanıt (JSON parçası):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **Notlar:** UTF‑8 kodlu, maksimum 5 MB boyutundaki düz metin dosyalarını destekler. Hız limiti: dakikada 100 istek.