---
title: "Excel 워크시트에서 이미지 삭제 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, 클라우드 API, 이미지 삭제, Excel 워크시트, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 이미지를 삭제합니다. DELETE 엔드포인트, 필요한 매개변수, 인증, 오류 코드 및 예제 코드를 알아보세요."
weight: 50
ArticleTitle: "Excel 워크시트에서 이미지 삭제 – Aspose.Cells Cloud API"
---

이 REST API는 Excel 워크시트에서 이미지를 삭제합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 필수 여부 | 설명                                           |
| ------------- | ------- | ---- | --------- | ---------------------------------------------- |
| name          | string  | path | 예       | 워크북 파일의 이름입니다.                      |
| sheetName     | string  | path | 예       | 이미지가 포함된 워크시트의 이름입니다.         |
| pictureIndex  | integer | path | 예       | 삭제할 이미지의 0부터 시작하는 인덱스입니다.   |
| folder        | string  | query |아니요   | 워크북이 저장된 폴더입니다.                    |
| storageName   | string  | query |아니요   | 스토리지 서비스의 이름입니다(선택 사항).       |

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**샘플 응답 헤더**

| 헤더          | 값                            |
|---------------|-------------------------------|
| Content-Type  | application/json              |
| Content-Length| (변수)                        |
| Date          | (서버 날짜)                   |

{{< /tab >}}

{{< /tabs >}}

### 오류 처리

| HTTP 코드 | 의미                                                    | 샘플 오류 페이로드                                                |
| --------- | ------------------------------------------------------- | ----------------------------------------------------------------- |
| 200       | 이미지가 성공적으로 삭제되었습니다.                    | `{ "Code": 200, "Status": "OK" }`                                 |
| 400       | 잘못된 요청 – 잘못된 매개변수.                          | `{ "Code": 400, "Message": "Invalid pictureIndex." }`             |
| 401       | 인증되지 않음 – 토큰 누락 또는 유효하지 않은 토큰.      | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404       | 찾을 수 없음 – 워크북, 워크시트 또는 이미지가 존재하지 않음. | `{ "Code": 404, "Message": "Resource not found." }`              |
| 500       | 내부 서버 오류.                                         | `{ "Code": 500, "Message": "Unexpected server error." }`          |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 가장 빠르게 할 수 있는 방법입니다. SDK가 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}