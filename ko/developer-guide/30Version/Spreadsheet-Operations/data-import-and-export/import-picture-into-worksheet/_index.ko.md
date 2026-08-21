---
title: "엑셀 워크시트에 그림 가져오기"
ArticleTitle: "엑셀 워크시트에 그림 가져오기 – Aspose.Cells Cloud API 가이드"
second_title: "문서"
linktype: "docs"
url: /ko/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "그림 가져오기, 엑셀, Aspose.Cells Cloud, REST API, v3.0"
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 엑셀 워크시트에 그림을 가져오는 방법을 알아보세요. 멀티파트 요청 예시, SDK 코드 예제, 오류 처리 가이드를 포함합니다. 명확한 단계로 빠르게 시작하세요."
weight: 19
---

엑셀 워크시트에 그림을 가져오면 로고, 차트, 다이어그램 등의 시각적 콘텐츠를 스프레드시트에 풍부하게 추가할 수 있습니다. 이 가이드에서는 Aspose.Cells Cloud **ImportPicture** 작업, 필요한 요청 형식 및 응답 처리 방법을 설명합니다.

**필수 조건:** 가져오기 작업을 호출하기 전에 유효한 JWT 인증 토큰과 Aspose Cloud 스토리지에 저장된 기존 워크북이 있어야 합니다.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

이 요청은 HTTP **POST** 요청이며, 콘텐츠 유형은 **multipart/related**입니다. (참고: [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))

- **첫 번째 파트**에는 그림을 배치할 위치와 방식을 설명하는 **ImportPictureOption**이라는 JSON 객체가 포함됩니다.
- **두 번째 파트**에는 이미지 파일(또는 Base64로 인코딩된 데이터)이 전달됩니다.

### ImportPictureOption – 정의

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert`는 **부울(boolean)** 유형입니다. `true`는 새 그림을 삽입하고, `false`는 기존 그림을 교체합니다._

### 주요 매개변수

**ImportPictureOption**

| 매개변수 이름         | 유형         | 설명                                                                                                                                                                      |
| --------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UpperLeftRow          | int          | 그림을 배치할 왼쪽 위 모서리의 행 인덱스입니다.                                                                                                                           |
| UpperLeftColumn       | int          | 그림을 배치할 왼쪽 위 모서리의 열 인덱스입니다.                                                                                                                           |
| LowerRightRow         | int          | 그림의 범위를 정의하는 오른쪽 아래 모서리의 행 인덱스입니다.                                                                                                             |
| LowerRightColumn      | int          | 그림의 범위를 정의하는 오른쪽 아래 모서리의 열 인덱스입니다.                                                                                                             |
| Filename              | string       | 그림 파일의 이름입니다.                                                                                                                                                   |
| Data                  | string       | 그림의 Base64로 인코딩된 이진 데이터입니다. (두 번째 파트로 파일을 전송하는 경우는 선택 사항입니다.)                                                                      |
| DestinationWorksheet  | string       | 그림을 삽입할 워크시트의 이름입니다.                                                                                                                                      |
| **IsInsert**          | **boolean**  | `true`는 새 그림을 삽입하고, `false`는 기존 그림을 교체합니다.                                                                                                            |
| ImportDataType        | string       | 가져올 데이터 유형입니다. (예: `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`) |
| Source                | FileSource   | `BatchData` 매개변수가 null일 때 데이터 파일의 위치를 나타냅니다.                                                                                                        |

### 응답

성공적인 요청은 다음과 유사한 JSON 페이로드와 함께 **HTTP 200**을 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

가능한 상태 코드:

| 코드 | 의미                                       |
| ---- | ------------------------------------------- |
| 200  | 가져오기 성공                               |
| 400  | 잘못된 요청 – 누락 또는 유효하지 않은 데이터 |
| 401  | 인증되지 않음 – 잘못되거나 누락된 토큰      |
| 500  | 내부 서버 오류                             |


## SDK를 사용하여 PostImportData API 사용하기

### PostImportData API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---