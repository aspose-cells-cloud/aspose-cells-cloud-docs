---
title: "حذف جميع جداول البيانات المحورية في ورقة عمل Excel"
description: "يحذف جميع جداول البيانات المحورية من ورقة عمل محددة باستخدام واجهة Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells، جدول محوري، حذف، واجهة REST API، Excel"
date: 2026-07-30
api_version: "v3.0"
---

# حذف جميع جداول البيانات المحورية في ورقة عمل Excel

## نظرة عامة
يقوم هذا الإجراء بإزالة **جميع** جداول البيانات المحورية من ورقة عمل محددة في ملف Excel. وهو مفيد عندما تحتاج إلى إعادة تعيين تحليلات ورقة العمل أو تنظيف جداول البيانات المحورية غير المستخدمة في استدعاء واحد.

## المتطلبات المسبقة
قبل استدعاء واجهة برمجة التطبيقات (API)، تأكد من إكمال الخطوات التالية:

1. **حساب Aspose Cloud** – سجّل حسابًا في Aspose Cloud إذا لم يكن لديك حساب بالفعل.  
2. **رمز JWT** – أنشئ رمز JWT (JSON Web Token) للمصادقة. راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) للحصول على التفاصيل.  
3. **إعداد التخزين** – قم برفع ملف Excel المستهدف إلى تخزين Aspose Cloud أو إلى تخزين خارجي متصل. لاحظ **المجلد** و**اسم التخزين** (إن وُجد) حيث يوجد الملف.

## المصادقة
تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud **مصادقة تعتمد على رمز JWT**. أضف الرمز في رأس الطلب `Authorization` في كل طلب:

```
Authorization: Bearer <jwt token>
```

## طلب HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### معاملات المسار
| الاسم | النوع | مطلوب | الوصف |
|------|--------|----------|-------------|
| `name` | نص | نعم | اسم ملف Excel (مثال: `Sample.xlsx`). |
| `sheetName` | نص | نعم | اسم ورقة العمل التي سيتم إزالة جميع جداول البيانات المحورية منها (مثال: `Sheet1`). |

### معاملات الاستعلام
| الاسم | النوع | مطلوب | الوصف |
|------|--------|----------|-------------|
| `folder` | نص | لا | المجلد الذي يحتوي على الملف. |
| `storageName` | نص | لا | اسم التخزين المراد استخدامه (إذا لم يكن الملف في التخزين الافتراضي). |

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## الاستجابة الناجحة
يعيد الخدمة كائنًا قياسيًا `CellsCloudResponse` يُبيّن حالة العملية.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## معالجة الأخطاء

| حالة HTTP | المعنى | مثال على حمولة الطلب |
|-------------|---------|-----------------|
| **400** | طلب غير صالح – معاملات مفقودة أو غير صحيحة | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | غير مصادق – رمز JWT غير صالح أو منتهٍ | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | غير موجود – الملف أو ورقة العمل غير موجودة | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## أمثلة باستخدام SDKs

تُظهر مقاطع الكود التالية كيفية استدعاء العملية باستخدام العديد من SDKs الخاصة بـ Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// تهيئة عميل الواجهة البرمجية
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// تكوين معاملات الطلب
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# تكوين عميل الواجهة البرمجية
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*SDKs إضافية (Go, PHP, Ruby, Swift, Perl, Android) متوفرة في [مستودع Aspose.Cells Cloud SDK](https://github.com/aspose-cells-cloud).*

## انظر أيضًا
- [حذف جدول محوري محدد](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [الحصول على جميع جداول البيانات المحورية في ورقة العمل](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [نظرة عامة على المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [مواصفات OpenAPI لـ DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*تم تحديث هذه الوثيقة آخر مرة في 2026-07-30. جميع المحتويات مشفرة بتنسيق UTF‑8.*
---