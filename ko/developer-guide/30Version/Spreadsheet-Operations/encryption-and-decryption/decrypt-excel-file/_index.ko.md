---
title: "엑셀 워크북 복호화"
second_title: "문서"
linktitle: "엑셀 파일 복호화"
type: docs
url: /ko/excel-file-decrypt/
aliases: [  /ko/decrypt-excel-workbooks/ , /ko/workbook/decrypt/ ]
keywords: "Aspose.Cells, 엑셀 복호화, REST API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크북을 복호화하는 방법을 배워보세요. 필수 매개변수, cURL 예제, SDK 코드 예제, 오류 처리 세부 정보를 포함합니다."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 엑셀 워크북을 복호화하는 방법"
weight: 50
---

**사전 요구 사항**

- 유효한 JWT 액세스 토큰.
- 워크북이 Aspose Cloud 스토리지에 업로드되어 있어야 하며, `folder` 쿼리 매개변수에 경로가 지정되어야 합니다.

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 필요로 합니다.

### 쿼리 매개변수

| 매개변수 이름 | 유형   | 설명                                      |
| -------------- | ------ | ------------------------------------------- |
| folder         | string | 원본 워크북이 위치한 폴더 경로.             |
| storageName    | string | 워크북이 저장된 스토리지 이름.              |

### 요청 본문 매개변수

| 매개변수 이름 | 유형                      | 설명                                   |
| -------------- | ------------------------- | ---------------------------------------- |
| encryption     | WorkbookEncryptionRequest | 복호화에 필요한 암호화 설정.             |

### WorkbookEncryptionRequest

| 매개변수 이름 | 유형    | 설명                                                                                                   |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| EncryptionType | string  | 암호화 알고리즘 (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer | 암호화 키의 길이(비트 단위).                                                                         |
| Password       | string  | 복호화에 사용되는 비밀번호.                                                                                 |

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**샘플 오류 응답**

```json
{
  "Code": "400",
  "Message": "잘못된 요청 매개변수입니다."
}
```

```json
{
  "Code": "401",
  "Message": "인증에 실패했습니다. 유효하지 않거나 누락된 JWT 토큰입니다."
}
```

```json
{
  "Code": "413",
  "Message": "페이로드가 너무 큽니다. 업로드된 파일이 허용된 크기를 초과했습니다."
}
```

```json
{
  "Code": "500",
  "Message": "내부 서버 오류입니다. 나중에 다시 시도해 주세요."
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                              |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

## SDK를 사용하여 DeleteDecryptWorkbook API 사용하는 방법

### DeleteDecryptWorkbook API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL**을 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---