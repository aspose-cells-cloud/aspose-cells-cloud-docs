---
title: ما هو الفرق بين معالجة الملفات المحلية ومعالجة الملفات السحابية في Aspose.Cells Cloud
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: معالجة الملفات المحلية مقابل معالجة الملفات السحابية
type: docs
url: /ar/learn/local-file-processing-vs-cloud-file-processing/
description: ما الفرق بين معالجة الملفات محليًا ومعالجة الملفات السحابية؟ تُعدّ معالجة الملفات محليًا ومعالجة الملفات السحابية نموذجين مختلفين تمامًا لإدارة البيانات، مع اختلافات جوهرية في البنية التحتية للتخزين، ومعالجة الأعمال، والوصول، وهيكل التكلفة، والأمان، والسيناريوهات المُطبقة.
weight: 10
kwords: Excel Cloud API، REST، جدول بيانات، PDF، CSV، Json، Markdown، معالجة الملفات المحلية مقابل معالجة الملفات السحابية
---
تُعدّ معالجة الملفات محليًا ومعالجة الملفات السحابية نموذجين مختلفين لإدارة البيانات، مع اختلافات جوهرية في البنية التحتية لتخزين الملفات، ومعالجة الأعمال، والوصول، وهيكل التكلفة، والأمان، والسيناريوهات المُطبقة. وتتمثل الاختلافات الرئيسية بينهما فيما يلي:

## 1. موقع تخزين الملفات والبنية الأساسية

- الملف المحلي:

تُخزَّن الملفات على أجهزة مادية يملكها المستخدم أو يُديرها، مثل القرص الصلب لجهاز الكمبيوتر الشخصي، أو الخوادم الداخلية، أو الأقراص الصلبة الخارجية المحمولة. ويمكن الوصول إلى هذه الأجهزة مباشرةً من خلال عميل السحابة Cells.
 - يتمتع العميل بالسيطرة المادية الكاملة على الأجهزة.
 - شراء وصيانة وتحديث وإخراج البنية التحتية من الخدمة هي مسؤولية المستخدم أو مؤسسته.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- ملف السحابة:

 تُخزَّن الملفات في مراكز بيانات بعيدة تُشغِّلها جهات خارجية مُزوِّدة لخدمات السحابة (التخزين السحابي Aspose، دروبوكس، AWS، السحابة Google، Azure Microsoft). تُمكِّن خدمات AWS، دروبوكس، السحابة Google، وAzure Microsoft المستخدمين من الوصول إلى التخزين السحابي Aspose.
 - يتمكن العملاء من الوصول إلى هذه الملفات عبر الإنترنت، بغض النظر عن موقع الأجهزة الأساسية وصيانتها.
 - البنية التحتية هي مسؤولية مزود الخدمة السحابية، ويستخدمها المستخدمون حسب الطلب.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. معالجة الأعمال

بغض النظر عن معالجة الملفات المحلية أو معالجة الملفات السحابية، يتم إكمال جميع عمليات المعالجة التجارية في خادم السحابة Cells،**لذلك فإن دعم الإنترنت مطلوب**.

## 3. الوصول إلى البيانات

- معالجة الملفات المحلية:

 - عادةً ما يكون الوصول مقتصرًا على الجهاز نفسه.
 - يعد التعاون بين عدة أشخاص أمرًا صعبًا.
 - عدم الراحة في تغيير المعدات أو الموقع.

- معالجة الملفات السحابية:

 - يمكنك الوصول إلى الملفات من أي جهاز (كمبيوتر، هاتف، جهاز لوحي) في أي وقت، وفي أي مكان، طالما كان لديك اتصال بالإنترنت.
 - دعم طبيعي للتعاون بين عدة أشخاص في الوقت الفعلي، حيث يمكن لمستخدمين متعددين تحرير نفس المستند في نفس الوقت، ويتعامل النظام تلقائيًا مع التحكم في الإصدار.
 - قدرة قوية على الحركة، ودعم مرن office، والعمل عن بعد.
  
## 4. هيكل التكلفة والأمان

- الملف المحلي:
  
 - تتطلب النفقات الرأسمالية المرتفعة في المرحلة المبكرة تكاليف معينة للدعم التشغيلي في المرحلة اللاحقة.
 يتم التحكم في الأمان المادي وأمان الشبكة من قبل المستخدمين أنفسهم.

- ملف السحابة:

 - استثمار أولي منخفض، ونفقات تشغيلية بشكل أساسي، والدفع عند الطلب.
 - الأمن والسلامة هي مسؤولية مزود الخدمة السحابية.

## 5. السيناريوهات القابلة للتطبيق

- الملف المحلي: لا يمكن تنفيذ عمليات الملف إلا محليًا.
- ملف السحابة: يمكن تنفيذ عمليات الملف محليًا أو في السحابة.
