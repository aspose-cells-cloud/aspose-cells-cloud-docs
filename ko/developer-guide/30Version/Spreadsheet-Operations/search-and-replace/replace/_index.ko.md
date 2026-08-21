---
title: "Excel 파일에서 텍스트 교체"
second_title: "문서"
linktitle: "스토리지 사용 없이 교체"
type: docs
url: /replace/ko/
keywords: "Excel 텍스트 교체, Aspose.Cells Cloud, REST API, 스프레드시트 교체, API, Excel 파일 텍스트 교체"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일의 기존 텍스트를 새로운 값으로 교체합니다. C#, Java, Python, Node.js, PHP, Ruby, Go, Perl용 SDK를 지원합니다."
weight: 80
---


## REST API

이 REST API는 Excel 파일의 데이터를 교체합니다.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.


### 요청 파라미터

| 파라미터 이름 | 유형   | 위치             | 설명                                   |
| -------------- | ------ | -------------------- | --------------------------------------------- |
| **file**       | 파일   | formData (multipart) | 처리할 Excel 파일입니다.                   |
| **text**       | 문자열 | query                | 교체할 텍스트 문자열입니다.                   |
| **newtext**    | 문자열 | query                | 교체할 텍스트입니다.                             |
| **password**   | 문자열 | query                | 보호된 워크북의 비밀번호입니다(선택 사항). |
| **sheetname**  | 문자열 | query                | 대상 워크시트 이름입니다(선택 사항).   |

### **응답**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[파일1 이름]",
      "Filesize" : [파일 크기],
      "FileContent" : "[Base64문자열]"
    },
    {
      "Filename" : "[파일2 이름]",
      "Filesize" : [파일 크기],
      "FileContent" : "[Base64문자열]"
    },
    {
      "Filename" : "[파일3 이름]",
      "Filesize" : [파일 크기],
      "FileContent" : "[Base64문자열]"
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (성공)                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청                 | 누락되거나 유효하지 않은 파라미터(예: 지원되지 않는 파일 유형)입니다. |
| 401  | 인증되지 않음                | 유효하지 않거나 누락된 JWT 토큰입니다. |
| 413  | 페이로드가 너무 큼           | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | 내부 서버 오류       | 예기치 않은 서버 오류입니다. |
## SDK를 사용하여 PostReplace API 사용하는 방법

### PostReplace API 사양


[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64문자열--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64문자열--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해 주므로 프로젝트 작업에 집중할 수 있습니다. 전체 Aspose.Cells Cloud SDK 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

---