---
title: "Excel 워크시트에 빈 행 추가"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 빈 행 추가"
second_title: "문서"
linktype: "Row"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, 빈 행 추가, 워크시트, REST API, 행 삽입, 클라우드 스프레드시트"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 빈 행을 삽입합니다. 다양한 SDK(C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift)를 지원하여 빠른 개발을 지원합니다."
weight: 20
---

이 REST API는 Excel 워크시트에 새 행을 추가합니다. 지정된 0부터 시작하는 인덱스 위치에 빈 행을 삽입합니다.

**필수 조건:**  
- 유효한 Aspose Cloud 엑세스 토큰(Bearer JWT)을 `Authorization` 헤더에 포함해야 합니다.  
- 대상 워크북은 Aspose Cloud 스토리지에 업로드되어 있어야 하며, `folder` 및 `storageName` 매개변수는 해당 워크북의 위치를 가리켜야 합니다.

**참고 사항:**  
- `rowIndex`는 0부터 시작합니다. 인덱스 0에 삽입하면 워크시트 상단에 행이 추가됩니다.  
- Excel 워크시트의 최대 행 수는 1,048,576행입니다. 이 한계를 초과하여 삽입하려고 하면

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형    | 위치 | 설명                                              |
| -------------- | ------- | -------- | -------------------------------------------------------- |
| name           | string  | path     | 워크북 파일 이름입니다.                                  |
| sheetName      | string  | path     | 워크시트 이름입니다.                                      |
| rowIndex       | integer | path     | 새 행이 삽입될 0부터 시작하는 인덱스입니다. |
| folder         | string  | query    | 워크북이 포함된 스토리지 내 폴더 경로입니다.   |
| storageName    | string  | query    | 사용할 Aspose Cloud 스토리지 이름입니다.             |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>"
```

> **참고:** 모든 Aspose.Cells Cloud 엔드포인트는 HTTPS를 요구합니다. 프로덕션 환경에서는 보안 `https://` 스키마를 사용하세요.

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

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함 |
| 400  | Bad Request                 | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | Unauthorized                | 잘못되었거나 누락된 JWT 토큰 |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함 |
| 500  | Internal Server Error       | 예기치 않은 서버 오류 |

*오류 응답 예시(예: 행 인덱스가 워크시트 한계를 초과하는 경우):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Row index out of range. Maximum rows allowed: 1048576."
}
```

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 극대화할 수 있습니다. SDK는 저수준 세부 정보를 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}