---
title: "Aspose.Cells Cloud Web API - Excel 차트를 이미지로 변환 - 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "스preadsheet 차트를 이미지로 변환하는 방법: 단계별 가이드"
linktitle: "차트를 이미지로 변환"
type: docs
url: /ko/convert-chart-to-image/
keywords: "차트를 이미지로 변환, Aspose.Cells, Excel 차트 내보내기, PNG, SVG, JPEG, BMP, TIFF"
description: "Aspose.Cells Cloud Web API를 사용하여 스프레드시트 파일에서 Excel 차트를 PNG, SVG, TIFF, JPEG 또는 BMP 이미지로 직접 변환합니다."
weight: 100
---

Excel 차트는 워크시트 내에 포함될 수 있는 데이터의 시각적 표현입니다. 이러한 차트를 이미지 형식으로 변환하면 Excel 없이도 문서, 웹 페이지, 보고서 등에서 차트를 쉽게 재사용할 수 있습니다.

로컬 스프레드시트 또는 Excel 파일의 차트를 이미지 파일로 변환합니다. 지원되는 **이미지 형식:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **차트를 이미지로 변환 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름      | 타입     | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                 | 필수 여부 |
| :----------------- | :------- | :------------------------- | :------------------------------------------------------------------- | :-------- |
| Spreadsheet        | 파일     | FormData                   | 차트를 포함하는 스프레드시트 파일을 업로드합니다.                     | 예        |
| worksheet          | 문자열   | 쿼리                       | 해당하는 경우 워크시트 이름을 지정합니다.                             | 아니요    |
| chartIndex         | 정수     | 쿼리                       | 변환할 차트의 인덱스입니다.                                           | 예        |
| format             | 문자열   | 쿼리                       | (필수) 원하는 이미지 유형(예: svg, png, jpg)입니다.                  | 예        |
| outPath            | 문자열   | 쿼리                       | (선택 사항) 출력 파일을 저장할 폴더 경로이며, 기본값은 null입니다.   | 아니요    |
| outStorageName     | 문자열   | 쿼리                       | 출력 파일을 저장할 저장소 이름입니다.                                 | 아니요    |
| fontsLocation      | 문자열   | 쿼리                       | 필요한 경우 사용자 정의 폰트를 지정합니다.                            | 아니요    |
| region             | 문자열   | 쿼리                       | 스프레드시트 지역을 설정합니다.                                        | 아니요    |
| password           | 문자열   | 쿼리                       | 스프레드시트 파일을 열기 위한 암호입니다.                             | 아니요    |

## **응답**

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

| 코드 | 의미                  | 설명                                                             |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK(성공)              | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.       |
| 400  | Bad Request(잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).         |
| 401  | Unauthorized(인증되지 않음) | 잘못되었거나 누락된 JWT 토큰.                                   |
| 413  | Payload Too Large(페이로드가 너무 큼) | 업로드한 파일이 크기 제한을 초과함.                            |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류.                                          |

## 차트를 이미지로 변환 API를 어디에 사용해야 하나요?

- **보고서 생성 및 대시보드**: Excel 데이터에서 차트를 자동으로 이미지(PNG, JPEG 등)로 변환하여 PDF 보고서, 웹 대시보드, PowerPoint 프레젠테이션 등에 삽입합니다.
- **웹/이메일 애플리케이션**: 사용자가 Excel 파일을 다운로드하거나 열지 않고도 웹 페이지나 이메일에 차트 이미지를 직접 제공합니다. 동적 보고 도구, 뉴스레터, 자동 알림 등에 유용합니다.
- **문서 처리 워크플로우**: 자동화 파이프라인(예: 청구서, 분석)에 통합하여 Excel 차트를 다른 형식(Word, PDF, HTML)에 삽입합니다.
- **모바일/데스크톱 애플리케이션**: 전체 스프레드시트 렌더링이 불필요하거나 비현실적인 앱에서 Excel 차트를 표시합니다.
- **아카이빙 및 시각화**: Excel 의존 없이 장기 저장, 썸네일, 빠른 미리보기를 위해 차트를 별도 이미지로 저장합니다.

## 차트를 이미지로 변환 API를 사용해야 하는 이유는 무엇인가요?

- **시각적 정확성 보존**: Excel에서 보는 그대로의 정확한 차트 서식(색상, 레이블, 배율 등)을 유지하여 전문적인 품질의 결과물을 제공합니다.
- **플랫폼 독립성**: Excel 설치가 필요 없습니다. REST API를 통해 Windows, Linux, macOS 등 다양한 플랫폼에서 실행되며 클라우드 기반 또는 서버 측 애플리케이션에 적합합니다.
- **자동화 및 확장성**: 여러 차트나 파일을 프로그래밍 방식으로 일괄 변환하여 수동 내보내기보다 시간을 절약합니다. 클라우드에서 대량 처리를 효율적으로 수행합니다.
- **유연한 출력 형식**: 인기 있는 이미지 형식(PNG, JPG, BMP, SVG 등)을 지원하여 다양한 시스템 및 미디어와 통합할 수 있습니다.
- **보안 및 신뢰성**: 클라이언트 측 도구에 민감한 데이터를 노출하지 않고 Aspose의 클라우드 환경에서 파일을 처리합니다. 높은 가용성과 일관된 성능을 제공합니다.
- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서도 함께 제공됩니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율성**: 워크북을 먼저 업로드하지 않고도 차트를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.

## SDK를 사용하여 차트를 이미지로 변환 API를 어떻게 사용하나요?

### 차트를 이미지로 변환 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">차트를 이미지로 변환 API 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화하여 짧은 코드로 차트를 이미지로 변환할 수 있으므로 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}