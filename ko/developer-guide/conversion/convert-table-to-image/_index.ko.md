---
title: "Aspose.Cells Cloud Web API - 로컬 Excel 테이블 데이터를 이미지 파일로 변환 - 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 테이블 데이터를 이미지 파일로 변환하는 방법: 단계별 가이드"
linktitle: "테이블을 이미지로 변환"
type: docs
url: /ko/convert-table-to-image/
keywords: "Aspose.Cells, 클라우드 API, 테이블을 이미지로 변환, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "Aspose.Cells Cloud API를 사용하여 로컬 Excel 스프레드시트 테이블을 빠르게 이미지 파일로 변환합니다. PNG, JPEG, TIFF, BMP, SVG 및 기타 형식을 지원합니다."
weight: 100
---

클라우드 API를 사용하여 로컬 Excel 파일에서 테이블 데이터를 [이미지](https://docs.fileformat.com/image/) 파일로 내보냅니다.

**지원되는 이미지 형식:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **테이블을 이미지로 변환 API**

이 엔드포인트를 사용하기 전에 다음 필수 조건을 충족해야 합니다:

- Aspose.Cells Cloud 인증을 통해 얻은 유효한 JWT 액세스 토큰.
- `outPath` 또는 `outStorageName` 매개변수를 사용하려는 경우 접근 가능한 스토리지 계정.
- 소스 워크북(로컬 Excel 파일)이 읽기 가능해야 하며, 보호되어 있는 경우 올바른 암호를 제공해야 합니다.

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름   | 유형     | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                   |
| :-------------- | :------- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | 파일     | FormData                    | 스프레드시트 파일을 업로드합니다.                                                                                                      |
| worksheet       | 문자열   | 쿼리                        | 스프레드시트/Excel의 워크시트 이름.                                                                                                    |
| tableName       | 문자열   | 쿼리                        | 변환할 테이블의 이름.                                                                                                                  |
| format          | 문자열   | 쿼리                        | 원하는 이미지 파일 형식(예: png, svg).                                                                                                 |
| outPath         | 문자열   | 쿼리                        | (선택 사항) 변환된 이미지가 저장될 폴더 경로입니다. 기본값은 null입니다.                                                              |
| outStorageName  | 문자열   | 쿼리                        | 출력 파일의 저장소 이름을 지정합니다.                                                                                                  |
| fontsLocation   | 문자열   | 쿼리                        | 필요 시 사용자 정의 폰트를 사용합니다.                                                                                                 |
| region          | 문자열   | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 미칩니다.                              |
| password        | 문자열   | 쿼리                        | 스프레드시트 파일에 접근하기 위한 암호입니다.                                                                                          |

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

| 코드 | 의미                   | 설명                                                         |
| ---- | ---------------------- | ------------------------------------------------------------ |
| 200  | OK (성공)              | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.       |
| 400  | 잘못된 요청            | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음          | 잘못되었거나 누락된 JWT 토큰.                                |
| 413  | 페이로드가 너무 큼     | 업로드된 파일이 크기 제한을 초과함.                          |
| 500  | 내부 서버 오류         | 예기치 않은 서버 오류.                                       |

## **어디서 Convert Table to Image API를 사용해야 하나요?**

- **정적 보고서 스냅샷**: 편집이 필요 없는 PDF 보고서, PowerPoint 슬라이드, 인쇄 문서 등에 포함하기 위해 재무 테이블, 계산 결과 또는 기타 서식이 적용된 데이터를 이미지로 변환합니다.
- **프레젠테이션 데이터 시각화**: 조건부 서식 또는 간단한 시각화가 포함된 복잡한 스프레드시트 테이블을 이미지로 변환하여 프레젠테이션(PPTX, Google 슬라이드)에 포함합니다.
- **문서 및 교육 자료**: 사용자 매뉴얼, 튜토리얼, 지식베이스 기사용으로 스프레드시트 예제, 템플릿 또는 데이터 입력 양식을 이미지로 캡처합니다.
- **썸네일 미리보기**: 파일 브라우저, 문서 라이브러리, 검색 결과 등을 위해 스프레드시트 주요 섹션의 작은 이미지 미리보기를 생성합니다.

## 왜 Convert Table to Image API를 사용해야 할까요?

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서를 제공합니다. 사용자 정의 렌더링 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 전체 워크북을 먼저 업로드하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **픽셀 수준 정확성**: 셀 서식, 수식(표시된 값), 테두리, 색상, 조건부 서식 등 Excel의 외관을 결과 이미지에 정확하게 재현합니다.
- **범용 호환성**: 이미지 형식(PNG, JPEG, TIFF, BMP, SVG 등)은 특수 소프트웨어 없이 모든 장치 및 플랫폼에서 볼 수 있어 최대한의 접근성을 보장합니다.

## SDK를 사용하여 Convert Table to Image API를 어떻게 사용하나요?

### Convert Table to Image API 사양

[Convert Table to Image API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
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

SDK를 사용하면 낮은 수준의 세부 사항을 추상화하여 최소한의 코드로 스프레드시트 테이블 데이터를 이미지로 변환할 수 있으므로 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}