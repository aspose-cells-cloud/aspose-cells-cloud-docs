---
title: "Aspose.Cells Cloud 파일 버전 조회 API – 파일 버전 히스토리 빠른 조회"
second_title: "문서"
ArticleTitle: "클라우드 기반 Excel 관리 – Aspose.Cells Cloud에서 파일 버전 히스토리 빠르게 조회"
linktype: "docs"
url: /ko/get-file-versions/
keywords: "Aspose Cells API, 파일 버전, 스프레드시트 버전 관리, 클라우드 저장소 API, REST, Excel 파일 히스토리"
description: "Aspose.Cells Cloud에 저장된 모든 Excel 파일에 대한 버전 히스토리 목록을 전체적으로 조회합니다. 저장소 선택, 인증, 상세 오류 코드를 지원합니다."
weight: 100
---

Aspose.Cells Cloud에 저장된 특정 스프레드시트에 대한 전체 버전 기록 목록을 조회합니다. 이 엔드포인트는 개발자가 클라우드 저장소에서 직접 변경 사항을 추적하고, 수정 이력을 감사하며, 버전 관리 워크플로우를 직접 구현할 수 있도록 지원합니다.

**GetFileVersions** API는 Aspose.Cells Cloud에 저장된 지정된 스프레드시트에 대한 모든 버전 기록을 반환합니다. 이를 통해 각 파일에 대한 변경 이력을 완전히 유지할 수 있습니다.

## **Excel API: 파일 버전 조회**

### 웹 API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **GetFileVersions** API의 요청 파라미터는 다음과 같습니다.

| 파라미터 이름 | 유형   | 위치 | 설명                                                                                      |
| ------------- | ------ | ---- | ----------------------------------------------------------------------------------------- |
| `path`        | String | Path | **필수.** 버전을 조회할 파일의 전체 경로.                                                 |
| `storageName` | String | Query | 선택 사항. 파일이 저장된 저장소 이름. 생략 시 기본 저장소가 사용됩니다.                   |

### **응답**

```json
{
  "Name": "FileVersions",
  "Description": [
    "지정된 문서에 대한 파일 버전 목록을 포함합니다."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["파일 버전 세부 정보의 컬렉션."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

성공 시, API는 위 예시와 같이 `FileVersion` 객체의 `Value` 배열을 포함하는 JSON 페이로드와 함께 **HTTP 200 OK**를 반환합니다.

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                       |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | Bad Request (잘못된 요청) | 누락되었거나 잘못된 파라미터(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized (인증되지 않음) | 잘못되었거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large (페이로드 너무 큼) | 업로드된 파일이 크기 제한을 초과함.                     |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                   |

## OpenAPI 명세서

[OpenAPI 명세서](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)는 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있는 포괄적인 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 활용하면 저수준 복잡성을 추상화하여 개발자가 핵심 기능에 집중할 수 있도록 도와줍니다. [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 Aspose.Cells Cloud SDK의 전체 목록을 확인할 수 있습니다.

다음 코드 예시는 다양한 프로그래밍 언어에서 Aspose.Cells 웹 서비스와 상호작용하는 방법을 설명합니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}