---
title: "Aspose.Cells Cloud 위치 기반 문자 제거 웹 API – Excel에서 특정 위치의 텍스트 삭제"
second_title: "문서"
ArticleTitle: "Excel 위치 기반 문자 제거기 – 특정 위치의 텍스트 삭제 – 온라인 단축코드"
linktitle: "위치 기반 문자 제거"
type: docs
url: /ko/remove-characters-by-position/
keywords: "Aspose.Cells Cloud, 위치 기반 문자 제거, Excel 텍스트 정리, 앞에서부터 N개 문자 삭제, 뒤에서부터 N개 문자 삭제, 특정 마커 앞 텍스트 제거, 특정 마커 뒤 텍스트 제거, 두 값 사이 텍스트 제거"
description: "Aspose.Cells Cloud 웹 API를 사용하여 Excel 셀에서 위치 기반으로 문자를 삭제하세요. 상위/하위 N개의 문자 또는 특정 마커 앞/뒤의 텍스트를 정확하게 삭제하세요."
weight: 100
---

Excel 셀에서 위치 기반으로 문자를 삭제하세요: 상위/하위 N개의 문자를 삭제하거나 지정된 마커 앞/뒤의 텍스트를 삭제하세요. Aspose.Cells Cloud 웹 API로 정밀한 텍스트 정리를 수행하세요.


## **소개**: 위치 기반으로 불필요한 문자 제거

**위치 모드**

- `theFirstNCharacters` – 시작 부분에서 N개의 문자 제거
- `theLastNCharacters` – 끝 부분에서 N개의 문자 제거
- `allCharactersBeforeText` – 지정된 부분 문자열의 첫 번째 등장 위치 앞의 모든 문자 삭제
- `allCharactersAfterText` – 지정된 부분 문자열의 첫 번째 등장 위치 뒤의 모든 문자 삭제
- `BetweenValues` – 두 사용자 정의 값 사이의 부분 문자열(및 선택적으로 구분 기호 자체) 제거

**옵션**

- `caseSensitive` – `BeforeText`, `AfterText`, `BetweenValues` 검색 시 대소문자를 구분할지 여부 결정

## **RemoveCharactersByPosition API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveCharactersByPosition** API의 요청 파라미터는 다음과 같습니다.

| 파라미터 이름           | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                             |
| ----------------------- | ------- | -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | 파일    | FormData                   | 처리할 스프레드시트 파일입니다. 지원되는 형식은 XLSX, XLS, ODS, CSV 등이 포함됩니다.                                                                               |
| Authorization           | 문자열  | 헤더                     | 인증용 Bearer 토큰 (필수).                                                                                                                             |
| theFirstNCharacters     | 정수    | 쿼리                     | 선택된 각 셀의 텍스트 시작 부분에서 제거할 문자 수입니다. 예: `3`은 처음 3개의 문자를 제거합니다.                                         |
| theLastNCharacters      | 정수    | 쿼리                     | 선택된 각 셀의 텍스트 끝 부분에서 제거할 문자 수입니다. 예: `2`는 마지막 2개의 문자를 제거합니다.                                                |
| allCharactersBeforeText | 문자열  | 쿼리                     | 각 셀에서 지정된 텍스트 문자열 앞에 나타나는 모든 문자를 제거합니다. 해당 텍스트가 여러 번 나타날 경우 첫 번째 등장 위치를 기준으로 제거합니다.         |
| allCharactersAfterText  | 문자열  | 쿼리                     | 각 셀에서 지정된 텍스트 문자열 뒤에 나타나는 모든 문자를 제거합니다. 해당 텍스트가 여러 번 나타날 경우 첫 번째 등장 위치를 기준으로 제거합니다.          |
| worksheet               | 문자열  | 쿼리                     | _(선택 사항)_ 문자 제거 작업을 적용할 워크시트 이름입니다. 생략 시 첫 번째 워크시트에 작업이 적용됩니다.                               |
| range                   | 문자열  | 쿼리                     | _(선택 사항)_ 문자 제거 작업을 적용할 셀 범위입니다. (예: `"A1:C10"`) 생략 시 지정된 워크시트의 사용된 모든 셀에 작업이 적용됩니다. |
| outPath                 | 문자열  | 쿼리                     | _(선택 사항)_ 처리된 워크북이 저장될 클라우드 스토리지 폴더 경로입니다. 생략 시 원본 폴더에 파일이 저장됩니다.                              |
| outStorageName          | 문자열  | 쿼리                     | 출력 파일이 저장될 클라우드 스토리지의 이름입니다.                                                                                                     |
| region                  | 문자열  | 쿼리                     | _(선택 사항)_ 텍스트 처리를 위한 로케일을 설정합니다. 언어별 문자 위치 및 인코딩과 관련하여 특히 중요합니다. (예: `"en-US"`, `"zh-CN"`)              |
| password                | 문자열  | 쿼리                     | _(선택 사항)_ 업로드된 스프레드시트가 암호로 보호되어 있는 경우, 파일을 열고 처리하기 위해 암호를 제공하세요.                                                      |

### **응답**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### 오류 코드

- **200 OK** – 요청이 성공적으로 처리되었으며, 처리된 파일이 반환됩니다.
- **400 Bad Request**: 잘못된 Aspose.Cells Cloud API URI입니다.
- **401 Unauthorized**: 잘못된 액세스 토큰 또는 잘못된 클라이언트 ID 및 비밀번호입니다.
- **404 Not Found**: 스프레드시트 파일에 접근할 수 없습니다.
- **500 Server Error**: 스프레드시트가 계산 데이터를 가져오는 중 문제가 발생했습니다.

## Remove Characters by Position API는 어디에 사용해야 하나요?

- **데이터 표준화**: 제품 코드 정리(리더 제로 또는 접미사 제거), 전화번호 정리(국가 코드 제거)
- **텍스트 추출**: 로그 파일에서 핵심 정보 추출(타임스탬프 또는 접두사 제거)
- **파일 처리**: 파일 이름 정리(일관된 접두사 또는 날짜 접미사 제거)
- **데이터 파싱**: 구조화된 텍스트 처리(대괄호 또는 특정 마커 사이의 콘텐츠 추출)
- **데이터베이스 관리**: 불러온 데이터 정리(고정 형식의 헤더/트레일러 문자 제거)

## 왜 Remove Characters by Position API를 사용해야 하나요?

- **정확하고 효율적**: 위치 기반 직접 삭제로 복잡한 정규식이 필요 없습니다.
- **유연한 설정**: 5가지 위치 모드와 대소문자 구분 옵션으로 다양한 시나리오를 처리할 수 있습니다.
- **배치 처리**: 단일 요청으로 전체 열을 정리하여 최대 10배까지 효율성을 높입니다.
- **스마트 파싱**: 두 구분 기호 사이의 콘텐츠 추출을 손쉽게 처리합니다.
- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어의 SDK를 제공하여 개발 속도를 높이고 포괄적인 문서를 제공합니다. 사용자 정의 텍스트 처리 로직을 구축하는 것에 비해 개발 부하를 크게 줄입니다.
- **비용 효율적**: 워크북을 먼저 업로드하지 않고도 문자를 제거할 수 있어 저장 공간을 절약하고 비용을 줄입니다.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 내부 세부 사항을 처리하므로, 최소한의 코드만으로 셀의 문자 제거 기능을 구현할 수 있습니다.  
Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---