---
title: "إلغاء حماية ملف Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "إلغاء حماية ملف Excel"
type: docs
url: /excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells، واجهة برمجة تطبيقات إلغاء حماية Excel، إزالة حماية ملف العمل، واجهة برمجة تطبيقات REST، جدول بيانات سحابي"
description: "تعرّف على كيفية إزالة الحماية من ملف عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن بناء الجملة المطلوبة، المعاملات، مثال cURL، ورمز SDK بلغات برمجة متعددة."
weight: 60
ArticleTitle: "إلغاء حماية ملف Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

استخدم هذه واجهة برمجة تطبيقات REST لإلغاء حماية ملف عمل Excel.

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات المسار (Path Parameters)

| المعامل      | النوع   | الوصف                                                     | الإجباري |
|-------------|---------|-----------------------------------------------------------|----------|
| **name**    | string  | اسم ملف ملف العمل (مع امتداد الملف).                       | نعم      |

### معاملات الاستعلام (Query Parameters)

| اسم المعامل     | النوع   | الوصف                                                   |
|----------------|---------|---------------------------------------------------------|
| folder         | string  | مسار المجلد الذي يحتوي على ملف العمل الأصلي.           |
| storageName    | string  | اسم خدمة التخزين التي يخزن فيها ملف العمل.             |

### معاملات جسم الطلب (Request Body Parameters)

| اسم المعامل   | النوع                      | الوصف                                               |
|--------------|----------------------------|-----------------------------------------------------|
| protection   | WorkbookProtectionRequest  | كائن يحدد إعدادات الحماية المراد إزالتها.          |

#### WorkbookProtectionRequest

| اسم المعامل     | النوع   | الوصف                                                                                      |
|----------------|---------|-------------------------------------------------------------------------------------------|
| ProtectionType | string  | نوع الحماية المراد إزالتها (`ALL`، `CONTENTS`، `NONE`، `OBJECTS`، `SCENARIOS`، `STRUCTURE`، `WINDOWS`). |
| Password       | string  | كلمة المرور المطلوبة لإزالة الحماية (اختيارية).                                          |

#### مثال cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### الاستجابة (ناجحة)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### استجابات الأخطاء (HTTPS Status Error Responses)

| حالة HTTP | الكود                | الوصف                                                       |
|----------|---------------------|-------------------------------------------------------------|
| 400      | BadRequest          | معاملات مفقودة أو غير صالحة.                               |
| 401      | Unauthorized        | رمز وصول غير صالح أو مفقود.                                |
| 404      | NotFound            | لم يتم العثور على ملف العمل المحدد في المجلد/خدمة التخزين المعطاة. |
| 500      | InternalServerError | خطأ غير متوقع في الخادم.                                   |

## كيفية استخدام DeleteUnProtectWorkbook API باستخدام مكتبات SDK

### مواصفات DeleteUnProtectWorkbook API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة تطبيقات السحابة باستخدام cURL.

### استخدام مكتبات SDK لـ Aspose.Cells Cloud

استخدام SDK يبسّط التكامل ويقلّل من كمية الكود المتكرر. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}