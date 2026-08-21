---
title: "워크시트 변환 – Aspose.Cells Cloud API 문서"
second_title: "문서"
ArticleTitle: "로컬 워크시트 스프레드시트 데이터를 이미지 파일로 변환하는 방법: 단계별 가이드"
linktype: "워크시트를 이미지로 변환"
type: docs
url: /ko/convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud, 워크시트를 이미지로 변환, 워크시트를 이미지 파일로 변환, Excel을 PNG로, Excel을 SVG로, Excel을 TIFF로, Excel을 JPEG로, Excel을 BMP로, 이미지 변환 API, REST API, 스프레드시트 이미지 내보내기, SDK 예제"
description: "Aspose.Cells Cloud API를 사용해 Excel 워크시트를 이미지 형식(PNG, SVG, TIFF, JPEG, BMP 등)으로 변환하는 단계별 가이드. 요청 매개변수, 응답 세부정보, 오류 코드, 사용 시나리오 및 SDK 코드 예제 포함."
weight: 100
---

Aspose.Cells Cloud API를 사용하여 로컬 Excel 파일의 워크시트 데이터를 [이미지](https://docs.fileformat.com/image/) 파일로 내보냅니다. 이 작업은 여러 이미지 형식을 지원하며 스프레드시트 데이터의 시각적 스냅샷을 생성할 때 적합합니다.

**지원되는 이미지 형식**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **워크시트를 이미지로 변환 API**

### 웹 API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                      |
| :------------ | :----- | :------------------------- | :---------------------------------------------------------------------------------------- |
| Spreadsheet   | File   | FormData                   | 스프레드시트 파일 업로드.                                                                 |
| worksheet     | String | Query                      | 변환할 워크시트 이름.                                                                     |
| format        | String | Query                      | 원하는 이미지 형식(`svg`, `png`, `tiff`, `jpeg`, `bmp` 등).                               |
| outPath       | String | Query                      | _(선택 사항)_ 출력 이미지가 저장될 폴더 경로; 기본값은 `null`.                            |
| outStorageName| String | Query                      | 출력 파일을 저장할 스토리지 위치 이름.                                                    |
| fontsLocation | String | Query                      | 서버에서 사용할 수 없는 폰트를 사용하려는 경우 사용자 정의 폰트 폴더 경로.                 |
| region        | String | Query                      | 스프레드시트 지역 설정(예: `en-US`).                                                      |
| password      | String | Query                      | 보호된 스프레드시트 파일을 열기 위해 필요한 비밀번호.                                     |

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

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                   |
| ---- | ------------------- | ------------------------------------------------------ |
| 200  | OK (성공)           | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함.   |
| 400  | Bad Request         | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).|
| 401  | Unauthorized        | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large   | 업로드한 파일이 크기 제한을 초과함.                     |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                  |

## **워크시트를 이미지로 변환 API를 어디에 사용해야 하나요?**

- **정적 보고서 스냅샷** – 편집이 필요 없는 PDF 보고서, PowerPoint 슬라이드, 인쇄 문서 등에 포함하기 위해 재무 표, 계산식 또는 기타 데이터를 이미지로 변환.
- **프레젠테이션용 데이터 시각화** – 조건부 서식이나 간단한 차트를 포함한 복잡한 스프레드시트 테이블을 프레젠테이션(PPTX, Google Slides 등)에 삽입 가능한 이미지로 변환.
- **문서화 및 교육 자료** – 사용자 매뉴얼, 튜토리얼, 지식베이스 문서 등에 사용할 스프레드시트 예제, 템플릿, 데이터 입력 양식을 이미지로 캡처.
- **썸네일 미리보기** – 파일 브라우저, 문서 라이브러리, 검색 결과 등에서 핵심 스프레드시트 영역의 작은 이미지 미리보기를 생성.

## **왜 워크시트를 이미지로 변환 API를 사용해야 하나요?**

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 체계적인 문서도 함께 제공됩니다. 사용자 정의 차트 렌더링 솔루션을 직접 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적** – 워크북을 영구적으로 저장하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **픽셀 수준 정확성 보장** – 셀 서식, 수식(표시된 값), 테두리, 색상, 조건부 서식 등을 출력 이미지에 정확하게 재현합니다.
- **범용 호환성** – PNG, JPEG, TIFF, BMP, SVG 등 이미지 형식은 특수 소프트웨어 없이 모든 장치 및 플랫폼에서 볼 수 있어 최대한의 접근성을 보장합니다.

## **SDK를 사용해 워크시트를 이미지로 변환 API를 사용하는 방법은?**

### 워크시트를 이미지로 변환 API 사양

[워크시트를 이미지로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 호출을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩됨)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 최소한의 코드로 워크시트 데이터를 이미지로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}