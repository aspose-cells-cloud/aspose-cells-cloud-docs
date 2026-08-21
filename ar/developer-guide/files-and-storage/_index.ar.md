---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – إدارة الملفات والمجلدات (الرفع، التنزيل، النسخ، النقل)"
second_title: "مستند"
ArticleTitle: "إدارة الملفات في السحابة لـ Excel – حلٌّ فعّال وآمن لتخزين ملفات Excel والتنظيم الذكي"
linktitle: "الملفات والتخزين"
type: docs
url: /ar/files-and-storage/
aliases: [/ar/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Aspose.Cells Cloud، واجهة برمجة تطبيقات تخزين الملفات، رفع ملف Excel، تنزيل ملف Excel، نسخ ملف، نقل ملف، حذف ملف، إدارة المجلدات، واجهة برمجة تطبيقات REST، أمثلة cURL"
description: "دليل شامل لإدارة ملفات Excel والمجلدات في مساحة التخزين الخاصة بـ Aspose.Cells Cloud. يشمل عمليات الرفع، التنزيل، النسخ، النقل، الحذف وإدارة المجلدات مع أمثلة cURL، المعاملات المطلوبة وملاحظات حول المصادقة."
weight: 100
---

توفر Aspose.Cells Cloud مجموعة شاملة من الوظائف المساعدة للعمل مع الملفات المخزَّنة في مساحة تخزين Aspose.Cells Cloud أو أي مساحة تخزين سحابية من طرف ثالث تختارها. للحصول على مساعدة في إعداد مساحة التخزين من طرف ثالث، يُرجى الرجوع إلى [مواضيع مساعدة واجهة مستخدم Aspose Cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**تقدم Aspose.Cells Cloud مجموعة متنوعة من واجهات برمجة التطبيقات لإدارة الملفات والمجلدات ومساحات التخزين.**

> **ملاحظة:** يجب أن تستخدم جميع استدعاءات واجهة برمجة التطبيقات بروتوكول **HTTPS**. انظر [دليل المصادقة](/ar/cells/authentication/) للحصول على تفاصيل حول كيفية الحصول على رمز JWT.

**المتطلبات المسبقة:** لاستخدام هذه الواجهات، يجب أن تكون لديك حساب Aspose Cloud ساري المفعول، والحصول على رمز وصول JWT، وتم تكوين موقع تخزين (إما مساحة تخزين Aspose Cloud أو مساحة تخزين من طرف ثالث متصلة).

**آخر تحديث:** 2024-12-01

## **كيفية رفع ملف**

### معلومات واجهة برمجة تطبيقات رفع الملف

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | المسار الذي سيتم رفع الملف إليه، بما في ذلك اسم الملف وامتداده (مثال: `/folder1/Report.xlsx`). |
| file        | ملف   | formData | الملف المراد رفعه. |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد استخدامها. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم رفع الملف بنجاح. |
| 400   | طلب غير صالح – معاملات مفقودة أو غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT غير صالح أو مفقود. |
| 404   | لم يتم العثور على مساحة التخزين. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على رفع ملف

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية رفع ملف باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: الحد الأقصى لحجم الملف المرفوع هو 100 ميغابايت. وقد تُطبّق قيود على معدل الطلبات.*

## **كيفية تنزيل ملف**

### معلومات واجهة برمجة تطبيقات تنزيل الملف

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | مسار الملف (مثال: `/folder/Report.xlsx`). |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد استخدامها. |
| versionId   | نص    | استعلام | مُعرّف إصدار الملف المراد تنزيله (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم تنزيل الملف؛ يتم إرجاع تيار ثنائي. |
| 400   | طلب غير صالح – معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على الملف. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على تنزيل ملف

{{< tabs tabTotal="2" tabID="13" tabName13="الطلب" tabName14="الاستجابة" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<بيانات ثنائية>"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: تحتوي الاستجابة على التيار الثنائي للملف. عند استخدام cURL، احفظ المخرجات في ملف باستخدام `-o filename.xlsx`.*

## **كيفية حذف ملف**

### معلومات واجهة برمجة تطبيقات حذف الملف

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | مسار الملف (مثال: `/folder/Report.xlsx`). |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد استخدامها. |
| versionId   | نص    | استعلام | مُعرّف إصدار الملف المراد حذفه (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم حذف الملف بنجاح. |
| 400   | طلب غير صالح – معاملات مفقودة أو غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT غير صالح. |
| 404   | لم يتم العثور على الملف. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على حذف ملف

{{< tabs tabTotal="2" tabID="15" tabName15="الطلب" tabName16="الاستجابة" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: حذف الملف هو إجراء دائم؛ تأكد من وجود نسخة احتياطية إن لزم الأمر.*

## **كيفية نسخ ملف**

### معلومات واجهة برمجة تطبيقات نسخ الملف

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل     | النوع | الموقع | الوصف |
|----------------|-------|--------|--------|
| srcPath        | نص    | المسار | مسار الملف المصدر (مثال: `/folder/Source.xlsx`). |
| destPath       | نص    | استعلام | مسار الملف الوجهة (مثال: `/folder/Destination.xlsx`). |
| srcStorageName | نص    | استعلام | اسم مساحة التخزين المصدر (اختياري). |
| destStorageName| نص    | استعلام | اسم مساحة التخزين الوجهة (اختياري). |
| versionId      | نص    | استعلام | مُعرّف إصدار الملف المراد نسخه (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم نسخ الملف بنجاح. |
| 400   | طلب غير صالح – معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على الملف المصدر. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على نسخ ملف

{{< tabs tabTotal="2" tabID="17" tabName17="الطلب" tabName18="الاستجابة" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: لا تؤدي عملية النسخ إلى إزالة الملف المصدر.*

## **كيفية نقل ملف**

### معلومات واجهة برمجة تطبيقات نقل الملف

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل     | النوع | الموقع | الوصف |
|----------------|-------|--------|--------|
| srcPath        | نص    | المسار | مسار الملف المصدر (مثال: `/folder/Source.xlsx`). |
| destPath       | نص    | استعلام | مسار الملف الوجهة (مثال: `/folder/Destination.xlsx`). |
| srcStorageName | نص    | استعلام | اسم مساحة التخزين المصدر (اختياري). |
| destStorageName| نص    | استعلام | اسم مساحة التخزين الوجهة (اختياري). |
| versionId      | نص    | استعلام | مُعرّف إصدار الملف المراد نقله (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم نقل الملف بنجاح. |
| 400   | طلب غير صالح – معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على الملف المصدر. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على نقل ملف

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: يحتفظ نقل الملف بتاريخ إصداراته.*

## **كيفية إنشاء مجلد**

### معلومات واجهة برمجة تطبيقات إنشاء المجلد

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | مسار المجلد المراد إنشاؤه (مثال: `folder1/folder2/`). |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد استخدامها. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم إنشاء المجلد بنجاح. |
| 400   | طلب غير صالح – مسار أو معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على إنشاء مجلد

{{< tabs tabTotal="2" tabID="3" tabName3="الطلب" tabName4="الاستجابة" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: المسارات المجلدية حساسة لحالة الأحرف.*

## **كيفية الحصول على الملفات داخل مجلد**

### معلومات واجهة برمجة تطبيقات الحصول على الملفات

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | مسار المجلد (مثال: `/folder`). |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد استخدامها. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | إرجاع قائمة بالملفات والمجلدات الفرعية. |
| 400   | طلب غير صالح – مسار غير صحيح. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على المجلد. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على الحصول على الملفات

{{< tabs tabTotal="2" tabID="5" tabName5="الطلب" tabName6="الاستجابة" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: تُسرد الاستجابة الملفات والمجلدات الفرعية الموجودة ضمن المسار المحدد.*

## **كيفية حذف مجلد**

### معلومات واجهة برمجة تطبيقات حذف المجلد

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع    | الموقع | الوصف |
|-------------|----------|--------|--------|
| path        | نص       | المسار | مسار المجلد (مثال: `/folder`). |
| storageName | نص       | استعلام | اسم مساحة التخزين المراد استخدامها. |
| recursive   | منطقي   | استعلام | ضع القيمة `true` لحذف المجلد بشكل تكراري. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم حذف المجلد بنجاح. |
| 400   | طلب غير صالح – معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على المجلد. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على حذف مجلد

{{< tabs tabTotal="2" tabID="7" tabName7="الطلب" tabName8="الاستجابة" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: يؤدي حذف المجلد باستخدام `recursive=true` إلى إزالة محتوياته بشكل دائم.*

## **كيفية نسخ مجلد**

### معلومات واجهة برمجة تطبيقات نسخ المجلد

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل     | النوع | الموقع | الوصف |
|----------------|-------|--------|--------|
| srcPath        | نص    | المسار | مسار المجلد المصدر (مثال: `/src`). |
| destPath       | نص    | استعلام | مسار المجلد الوجهة (مثال: `/dst`). |
| srcStorageName | نص    | استعلام | اسم مساحة التخزين المصدر (اختياري). |
| destStorageName| نص    | استعلام | اسم مساحة التخزين الوجهة (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم نسخ المجلد بنجاح. |
| 400   | طلب غير صالح – معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على المجلد المصدر. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على نسخ مجلد

{{< tabs tabTotal="2" tabID="21" tabName21="الطلب" tabName22="الاستجابة" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: تُنشئ عملية النسخ مجلدًا جديدًا يحتوي على نفس المحتويات الموجودة في المجلد المصدر.*

## **كيفية نقل مجلد**

### معلومات واجهة برمجة تطبيقات نقل المجلد

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل     | النوع | الموقع | الوصف |
|----------------|-------|--------|--------|
| srcPath        | نص    | المسار | مسار المجلد المصدر (مثال: `/folder`). |
| destPath       | نص    | استعلام | مسار المجلد الوجهة (مثال: `/dst`). |
| srcStorageName | نص    | استعلام | اسم مساحة التخزين المصدر (اختياري). |
| destStorageName| نص    | استعلام | اسم مساحة التخزين الوجهة (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | تم نقل المجلد بنجاح. |
| 400   | طلب غير صالح – معاملات غير صحيحة. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على المجلد المصدر. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على نقل مجلد

{{< tabs tabTotal="2" tabID="23" tabName23="الطلب" tabName24="الاستجابة" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*ملاحظة: يحتفظ نقل المجلد بهيكله الداخلي ونسخ إصدارات ملفاته.*

## **كيفية التحقق من وجود مساحة تخزين**

### معلومات واجهة برمجة تطبيقات التحقق من وجود مساحة التخزين

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| storageName | نص    | المسار | اسم مساحة التخزين المراد التحقق من وجودها. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | إرجاع معلومة وجود مساحة التخزين (`true` أو `false`). |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على مساحة التخزين. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على التحقق من وجود مساحة التخزين

{{< tabs tabTotal="2" tabID="33" tabName33="الطلب" tabName34="الاستجابة" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية التحقق من وجود ملف أو مجلد**

### معلومات واجهة برمجة تطبيقات التحقق من وجود كائن

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | مسار الملف أو المجلد (مثال: `/file.xlsx` أو `/folder`). |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد التحقق من وجودها. |
| versionId   | نص    | استعلام | مُعرّف إصدار الملف (اختياري). |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | إرجاع معلومة وجود الكائن. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على الملف أو المجلد. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على التحقق من وجود كائن

{{< tabs tabTotal="2" tabID="37" tabName37="الطلب" tabName38="الاستجابة" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية الحصول على استخدام القرص**

### معلومات واجهة برمجة تطبيقات الحصول على استخدام القرص

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| storageName | نص    | استعلام | اسم مساحة التخزين المراد الاستعلام عنها. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | إرجاع معلومات استخدام القرص. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على الحصول على استخدام القرص

{{< tabs tabTotal="2" tabID="40" tabName40="الطلب" tabName41="الاستجابة" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية الحصول على إصدارات الملف**

### معلومات واجهة برمجة تطبيقات الحصول على إصدارات الملف

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

المعاملات المطلوبة مذكورة أدناه:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| path        | نص    | المسار | مسار الملف (مثال: `/file.xlsx`). |
| storageName | نص    | استعلام | اسم مساحة التخزين المراد الاستعلام عنها. |

**استجابات HTTP**

| الرمز | الوصف |
|-------|--------|
| 200   | إرجاع قائمة بإصدارات الملف. |
| 401   | غير مُعتمد – رمز JWT مفقود أو غير صالح. |
| 404   | لم يتم العثور على الملف. |
| 500   | خطأ داخلي في الخادم. |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) واجهة برمجة تطبيقات قابلة للوصول العام، مما يمكّن من إجراء تفاعلات REST مباشرةً من متصفح الويب.

### مثال على الحصول على إصدارات الملف

{{< tabs tabTotal="2" tabID="46" tabName46="الطلب" tabName47="الاستجابة" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}