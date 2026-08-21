---
title: "Aspose.Cells Cloud API에서 SmartMarker 작업 사용하기"
type: docs
url: /ko/tasks/smartmarker/
aliases: [  /ko/working-with-smartmarker-task/ ]
keywords: "SmartMarker 작업, Aspose.Cells Cloud, REST API, Excel, 스프레드시트 자동화"
description: "요청 스키마 및 오류 처리를 포함하여 cURL 및 SDK 예제를 통해 Aspose.Cells Cloud API의 SmartMarker 작업 사용 방법을 알아보세요."
weight: 60
ArticleTitle: "Aspose.Cells Cloud API에서 SmartMarker 작업 사용하기"
---

## REST API

**SmartMarker**는 Aspose.Cells Cloud API의 기능으로, XML 또는 JSON 소스의 데이터를 Excel 템플릿 내의 플레이스홀더에 병합하여 완전히 채워진 워크북을 생성합니다. 이 기능은 주로 보고서 생성, 메일 병합, 데이터 기반 스프레드시트 작성에 사용됩니다.

**사전 요구 사항**

- Aspose.Cells Cloud API 버전 3.0 이상  
- 유효한 OAuth2/JWT 액세스 토큰 (`Authorization: Bearer <token>` 헤더에 전달)  
- 소스 파일(템플릿 워크북 및 데이터 파일)이 Aspose Cloud 저장소에 업로드되었거나 지원되는 파일 시스템 유형을 통해 접근 가능해야 함  
- HTTPS 엔드포인트 (모든 요청은 TLS를 사용해야 함)

| **API** | **유형** | **설명** | **리소스 링크** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | 작업 실행 | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 SmartMarker 작업을 실행하고 결과 워크북을 저장하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
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
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 요청 스키마 (발췌)

| 요소 | 유형 | 필수 여부 | 설명 |
| ------- | ---- | -------- | ----------- |
| `TaskData` | object | 예 | 하나 이상의 `TaskDescription` 객체를 포함하는 루트 요소 |
| `Tasks` | object 배열 | 예 | 순차적으로 실행될 작업들의 컬렉션 |
| `TaskDescription.TaskType` | string | 예 | 작업 유형 (`SmartMarker`, `SaveResult` 등) |
| `SmartMarkerTaskParameter.SourceWorkbook` | object | 예 | 템플릿 워크북의 위치 지정 |
| `SmartMarkerTaskParameter.DestinationWorkbook` | object | 예 | 중간 워크북이 저장될 위치 지정 |
| `SmartMarkerTaskParameter.xmlFile` | object | 예 | SmartMarker에서 사용하는 데이터 소스(XML/JSON) |
| `SaveResultTaskParameter.ResultDestination` | object | 예 | 최종 워크북 반환 방식 지정 (예: `OutputStream`) |

### 오류 처리

API는 다음과 같은 HTTP 상태 코드를 반환할 수 있습니다:

- **400 Bad Request** – 요청 페이로드가 잘못되었거나 필수 필드가 누락됨  
- **401 Unauthorized** – 잘못되었거나 누락된 인증 토큰  
- **404 Not Found** – 지정된 소스 파일 중 하나를 찾을 수 없음  
- **500 Internal Server Error** – 예기치 않은 서버 측 오류 발생  

응답 본문에서 `Code`와 설명적인 `Message`를 포함하는 `Error` 객체를 확인하세요.

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}
```csharp
var xml = @"<TaskData>
    <Tasks>
        <TaskDescription>
            <TaskType>SmartMarker</TaskType>
            <SmartMarkerTaskParameter>
                <SourceWorkbook>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>Designer.xlsx</FilePath>
                </SourceWorkbook>
                <DestinationWorkbook>
                    <FileSourceType>InMemoryFiles</FileSourceType>
                    <FilePath>Temp.xlsx</FilePath>
                </DestinationWorkbook>
                <xmlFile>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>DataSet.xml</FilePath>
                </xmlFile>
            </SmartMarkerTaskParameter>
        </TaskDescription>
        <TaskDescription>
            <TaskType>SaveResult</TaskType>
            <SaveResultTaskParameter>
                <ResultSource>InMemoryFiles</ResultSource>
                <ResultDestination>
                    <DestinationType>OutputStream</DestinationType>
                    <InputFile>Temp.xlsx</InputFile>
                    <OutputFile>Output.xlsx</OutputFile>
                </ResultDestination>
            </SaveResultTaskParameter>
        </TaskDescription>
    </Tasks>
</TaskData>";

ServiceHelper helper = new ServiceHelper(sid, key);
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}