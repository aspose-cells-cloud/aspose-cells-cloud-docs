---
title: "Grafiğin Kategori Ekseni Güncelleme"
type: docs
url: /tr/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart, Category Axis, REST API, Excel, Cloud SDK"
description: "Aspose.Cells Cloud REST API kullanılarak bir Excel çalışma sayfasındaki bir grafiğin kategori eksenini günceller."
ArticleTitle: "Grafiğin Kategori Ekseni Güncelleme – Aspose.Cells Cloud API"
---

Bu REST API, bir grafiğin kategori eksenini günceller.

## PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama |
| -------------- | -------- | ------ | -------- |
| name           | string   | path   | Excel dosyasının adı. |
| sheetName      | string   | path   | Grafiğin bulunduğu çalışma sayfasının adı. |
| chartIndex     | integer  | path   | Güncellenecek grafiğin sıfır tabanlı dizini. |
| axis           | object   | body   | Kategori ekseninin özelliklerini tanımlayan JSON nesnesi. |
| folder         | string   | query  | Dosyanın bulunduğu bulut depolama klasörü (isteğe bağlı). |
| storageName    | string   | query  | Depolama adı (isteğe bağlı). |

**İstek Gövdesi Şeması – `axis` nesnesi**

| Özellik | Tür      | Açıklama |
|---------|----------|----------|
| IsAutomaticMajorUnit | boolean | Ana birimin otomatik olarak hesaplanıp hesaplanmadığını belirler. |
| MajorUnit | number | `IsAutomaticMajorUnit` değeri `false` olduğunda ana birimin değeri. |
| IsAutomaticMinorUnit | boolean | İkincil birimin otomatik olarak hesaplanıp hesaplanmadığını belirler. |
| MinorUnit | number | `IsAutomaticMinorUnit` değeri `false` olduğunda ikincil birimin değeri. |
| Title | object | Eksen için başlık ayarları (örneğin, `Text`, `Font`, `Visible`). |
| TickLabelPosition | string | Tikel etiketlerin konumu (örneğin, `Low`, `High`, `NextToAxis`). |
| ... | ... | API spesifikasyonunda tanımlanan ek eksen özellikleri. |

**HTTP Durum Kodları**

| Kod | Anlam                     | Açıklama                                      |
|-----|---------------------------|-----------------------------------------------|
| 200 | OK (Tamam)                | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (İstek Gövdesi Çok Büyük) | Yüklenecek dosya boyut sınırlarını aşar. |
| 500 | Internal Server Error (Sunucu İç Hatası) | Beklenmeyen sunucu hatası. |

**Ön Koşullar / Kimlik Doğrulama**

Bu uç noktayı çağırmak için Aspose.Cells Cloud kimlik doğrulama hizmetinden (`/connect/token`) bir JWT erişim belirteci almanız ve belirteci aşağıdaki örnekte gösterildiği gibi `Authorization` başlığında dahil etmeniz gerekir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Örnek Yanıt**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis), herkese açık bir erişilebilir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

### Notlar

* Uç nokta HTTPS gerektirir; HTTP kullanılması tarayıcılarda karışık içerik uyarılarına neden olabilir.
* Tüm yer tutucu değerler (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) gerçek tanımlayıcılarla değiştirilmelidir.
* Kategori eksenini güncelleme için desteklenen grafik türleri API referansında listelenmiştir.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye ayrıntıları işler ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istekte bulunulacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}
---