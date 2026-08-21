---
title: إضافة شرط إلى التنسيق الشرطي
description: تعلّم كيفية إضافة شرط إلى تنسيق شرطي في ورقة عمل باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمّن عنوان URL للنقطة الطرفية، المُعلمات، المصادقة، مثال cURL، مقاطع كود SDK، ومعالجة الأخطاء.
keywords: "Aspose.Cells Cloud، التنسيق الشرطي، إضافة شرط، واجهة REST API، Excel، ورقة العمل"
type: docs
url: /ar/conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# إضافة شرط إلى التنسيق الشرطي

أضف شرطًا إلى قاعدة تنسيق شرطي موجودة في ورقة عمل باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0).

---

## المتطلبات الأساسية

| المتطلب | التفاصيل |
|---------|----------|
| **المصادقة** | رمز وصول JWT صالح (Bearer) تم الحصول عليه عبر تدفق OAuth 2.0. |
| **إصدار الواجهة** | الإصدار 3.0 – يحتوي عنوان URL للنقطة الطرفية على `/v3.0/`. |
| **المخزن | يجب أن يكون المصنف موجودًا في موقع مخزن يمكن الوصول إليه من قِبل Aspose.Cells Cloud (الافتراضي هو `Default`). |
| **الأذونات** | إذن للقراءة والكتابة على المصنف المستهدف. |
| **التنسيقات المدعومة** | أي تنسيق مصنف مدعوم من قِبل Aspose.Cells (مثل `.xlsx`، `.xls`، `.xlsm`). |

---

## النقطة الطرفية

**طريقة HTTP:** `PUT`  
**عنوان URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| المُعلمة | الموقع | النوع | الإلزام | الوصف |
|---------|--------|-------|---------|--------|
| `name` | المسار | نص | **نعم** | اسم ملف المصنف (مع الامتداد). |
| `sheetName` | المسار | نص | **نعم** | اسم ورقة العمل التي تحتوي على التنسيق الشرطي. |
| `index` | المسار | عدد صحيح | **نعم** | المؤشر البالغ الصفر (zero-based) لمجموعة التنسيق الشرطي المراد تعديلها. |
| `type` | الاستعلام | نص | **نعم** | نوع الشرط. القيم المسموح بها: `CellValue`، `Expression`، `ColorScale`، `DataBar`، `IconSet`، `Top10`، `UniqueValues`، `DuplicateValues`، `ContainsText`، `NotContainsText`، `BeginsWith`، `EndsWith`، `ContainsBlanks`، `NotContainsBlanks`، `ContainsErrors`، `NotContainsErrors`، `TimePeriod`، `AboveAverage`. |
| `operatorType` | الاستعلام | نص | **نعم** | العامل التشغيلي للشرط. القيم المسموح بها: `Between`، `Equal`، `GreaterThan`، `GreaterOrEqual`، `LessThan`، `None`، `NotBetween`، `NotEqual`. |
| `formula1` | الاستعلام | نص | **نعم** | الصيغة أو القيمة الأولى المرتبطة بالشرط. |
| `formula2` | الاستعلام | نص | لا | الصيغة أو القيمة الثانية (مطلوبة فقط للعوامل التي تتطلب قيمتين، مثل `Between`). |
| `folder` | الاستعلام | نص | لا | المجلد الموجود فيه المصنف داخل المخزن. |
| `storageName` | الاستعلام | نص | لا | اسم خدمة التخزين. |

> **ملاحظة:** جميع المُعلمات المسار (`name`، `sheetName`، `index`) ومُعلمات الاستعلام `type`، `operatorType`، و`formula1` إلزامية. أما `formula2` و`folder` و`storageName` فهي اختيارية.

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*استبدل `<jwt_token>` برمز وصول صالح، وضبط القيم `name` و`sheetName` و`index` وقيم معلمات الاستعلام حسب الحاجة.*

---

## الاستجابة الناجحة

```json
{
  "Code": "200",
  "Status": "OK"
}
```

تشير الاستجابة إلى أن الشرط تمت إضافته بنجاح. تُعيد العملية كائنًا عامًّا من نوع `CellsCloudResponse` يحتوي على رمز حالة HTTP ورسالة حالة موجزة.

---

## استجابات الأخطاء

| رمز HTTP | السبب | مثال جسم الاستجابة |
|----------|--------|-------------------|
| **400** | طلب سيء – معلمات مفقودة أو غير صالحة. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | غير مصرّح به – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | غير موجود – المصنف أو ورقة العمل أو المؤشر الخاص بالتنسيق الشرطي غير موجود. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## ملاحظات ومتاهات شائعة

* **ترميز المُعلمات** – قم بترميز الأحرف الخاصة في `formula1`/`formula2` داخل عنوان URL (مثل تحويل المسافات إلى `%20`).  
* **توافق العوامل** – بعض العوامل (مثل `Between`) تتطلب كلًا من `formula1` و`formula2`. تجنّب استخدام `formula2` للعوامل التي تتطلب قيمة واحدة فقط.  
* **مؤشر التنسيق الشرطي** – المؤشر يبدأ من الصفر (zero-based). استخدم النقطة الطرفية **Get Conditional Formattings** لاسترجاع المؤشر الصحيح إذا لم تكن متأكدًا.  
* **مجلد التخزين** – إذا كان المصنف موجودًا في مجلد غير افتراضي، فزوّد المُعلمة `folder` في الاستعلام؛ وإلا ستفترض الواجهة أن المجلد الجذري هو المكان.  
* **تقييد معدل الطلبات** – تطبّق Aspose.Cells Cloud حدودًا للطلبات لكل حساب. إذا حصلت على استجابة برمز 429، فقم بتأخير محاولتك اللاحقة لفترة قصيرة.  

---

## أمثلة على SDK

فيما يلي مقاطع جاهزة للتشغيل لأشهر SDKs. استبدل القيم العنصرية (`YOUR_FILE`، `YOUR_SHEET`، إلخ) ببياناتك الخاصة.

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
        string folder = null;          // اختياري
        string storageName = null;     // اختياري

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

> **SDKs المفقودة** – إذا كانت لغة تحتاجها غير مذكورة هنا، فراجع **مرجع API العام** وقم بإنشاء طلب HTTP يدويًا.

---

## انظر أيضًا

- **[Get Conditional Formattings](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – استرجاع قائمة قواعد التنسيق الشرطي لورقة العمل.  
- **[Delete Conditional Formatting](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – حذف قاعدة تنسيق شرطي موجودة.  
- **[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – التعريف الكامل قابل للقراءة بالآلة لهذه العملية.  

---