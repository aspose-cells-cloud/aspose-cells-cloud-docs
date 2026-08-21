---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud لإزالة التكرار في substrings – تنظيف النص المتكرر في Excel"
second_title: "مستند"
ArticleTitle: "أداة إزالة substrings المتكررة في Excel – تنظيف النصوص المتكررة في الخلايا"
linktype: "docs"
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells, substrings متكررة, واجهة برمجة تطبيقات Excel, تنظيف النصوص, سحابة"
description: "قم بإزالة substrings المتكررة من خلايا Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud مع الحفاظ على التنسيق والتحقق من الصحة."
weight: 100
---

قم بإزالة substrings المتكررة من خلايا Excel باستخدام كشف ذكي. احتفظ بالتنسيق الأصلي دون تغيير أثناء إزالة النصوص الزائدة باستخدام واجهة برمجة تطبيقات إزالة التكرار في Aspose.Cells.

## **مقدمة**: إزالة الأحرف غير المرغوب فيها بدقة

تقوم واجهة برمجة تطبيقات "منقي substrings المتكررة" بإزالة substrings المتكررة داخل خلايا محددة ضمن نطاق Excel، مع الحفاظ على تنسيق الخلايا وتحقق البيانات والهياكل الأخرى الخاصة بملف العمل. وتُعالج كل خلية على حدة، مع الاحتفاظ بظهور substring المتكرر الأول فقط.

### **خيارات مصدر البيانات**

| الحقل       | النوع  | الإجبارية | الوصف                                                     |
| ----------- | ------ | ---------- | --------------------------------------------------------- |
| `workbook`  | ملف    | نعم        | ملف workbook Excel (.xlsx, .xlsm)                         |
| `range`     | سلسلة | نعم        | النطاق المستهدف للمعالجة (مثل "A1:D100"، "Sheet1!A:D")    |

### **خيارات الفواصل**

| الحقل                               | النوع     | القيمة المبدئية | الوصف                                                                                                                                               |
| ----------------------------------- | --------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                        | سلسلة    | `"preset"`       | الخيارات: `preset`، `custom`، `comma`، `semicolon`، `space`، `tab`، `line-break` أو سلسلة فواصل مخصصة (تُعامل الأحرف المتعددة كفصل مركب)             |
| `treatConsecutiveDelimitersAsOne`  | منطقي    | `false`          | دمج الفواصل المتتالية في مُفرِّق واحد فقط                                                                                                          |
| `caseSensitive`                    | منطقي    | `false`          | يحدد ما إذا كانت المقارنة حساسة لحالة الأحرف. وعند القيمة `false`، تُتجاهل حالة الأحرف أثناء اكتشاف التكرار.                                        |

## **واجهة برمجة تطبيقات RemoveDuplicateSubstrings**

### واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معاملات الطلب الخاصة بواجهة برمجة تطبيقات **RemoveDuplicateSubstrings** هي:

