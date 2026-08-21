---
title: "Excel 파일 복구"
second_title: "문서"
type: docs
linktitle: "Excel 파일 복구"
url: /ko/repair-excel-files/
keywords: "Aspose Cells, Excel 복구 API, 손상된 XLSX, 스프레드시트 복구, 클라우드 API"
description: "Aspose.Cells Cloud REST API를 사용하여 손상된 Excel 파일(XLS, XLSX, XLSM, XLSB, ODS)을 복구합니다. 하나 이상의 파일을 업로드하고 출력 형식을 선택한 후 Base64 형식으로 복구된 파일을 받습니다. 별도의 설치가 필요 없습니다."
weight: 39
---

이 REST API는 Excel 파일을 **복구**할 수 있습니다.

- XLS, XLSX, XLSM, XLSB, ODS 및 기타 스프레드시트 형식을 복구합니다.  
- 단일 요청 내에서 여러 파일을 업로드할 수 있습니다.

Aspose.Cells Cloud Excel 복구는 별도의 설치 없이 온라인으로 손상된 Excel 파일에서 데이터를 복구합니다. 손상된 Excel 파일은 열 수 없어 문제가 됩니다. Aspose.Cells Cloud Excel 복구 앱을 사용하여 이러한 파일에서 데이터를 복구해 볼 수 있습니다.

## REST API

**Excel 파일 복구**(Repair Excel Files) 엔드포인트는 손상된 스프레드시트 파일을 복구하고 복구된 콘텐츠를 반환합니다.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치                         | 설명 |
|---------------|--------|------------------------------|------|
| file          | file   | formData (multipart)         | 업로드할 파일 |
| format        | string | query                        | 원하는 출력 형식입니다. 생략 시(null), 출력 형식은 입력 파일과 동일한 형식으로 기본 설정됩니다. |

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[병합된 파일 이름]",
    "Filesize" : [파일 크기],
    "FileContent" : "[Base64String]"
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error        | 예기치 않은 서버 오류. |

## SDK를 사용하여 PostRepair API 사용하는 방법

### PostRepair API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/LightCells/PostRepair)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하여 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

성공 시 서비스는 `Files` 배열을 포함하는 JSON 페이로드와 함께 HTTP 200 상태 코드를 반환합니다. 오류 상황에는 표준 HTTP 상태 코드를 사용합니다.

- **400 Bad Request** – 잘못된 매개변수 또는 복구 불가능한 파일.  
- **401 Unauthorized** – 누락되거나 잘못된 JWT 토큰.  
- **413 Payload Too Large** – 업로드된 파일이 허용된 크기를 초과함.  
- **500 Internal Server Error** – 예기치 않은 서버 측 오류.

## 클라우드 SDK Family

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
---