---
title: "Excel 워크시트 이동 – Aspose.Cells Cloud API(v3.0)"
second_title: "문서"
linktitle: "이동"
type: docs
url: /ko/worksheets/move/
aliases: [/ko/move-excel-worksheets/]
keywords: "Aspose.Cells Cloud, 워크시트 이동, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 Excel 워크시트를 새 위치로 이동하는 방법을 배워보세요. 엔드포인트, 필요한 매개변수, cURL 예제 및 C#, Java, Python 등 다양한 언어의 SDK 코드를 포함합니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API v3.0을 사용하여 Excel 워크시트 이동하는 방법"
---

이 REST API는 Excel 워크북 내에서 워크시트를 이동합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                                                                                           |
| ------------- | ------ | ---- | -------------------------------------------------------------------------------------------------------------- |
| name          | string | path | Excel 파일의 이름.                                                                                             |
| sheetName     | string | path | 이동할 워크시트의 이름.                                                                                        |
| moving        | object | body | 이동 대상 워크시트(`DestinationWorksheet`) 및 상대 위치(`Position`)를 지정하는 JSON 객체.                       |
| folder        | string | query | 워크북이 저장된 폴더 경로.                                                                                     |
| storageName   | string | query | 스토리지 서비스의 이름.                                                                                        |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 단일 요청으로 워크시트를 이동하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                              |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용되었고, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과합니다. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

**샘플 오류 페이로드**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "필수 매개변수 'moving'이 누락되었습니다."
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}