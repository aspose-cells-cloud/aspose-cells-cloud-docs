---
title: "Sütunları Grupla – Aspise.Cells Bulut API Dokümantasyonu"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki sütunları gruplayın. İstek sözdizimi, parametreler, cURL ve SDK örnekleri ile yanıt detaylarını içerir."
keywords: "Aspose.Cells, sütunları grupla, Excel API, REST, bulut SDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Excel Çalışma Sayfasında Sütunları Gruplama

**API sürümü:** v3.0  
**İşlem:** `PostGroupWorksheetColumns` – Çalışma sayfasındaki sütunları gruplar.

---

## Genel Bakış

Bu REST API, bir çalışma sayfasındaki sütunların bir aralığını gruplamanızı sağlar. Gruplanan sütunlar gösterilebilir veya gizlenebilir; bu sayede Microsoft Excel'deki gibi daraltılabilir bölümler oluşturabilirsiniz.

---

## Ön Gereksinimler

- Aspose Cloud kimlik doğrulama hizmetinden alınmış geçerli bir **JWT erişim belirteci**.  
- Çalışma kitabının konumu, Aspose.Cells Cloud'un erişebilmesi gerekmektedir (varsayılan depo veya özel depo adı).  
- Gerekli SDK sürümü (SDK kullanılıyorsa): **v3.0** API sürümünü destekleyen en son sürüm.  

---

## Kimlik Doğrulama

Tüm istekler **Bearer token** kimlik doğrulaması gerektirir.

```http
Authorization: Bearer <access_token>
```

Belirteç almayle ilgili ayrıntılar için [JWT kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakınız.

---

## HTTP İsteği

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parametre | Konum | Gerekli | Açıklama |
|-----------|--------|---------|-------------|
| `name` | Yol | Evet | Çalışma kitabı dosya adı (örneğin, `test.xlsx`). |
| `sheetName` | Yol | Evet | Gruplandırılacak sütunları içeren çalışma sayfası. |
| `firstIndex` | Sorgu | Evet | Gruba dahil edilecek ilk sütunun sıfır tabanlı dizini. |
| `lastIndex` | Sorgu | Evet | Gruba dahil edilecek son sütunun sıfır tabanlı dizini. |
| `hide` | Sorgu | Hayır | `true` ise gruplanan sütunlar gizlenir; aksi takdirde görünür kalırlar. |
| `folder` | Sorgu | Hayır | Çalışma kitabının bulunduğu klasörün yolu. |
| `storageName` | Sorgu | Hayır | Dosyanın bulunduğu depolama hizmetinin adı. |

---

## İstek Örneği (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Not:** İstek, şifreli iletişimi sağlamak için **HTTPS** kullanır.

---

## Yanıt

### Başarılı (200)

| Alan | Tür | Açıklama |
|--------|---------|-------------|
| `Code` | tamsayı | HTTP durum kodu (`200`). |
| `Status` | dize | İşlemin metinsel durumu (`OK`). |

**Örnek**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Hata (örneğin, 400 Bad Request)

| Alan | Tür | Açıklama |
|--------------|---------|-------------|
| `Code` | tamsayı | HTTP durum kodu (`400`, `401`, `404`, `500`, …). |
| `Status` | dize | Metinsel durum (`Error`). |
| `ErrorMessage` | dize | Sorunun insan tarafından okunabilir açıklaması. |
| `ErrorCode` | dize | Hataya ait programatik tanımlayıcı. |

**Örnek – Geçersiz İstek**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Geçersiz sütun dizini.",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK Örnekleri

Aşağıdaki kod parçacıkları, desteklenen SDK'lar kullanılarak **Çalışma Sayfası Sütunlarını Gruplama** işleminin nasıl çağrılacağını göstermektedir.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Notlar

- **Gruplama davranışı:** API, Excel'de genişletilebilir veya daraltılabilir bir sütun grubu oluşturur. `hide=true` ayarı, grubu hemen daraltır.  
- **Sıfır tabanlı dizinleme:** `firstIndex` ve `lastIndex` parametreleri **0** değerinden başlar; bir çalışma sayfasındaki ilk sütunun dizini 0’dır.  
- **Depolama dikkatleri:** Çalışma kitabı varsayılan depolama dışındaki bir yerde bulunuyorsa, hem `folder` hem de `storageName` sorgu parametrelerini belirtmelisiniz.  

---

## Ayrıca Bakınız

- [Kimlik Doğrulama – JWT belirteç tabanlı](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Çalışma Sayfası Sütunlarını Gruplama için OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDK'ları (GitHub)](https://github.com/aspose-cells-cloud)  
- [Excel Çalışma Sayfasında Satırları Gruplama](/rows/group/)  

---

> *Ekran Görüntüsü:* ![Excel çalışma sayfasında gruplanmış sütunları gösteren ekran görüntüsü](./images/group-columns.png){: .img-fluid alt="Excel çalışma sayfasında gruplanmış sütunları gösteren ekran görüntüsü" }

*Yukarıdaki yer tutucu görüntü, sütun gruplamanın görsel sonucunu gösteren gerçek bir ekran görüntüsü ile değiştirilmelidir.*