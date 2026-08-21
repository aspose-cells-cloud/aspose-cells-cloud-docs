---
title: "Aspose.Cells Cloud API로 Excel 워크북 암호화하기 – 빠른 cURL 및 SDK 예제"
second_title: "문서"
linktitle: "Excel 파일 암호화"
type: docs
url: /ko/excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/, /workbook/encrypt/]
keywords: "Aspose Cells 워크북 암호화, Excel 암호화 API, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크북을 암호화하는 방법을 알아보세요. cURL 명령어, SDK 코드 예제(C#, Java, Python 등), 필수 매개변수 및 오류 처리가 포함됩니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API로 Excel 워크북 암호화하기 – cURL 및 SDK 예제"
---

이 REST API는 Excel **워크북**을 암호화합니다.

**사전 조건:** 이 엔드포인트를 호출하기 전에 유효한 JWT 토큰을 보유하고 워크북을 스토리지 위치에 업로드해야 합니다.

## PostEncryptDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **쿼리 매개변수**

| 매개변수 이름 | 유형   | 필수 여부 | 설명                                      |
| -------------- | ------ | -------- | ----------------------------------------- |
| folder         | string | ✗        | 원본 워크북이 위치한 폴더 경로입니다.     |
| storageName    | string | ✗        | 사용할 스토리지 이름입니다.               |

### **요청 본문 매개변수**

| 매개변수 이름 | 유형                      | 필수 여부 | 설명                              |
| -------------- | ------------------------- | -------- | --------------------------------- |
| encryption     | WorkbookEncryptionRequest | ✓        | 워크북에 적용할 암호화 설정입니다. |

#### **WorkbookEncryptionRequest**

| 매개변수 이름 | 유형    | 필수 여부 | 설명                                                                                       |
| -------------- | ------- | -------- | ------------------------------------------------------------------------------------------ |
| EncryptionType | string  | ✓        | 암호화 알고리즘입니다. 지원되는 값 및 의미는 아래 표를 참조하세요.                         |
| KeyLength      | integer | ✗        | 암호화 키의 길이(비트 단위). `XOR` 및 `Compatible`의 경우 무시됩니다.                    |
| Password       | string  | ✓        | 암호화에 사용되는 비밀번호입니다.                                                          |

#### **EncryptionType 값**

| 값                                | 설명                                               |
| --------------------------------- | -------------------------------------------------- |
| `XOR`                             | 간단한 XOR 알고리즘(레거시, 낮은 보안 수준).        |
| `Compatible`                      | Excel 97-2003 호환 암호화(40비트).                 |
| `EnhancedCryptographicProviderV1` | SHA-1 해시를 사용한 AES-128.                        |
| `StrongCryptographicProvider`     | SHA-512 해시를 사용한 AES-256(가장 강력한 수준).    |

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                             |
|------|-----------------------|------------------------------------------------------------------|
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됨.      |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).         |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                                      |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함.                              |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                           |

## SDK를 사용하여 PostEncryptDocument API 사용하기

### PostEncryptDocument API 사양

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# XOR 알고리즘(128비트 키)과 비밀번호 "mateen"을 사용하여 워크북 "test.xlsx" 암호화
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**가능한 오류 응답**

| HTTP 상태 | 코드                | 메시지                                          |
| --------- | ------------------- | ----------------------------------------------- |
| 400       | BadRequest          | 누락되거나 잘못된 매개변수.                     |
| 401       | Unauthorized        | 인증 토큰이 없거나 유효하지 않습니다.             |
| 403       | Forbidden           | 스토리지에 액세스할 수 있는 권한이 부족합니다.  |
| 500       | InternalServerError | 예기치 않은 서버 오류.                          |

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 크게 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}