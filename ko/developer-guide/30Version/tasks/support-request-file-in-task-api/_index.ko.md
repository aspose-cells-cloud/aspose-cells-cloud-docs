---
title: "Task API에서 요청 파일 지원"
second_title: "문서"
type: docs
url: /ko/tasks/support-request-file/
aliases: [  /ko/support-request-file-in-task-api/ ]
keywords: "Aspose.Cells, REST API, Excel, 클라우드"
description: "Aspose.Cells Cloud API는 Excel 워크북에 대한 요청 파일의 작업 기반 처리를 가능하게 합니다."
weight: 10
ArticleTitle: "Aspose.Cells Task API에서 요청 파일 지원"
---

## REST API

| **API** | **유형** | **설명** | **리소스 링크** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | 작업 실행 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**요청 매개변수**

| 매개변수 | 유형 | 필수 여부 | 설명 |
|-----------|------|----------|-------------|
| TaskDescription | object | 예 | 단일 작업 정의를 담은 컨테이너입니다. |
| TaskType | string | 예 | 작업 유형 (예: `ImportData`, `SaveResult`) |
| Workbook.FileSourceType | string | 예 | 워크북 파일의 소스 (`CloudFileSystem`, `InMemoryFiles`) |
| Workbook.FilePath | string | 예 | 선택한 소스 내 워크북 파일의 경로 |
| ImportBatchDataOption.DestinationWorksheet | string | 예 | 데이터를 가져올 대상 워크시트 이름 |
| ImportBatchDataOption.IsInsert | boolean | 예 | 행을 삽입할지 여부 (`true`: 삽입, `false`: 덮어쓰기) |
| ImportBatchDataOption.Source.FileSourceType | string | 예 | 요청 파일의 소스 (`RequestFiles`) |
| ImportBatchDataOption.Source.FilePath | string | 예 | 배치 데이터를 포함한 요청 파일의 경로 |
| SaveResultTaskParameter.ResultSource | string | 예 | 결과 파일의 소스 (`InMemoryFiles`) |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | 예 | 결과의 저장 대상 유형 (`CloudFileSystem`) |
| SaveResultTaskParameter.ResultDestination.InputFile | string | 예 | 입력 워크북 파일 이름 |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | 예 | 원하는 출력 파일 이름 |

**응답**

| 필드 | 유형 | 설명 |
|-------|------|-------------|
| Code | integer | HTTP 상태 코드 (예: 성공 시 200) |
| Status | string | 작업 상태 (`OK` 또는 오류 메시지) |
| Result | object | 생성된 파일 등 작업 실행의 세부 결과 |

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
  -d '{
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet1",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml.txt"
              }
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet2",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml_2.txt"
              }
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "CloudFileSystem",
              "InputFile": "TaskBook.xlsx",
              "OutputFile": "ImpDataBook.xlsx"
            }
          }
        }
      }
    ]
  }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

관련 작업에 대한 자세한 정보는 [ImportData 작업](/cells/tasks/importdata/) 및 [SaveResult 작업](/cells/tasks/save-result/) 페이지를 참고하십시오.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트의 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}