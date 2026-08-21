---
title: "스토리지 사용 없이 데이터 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "스토리지 없이 데이터 가져오기"
type: docs
url: /import/without-using-storage/
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: "Aspose.Cells, 클라우드 API, 스토리지 없이 데이터 가져오기, Excel 가져오기 API, REST 가져오기"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에 스토리지 없이 데이터를 가져오는 방법을 알아보세요. 요청 형식, 매개변수, cURL 예제, SDK 코드 및 오류 처리를 포함합니다."
weight: 10
ArticleTitle: "스토리지 사용 없이 데이터 가져오기 – Aspose.Cells Cloud API"
---

Excel 데이터 가져오기는 많은 요인이 결과에 영향을 미치기 때문에 복잡할 수 있습니다. 이러한 모든 요인은 **가져오기** 과정 중에 고려되어야 합니다. Aspose.Cells Cloud는 전문 수준의 품질로 다양한 형식과 데이터 유형을 Excel 파일로 쉽게 가져올 수 있습니다.

이 REST API는 Excel 파일로 **데이터**를 가져옵니다.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형            | 위치       | 설명                                                                                                                                     |
| ------------- | --------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| file          | 파일            | formData   | 업로드할 Excel 파일.                                                                                                                     |
| ImportOption  | ImportOption    | JSON 본문  | 가져올 데이터, 데이터 유형(`IntArray`, `DoubleArray`, `StringArray` 등), 워크시트 내 배치 위치를 정의하는 JSON 객체입니다.                |

**ImportOption** 매개변수에 대한 자세한 내용은 **ImportData 옵션 참조** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter)를 확인하세요.

**사전 요구 사항:**  
사전에 유효한 JWT 토큰을 생성해야 하며, 파일 크기는 서비스 제한(일반적으로 100MB)을 초과할 수 없습니다. 지원되는 파일 형식은 XLS, XLSX, CSV 및 ODS입니다. 프로그래밍 방식 접근을 선호하는 경우 적절한 SDK가 설치되어 있는지 확인하세요.

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                      |
|------|-----------------------|-----------------------------------------------------------|
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됨. |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).   |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과함.                        |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                     |

**참고:**  
요청을 전송할 때 `Content-Type: multipart/form-data` 헤더는 `-F` 플래그에 의해 자동으로 설정됩니다. 큰 페이로드의 경우 가져오기 전에 데이터를 압축하고 일시적 오류에 대한 재시도 로직을 구현하는 것이 좋습니다.

## SDK를 사용하여 PostImportData API 사용 방법

### PostImportData API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*`-F` 플래그는 자동으로 `Content-Type: multipart/form-data`를 설정합니다.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}