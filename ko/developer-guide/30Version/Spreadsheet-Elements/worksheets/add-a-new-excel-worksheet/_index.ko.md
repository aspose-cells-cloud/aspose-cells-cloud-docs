---
title: "Excel 워크시트 추가"
ArticleTitle: "Excel 워크시트 추가 - Aspose.Cells Cloud API 가이드"
second_title: "문서"
linktitle: "추가"
type: docs
url: /ko/worksheets/add/
aliases: [  /ko/add-a-new-excel-worksheet/ ]
keywords: "Excel 워크시트 추가, Aspose.Cells Cloud, REST API, 워크시트 PUT, Excel 워크북, API 요청"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에 새 워크시트를 추가하는 단계별 가이드. 요청 세부 정보, cURL 예제, 여러 프로그래밍 언어의 SDK 코드 스니펫 포함."
weight: 20
---

이 REST API는 기존 워크북에 새 워크시트를 추가합니다.

**사전 조건**: 이 엔드포인트를 호출하려면 유효한 Aspose Cloud 인증 토큰이 필요하며, 대상 워크북은 Aspose Cloud 스토리지에 업로드되어 있어야 하며, 사용 중인 커스텀 스토리지의 스토리지 이름을 알고 있어야 합니다.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **요청 매개변수**

| 매개변수 이름 | 유형    | 위치 | 설명                                               |
| ------------- | ------- | ---- | ---------------------------------------------------- |
| name          | string  | path | 워크북 파일의 이름.                                |
| sheetName     | string  | path | 생성할 새 워크시트의 이름.                         |
| position      | integer | query | 워크시트를 삽입할 0부터 시작하는 위치.             |
| sheettype     | string  | query | 새 시트의 유형(예: **Chart**, **Dialog**).        |
| folder        | string  | query | 워크북이 포함된 폴더.                              |
| storageName   | string  | query | Aspose Cloud 스토리지의 이름.                      |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**가능한 응답 상태 코드**

| 상태 코드 | 설명                                              |
|-----------|---------------------------------------------------|
| 200       | 워크시트가 성공적으로 추가되었습니다.              |
| 400       | 잘못된 요청 – 잘못된 매개변수.                     |
| 401       | 인증되지 않음 – 인증 토큰 누락 또는 유효하지 않음. |
| 404       | 찾을 수 없음 – 워크북 또는 폴더가 존재하지 않음.   |
| 500       | 내부 서버 오류 – 예기치 않은 조건.                 |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}