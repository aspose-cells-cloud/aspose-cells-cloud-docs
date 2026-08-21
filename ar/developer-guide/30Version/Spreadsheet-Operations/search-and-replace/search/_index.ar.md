---
title: "البحث عن نص في ملفات Excel – واجهة برمجة التطبيقات السحابية Aspose.Cells"
description: "ابحث عن نص محدد في ملفات Excel (XLS وXLSX وXLSM وXLSB) وملفات OpenDocument Spreadsheet (ODS) باستخدام واجهة برمجة التطبيقات السحابية Aspose.Cells. تتضمن تفاصيل الطلب وأمثلة باستخدام cURL وSDKs، بالإضافة إلى معالجة الأخطاء."
keywords: "Aspose.Cells، Excel، بحث، API، REST"
type: docs
url: /ar/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# البحث عن نص في ملفات Excel – واجهة برمجة التطبيقات السحابية Aspose.Cells

## نظرة عامة
تقدم Aspose.Cells Cloud نقطة نهاية **POST** تتيح لك البحث عن سلسلة نصية محددة داخل كتب عمل Excel (XLS وXLSX وXLSM وXLSB) وملفات OpenDocument Spreadsheet (ODS). وتُعيد الواجهة الخلوية كل خلية تحتوي على النص المطلوب مع رابط يُشير إلى ورقة العمل التي تم العثور على التطابق فيها.

> **حالات الاستخدام**  
> - التحقق من وجود قيمة محددة في تقرير قبل معالجته بشكل إضافي.  
> - بناء أداة سريعة للبحث والاستبدال (find-and-replace) تقوم أولاً بإدراج جميع الحالات.  
> - إنشاء فهرس للمصطلحات المفتاحية عبر دفعة من جداول البيانات.

---

## المتطلبات الأساسية
| المتطلب | التفاصيل |
|---------|----------|
| **المصادقة** | رمز JWT يُستحصل عبر تدفق OAuth في Aspose Cloud. يجب أن يتضمن الرمز النطاق **Cells**. |
| **التنسيقات المدعومة** | XLS وXLSX وXLSM وXLSB وODS |
| **أقصى حجم للملف** | 150 ميغابايت (مضغوط). الملفات الأكبر تُعيد الرمز **413 Payload Too Large**. |
| **الرؤوس المطلوبة** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **الصلاحيات** | يجب أن يمتلك الرمز صلاحية *قراءة* على وحدة التخزين المستهدفة (عند استخدام وحدة تخزين عن بُعد) – ولا يُطلب هذا عند رفع الملف كـ `multipart/form-data`. |

*نصيحة:* استخدم نقطة النهاية **/connect/token** لتوليد رمز JWT. راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) للحصول على التفاصيل.

---

## نقطة النهاية

| العنصر | القيمة |
|--------|--------|
| **طريقة HTTP** | `POST` |
| **الرابط** | `https://api.aspose.cloud/v3.0/cells/search` |
| **الغرض** | البحث عن نص محدد داخل كتاب عمل Excel تم رفعه. |
| **الأمان** | رمز JWT (Bearer) – راجع *المتطلبات الأساسية* أعلاه. |

---

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات السحابية Aspose.Cells آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

## معلمات الطلب

| الاسم | النوع | الموقع | الإلزام | الوصف |
|------|-------|--------|---------|--------|
| `file` | **ملف** | `formData` (multipart) | **نعم** | ملف جدول البيانات المراد رفعه. |
| `text` | **نص** | سلسلة الاستعلام | **نعم** | السلسلة النصية المراد البحث عنها. |
| `password` | **نص** | سلسلة الاستعلام | لا | كلمة المرور لفتح كتاب عمل محمي، إن لزم الأمر. |
| `sheetname` | **نص** | سلسلة الاستعلام | لا | اسم ورقة العمل التي تُحدُّ فيها عملية البحث. إن لم يُحدَّد، تُبحث جميع أوراق العمل. |
| `checkExcelRestriction` | **منطقي** | سلسلة الاستعلام | لا (الافتراضي: `true`) | عند `true`، تتحقق الواجهة من القيود الخاصة بـ Excel (مثل الخلايا المقروءة فقط) قبل البحث. |

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*استبدل `<jwt-token>` برمز صالح وضبط معلمات الاستعلام حسب الحاجة.*

---

## الاستجابة الناجحة

**HTTP 200 – نجح البحث؛ تحتوي الاستجابة على عناصر النص التي تم العثور عليها.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### حقول الاستجابة

| الحقل | النوع | الوصف |
|-------|-------|--------|
| `Status` | نص | حالة الطلب العامة (`OK` للنجاح). |
| `Code` | عدد صحيح | رمز حالة HTTP (200). |
| `TextItems.link` | كائن | رابط هايبرميديا لمجموعة الموارد. |
| `TextItems.TextItemList` | مصفوفة | قائمة التطابقات. كل عنصر يحتوي على: |
| `Text` | نص | قيمة الخلية التي طابقت نص البحث. |
| `link` | كائن | رابط تشعبي إلى ورقة العمل التي تم العثور على التطابق فيها (`Href` يشير إلى `Workbook/worksheets/SheetName`). |

---

## استجابات الأخطاء

| كود HTTP | المعنى | السبب الشائع | مثال على الجسم |
|-----------|---------|---------------|----------------|
| **400** | طلب غير صحيح | معلمات مطلوبة مفقودة، أو نوع ملف غير مدعوم، أو قيم استعلام غير صالحة. | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401** | غير مصادق عليه | رمز JWT مفقود أو غير صالح. | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }` |
| **413** | حملة مفرطة الحجم | تجاوز حجم الملف المرفوع الحد المسموح به البالغ 150 ميغابايت. | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }` |
| **500** | خطأ داخلي في الخادم | مشكلة غير متوقعة من جانب الخادم. | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }` |

---

## أمثلة باستخدام SDKs

فيما يلي مقاطع كود مبسطة لعملية **PostSearch** باستخدام واجهات برمجة التطبيقات الرسمية لـ Aspose.Cells Cloud SDKs. استبدل `YOUR_JWT_TOKEN` ومسار الملف بقيمك الخاصة.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(تتوفر SDKs للغات PHP وRuby وGo وPerl في [مستودع Aspose.Cells Cloud على GitHub](https://github.com/aspose-cells-cloud).)*

---

## ملاحظات إضافية

- يُعد **`checkExcelRestriction`** افتراضيًا `true`. عيّنه على `false` فقط عندما تكون متأكدًا من أن كتاب العمل لا يحتوي على خلايا محمية قد تعيق عملية البحث.
- تُعيد الواجهة **روابط هايبرميديا** (`Href`) يمكن استخدامها مع نقاط نهاية Aspose.Cells Cloud الأخرى (مثل تنزيل ورقة العمل أو استرجاع تنسيق الخلية).
- عند البحث في كتب عمل كبيرة، فكّر في تضييق النطاق باستخدام معلمة `sheetname` لتحسين زمن الاستجابة.

---

## روابط ذات صلة

- **دليل المصادقة** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **مواصفات OpenAPI لـ PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **واجهات برمجة التطبيقات SDK لـ Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>
- **الحدود المفروضة ومعدلات الحصص** – <https://docs.aspose.cloud/total/getting-started/limits/>

---