| اسم المعامل                     | النوع   | المسار/سلسلة الاستعلام/جسم الطلب HTTP | الوصف                                                                                                                                                                             |
| :------------------------------ | :------ | :------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | ملف    | FormData                              | ملف جدول البيانات المراد معالجته. تشمل التنسيقات المدعومة XLSX وXLS وODS وCSV وما إلى ذلك.                                                                                        |
| delimiters                      | سلسلة  | Query                                 | يحدد حرفًا أو أكثر كفواصل تُستخدم لتقسيم محتوى الخلية إلى substrings للكشف عن التكرار وإزالته. يمكن تحديد فواصل متعددة (مثل `",;"`).                                               |
| treatConsecutiveDelimitersAsOne | منطقي | Query                                 | عند تعيينها على `true`، تُعامل أحرف الفواصل المتتالية كمُفرِّق واحد. وعند القيمة `false`، تُعالَج كل فاصلة على حدة.                                                               |
| caseSensitive                   | منطقي | Query                                 | عند القيمة `true`، يأخذ الكشف عن التكرار حالة الأحرف بعين الاعتبار (مثل "Text" ≠ "text"). وعند القيمة `false`، تُتجاهل حالة الأحرف أثناء مقارنة التكرار.                           |
| worksheet                       | سلسلة | Query                                 | _(اختياري)_ اسم ورقة العمل التي سيتم تطبيق إزالة substrings المتكررة عليها. وعند حذفها، تُطبَّق العملية على الورقة الأولى فقط.                                                   |
| range                           | سلسلة | Query                                 | _(اختياري)_ النطاق الخلوي الذي سيتم تطبيق إزالة substrings المتكررة عليه (مثل `"A1:C10"`). وعند حذفها، تُطبَّق العملية على جميع الخلايا المستخدمة في ورقة العمل المحددة.           |
| outPath                         | سلسلة | Query                                 | _(اختياري)_ مسار مجلد مخزن السحابة الذي سيتم حفظ workbook المعالج فيه. وعند حذفها، يُحفظ الملف في المجلد الأصلي.                                                                 |
| outStorageName                  | سلسلة | Query                                 | اسم مخزن السحابة الذي سيتم حفظ ملف الإخراج فيه.                                                                                                                                  |
| region                          | سلسلة | Query                                 | _(اختياري)_ يضبط الإعدادات الإقليمية لمعالجة النص، والتي قد تؤثر على تفسير الفواصل وقواعد الحساسية لحالة الأحرف لبعض اللغات (مثل `"en-US"`, `"tr-TR"`).                           |
| password                        | سلسلة | Query                                 | _(اختياري)_ إذا كان جدول البيانات المرفوع محميًا بكلمة مرور، فوفّر كلمة المرور لفتح الملف ومعالجته.                                                                              |

**مثال على الطلب (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

### **الاستجابة**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### **رموز الحالة**

| الكود | المعنى                                  | الوصف                                                                                         |
|------|-----------------------------------------|------------------------------------------------------------------------------------------------|
| 200  | ناجح (OK)                               | نجح الطلب ويُعاد workbook المعالج.                                                             |
| 202  | مقبول (Accepted)                        | تم قبول الطلب للمعالجة غير المتزامنة.                                                         |
| 400  | طلب غير صالح (Bad Request)              | الطلب غير مهيأ بشكل صحيح أو يحتوي على معاملات غير صالحة.                                      |
| 401  | غير مخوّل (Unauthorized)                 | فشلت المصادقة أو رمز المصادقة مفقود/غير صالح.                                                |
| 404  | غير موجود (Not Found)                   | لا يمكن العثور على workbook أو المورد المحدد.                                                 |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | حدث خطأ غير متوقع من جانب الخادم.                                                             |

## أين يجب استخدام واجهة برمجة تطبيقات إزالة substrings المتكررة؟

- **سيناريوهات تنظيف البيانات وتوحيدها**: تنظيف العلامات مثل `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **البيانات التقنية والتشغيلية**: تنظيف إدخالات السجلات ذات رموز الأخطاء المتكررة، وإزالة معرّفات الحاويات/الرفوف المتكررة، وما إلى ذلك.
- **إدارة المحتوى والوسائط**: إزالة تكرار علامات المهارات، وإزالة إدخالات الشهادات الزائدة.

## لماذا يجب استخدام واجهة برمجة تطبيقات إزالة substrings المتكررة؟

- **أتمتة المهام اليدوية**: تخلّص من التعديلات المُملة وقلّل من أخطاء البشر.  
- **الحفاظ على سلامة البيانات**: تبقى ألوان الخلايا والخطوط والحدود والتنسيق الشرطي دون تغيير؛ وتُحتفظ بقوائم التنزّل وقواعد التحقق.  
- **معالجة مرنة**: لا تعتمد على نوع الفاصل، وتتيح التحكم الاختياري في الحساسية لحالة الأحرف وحماية الرؤوس.  
- **مصممة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يُمكّن من تطوير سريع مع توثيق شامل.  
- **فعالة من حيث التكلفة**: تتم العملية في السحابة، مما يلغي الحاجة إلى تخزين الملفات الوسيطة محليًا.  

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع التطوير. وتتولى SDK التفاصيل الأساسية، مما يسمح لك بتنفيذ إزالة substrings المتكررة للخلايا برمز معدود. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

توضّح أمثلة الشيفرة التالية كيفية إجراء مكالمات لخدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}
---