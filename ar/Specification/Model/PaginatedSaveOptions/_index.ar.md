﻿---
title: خيار الحفظ المرقّم
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/specification/model/paginatedsaveoptions/
description: "Aspose.Cells مواصفات النموذج السحابي: PaginatedSaveOptions. تعامل بسهولة مع Excel ومستندات جداول البيانات الأخرى التي تحتوي على ميزات مثل الفتح والتوليد والتحرير والتقسيم والدمج والمقارنة والتحويل"
kwords: Excel، Office، جدول البيانات، Cloud REST API، PaginatedSaveOptions
weight: 50
---
## **مرقّمة SaveOptions**

 يمثل خيارات ترقيم الصفحات.

| اسم الخاصية| نوع الملكية| لاغية| يقرأ فقط| القيمة الافتراضية| وصف|
|:- |:- |:- |:- |:- |:- |
| الخط الافتراضي| خيط| حقيقي| خطأ شنيع|| عندما تكون الأحرف الموجودة في Excel هي Unicode ولم يتم تعيينها بالخط الصحيح في نمط الخلية، فقد تظهر ككتلة في pdf أو image. قم بتعيين الخط الافتراضي مثل MingLiu أو MS Gothic لإظهار هذه الأحرف. إذا لم يتم تعيين هذه الخاصية، فسيستخدم Aspose.Cells الخط الافتراضي للنظام لإظهار أحرف Unicode هذه.|
| CheckWorkbookDefaultFont| منطقية| حقيقي| خطأ شنيع|| عندما تكون الأحرف الموجودة في Excel هي Unicode ولم يتم تعيينها بالخط الصحيح في نمط الخلية، فقد تظهر ككتلة في pdf، image. اضبط هذا على "صحيح" لمحاولة استخدام الخط الافتراضي للمصنف لإظهار هذه الأحرف أولاً.|
| توافق CheckFont| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كان سيتم التحقق من توافق الخط لكل حرف في النص.|
| IsFontSubstitutionCharGranularity| منطقية| حقيقي| خطأ شنيع||يشير إلى ما إذا كان سيتم استبدال خط الحرف فقط عندما لا يكون خط الخلية متوافقًا معه.|
| OnePagePerSheet| منطقية| حقيقي| خطأ شنيع|| إذا كانت قيمة OnePagePerSheet صحيحة، فسيتم إخراج كل محتوى ورقة واحدة إلى صفحة واحدة فقط في النتيجة. سيكون حجم الورق الخاص بإعداد الصفحات غير صالح، وستظل الإعدادات الأخرى لإعداد الصفحات سارية المفعول.|
| كافة الأعمدة في OnePagePerSheet| منطقية| حقيقي| خطأ شنيع|| إذا كانت قيمة AllColumnsInOnePagePerSheet صحيحة، فسيتم إخراج كل محتوى العمود في ورقة واحدة إلى صفحة واحدة فقط في النتيجة. سيتم تجاهل عرض حجم الورق لإعداد الصفحات، وستظل الإعدادات الأخرى لإعداد الصفحات سارية المفعول.|
| تجاهل الخطأ| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كنت بحاجة إلى إخفاء الخطأ أثناء العرض. يمكن أن يكون الخطأ خطأ في الشكل أو الصورة أو عرض المخطط وما إلى ذلك.|
| إخراج صفحة فارغة عندما لا شيء للطباعة| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كان سيتم إخراج صفحة فارغة عندما لا يكون هناك أي شيء لطباعته.|
| فهرس الصفحة| عدد صحيح| حقيقي| خطأ شنيع|| الحصول على أو تعيين الفهرس المستند إلى 0 للصفحة الأولى المراد حفظها.|
| عدد الصفحات| عدد صحيح| حقيقي| خطأ شنيع|| الحصول على أو تعيين عدد الصفحات المراد حفظها.|
| نوع صفحة الطباعة| خيط| حقيقي| خطأ شنيع|| يشير إلى الصفحات التي لن تتم طباعتها.|
| نوع خط الشبكة| خيط| حقيقي| خطأ شنيع|| الحصول على أو تعيين نوع خط الشبكة.|
| نوع النص المتقاطع| خيط| حقيقي| خطأ شنيع|| الحصول على أو تعيين عرض نوع النص عندما يكون عرض النص أكبر من عرض الخلية.|
| DefaultEditLanguage| خيط| حقيقي| خطأ شنيع|| الحصول على لغة التحرير الافتراضية أو تعيينها.|
| EmfRenderSetting| خيط| حقيقي| خطأ شنيع|||
| MergeAreas| منطقية| حقيقي| خطأ شنيع|||
| فرز الأسماء الخارجية| منطقية| حقيقي| خطأ شنيع|||
| UpdateSmartArt| منطقية| حقيقي| خطأ شنيع|||
| حفظ التنسيق| خيط| حقيقي| خطأ شنيع|||
| CachedFileFolder| خيط| حقيقي| خطأ شنيع|||
| امسح البيانات| منطقية| حقيقي| خطأ شنيع|||
| إنشاء دليل| منطقية| حقيقي| خطأ شنيع|||
| تمكينHTTPCompression| منطقية| حقيقي| خطأ شنيع|||
| RefreshChartCache| منطقية| حقيقي| خطأ شنيع|||
| أسماء الفرز| منطقية| حقيقي| خطأ شنيع|||
| التحقق من صحة المناطق المندمجة| منطقية| حقيقي| خطأ شنيع|||

**اسم الوالدين** : [خيارات الحفظ](/specification/model/saveoptions)

**اسم الاطفال** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [خيارات PptxSave](pptxsaveoptions) 
	-  [خيارات XpsSave](xpssaveoptions) 
