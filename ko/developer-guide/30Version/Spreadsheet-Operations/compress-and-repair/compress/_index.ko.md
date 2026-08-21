---
title: "엑셀 파일의 데이터 압축"
ArticleTitle: "엑셀 파일의 데이터 압축 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /compress-excel-files/
aliases: [/compress/]
keywords: "엑셀 파일 압축, aspose cells 클라우드, 엑셀 압축, 스프레드시트 압축, rest api, 파일 압축"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 파일(XLS, XLSX, XLSM, XLSB, ODS)을 압축합니다. 압축 수준을 설정하고, 여러 파일을 처리하며, SDK를 통해 통합할 수 있습니다."
weight: 39
---

## Aspose.Cells Cloud 웹 서비스의 PostCompress API

**사전 조건:**  
- 인증을 위해 유효한 JWT 토큰이 필요합니다.  
- 지원되는 파일 형식은 XLS, XLSX, XLSM, XLSB, ODS입니다.  
- 요청당 최대 허용 파일 크기는 500MB입니다(서비스 제한 사항에 따름).

이 REST API는 엑셀 파일 내의 데이터를 압축합니다.

- XLS, XLSX, XLSM, XLSB, ODS 압축  
- 빠르게 여러 엑셀 스프레드시트 파일 압축  
- 압축 수준 선택 가능  
- 여러 파일 지원

### 웹 API 엔드포인트

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                      |
|---------------|---------|----------------------------|-------------------------------------------|
| file          | file    | formData                   | 업로드할 파일                             |
| CompressLevel | integer | query                      | 압축 수준(0~100); 값이 클수록 더 강한 압축 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명                                  |
| ------------- | ---- | ------------------------------------- |
| data          | file | 압축할 워크북 파일의 이진 콘텐츠입니다. |

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[병합된 파일 이름]",
    "Filesize" : [파일 크기],
    "FileContent" : "[Base64 문자열]"
}
```

*참고:* `FileContent`는 Base64로 인코딩된 압축된 워크북을 포함합니다. 이 문자열의 길이는 압축된 파일의 크기에 해당하며, 표준 Base64 유틸리티를 사용해 디코딩하여 이진 엑셀 파일을 복원할 수 있습니다.

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                         |
|------|-----------------------|----------------------------------------------|
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized          | 유효하지 않거나 누락된 JWT 토큰              |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함           |
| 500  | Internal Server Error | 예기치 않은 서버 오류                         |

## SDK를 사용하여 PostCompress API 사용하기

### PostCompress API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도가 가장 빨라집니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}
---