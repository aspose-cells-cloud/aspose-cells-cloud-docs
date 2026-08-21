---
title: "Excel 파일에 그림 추가"
second_title: "문서"
linktype: "추가"
type: docs
url: /pictures/add/
aliases: [/add-pictures-to-excel-worksheet/]
keywords: "Aspose.Cells, Excel, 그림 추가, REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 이미지를 추가합니다. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift용 SDK가 플랫폼 간 통합을 간소화합니다."
weight: 20
ArticleTitle: "Excel 워크시트에 그림 추가 – Aspose.Cells Cloud API"
---

이 REST API는 Excel 워크시트에 새 그림을 추가합니다.  
**필수 조건:** 유효한 Aspose Cloud 인증 토큰, 지원되는 스토리지에 저장된 기존 워크북, 워크시트를 수정할 수 있는 적절한 권한이 필요합니다.

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름      | 유형     | 위치   | 설명                                                                                      |
| ----------------- | ------- | ------ | ----------------------------------------------------------------------------------------- |
| name              | string  | 경로   | 워크북 이름.                                                                              |
| sheetName         | string  | 경로   | 워크시트 이름.                                                                            |
| picture           | object  | 본문   | 그림 객체(이진 데이터).                                                                   |
| upperLeftRow      | integer | 쿼리   | 그림을 배치할 왼쪽 상단 행의 0부터 시작하는 인덱스.                                       |
| upperLeftColumn   | integer | 쿼리   | 그림을 배치할 왼쪽 상단 열의 0부터 시작하는 인덱스.                                       |
| lowerRightRow     | integer | 쿼리   | 그림 영역의 오른쪽 하단 행의 0부터 시작하는 인덱스.                                       |
| lowerRightColumn  | integer | 쿼리   | 그림 영역의 오른쪽 하단 열의 0부터 시작하는 인덱스.                                       |
| picturePath       | string  | 쿼리   | 그림 파일의 경로. 생략 시 요청 본문에 그림 데이터를 제공해야 합니다.                     |
| folder            | string  | 쿼리   | 워크북이 포함된 폴더.                                                                     |
| storageName       | string  | 쿼리   | 스토리지 서비스 이름.                                                                     |

**요청 본문 참고:** `picturePath`를 생략할 경우, 요청 본문에 `multipart/form-data`를 사용하여 이진 이미지 데이터를 전송하세요.

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                           |
|-----|---------------------------|------------------------------------------------|
| 200 | OK (성공)                 | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400 | 잘못된 요청               | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401 | 인증되지 않음             | 유효하지 않거나 누락된 JWT 토큰.               |
| 413 | 페이로드가 너무 큼        | 업로드된 파일이 크기 제한을 초과함.            |
| 500 | 내부 서버 오류            | 예기치 않은 서버 오류.                         |

**예시 200 응답 스키마**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**참고:** 최대 그림 크기는 10MB이며, 이를 초과하는 파일은 `400 Bad Request` 응답으로 거부됩니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
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

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고:** 지원되는 이미지 형식은 PNG, JPEG, BMP, GIF입니다. 최대 그림 크기는 10MB이며, 이를 초과하는 파일은 `400 Bad Request` 응답으로 거부됩니다.