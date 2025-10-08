---
title: حذف المجلد
second_title: Documen
linktitle: حذف المجلد
type: docs
url: /ar/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: تعرف على كيفية حذف مجلد في Aspose.Cells باستخدام deleteFolder API، بما في ذلك المعلمات وأمثلة التعليمات البرمجية
weight: 100
kwords: Excel API، Office السحابة، REST API، إدارة جداول البيانات، PDF، CSV، JSON، Markdown، حذف مجلد في ورقة عمل Excel
---
## **Excel API : حذف المجلد**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **وصف الوظيفة**

يتيح `deleteFolder` API للمستخدمين إزالة مجلد محدد من التخزين السحابي المرتبط بـ Aspose.Cells. يمكن أن يكون هذا مفيدًا للحفاظ على التنظيم وإدارة التخزين بشكل فعال.

###  معلمات الطلب**حذف المجلد** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| مسار المجلد الذي سيتم حذفه.|
| اسم التخزين| خيط| استفسار| اسم التخزين الذي يقع فيه المجلد.|
| متكرر| منطقي| استفسار| يشير إلى ما إذا كان يجب أن يكون الحذف متكررًا، وإزالة جميع المحتويات داخل المجلد أيضًا.|

### **وصف الاستجابة**

```json
{
Void
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. تُعالج حزمة تطوير البرمجيات (SDK) التفاصيل البسيطة، مما يُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
