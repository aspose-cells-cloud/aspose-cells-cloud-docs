---
title: الملفات والتخزين
second_title: Documen
type: docs
url: /ar/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: دليل شامل لاستخدام سحابة Aspose Cells لعمليات تخزين الملفات، بما في ذلك تحميلها وتنزيلها وإدارتها. يدعم SDK لغات برمجة متنوعة مثل Android وGo وNodeJS وRuby وSwift.
weight: 100
kwords: Aspose Cells، التخزين السحابي، REST API، إدارة الملفات، Excel، PDF، CSV، JSON، Markdow
---
 يوفر Aspose.Cells Cloud وظائف مساعدة شاملة للتعامل مع الملفات المُحمّلة على Aspose.Cells Cloud Storage أو أي خدمة تخزين سحابي أخرى من اختيارك. للحصول على مساعدة في إعداد خدمة تخزين خارجية، يُرجى مراجعة[Aspose مواضيع مساعدة واجهة المستخدم السحابية](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**توفر Aspose.Cells Cloud مجموعة من واجهات برمجة التطبيقات الخاصة بتشغيل الملفات والمجلدات والتخزين.**

## **كيفية تحميل ملف**

### تحميل الملف API معلومات

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق|مسار تحميل الملف، بما في ذلك اسم الملف وامتداده (مثلاً، /file.ext أو /Folder 1/file.ext). إذا كان المحتوى متعدد الأجزاء ولم يتضمن المسار اسم الملف، فسيحاول استرجاعه من معلمة اسم الملف في رأس Content-Disposition.|
| ملف| ملف| نموذج البيانات| الملف للتحميل|
| اسم التخزين| خيط| استفسار| اسم التخزين|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال لتحميل الملف

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية تنزيل ملف**

### تنزيل الملف API المعلومات

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار الملف (على سبيل المثال، '/folder/file.ext')|
| اسم التخزين| خيط| استفسار| اسم التخزين|
| معرف الإصدار| خيط| استفسار| معرف إصدار الملف للتنزيل|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### تنزيل ملف المثال

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```bash
{
    Stream
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية حذف ملف**

### معلومات حذف الملف API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار الملف (على سبيل المثال، '/folder/file.ext')|
| اسم التخزين| خيط| استفسار| اسم التخزين|
| معرف الإصدار| خيط| استفسار| معرف إصدار الملف الذي يجب حذفه|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية نسخ ملف**

### نسخ الملف API معلومات

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| مسار src| خيط| طريق| مسار ملف المصدر (على سبيل المثال، '/folder/file.ext')|
|مسار الوجهة| خيط| استفسار| مسار ملف الوجهة|
| اسم تخزين src| خيط| استفسار| اسم مصدر التخزين|
| اسم التخزين| خيط| استفسار| اسم تخزين الوجهة|
| معرف الإصدار| خيط| استفسار| معرف إصدار الملف الذي سيتم نسخه|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال على نسخ الملف

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

{{< tab tabNum="17" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية نقل ملف**

### نقل الملف API معلومات

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| مسار src| خيط| طريق| مسار ملف المصدر (على سبيل المثال، '/src.ext')|
|مسار الوجهة| خيط| استفسار| مسار ملف الوجهة (على سبيل المثال، '/dest.ext')|
| اسم تخزين src| خيط| استفسار| اسم مصدر التخزين|
| اسم التخزين| خيط| استفسار| اسم تخزين الوجهة|
| معرف الإصدار| خيط| استفسار| معرف إصدار الملف الذي سيتم نقله|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال لنقل الملف

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية إنشاء مجلد**

### إنشاء مجلد API معلومات

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق|مسار المجلد المراد إنشاؤه (على سبيل المثال، 'المجلد_1/مجلد_2/') |
| اسم التخزين| خيط| استفسار| اسم التخزين|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال لإنشاء مجلد

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية الحصول على الملفات في مجلد**

### الحصول على معلومات الملفات API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار المجلد (على سبيل المثال، '/folder')|
| اسم التخزين| خيط| استفسار| اسم التخزين|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال للحصول على الملفات

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية حذف مجلد**

### حذف معلومات المجلد API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار المجلد (على سبيل المثال، '/folder')|
| اسم التخزين| خيط| استفسار| اسم التخزين|
| متكرر| منطقي| استفسار|خطأ شنيع|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال على حذف المجلد

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}

{{< tab tabNum="7" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية نسخ مجلد**

### نسخ معلومات المجلد API

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| مسار src| خيط| طريق| مسار المجلد المصدر (على سبيل المثال، '/src')|
|مسار الوجهة| خيط| استفسار| مسار المجلد الوجهة (على سبيل المثال، '/dst')|
| اسم تخزين src| خيط| استفسار| اسم مصدر التخزين|
| اسم التخزين| خيط| استفسار| اسم تخزين الوجهة|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال على نسخ المجلد

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية نقل مجلد**

### نقل المجلد API معلومات

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| مسار src| خيط| طريق| مسار المجلد الذي سيتم نقله (على سبيل المثال، '/folder')|
|مسار الوجهة| خيط| استفسار| مسار المجلد الوجهة الذي سيتم النقل إليه (على سبيل المثال، '/dst')|
| اسم تخزين src| خيط| استفسار| اسم مصدر التخزين|
| اسم التخزين| خيط| استفسار| اسم تخزين الوجهة|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال لنقل المجلد

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية التحقق من وجود مساحة تخزين**

### معلومات التخزين API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم التخزين| خيط| طريق| اسم التخزين|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال على وجود مساحة تخزين

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```bash
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية التحقق من وجود ملف أو مجلد**

### الكائن موجود API معلومات

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار الملف أو المجلد (على سبيل المثال، '/file.ext' أو '/folder')|
| اسم التخزين| خيط| استفسار| اسم التخزين|
| معرف الإصدار| خيط| استفسار| معرف إصدار الملف|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال على وجود الكائن

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```bash
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية الحصول على استخدام القرص**

### الحصول على معلومات استخدام القرص API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم التخزين| خيط| استفسار| اسم التخزين|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### الحصول على مثال لاستخدام القرص

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}

{{< tab tabNum="40" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
```

{{< /tab >}}
{{< /tabs >}}

## **كيفية الحصول على إصدارات الملفات**

### الحصول على معلومات إصدارات الملف API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار الملف (على سبيل المثال، '/file.ext')|
| اسم التخزين| خيط| استفسار| اسم التخزين|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### مثال للحصول على إصدارات الملف

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى السحابة API باستخدام cURL.

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}
