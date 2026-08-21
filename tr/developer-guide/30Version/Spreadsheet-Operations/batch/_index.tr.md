---
title: "Excel dosyalarının toplu işlenmesi: Dönüştür, Kilitle, Korumalı Yap, Böl ve Kilidini Kaldır"
second_title: "Belge"
linktitle: "Toplu Excel dosyaları"
type: docs
url: /tr/batch/
keywords: "Toplu işleme, Excel, dönüştürme, kilitleme, koruma, bölme, kilidini kaldırma, Aspose.Cells Cloud API, API referansı, toplu işlemler"
description: "Aspose.Cells Cloud API, birden fazla Excel dosyasının dönüştürme, kilitleme, koruma, bölme ve kilidini kaldırma gibi işlemler için toplu olarak işlenmesini sağlar. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift için SDK desteği ile ayrıntılı API spesifikasyonlarını içerir."
weight: 35
ArticleTitle: "Excel Dosyalarının Toplu İşlenmesi – Aspose.Cells Cloud API ile Dönüştür, Kilitle, Korumalı Yap, Böl ve Kilidini Kaldır"
---

Aspose.Cells Cloud API, tek bir istekte birden fazla Excel dosyası üzerinde yaygın işlemler gerçekleştirmenizi sağlayan toplu işlem uç noktaları sağlar. Aşağıda, her biri için özet API spesifikasyonlarıyla birlikte mevcut toplu işlemlere hızlı bir genel bakış verilmiştir.

- **["Excel Dosyalarını Toplu Dönüştür"](https://docs.aspose.cloud/cells/batch/convert "Excel Dosyalarını Toplu Dönüştür")**  
  *Birden fazla Excel dosyasını tek bir istekte seçilen bir çıktı formatına dönüştürün.*  

  **API Detayları**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Parametreler**  

  | Ad            | Tür      | Açıklama                                       |
  |---------------|----------|------------------------------------------------|
  | files         | file[]   | Dönüştürülecek bir veya daha fazla Excel dosyası. |
  | outputFormat  | string   | İstenen çıktı formatı (örneğin, pdf, csv, html). |
  | storage       | string   | (İsteğe bağlı) Bulut depolama adı.             |

  **Yanıtlar**  

  | Kod  | Açıklama                                    |
  |------|---------------------------------------------|
  | 200  | Dönüştürme başarılı; dosyaları döndürür.    |
  | 400  | Geçersiz parametreler sağlandı.             |
  | 401  | Yetkisiz erişim – eksik veya geçersiz token. |
  | 500  | İç sunucu hatası.                           |

- **["Excel Dosyalarını Toplu Kilitle"](https://docs.aspose.cloud/cells/batch/lock "Excel Dosyalarını Toplu Kilitle")**  
  *Birden fazla Excel dosyasına aynı anda bir şifre ile kilitleme uygulayın.*  

  **API Detayları**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametreler**  

  | Ad       | Tür    | Açıklama                              |
  |----------|--------|---------------------------------------|
  | files    | array  | Dosya tanımlayıcılarının veya URL'lerin listesi. |
  | password | string | Çalışma kitaplarını kilitlemek için kullanılacak şifre. |
  | storage  | string | (İsteğe bağlı) Bulut depolama adı.     |

  **Yanıtlar**  

  | Kod  | Açıklama                                  |
  |------|-------------------------------------------|
  | 200  | Dosyalar başarıyla kilitlendi.           |
  | 400  | Eksik veya geçersiz parametreler.        |
  | 401  | Yetkisiz erişim.                          |
  | 500  | Sunucu hatası.                            |

- **["Excel Dosyalarını Toplu Korumalı Yap"](https://docs.aspose.cloud/cells/batch/protect "Excel Dosyalarını Toplu Korumalı Yap")**  
  *Birden fazla çalışma kitabına koruma ayarları (örneğin, salt okunur, yapı) ekleyin.*  

  **API Detayları**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametreler**  

  | Ad            | Tür    | Açıklama                                            |
  |---------------|--------|-----------------------------------------------------|
  | files         | array  | Dosya tanımlayıcılarının veya URL'lerin listesi.   |
  | protection    | object | Koruma seçenekleri (örneğin, readOnly, structure). |
  | storage       | string | (İsteğe bağlı) Bulut depolama adı.                 |

  **Yanıtlar**  

  | Kod  | Açıklama                                  |
  |------|-------------------------------------------|
  | 200  | Koruma başarıyla uygulandı.               |
  | 400  | Geçersiz istek verisi.                    |
  | 401  | Kimlik doğrulama başarısız oldu.          |
  | 500  | Beklenmeyen sunucu hatası.                |

- **["Toplu Bölme"](https://docs.aspose.cloud/cells/batch/split "Toplu Bölme")**  
  *Büyük Excel çalışma kitaplarını sayfa bazında veya satır aralıklarına göre daha küçük dosyalara bölün.*  

  **API Detayları**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametreler**  

  | Ad          | Tür    | Açıklama                                        |
  |-------------|--------|-------------------------------------------------|
  | files       | array  | Bölünecek dosyalar.                             |
  | splitBy     | string | Kriter: "worksheet" veya "rowRange".            |
  | criteria    | object | Seçilen bölme yöntemi için detaylar.            |
  | storage     | string | (İsteğe bağlı) Bulut depolama adı.              |

  **Yanıtlar**  

  | Kod  | Açıklama                                    |
  |------|---------------------------------------------|
  | 200  | Bölme işlemi tamamlandı; parçaları döndürür. |
  | 400  | Yanlış bölme parametreleri.                  |
  | 401  | Yetkisiz istek.                             |
  | 500  | İşlem hatası.                               |

- **["Toplu Kilidi Kaldır"](https://docs.aspose.cloud/cells/batch/unlock "Toplu Kilidi Kaldır")**  
  *Birden fazla Excel dosyasının şifre korumasını tek bir çağrıda kaldırın.*  

  **API Detayları**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametreler**  

  | Ad       | Tür    | Açıklama                             |
  |----------|--------|--------------------------------------|
  | files    | array  | Kilidi açık dosyaların tanımlayıcılarının veya URL'lerin listesi. |
  | password | string | Dosyaların mevcut şifresi.           |
  | storage  | string | (İsteğe bağlı) Bulut depolama adı.    |

  **Yanıtlar**  

  | Kod  | Açıklama                                   |
  |------|--------------------------------------------|
  | 200  | Dosyaların kilidi başarıyla kaldırıldı.    |
  | 400  | Yanlış şifre veya eksik dosyalar.          |
  | 401  | Yetkisiz erişim.                           |
  | 500  | Sunucu tarafında hata.                     |
---