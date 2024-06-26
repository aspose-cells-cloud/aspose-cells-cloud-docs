﻿---
title: PageSetu
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/specification/model/pagesetup/
description: "Aspose.Cells مواصفات النموذج السحابي: PageSetup. تعامل بسهولة مع Excel ومستندات جداول البيانات الأخرى التي تحتوي على ميزات مثل الفتح والتوليد والتحرير والتقسيم والدمج والمقارنة والتحويل"
kwords: Excel, Office, جدول البيانات, Cloud REST API, PageSetup
weight: 50
---
## **اعداد الصفحة**

 إعداد صفحة الطباعة إكسل

| اسم الخاصية| نوع الملكية| لاغية| يقرأ فقط| القيمة الافتراضية| وصف|
|:- |:- |:- |:- |:- |:- |
| اسود و ابيض| منطقية| حقيقي| خطأ شنيع|| يمثل ما إذا كانت سيتم طباعة عناصر المستند باللونين الأبيض والأسود.|
| الهامش السفلي| عائم| حقيقي| خطأ شنيع|| يمثل حجم الهامش السفلي بوحدة السنتيمتر.|
| مركزأفقيا| منطقية| حقيقي| خطأ شنيع|| تمثيل ما إذا كانت الورقة مطبوعة في المنتصف أفقيًا.|
| مركز عموديا| منطقية| حقيقي| خطأ شنيع|| تمثل ما إذا كانت الورقة مطبوعة في المنتصف عموديًا.|
| رقم الصفحة الأولى| عدد صحيح| حقيقي| خطأ شنيع|| يمثل رقم الصفحة الأولى التي سيتم استخدامها عند طباعة هذه الورقة.|
| FitToPagesTall| عدد صحيح| حقيقي| خطأ شنيع||يمثل عدد الصفحات التي سيتم تغيير حجم ورقة العمل إليها عند طباعتها. القيمة الافتراضية هي 1.|
| FitToPagesWide| عدد صحيح| حقيقي| خطأ شنيع|| يمثل عدد الصفحات التي سيتم تغيير حجم ورقة العمل إليها عند طباعتها. القيمة الافتراضية هي 1.|
| هامش التذييل| عائم| حقيقي| خطأ شنيع|| يمثل المسافة من أسفل الصفحة إلى التذييل بوحدة السنتيمتر.|
| HeaderMargin| عائم| حقيقي| خطأ شنيع|| يمثل المسافة من أعلى الصفحة إلى الرأس، بوحدة السنتيمتر.|
| IsAutoFirstPageNumber| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كان رقم الصفحة الأول قد تم تعيينه تلقائيًا.|
| IsHFAlignMargins| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كانت هوامش الرأس والتذييل تتماشى مع هوامش الصفحة. إذا كانت هذه الخاصية صحيحة، فسيتم محاذاة الرأس والتذييل الأيسر مع الهامش الأيسر، وسيتم محاذاة الرأس والتذييل الأيمن مع الهامش الأيمن. يتم تمكين هذا الخيار بشكل افتراضي.|
|IsHFDiffFirst| منطقية| حقيقي| خطأ شنيع|| صحيح يعني أن رأس/تذييل الصفحة الأولى يختلف عن الصفحات الأخرى.|
| IsHFDiffOddEven| منطقية| حقيقي| خطأ شنيع|| صحيح يعني أن رأس/تذييل الصفحات الفردية يختلف عن الصفحات الفردية.|
| IsHFScaleWithDoc| منطقية| حقيقي| خطأ شنيع|| يشير إلى ما إذا كان سيتم تغيير حجم الرأس والتذييل باستخدام مقياس المستند. ينطبق فقط على Excel 2007.|
| IsPercentScale| منطقية| حقيقي| خطأ شنيع|| إذا كانت هذه الخاصية False، فإن الخاصيتين FitToPagesWide وFitToPagesTall تتحكمان في كيفية تغيير حجم ورقة العمل.|
| الهامش الأيسر| عائم| حقيقي| خطأ شنيع|| يمثل حجم الهامش الأيسر بوحدة السنتيمتر.|
| طلب| خيط| حقيقي| خطأ شنيع|| يمثل الترتيب الذي يستخدمه Microsoft Excel لترقيم الصفحات عند طباعة ورقة عمل كبيرة.|
| توجيه| خيط| حقيقي| خطأ شنيع|| يمثل اتجاه طباعة الصفحة.|
| حجم الورق| خيط| حقيقي| خطأ شنيع|| يمثل حجم الورق.|
| منطقة الطباعة| خيط| حقيقي| خطأ شنيع|| يمثل النطاق المراد طباعته.|
| طباعة التعليقات| خيط| حقيقي| خطأ شنيع|| يمثل الطريقة التي تتم بها طباعة التعليقات مع الورقة.|
| نسخ الطباعة| عدد صحيح| حقيقي| خطأ شنيع||الحصول على عدد النسخ المراد طباعتها وتعيينها.|
| طباعة مسودة| منطقية| حقيقي| خطأ شنيع|| يمثل ما إذا كانت الورقة ستتم طباعتها بدون رسومات.|
| أخطاء الطباعة| خيط| حقيقي| خطأ شنيع|| يحدد نوع خطأ الطباعة المعروض.|
| طباعة خطوط الشبكة| منطقية| حقيقي| خطأ شنيع|| يمثل ما إذا كانت خطوط شبكة الخلايا مطبوعة على الصفحة.|
| عناوين الطباعة| منطقية| حقيقي| خطأ شنيع|| يمثل ما إذا تمت طباعة عناوين الصفوف والأعمدة مع هذه الصفحة.|
| جودة الطباعة| عدد صحيح| حقيقي| خطأ شنيع|| يمثل جودة الطباعة.|
| PrintTitleColumns| خيط| حقيقي| خطأ شنيع|| يمثل الأعمدة التي تحتوي على الخلايا المراد تكرارها على الجانب الأيسر من كل صفحة.|
| PrintTitleRows| خيط| حقيقي| خطأ شنيع|| يمثل الصفوف التي تحتوي على الخلايا المراد تكرارها في أعلى كل صفحة.|
| الهامش الأيمن| عائم| حقيقي| خطأ شنيع|| يمثل حجم الهامش الأيمن بوحدة السنتيمتر.|
| الهامش العلوي| عائم| حقيقي| خطأ شنيع|| يمثل حجم الهامش العلوي بوحدة السنتيمتر.|
| تكبير| عدد صحيح| حقيقي| خطأ شنيع|| يمثل عامل التحجيم في المئة. يجب أن يكون بين 10 و 400.|
| رأس| حاوية| حقيقي| خطأ شنيع|| يمثل رأس الصفحة.|
| تذييل| حاوية| حقيقي| خطأ شنيع||يمثل تذييل الصفحة.|
| وصلة| الفئة: الرابط| حقيقي| خطأ شنيع|||

**اسم الوالدين** : [LinkElement](/specification/model/linkelement)

