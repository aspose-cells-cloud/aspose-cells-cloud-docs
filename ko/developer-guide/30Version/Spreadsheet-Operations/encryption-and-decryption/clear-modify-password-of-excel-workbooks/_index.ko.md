---
title: "엑셀 워크북에서 쓰기 방지(암호) 제거하기"
second_title: "문서"
linktype: "엑셀 파일 암호 해제"
type: docs
url: /ko/clear-excel-files-password/
aliases:
  [
    "/cells/ko/clear-modify-password-of-excel-workbooks/",
    "/cells/ko/workbook/clear-modify-password/",
    "/cells/ko/workbook/password/clear/",
  ]
keywords: "Aspose.Cells, Excel, 암호 제거, 쓰기 방지, REST API, SDK 예제"
description: "Aspose.Cells Cloud REST API를 사용해 엑셀 워크북의 쓰기 방지(암호)를 삭제하는 방법을 알아보세요. cURL 예제, 인증 단계 및 SDK 코드 예제가 포함되어 있습니다."
weight: 110
ArticleTitle: "엑셀 워크북에서 쓰기 방지(암호) 제거하기"
---

이 REST API는 엑셀 워크북에서 **쓰기 방지(암호)** 를 제거하여 프로그래밍 방식으로 **엑셀 파일 암호 보호를 해제**할 수 있도록 합니다.

**필수 조건:** 유효한 JWT 토큰을 획득하고, 워크북이 지원되는 저장소 위치에 저장되어 있어야 하며, API 버전 v3.0을 사용해야 합니다.

보호를 추가하려면 [엑셀 보호](/ko/cells/protect/) 가이드를 참조하세요.

## DeleteDocumentUnprotectFromChanges API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/ko/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                            |
| ------------- | ------ | ---- | ----------------------------------------------- |
| `name`        | string | path | 엑셀 워크북의 이름입니다.                        |
| `folder`      | string | query | 워크북이 포함된 폴더입니다(선택 사항).          |
| `storageName` | string | query | 저장소 서비스의 이름입니다(선택 사항).          |


### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                               |
| ---- | ------------------------- | -------------------------------------------------- |
| 200  | OK                        | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | 잘못된 요청                | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | 인증되지 않음              | 잘못되거나 누락된 JWT 토큰                          |
| 413  | 페이로드가 너무 큼         | 업로드된 파일이 크기 제한을 초과함                  |
| 500  | 내부 서버 오류             | 예기치 않은 서버 오류                               |

## SDK를 사용하여 DeleteDocumentUnprotectFromChanges API 사용하는 방법

### DeleteDocumentUnprotectFromChanges API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/ko#/Workbook/DeleteDocumentUnprotectFromChanges)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 실행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 REST API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}