---
title: "CellsObjectOperate Görevi Kullanılarak Pivot Tablolarla Çalışmak"
type: docs
url: /tr/tasks/cells-object-operate/pivottable/
aliases: [  /tr/working-with-pivot-table-using-cellsobjectoperate-task/ ]
keywords: "Aspose Cells pivot tablo API'si, CellsObjectOperate, Excel REST API"
description: "Aspose.Cells Cloud’ın CellsObjectOperate görevi ile Excel’de pivot tablo nasıl oluşturulacağını öğrenin. cURL örneği, parametre kılavuzu ve SDK referanslarını içerir."
weight: 10
---

Bu REST API, **CellsObjectOperate** görevini kullanarak bir pivot tablo **oluşturur**.

**PivotTableOperateParameter**

| Parametre Adı       | Tür           | Açıklama                                                                 |
|---------------------|---------------|--------------------------------------------------------------------------|
| DestCellName        | string        | Pivot tablonun sol‑üst hücresi (örn. `C1`).                              |
| SourceData          | string        | Kaynak verileri içeren aralık (örn. `Sheet2!A1:E8`).                    |
| TableName           | string        | Yeni pivot tabloya verilen isim.                                         |
| UseSameSource       | string        | `true` / `false` – Pivot tablonun aynı kaynak çalışma kitabını kullanıp kullanmadığı. |
| PivotTableIndex     | integer       | Çalışma sayfasında birden fazla tablo olduğunda pivot tablonun indeksi.  |
| PivotFieldRows      | integer[]     | Satırlar alanına yerleştirilecek alanların sıfır‑tabanlı indeksleri.     |
| PivotFieldColumns   | integer[]     | Sütunlar alanına yerleştirilecek alanların sıfır‑tabanlı indeksleri.     |
| PivotFieldData      | integer[]     | Veri olarak özetlenecek alanların sıfır‑tabanlı indeksleri.              |

## REST API

| **API**               | **Tür** | **Açıklama** | **Kaynak Bağlantısı** |
|-----------------------|---------|--------------|------------------------|
| /cells/task/runtask   | POST    | Görevi Çalıştır | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Öncelikli Gereksinimler
API’yi çağırmadan önce şunları yapmanız gerekir:

1. Bir Aspose.Cloud hesabı oluşturun ve bir uygulama oluşturarak **istemci kimliği** ve **istemci gizli anahtarı** alın.  
2. İstemci kimlik bilgilerini kullanarak `/connect/token` uç noktasından bir **JWT belirteci** isteyin.  
3. Her isteğin `Authorization: Bearer <jwt token>` başlığına belirteci ekleyin.  

Artık **cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetlerine erişebilirsiniz.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# cURL örneği – veri içe aktarma (adım 1)
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
            <!-- Örnek satırlar – sadece kısa olması için bazıları gösterilmiştir -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Spor</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Yıl</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Çeyrek</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Satışlar</value></CellValue>
            <!-- …daha fazla satır açıklık olması için atlanmıştır… -->
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
Mümkün HTTP durum kodları:
- **200 OK** – Pivot tablo başarıyla oluşturuldu. Yanıt gövdesi, işlem durumunu sorgulamak için kullanılabilen bir `TaskId` içerir.
- **400 Bad Request** – Geçersiz XML yükü veya eksik gerekli parametreler.
- **401 Unauthorized** – JWT belirteci eksik veya geçersiz.
- **500 Internal Server Error** – Beklenmeyen sunucu‑tarafı hata.

Başarılı yanıt örneği (XML):

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

## Bulut SDK Geliştirme Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir: