---
---
title: "كيفية العمل مع حذف أوراق العمل في ملف Excel"
second_title: "Document"
linktype: "حذف"
type: docs
url: /ar/worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, حذف ورقة عمل, Excel, C#, Java, Python"
description: "تعلم كيفية حذف ورقة عمل واحدة أو عدة أوراق عمل من ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل أمثلة بلغات C# وJava وPython، والمتطلبات المسبقة، ونصائح معالجة الأخطاء، والعمليات ذات الصلة."
weight: 20
ArticleTitle: "حذف ورقة/أوراق عمل في ملف Excel باستخدام واجهة Aspose.Cells Cloud API"
---

## العمل مع حذف أوراق العمل في ملف Excel

عندما تُولّد تطبيقات ملفات Excel ديناميكيًا أو تُعدّلها، قد تحتاج إلى إزالة أوراق العمل التي لم تعد مطلوبة—مثل التقارير المؤقتة أو أوراق العمل البديلة أو البيانات القديمة. وتُسهّل واجهة Aspose.Cells Cloud API حذف ورقة عمل واحدة أو عدة أوراق عمل في طلب واحد.

**مرجع الواجهة البرمجية**

| العنصر | التفاصيل |
|--------|----------|
| **طريقة HTTP** | `DELETE` |
| **النقطة الطرفية** | `/cells/{fileName}/worksheets` |
| **معامِلات المسار** | `fileName` – اسم ملف Excel (مطلوبة) |
| **معامِلات الاستعلام** | `sheetName` – اسم ورقة العمل المراد حذفها (اختيارية، لحذف ورقة واحدة) <br> `folder` – مسار المجلد في التخزين (اختياري) <br> `storage` – اسم التخزين (اختياري) |
| **جسم الطلب** | *لا يوجد* |
| **استجابة النجاح** | `200 OK` – تم حذف ورقة/أوراق العمل بنجاح. تُعيد كائن JSON يحتوي على حالة العملية. |
| **استجابات الأخطاء** | `400 Bad Request` – معامِلات غير صالحة <br> `401 Unauthorized` – فشل المصادقة <br> `404 Not Found` – ملف أو ورقة عمل غير موجودة <br> `500 Internal Server Error` – مشكلة من جانب الخادم |

**الطلب**

لحذف ورقة عمل واحدة أو أكثر، أرسل طلب `DELETE` إلى النقطة الطرفية المذكورة أعلاه، بما فيذ المعامل المطلوب `fileName`، واخياريًا المعامل `sheetName` في استعلام العنوان لحذف ورقة عمل واحدة. عند إغفال `sheetName`، تحذف جميع أوراق العمل في الملف.

**المعامِلات**

- `fileName` (سلسلة نصية، مطلوبة): اسم ملف Excel، بما في ذلك الامتداد.  
- `sheetName` (سلسلة نصية، اختيارية): اسم ورقة العمل المحددة المراد حذفها. عند إغفالها، تحذف الواجهة جميع أوراق العمل.  
- `folder` (سلسلة نصية، اختيارية): مسار المجلد الذي يحتوي على الملف في التخزين.  
- `storage` (سلسلة نصية، اختيارية): اسم تخزين Aspose Cloud المراد استخدامه.

**الاستجابات**

- **200 OK** – مثال على JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "تم حذف ورقة/أوراق العمل بنجاح."
  }
  ```
- **400 Bad Request** – معامِلات طلب غير صالحة.  
- **401 Unauthorized** – رمز المصادقة مفقود أو غير صالح.  
- **404 Not Found** – الملف أو ورقة العمل المحددة غير موجودة.  
- **500 Internal Server Error** – خطأ غير متوقع في الخادم.

**أمثلة**

*فيما يلي مقتطفات كود قصيرة تُظهر كيفية استدعاء نقطة حذف الواجهة باستخدام ثلاث لغات شائعة.*

**مثال بلغة C#**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"الحالة: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"خطأ: {ex.Message}");
}
```

**مثال بلغة Java**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("الحالة: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("خطأ: " + e.getMessage());
        }
    }
}
```

**مثال بلغة Python**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"الحالة: {response.status}")
except ApiException as e:
    print(f"خطأ: {e}")
```

**معالجة الأخطاء**

- تأكد من صلاحية رمز المصادقة قبل إرسال الطلب.  
- تحقق من رمز حالة الاستجابة؛ وعالج الأكواد `400` و`401` و`404` و`500` وفقًا لذلك.  
- استخدم كتل try-catch (أو ما يعادلها) لالتقاط استثناءات الشبكة أو SDK.

**العمليات ذات الصلة**

- [إضافة ورقة عمل](/ar/worksheets/add/) – إنشاء ورقة عمل جديدة في ملف موجود.  
- [نسخ ورقة عمل](/ar/worksheets/copy/) – تكرار ورقة عمل موجودة.  
- [إعادة تسمية ورقة عمل](/ar/worksheets/rename/) – تغيير اسم ورقة عمل.  
- [نقل ورقة عمل](/ar/worksheets/move/) – إعادة ترتيب أوراق العمل داخل الملف.  
---