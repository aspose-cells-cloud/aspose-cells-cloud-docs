---
title: "다른 워크시트에서 콘텐츠 및 서식 복사"
second_title: "Document"
linktype: "복사"
type: docs
url: /ko/worksheets/copy/
aliases: [/copy-excel-worksheet/]
keywords: "Aspose Cells 워크시트 복사 API, Excel 시트 복사 REST, Aspose Cloud SDK 복사, 스프레드시트 워크시트 복사"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트와 그 서식을 새 시트로 복사하는 방법을 알아보세요. C#, Java, Python 등 다양한 언어에 대한 엔드포인트, 매개변수, cURL 및 SDK 예제가 포함되어 있습니다."
weight: 20
---

이 REST API는 동일한 워크북 내에서 워크시트와 그 서식을 새 시트로 복사합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형   | 위치 | 설명                                                              |
| ---------------- | ------ | ---- | ----------------------------------------------------------------- |
| `name`           | string | path | 워크북 파일의 이름.                                               |
| `sheetName`      | string | path | 대상 워크시트(새 시트)의 이름.                                    |
| `sourceSheet`    | string | query | 복사할 워크시트의 이름.                                           |
| `options`        | object | body | 복사 옵션을 포함하는 JSON 객체(예: 열 너비, 수식 등).             |
| `sourceWorkbook` | string | query | 현재 워크북과 다른 경우 원본 워크북의 이름.                       |
| `sourceFolder`   | string | query | 원본 워크북이 저장된 폴더 경로.                                   |
| `folder`         | string | query | 대상 워크북이 저장될 폴더 경로.                                   |
| `storageName`    | string | query | 사용할 스토리지 서비스의 이름.                                    |

### 요청 및 응답 예시

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 오류 처리

API는 표준 HTTP 상태 코드와 함께 JSON 오류 본문을 반환합니다. 일반적인 응답은 다음과 같습니다:

| HTTP 코드 | 설명                                                     | 샘플 JSON 오류 본문                                         |
| --------- | -------------------------------------------------------- | ----------------------------------------------------------- |
| 400       | 잘못된 요청 – 누락되거나 잘못된 매개변수.                 | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401       | 인증 실패 – 누락되거나 잘못된 토큰.                       | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404       | 찾을 수 없음 – 워크북, 워크시트 또는 폴더가 존재하지 않음. | `{ "Code": 404, "Message": "Resource not found." }`         |
| 500       | 내부 서버 오류 – 예기치 않은 조건.                        | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}