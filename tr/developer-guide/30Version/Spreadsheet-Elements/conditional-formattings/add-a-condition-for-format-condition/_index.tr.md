---
title: Koşullu Biçimlendirmeye Koşul Ekleme
description: Aspose.Cells Cloud REST API (v3.0) kullanarak bir çalışma sayfasının koşullu biçimlendirmesine bir koşul eklemenin nasıl yapılacağını öğrenin. Uç nokta, parametreler, kimlik doğrulama, cURL örneği, SDK kod parçacıkları ve hata işleme içerir.
keywords: "Aspose.Cells Cloud, Koşullu Biçimlendirme, Koşul Ekle, REST API, Excel, Çalışma Sayfası"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# Koşullu Biçimlendirmeye Koşul Ekleme

Aspose.Cells Cloud REST API (v3.0) kullanarak bir çalışma sayfasındaki mevcut koşullu biçimlendirme kuralına bir koşul ekleyin.

---

## Ön Gereksinimler

| Gereksinim | Detaylar |
|-----------|----------|
| **Kimlik Doğrulama** | OAuth 2.0 akışı aracılığıyla alınmış geçerli bir JWT erişim belirteci (Bearer). |
| **API Sürümü** | v3.0 – uç nokta URL’si `/v3.0/` içerir. |
| **Depo** | Çalışma kitabının Aspose.Cells Cloud tarafından erişilebilir bir depolama konumunda bulunması gerekir (varsayılan: `Default`). |
| **İzinler** | Hedef çalışma kitabında Okuma/Yazma izni. |
| **Desteklenen Formatlar** | Aspose.Cells tarafından desteklenen herhangi bir çalışma kitabı formatı (örn. `.xlsx`, `.xls`, `.xlsm`). |

---

## Uç Nokta

**HTTP Yöntemi:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parametre | Konum | Tür | Gerekli | Açıklama |
|-----------|-------|-----|---------|----------|
| `name` | Yol | string | **Evet** | Çalışma kitabı dosyasının adı (uzantı dahil). |
| `sheetName` | Yol | string | **Evet** | Koşullu biçimlendirmeyi içeren çalışma sayfasının adı. |
| `index` | Yol | integer | **Evet** | Düzenlenecek koşullu biçimlendirme koleksiyonunun sıfır tabanlı indeksi. |
| `type` | Sorgu | string | **Evet** | Koşul türü. İzin verilen değerler: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Sorgu | string | **Evet** | Koşul için operatör. İzin verilen değerler: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Sorgu | string | **Evet** | Koşul ile ilişkili ilk formül/değer. |
| `formula2` | Sorgu | string | Hayır | İkinci formül/değer (yalnızca iki değer gerektiren operatörler için gerekli, örneğin `Between`). |
| `folder` | Sorgu | string | Hayır | Çalışma kitabının bulunduğu depodaki klasör. |
| `storageName` | Sorgu | string | Hayır | Depolama hizmetinin adı. |

> **Not:** Tüm yol parametreleri (`name`, `sheetName`, `index`) ve `type`, `operatorType`, `formula1` sorgu parametreleri zorunludur. `formula2`, `folder` ve `storageName` ise isteğe bağlıdır.

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*`<jwt_token>` ifadesini geçerli bir erişim belirteci ile değiştirin ve gerekli durumlara göre `name`, `sheetName`, `index` ve sorgu değerlerini ayarlayın.*

---

## Başarılı Yanıt

```json
{
  "Code": "200",
  "Status": "OK"
}
```

Yanıt, koşulun başarıyla eklendiğini gösterir. İşlem, HTTP durum kodunu ve kısa durum mesajını içeren genel bir `CellsCloudResponse` nesnesi döndürür.

---

## Hata Yanıtları

| HTTP Kodu | Sebep | Örnek Gövde |
|-----------|-------|--------------|
| **400** | Geçersiz İstek – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Yetkisiz – eksik veya geçersiz JWT belirteci. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Bulunamadı – çalışma kitabı, çalışma sayfası veya koşullu biçimlendirme indeksi mevcut değil. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | Sunucu İçi Hata – beklenmeyen sunucu hatası. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Notlar ve Yaygın Hatalar

* **Parametre Kodlama** – `formula1`/`formula2` içindeki özel karakterler URL ile kodlanmalıdır (örn. boşluklar → `%20`).  
* **Operatör Uyumluluğu** – Bazı operatörler (örn. `Between`) hem `formula1` hem de `formula2` gerektirir. Tek değer gerektiren operatörler için `formula2` atlanmalıdır.  
* **Koşullu Biçimlendirme İndeksi** – İndeks sıfır tabanlıdır. İndeksten emin değilseniz doğru indeksi almak için **Koşullu Biçimlendirmeleri Al** uç noktasını kullanın.  
* **Depo Klasörü** – Çalışma kitabının varsayılan olmayan bir klasörde yer alıyorsa `folder` sorgu parametresini belirtmelisiniz; aksi takdirde API kök klasörü varsayar.  
* **Ortam Sınırlandırma** – Aspose.Cells Cloud, hesap başına istek sınırları uygular. 429 yanıtı alırsanız, kısa bir gecikmeden sonra tekrar deneyin.

---

## SDK Örnekleri

En popüler SDK'lar için çalıştırılabilir kod parçacıkları aşağıdadır. Yer tutucu değerleri (`YOUR_FILE`, `YOUR_SHEET` vb.) kendi verilerinizle değiştirin.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // isteğe bağlı
        string storageName = null;     // isteğe bağlı

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **Eksik SDK’lar** – İhtiyacınız olan bir dil listelenmemişse, genel **API Referansı** sayfasına bakın ve HTTP isteğini manuel olarak oluşturun.

---

## Aşağıdakilere Bakın

- **[Koşullu Biçimlendirmeleri Al](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Bir çalışma sayfasının koşullu biçimlendirme kurallarının listesini alın.  
- **[Koşullu Biçimlendirmeyi Sil](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Mevcut bir koşullu biçimlendirme kuralını kaldırın.  
- **[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Bu işlemin tam makineyle okunabilir tanımı.  

---