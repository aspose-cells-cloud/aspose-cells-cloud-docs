---
title: "واجهة برمجة تطبيقات رفع الملفات في Aspose.Cells Cloud – واجهة لرفع الملفات بسرعة في السحابة"
second_title: "مستند"
ArticleTitle: "واجهة برمجة تطبيقات رفع الملفات في Aspose.Cells Cloud – واجهة لرفع الملفات بسرعة في السحابة"
linktype: "رفع ملف"
type: docs
url: /upload-file/
keywords: "Aspose.Cells، رفع ملف، واجهة برمجة تطبيقات Excel، التخزين السحابي، واجهة برمجة تطبيقات REST"
description: "دليل لرفع الملفات باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud، يغطي معلمات الطلب، كود حالات HTTP، معالجة الأخطاء، وأمثلة على الكود."
weight: 100
---

تتيح واجهة برمجة التطبيقات **uploadFile** للمطورين رفع الملفات مباشرةً إلى التخزين السحابي لمعالجتها باستخدام Aspose Cells.

## **واجهة برمجة تطبيقات Aspose Cells: رفع ملف**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معلمات الطلب لواجهة برمجة التطبيقات **uploadFile** هي:

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
| :---------- | :---- | :---------------------------------- | :---- |
| UploadFiles | ملف | FormData | رفع الملفات إلى التخزين السحابي. |
| path | نص (String) | المسار | المسار الوجهة في التخزين السحابي. حدد المسار الذي يجب رفع الملف إليه. |
| storageName | نص (String) | استعلام (Query) | اسم التخزين الذي سيتم رفع الملف إليه. |

### **الاستجابة**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["نتيجة رفع الملف"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["قائمة بأسماء الملفات المرفوعة"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["قائمة بالأخطاء."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

ترجع واجهة برمجة التطبيقات أكواد حالات HTTP التالية:

| كود الحالة (Status Code) | الوصف |
| ------------------------- | ------ |
| **200 OK** | تم رفع الملف بنجاح. |
| **400 Bad Request** | معلمات غير صالحة أو طلب غير مهيأ بشكل صحيح. |
| **401 Unauthorized** | رمز مصادقة مفقود أو غير صالح. |
| **403 Forbidden** | صلاحيات غير كافية للتخزين المحدد. |
| **500 Internal Server Error** | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة برمجة تطبيقات رفع الملفات مع مكتبات SDK؟

### مواصفات OpenAPI

توفر [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) وصفًا مفصّلًا لواجهة برمجة التطبيقات، مما يمكّن المطورين من التفاعل معها مباشرةً عبر متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبات SDK يعزز كفاءة التطوير من خلال إدارة التفاصيل منخفضة المستوى، مما يسمح للمطورين بالتركيز على مهام المشروع. قم بزيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة شاملة لمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**راجع أيضًا**

- [واجهة برمجة تطبيقات تنزيل الملف](/download-file/) – استرجاع ملف من التخزين السحابي.
- [واجهة برمجة تطبيقات نسخ الملف](/copy-file/) – نسخ ملف داخل التخزين السحابي.
- [واجهة برمجة تطبيقات حذف الملف](/delete-file/) – إزالة ملف من التخزين السحابي.