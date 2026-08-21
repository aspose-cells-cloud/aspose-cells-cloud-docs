---
title: "العمل مع جداول البيانات المحورية باستخدام مهمة CellsObjectOperate"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "واجهة برمجة تطبيقات جداول البيانات المحورية لـ Aspose Cells، CellsObjectOperate، واجهة برمجة تطبيقات Excel عبر الويب"
description: "تعلم كيفية إنشاء جدول بيانات محوري في Excel باستخدام مهمة CellsObjectOperate من Aspose.Cells Cloud. يتضمن مثالًا باستخدام cURL، ودليل المعاملات، وروابط لواجهات برمجة التطبيقات (SDKs)."
weight: 10
---

تقوم هذه **واجهة برمجة تطبيقات REST** بإنشاء جدول بيانات محوري باستخدام المهمة **CellsObjectOperate**.

**PivotTableOperateParameter**

| اسم المعامل              | النوع          | الوصف                                                                 |
|-------------------------|----------------|------------------------------------------------------------------------|
| DestCellName            | نص (string)    | الخلية العلوية اليسرى للجدول المحوري (مثل `C1`).                      |
| SourceData              | نص (string)    | النطاق الذي يحتوي على البيانات المصدرية (مثل `Sheet2!A1:E8`).         |
| TableName               | نص (string)    | الاسم المعين للجدول المحوري الجديد.                                    |
| UseSameSource           | نص (string)    | `true` / `false` – ما إذا كان الجدول المحوري يستخدم ملف العمل نفسه كمصدر. |
| PivotTableIndex         | عدد صحيح (integer) | فهرس الجدول المحوري عند وجود جداول متعددة في الورقة.                 |
| PivotFieldRows          | مصفوفة من الأعداد الصحيحة (integer[]) | فهارس المجالات (البداية من الصفر) التي سيتم وضعها في منطقة الصفوف. |
| PivotFieldColumns       | مصفوفة من الأعداد الصحيحة (integer[]) | فهارس المجالات (البداية من الصفر) التي سيتم وضعها في منطقة الأعمدة. |
| PivotFieldData          | مصفوفة من الأعداد الصحيحة (integer[]) | فهارس المجالات (البداية من الصفر) التي سيتم تجميعها كبيانات.      |

## واجهة برمجة تطبيقات REST

| **واجهة برمجة التطبيقات** | **النوع** | **الوصف** | **الرابط إلى المورد** |
|--------------------------|-----------|------------|----------------------|
| /cells/task/runtask       | POST      | تشغيل المهمة | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

تعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) على واجهة برمجة تطبيقات قابلة للوصول من خارج النظام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

### المتطلبات المسبقة
قبل استدعاء واجهة برمجة التطبيقات، يجب عليك:

1. التسجيل في حساب Aspose.Cloud وإنشاء تطبيق للحصول على **مُعرّف العميل (client ID)** و**سر العميل (client secret)**.  
2. طلب **رمز JWT** من نقطة النهاية `/connect/token` باستخدام بيانات اعتماد العميل.  
3. تضمين الرمز في رأس الطلب `Authorization: Bearer <jwt token>` في كل طلب.  

يمكنك الآن استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# مثال على cURL – استيراد البيانات (الخطوة 1)
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jwt token>" \
  -d '
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Book1.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <BatchData>
            <!-- صفوف نموذجية – مُعرَض عدد قليل منها فقط للإيجاز -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>نوع الرياضة</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>السنة</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>الربع</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>المبيعات</value></CellValue>
            <!-- …صفوف إضافية مُهمَلة للإيجاز… -->
          </BatchData>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>CellsObjectOperate</TaskType>
      <CellsObjectOperateTaskParameter>
        <OperateObject>
          <OperateObjectType>ListObject</OperateObjectType>
          <Position>
            <Workbook>
              <FileSourceType>InMemoryFiles</FileSourceType>
              <FilePath>Book1.xlsx</FilePath>
            </Workbook>
            <SheetName>Sheet1</SheetName>
            <ListObjectIndex>0</ListObjectIndex>
          </Position>
        </OperateObject>

        <PivotTableOperateParameter>
          <OperateType>Add</OperateType>
          <SourceData>=Sheet2!A1:E8</SourceData>
          <DestCellName>C1</DestCellName>
          <TableName>TestPivot</TableName>
          <UseSameSource>true</UseSameSource>
          <PivotTableIndex>0</PivotTableIndex>
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
        </PivotTableOperateParameter>

        <DestinationWorkbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>Book001.xlsx</FilePath>
        </DestinationWorkbook>
      </CellsObjectOperateTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Book001.xlsx</InputFile>
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
قد تكون رموز حالة HTTP الممكنة كما يلي:
- **200 OK** – تم إنشاء الجدول المحوري بنجاح. تحتوي نص الاستجابة على `مُعرّف المهمة (TaskId)` يمكن استخدامه للاستعلام عن حالة العملية.
- **400 Bad Request** – payload XML غير صالح أو معاملات مطلوبة مفقودة.
- **401 Unauthorized** – رمز JWT مفقود أو غير صالح.
- **500 Internal Server Error** – خطأ غير متوقع في الخادم.

مثال على استجابة ناجحة (XML):

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## مجموعة أدوات التطوير (Cloud SDK Family)

استخدام أدوات التطوير (SDKs) هو أفضل طريقة لتسريع عملية التطوير. فتتولى أدوات SDK إدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK مختلفة: