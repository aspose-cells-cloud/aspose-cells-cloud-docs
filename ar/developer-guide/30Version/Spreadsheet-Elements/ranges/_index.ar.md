---
title: "العمل مع النطاقات في Excel"
second_title: "المستند"
linktype: "النطاق"
type: docs
url: /ar/ranges/
aliases: [  /ar/working-with-ranges/ ]
keywords: "Aspose.Cells, النطاق في Excel, واجهة REST API, SDK, .NET, Java, Python, دمج الخلايا, نسخ نطاق, تعيين قيمة النطاق"
description: "تعرّف على كيفية استرجاع النطاقات وتعديلها وتنسيقها ودمجها ونقلها ونسخها باستخدام واجهة Aspose.Cells Cloud REST API. يتضمّن أمثلة لرموز SDK مكتوبة بلغات .NET وJava وPython وغيرها."
weight: 100
ArticleTitle: "العمل مع النطاقات في Excel – مستندات Aspose.Cells Cloud"
---

يمثّل **النطاق (Range)** خليةً واحدة أو صفًّا كاملاً أو عمودًا كاملاً أو كتلة متصلة من الخلايا، أو نطاقًا ثلاثي الأبعاد (3-D) يمتد عبر ورقات عمل متعددة.

## العمل مع النطاقات في ملف Excel

توفر واجهة Aspose.Cells Cloud REST API نقاط نهاية مخصّصة لكل عملية نطاق. وتشير القائمة التالية إلى أمثلة تفصيلية للاستخدام، مع ذكر طريقة HTTP المقابلة ونقطة النهاية لسهولة المرجع السريع.

- [الحصول على النطاقات المسماة داخل المصنف](/cells/get-named-ranges-inside-the-workbook/) – يسترجع جميع النطاقات المسماة المعرّفة داخل مصنف، مع إرجاع عناوينها ونطاق تطبيقها (الscope). **واجهة برمجة التطبيقات (API)**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [الحصول على بيانات الخلايا بناءً على النطاق المسماة](/cells/get-cells-data-based-on-named-range/) – يُعيد قيم الخلايا التي تنتمي إلى نطاق مُسَمًّى مُحدّد. **واجهة برمجة التطبيقات (API)**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [تغيير ارتفاع الصفوف داخل النطاق](/cells/cells/change-heights-of-rows-inside-the-range/) – يضبط ارتفاع كل صف يقع داخل النطاق المُعطى. **واجهة برمجة التطبيقات (API)**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [تغيير عرض الأعمدة داخل النطاق](/cells/cells/change-widths-of-columns-inside-the-range/) – يعدل عرض الأعمدة المتقاطعة مع النطاق. **واجهة برمجة التطبيقات (API)**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [دمج مجموعة من الخلايا في خلية واحدة](/cells/combines-a-range-of-cells-into-a-single-cell/) – يدمج الخلايا المحدّدة في خلية واحدة، مع الحفاظ على القيمة الموجودة في الخلية العلوية اليسرى. **واجهة برمجة التطبيقات (API)**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [نسخ نطاق داخل ورقة عمل مع خيارات اللصق](/cells/copy-range-in-a-worksheet-with-paste-options/) – ينسخ نطاقًا مصدريًّا إلى نطاقٍ مقصود مع إمكانية تحديد نوع اللصق (قيم، تنسيقات، صيغ، إلخ). **واجهة برمجة التطبيقات (API)**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [تطبيق التنسيق على النطاق](/cells/set-the-style-of-the-range/) – يطبّق تنسيقات الخط والتعبئة والحدود والمحاذاة على كل خلية داخل النطاق. **واجهة برمجة التطبيقات (API)**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [إلغاء دمج الخلايا المدمجة داخل النطاق](/cells/unmerge-merged-cells-of-the-range/) – يعكس عملية الدمج السابقة، مُستعيدًا الخلايا الفردية الأصلية. **واجهة برمجة التطبيقات (API)**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [نقل النطاق المسماة مع ورقة عمل Excel](/cells/move-a-named-ranged-with-a-excel-worksheet/) – يعيد تحديد موقع النطاق المسماة إلى عنوان جديد داخل نفس ورقة العمل أو إلى ورقة عمل أخرى. **واجهة برمجة التطبيقات (API)**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [تعيين قيمة النطاق في ورقة عمل Excel](/cells/ranges/set-value/) – يكتب قيمةً واحدة أو مصفوفة من القيم داخل النطاق المحدّد. **واجهة برمجة التطبيقات (API)**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

جميع الطلبات والاستجابات بصيغة JSON. تأكد من تضمين رأس `Authorization` مع رمز وصولك للتوثيق.