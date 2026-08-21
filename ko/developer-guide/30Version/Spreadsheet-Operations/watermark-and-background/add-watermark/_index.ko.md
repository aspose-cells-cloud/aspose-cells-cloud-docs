---
title: "Excel 파일에 워터마크 추가"
second_title: "문서"
linktitle: "Excel 파일에 워터마크 추가"
type: docs
url: /ko/add-watermark-into-excel-files/
aliases: [  /ko/watermark/ ]
keywords: "Excel에 워터마크 추가, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크북에 텍스트 워터마크를 추가하는 방법을 알아보세요. cURL 예제, 필요한 매개변수 및 응답 세부정보 포함."
weight: 39
ArticleTitle: "Excel 파일에 워터마크 추가 – Aspose.Cells Cloud 문서"
---

이 REST API는 Excel 파일에 **워터마크**를 추가합니다.

**필수 조건:** 유효한 JWT 액세스 토큰을 획득해야 하며, Excel 파일이 지원되는 형식(예: `.xlsx`, `.xls`)인지 확인해야 합니다.  
**배경 설명:** 워터마크는 워크시트마다 적용되는 반투명 텍스트 오버레이로, 소유권 또는 기밀성 여부를 표시합니다.

## PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치                     | 설명                                                |
| ------------- | ------ | ------------------------ | --------------------------------------------------- |
| `file`        | file   | formData (multipart body) | 워터마크를 적용할 Excel 파일입니다.                 |
| `text`        | string | query                    | 표시할 워터마크 텍스트입니다.                       |
| `color`       | string | query                    | ARGB 16진수 형식의 워터마크 색상(예: `004433ff`).   |

### **응답**

JSON 응답에는 **Files** 배열이 포함됩니다. 각 파일 객체는 다음과 같은 정보를 제공합니다:

- **Filename** – 처리된 워크북의 이름입니다.  
- **FileSize** – 파일의 크기(바이트 단위)입니다.  
- **FileContent** – 워터마크가 적용된 Excel 파일의 Base64 인코딩 콘텐츠입니다. 실제 파일을 얻으려면 이를 디코딩해야 합니다.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[파일1 이름]",
            "Filesize" : [파일 크기],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[파일2 이름]",
            "Filesize" : [파일 크기],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[파일3 이름]",
            "Filesize" : [파일 크기],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함 |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰                        |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함                |
| 500  | Internal Server Error        | 예기치 않은 서버 오류                             |

## SDK를 사용하여 PostWatermark API 사용 방법

### PostWatermark API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 필요한 인증 헤더를 포함한 전체 요청을 보여줍니다. `<your-jwt-token>`을 Aspose 인증 엔드포인트에서 획득한 유효한 JWT 액세스 토큰으로 바꾸세요.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 정보를 추상화하여 비즈니스 로직에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}