---
title: "Excel 워크시트에서 도형 업데이트하기"
second_title: "문서"
linktitle: "업데이트"
type: docs
url: /ko/shapes/update/
aliases: [  /ko/update-a-shape-inside-the-worksheet/ ]
keywords: "Excel 도형 업데이트 API, Aspose.Cells Cloud, Excel 도형 업데이트, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 도형을 업데이트하는 방법을 알아보세요. HTTPS 엔드포인트, 인증 세부 정보, DTO 스키마, 단계별 사용법, cURL 예제, 여러 언어의 SDK 코드 샘플이 포함됩니다."
ArticleTitle: "Excel 워크시트에서 도형 업데이트하기 - Aspose.Cells Cloud API"
weight: 31
---

이 REST API는 Excel 워크시트의 도형을 업데이트합니다.

## 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### 요청 매개변수

| 매개변수 이름    | 유형    | 위치   | 설명                                                                               |
| ---------------- | ------- | ------ | ---------------------------------------------------------------------------------- |
| **name**         | string  | path   | 워크북 파일의 이름.                                                                |
| **sheetName**    | string  | path   | 도형이 포함된 워크시트 이름.                                                       |
| **shapeindex**   | integer | path   | 워크시트 내 도형의 0부터 시작하는 인덱스.                                          |
| **dto**          | object  | body   | 업데이트된 속성을 포함하는 도형 데이터 전송 객체(DTO, 아래 *DTO 스키마* 참조).     |
| **folder**       | string  | query  | 워크북이 저장된 폴더.                                                              |
| **storageName**  | string  | query  | Aspose Cloud 저장소의 이름.                                                        |

### DTO 스키마

`dto` 객체는 업데이트 가능한 속성을 포함합니다. 별도로 명시되지 않으면 모든 필드는 선택 사항입니다.

| 필드                | 유형    | 필수 여부 | 설명                                                                         |
| ------------------- | ------- | --------- | ---------------------------------------------------------------------------- |
| **Name**            | string  | 아니요    | 도형의 새 이름.                                                              |
| **UpperLeftRow**    | integer | 아니요    | 도형의 왼쪽 상단 모서리 행 인덱스.                                           |
| **UpperLeftColumn** | integer | 아니요    | 도형의 왼쪽 상단 모서리 열 인덱스.                                           |
| **Width**           | integer | 아니요    | 도형의 너비(포인트 단위).                                                    |
| **Height**          | integer | 아니요    | 도형의 높이(포인트 단위).                                                    |
| **RotationAngle**   | integer | 아니요    | 각도 단위의 회전 각도.                                                       |
| **IsHidden**        | boolean | 아니요    | 도형을 숨길지 여부(`true`이면 숨김).                                        |
| **IsLocked**        | boolean | 아니요    | 도형을 잠글지 여부(`true`이면 잠김).                                        |
| **Font**            | object  | 아니요    | 글꼴 설정(하위 속성은 OpenAPI 사양 참조).                                   |
| **...**             | …       | 아니요    | `HtmlText`, `AlternativeText`, `ZOrderPosition` 등 추가 속성.               |

> 전체 목록은 공식 OpenAPI 사양을 참조하세요: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### 요청 헤더

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(인증 단계에서 획득한 JWT 토큰)_

### 요청 본문 (예시)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## cURL을 사용한 예제 (명령줄 도구)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### 응답

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**오류 처리** – API는 다음과 같은 상태 코드를 반환할 수 있습니다:

| 코드 | 의미                | 일반적인 원인                                     |
| ---- | ------------------- | ------------------------------------------------ |
| 400  | 잘못된 요청(Bad Request) | 유효하지 않은 JSON 또는 필수 필드 누락.          |
| 401  | 인증되지 않음(Unauthorized) | 누락되었거나 유효하지 않은 JWT 토큰.            |
| 404  | 찾을 수 없음(Not Found) | 워크북, 워크시트 또는 도형 인덱스가 존재하지 않음. |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 측 문제.                      |

**오류 응답 예시**

*400 – 잘못된 요청(Bad Request)*

```json
{
  "Code": 400,
  "Message": "Invalid request payload. 'Name' field exceeds maximum length."
}
```

*401 – 인증되지 않음(Unauthorized)*

```json
{
  "Code": 401,
  "Message": "Authentication failed. Invalid or expired JWT token."
}
```

*404 – 찾을 수 없음(Not Found)*

```json
{
  "Code": 404,
  "Message": "The specified workbook, worksheet, or shape index was not found."
}
```

*500 – 내부 서버 오류(Internal Server Error)*

```json
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}