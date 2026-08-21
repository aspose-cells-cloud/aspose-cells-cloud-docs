---
title: "CellsObjectOperate 작업을 사용한 피벗 테이블 작업"
type: docs
url: /tasks/cells-object-operate/pivottable/
aliases: [/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "Aspose Cells 피벗 테이블 API, CellsObjectOperate, Excel REST API"
description: "Aspose.Cells Cloud의 CellsObjectOperate 작업을 사용하여 Excel에서 피벗 테이블을 생성하는 방법을 알아보세요. cURL 예제, 매개변수 가이드, SDK 참조가 포함됩니다."
weight: 10
---

이 REST API는 **CellsObjectOperate** 작업을 사용하여 **피벗 테이블을 생성**합니다.

**PivotTableOperateParameter**

| 매개변수 이름         | 유형          | 설명                                                                 |
|----------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName         | string        | 피벗 테이블의 좌상단 셀 (예: `C1`).                                         |
| SourceData           | string        | 원본 데이터가 포함된 범위 (예: `Sheet2!A1:E8`).                             |
| TableName            | string        | 새 피벗 테이블에 할당된 이름.                                               |
| UseSameSource        | string        | `true` / `false` – 피벗 테이블이 동일한 원본 워크북을 사용하는지 여부.     |
| PivotTableIndex      | integer       | 워크시트에 여러 테이블이 존재할 경우 피벗 테이블의 인덱스.                  |
| PivotFieldRows       | integer[]     | 행 영역에 배치할 필드의 0부터 시작하는 인덱스.                              |
| PivotFieldColumns    | integer[]     | 열 영역에 배치할 필드의 0부터 시작하는 인덱스.                              |
| PivotFieldData       | integer[]     | 데이터로 집계할 필드의 0부터 시작하는 인덱스.                               |

## REST API

| **API**               | **유형** | **설명** | **리소스 링크** |
|-----------------------|----------|----------|-------------------|
| /cells/task/runtask   | POST     | 작업 실행 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### 사전 조건
API를 호출하기 전에 다음을 수행해야 합니다:

1. Aspose.Cloud 계정을 등록하고 애플리케이션을 생성하여 **클라이언트 ID** 및 **클라이언트 비밀키**를 받습니다.  
2. 클라이언트 자격 증명을 사용하여 `/connect/token` 엔드포인트에서 **JWT 토큰**을 요청합니다.  
3. 모든 요청의 `Authorization: Bearer <jwt token>` 헤더에 토큰을 포함시킵니다.  

이제 **cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 접근할 수 있습니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# cURL 예제 – 데이터 가져오기 (단계 1)
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
            <!-- 샘플 행 – 간결함을 위해 일부만 표시 -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>스포츠</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>연도</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>분기</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>매출</value></CellValue>
            <!-- …명확성을 위해 추가 행 생략… -->
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
발생 가능한 HTTP 상태 코드:
- **200 OK** – 피벗 테이블이 성공적으로 생성됨. 응답 본문에는 작업 상태를 조회하는 데 사용할 수 있는 `TaskId`가 포함됨.
- **400 Bad Request** – 잘못된 XML 페이로드 또는 필수 매개변수 누락.
- **401 Unauthorized** – JWT 토큰 누락 또는 유효하지 않음.
- **500 Internal Server Error** – 예기치 않은 서버 측 오류.

성공 응답 예시(XML):

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

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:
---