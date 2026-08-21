---
title: "AutoFitterOptions – Özellikler ve Kullanım Kılavuzu | Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "AutoFitterOptions"
type: docs
url: /auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Excel otomatik sığdırma, satır yüksekliği, birleştirilmiş hücreler, API"
description: "Aspose.Cells Cloud API'deki AutoFitterOptions nesnesi ile satır yüksekliği otomatik sığdırma, birleştirilmiş hücrelerin ele alınması, gizli satır/sütunların işlenmesi, dil ayarları ve oluşturma davranışını nasıl kontrol edebileceğinizi öğrenin."
weight: 79
ArticleTitle: "AutoFitterOptions – Aspose.Cells Cloud için Özellikler ve Kullanım Kılavuzu"
---

# AutoFitterOptions Özellikleri

`AutoFitterOptions` nesnesi, Aspose.Cells Cloud tarafından gerçekleştirilen otomatik satır yüksekliği ayarlamasını ince ayar yapmanızı sağlar. Birleştirilmiş hücrelerin işlenmesi, gizli satır/sütunların ele alınması, dil-özelinde biçimlendirme veya oluşturma-özelinde davranış üzerinde kesin kontrol gerektirdiğinde kullanışlıdır.

**Önkoşullar** – Bu özellikleri kullanmak için **Cells.ReadWrite** kapsamını içeren geçerli bir OAuth 2.0 erişim belirteci ile kimlik doğrulaması yapmış olmanız gerekir. İstek, v3.0 API’yi destekleyen tüm SDK sürümleriyle çalışır.

| Adı                        | Tür          | Açıklama                                                                                       | Notlar                                                                                                         |
| -------------------------- | ------------ | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**   | Birleştirilmiş hücrelerin nasıl otomatik sığdırılacağını belirler.                             | İzin verilen değerler: `All`, `First`, `None`. Varsayılan: `All`. Örnek JSON: `"AutoFitMergedCellsType":"All"` |
| **IgnoreHidden**           | **boolean**  | **true** olduğunda, otomatik sığdırma işlemi sırasında gizli satır ve sütunlar dikkate alınmaz. | Varsayılan: `false`. Örnek JSON: `"IgnoreHidden":false`                                                       |
| **OnlyAuto**               | **boolean**  | Yalnızca yükseklikleri manuel olarak özelleştirilmemiş satırların otomatik sığdırılmasını belirtir. | Varsayılan: `false`. Örnek JSON: `"OnlyAuto":false`                                                           |
| **DefaultEditLanguage**    | **string**   | Çalışma kitabının varsayılan düzenleme dilini ayarlar.                                         | Varsayılan: sistem dili (örn. `"en-US"`). Örnek JSON: `"DefaultEditLanguage":"en-US"`                         |
| **MaxRowHeight**           | **double**   | Satırlar otomatik sığdırılırken uygulanacak maksimum satır yüksekliği (nokta cinsinden). **0** değeri sınır olmadığını belirtir. | Varsayılan: `0`. Örnek JSON: `"MaxRowHeight":0`                                                               |
| **AutoFitWrappedTextType** | **string**   | Hücrelerdeki satır sonu yapılmış metnin nasıl otomatik sığdırılacağını kontrol eder.           | İzin verilen değerler: `All`, `OnlyWrapped`, `None`. Varsayılan: `All`. Örnek JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**   | Otomatik sığdırma işlemi sırasında kullanılan biçimlendirme stratejisini belirtir.             | Yaygın değerler: `AutoFit`, `PreserveExisting`. Varsayılan: `AutoFit`. Örnek JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**   | Otomatik sığdırmanın oluşturma amaçlı (örn. PDF, resim) olup olmadığını belirtir.              | İzin verilen değerler: `True`, `False`. Varsayılan: `False`. Örnek JSON: `"ForRendering":"False"`             |

Aşağıda, `AutoFitterOptions` yapılandırması için API’ye gönderilebilecek tipik bir JSON yükü örneği verilmiştir.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Bu seçenekleri bir çalışma kitabına uygulayan örnek bir `cURL` isteği:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Uç nokta referansı**

| Yöntem | URL | Gerekli Parametreler | Açıklama |
|--------|-----|---------------------|----------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (JSON gövdesi) | Belirtilen `AutoFitterOptions` değerlerini hedef çalışma kitabına uygular. |
| GET    | `/cells/workbook/autoFitter` | *hiçbiri* | Çalışma kitabının geçerli `AutoFitterOptions` ayarlarını getirir. |

**PUT uç noktası için istek parametreleri**

| Parametre                | Tür     | Gerekli | Açıklama |
|--------------------------|---------|---------|----------|
| AutoFitMergedCellsType   | string  | Evet    | Birleştirilmiş hücrelerin nasıl otomatik sığdırılacağı (`All`, `First`, `None`). |
| IgnoreHidden             | boolean | Hayır   | Gizli satır/sütunların dikkate alınıp alınmayacağı. |
| OnlyAuto                 | boolean | Hayır   | Yalnızca manuel yükseklik ayarı yapılmamış satırları sığdır. |
| DefaultEditLanguage      | string  | Hayır   | Düzenleme dili (örn. `en-US`). |
| MaxRowHeight             | double  | Hayır   | Maksimum satır yüksekliği (nokta cinsinden); `0` = sınırsız. |
| AutoFitWrappedTextType   | string  | Hayır   | Satır sonu yapılmış metnin nasıl ele alınacağı (`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | Hayır   | Biçimlendirme stratejisi (`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | Hayır   | Oluşturma için otomatik sığdırma uygula (`True`, `False`). |

Tipik yanıt kodları:

- **200 OK** – İşlem başarıyla tamamlandı.  
- **400 Bad Request** – Geçersiz JSON yükü veya desteklenmeyen değer.  
- **401 Unauthorized** – Eksik veya geçersiz kimlik doğrulama belirteci.  
- **500 Internal Server Error** – Beklenmeyen sunucu hatası.

**Örnek GET yanıtı**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Bu örnekler, `AutoFitterOptions` modelini Aspose.Cells Cloud API içinde nasıl yapılandırıp çağıracığınızı göstermektedir.