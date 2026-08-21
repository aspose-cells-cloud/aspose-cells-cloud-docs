---
title: "Aspose.Cells Cloud AI – Kullanıcı Görevini Parçalama API’si (v4.0) | SMART Görev Planlama"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud AI Görev Parçalama API’si ile Kullanıcı Hedeflerini Sıralı Eylem Planlarına Nasıl Dönüştürebilirsiniz?"
linktype: "Decompose User Task"
type: docs
url: /tr/decompose-user-task/
keywords: "Aspose.Cells AI, görev parçalama API’si, SMART görev planlama, Redmine içe aktarma, proje otomasyonu"
description: "Aspose.Cells Cloud AI ile serbest metin hedefleri, SMART kriterlerine uygun ve saat bazlı tahminler içeren görev listelerine dönüştürün. Redmine, Jira veya Azure DevOps için tek bir PUT isteğiyle CSV/XLSX çıktısı alın."
weight: 100
---

**DecomposeUserTask** uç noktası, kullanıcı tarafından tanımlanan serbest metin görev açıklamasını, SMART kriterlerine uygun şekilde detaylı ve sıralı bir eylem planına dönüştüren bir REST uç noktasıdır. Saat bazlı süre tahminlerini otomatik olarak atar, çıktıyı Redmine ile uyumlu içe aktarma formatına dönüştürür ve proje aşamaları (milestone) düğümlerini oluşturur. Sadece ham görev listesi ve isteğe bağlı süre tahminlerini sağlarsanız, API doğrudan proje yönetim araçlarına aktarılabilir bir dosyayı (CSV, XLSX vb.) doğrudan döndürür; böylece görev分解’yi otomatikleştirir ve manuel çabayı azaltır.

## **Kullanıcı Görevini Parçalama API’si**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı     | Tür     | Konum | Gerekli / İsteğe Bağlı | Açıklama                                                                                                                                                                                                                              |
| :---------------- | :------ | :---- | :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| TaskDescription   | string  | Gövde | Gerekli                | Kullanıcının genel hedefinin düz metin olarak açıklaması. Hizmet açıklamayı ayrıştırır ve bireysel görevler oluşturur. Örnek: “3. çeyrek için pazarlama kampanyası başlatın, içerik oluşturma, e-posta gönderimi ve sosyal medya reklamlarını içerir.” |

### **Yanıt**

Başarılı yanıt (200 OK)  
Content-Type: `application/octet-stream` (ikili dosya akışı)

Başlıklar:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <bayt cinsinden boyut>`

Aynı yapı XLSX/ODS formatları için de kullanılır; sütunlar ilk çalışma sayfasına yerleştirilir.

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Bad Request           | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized          | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Payload Too Large     | Yüklenen dosya boyut sınırnını aşıyor.                            |
| 500 | Internal Server Error | Beklenmeyen sunucu hatası.                                        |

**Hata Yanıt Örneği (400 Bad Request)**

```json
{
  "code": "InvalidParameter",
  "message": "'TaskDescription' alanı gerekli olup boş bırakılamaz."
}
```

**Örnek İstek Gövdesi (JSON)**

```json
{
  "TaskDescription": "Mevcut sistemde görev bölme özelliği için bir web API’si geliştirin."
}
```

**Örnek Yanıt**  
API, oluşturulan dosyayı içeren ikili bir akış döndürür. Bir CSV yanıtının ilk birkaç satırını önizlemek için akışı çözümler ve başlık satırını görüntüleyebilirsiniz; örneğin:

```
ID,Subject,Trucker,Estimated Duration,Description
1	Görev bölme API’si için gereksinim toplama	Business Analyst	8	Yeni görev bölme uç noktası için işlevsel ve işlevsel olmayan gereksinimleri, kullanıcı hikayelerini ve kabul kriterlerini toplayın.
2	API spesifikasyonu (OpenAPI)	Business Analyst	6	POST /tasks/split için OpenAPI sözleşmesini tanımlayın; istek şemasını, yanıt formatlarını, hata kodlarını ve güvenlik gereksinimlerini içerir.
3	Bölme algoritması ve veri modeli tasarımı	Solution Architect	5	Bir üst görevi alt görevlere bölen temel algoritmayı tasarlayın ve hiyerarşiyi ve meta verileri depolamak için veri modelini (veritabanı tabloları / varlıkları) genişletin.
4	Mimari entegrasyon değerlendirmesi	Solution Architect	4	Mevcut hizmetler, olay akışları ve veritabanı geçişleri üzerindeki etkiyi analiz edin; entegrasyon planını oluşturun.
...
```

## Kullanıcı Görevini Parçalama API’si nerede kullanılmalıdır?

- **Proje başlangıcı**: Yüksek seviyeli proje tanımını, saat tahminleriyle birlikte Redmine ile uyumlu görev listesine dönüştürün; böylece hemen sprint planlaması yapılabilir.
- **Pazarlama otomasyonu**: Kampanya hedeflerini yürütülebilir adımlara bölün, CSV olarak dışa aktarın ve ekipler arası koordinasyon için görev yönetim araçlarına aktarın.
- **Kaynak atama**: Her alt görev için saat bazlı tahminler üretin; böylece proje başlamadan önce yöneticiler ekibin iş yükünü dengeleyebilir.
- **Aşama izleme**: Otomatik olarak Gantt çizelgesi araçlarıyla senkronize edilebilecek aşamalar (milestone) düğümleri oluşturun; böylece her fazın net bir teslim edilebilir ürünü olur.

## Kullanıcı Görevini Parçalama API’si neden kullanılmalıdır?

- **SMART uyumlu çıktı**, oluşturulan her görevin Specific (Spesifik), Measurable (Ölçülebilir), Achievable (Ulaşılabilecek), Relevant (İlgili) ve Time-bound (Zaman sınırlı) kriterlerini karşılamasını sağlar.
- **Dahili saat bazlı süre tahmini**, manuel hesaplama gereksinimini ortadan kaldırır ve tahmin doğruluğunu artırır.
- **Hemen içe aktarılabilir dosya formatları** (CSV, XLSX vb.), Redmine, Jira, Azure DevOps ve diğer proje yönetim platformlarıyla entegrasyonu kolaylaştırır.
- **Tek istekli otomasyon**, tek bir istekle görev分解 yaparak proje başlatmayı hızlandırır ve manuel çabayı en aza indirir.

## Kullanıcı Görevini Parçalama API’si Nasıl SDK’larla Kullanılır?

### Kullanıcı Görevini Parçalama API’si Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">Kullanıcı Görevini Parçalama API’si Spesifikasyonu</a>, REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için erişilebilir bir programlama arayüzü sağlar.

## Excel API SDK’si

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak Kullanıcı Görevini Parçalama API’si uç noktasını kısa kodla çağırmaya izin verdiğinden en hızlı gelişim yoludur.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.  
Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetleriyle nasıl etkileşime girileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---