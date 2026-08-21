---
title: "Excel에 텍스트 추가: 스프레드시트 웹 API로 효율적으로 데이터 삽입하기"
second_title: "문서"
linktitle: "텍스트 추가"
type: docs
url: /ko/excel-add-text/
keywords: "Excel, Aspose.Cells, 텍스트 추가, 스프레드시트 API, REST API, Office Cloud, 텍스트 삽입, Excel API"
description: "Aspose.Cells Cloud API를 통해 Excel 스프레드시트의 지정된 위치에 텍스트를 추가합니다."
weight: 100
---

스프레드시트 내 지정된 위치에 텍스트 콘텐츠를 추가합니다. 이 작업을 수행하려면 추가할 텍스트와 삽입 위치를 정의하는 객체가 필요합니다.

## **Excel API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### **기능 설명**

이 메서드는 지정된 셀에 새 텍스트를 안전하게 추가하며, 여러 삽입 모드와 포맷 처리를 지원합니다.

- **선택한 셀의 시작 부분에 텍스트 추가**  
  선택한 모든 셀 앞에 텍스트를 추가하여 데이터 입력의 일관성을 보장합니다. 제품 코드, 카테고리, 접두사와 같은 공통 식별자나 라벨을 추가할 때 적합합니다.

- **특정 텍스트 앞 또는 뒤에 문자 삽입**  
  선택한 셀 내의 대상 텍스트 앞 또는 뒤에 문자를 배치하여 구조화되고 체계적인 콘텐츠를 쉽게 만들 수 있습니다.

- **모든 선택한 셀의 끝에 동일한 텍스트 추가**  
  여러 셀의 끝에 동일한 텍스트를 한 번의 작업으로 추가하여 데이터 입력을 간소화하고 일관된 외관을 보장합니다.

- **지정된 문자 수 뒤에 텍스트 삽입**  
  대상 범위 내 각 셀의 시작 또는 끝에서 정의된 문자 수 뒤에 텍스트를 삽입합니다. 일반적인 사용 사례로는 코드, 타임스탬프 또는 사용자 정의 구분자 포맷팅이 있습니다.

### **요청 매개변수**

| 매개변수 이름 | 타입  | 위치 | 설명                                                                 |
| ------------ | ----- | ---- | ------------------------------------------------------------------- |
| addTextOptions | 클래스 | 본문 | 추가할 텍스트 콘텐츠와 텍스트를 추가할 위치를 지정합니다. |

### **응답**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                              |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized                | 유효하지 않거나 누락된 JWT 토큰 |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함 |
| 500  | Internal Server Error       | 예기치 않은 서버 오류 |

## SDK를 사용한 PostAddTextContent API 사용 방법

### PostAddTextContent API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 기반 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 최대한 높이는 가장 효율적인 방법입니다. SDK는 저수준 세부 사항을 처리하므로, 개발자는 프로젝트의 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}