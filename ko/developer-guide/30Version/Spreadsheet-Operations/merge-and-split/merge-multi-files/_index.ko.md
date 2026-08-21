---
title: "여러 Excel 파일을 단일 워크북으로 병합"
second_title: "문서"
linktitle: "여러 Excel 파일 병합"
type: docs
url: /ko/merge-multi-files-into-excel/
aliases: [  /ko/merge/multi-files/ ]
keywords: "Aspose.Cells Cloud, 여러 Excel 파일 병합, REST API, 스프레드시트 병합, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 여러 Excel 워크북을 하나의 파일로 병합하는 방법을 알아보세요. HTTPS 엔드포인트, cURL 명령어, SDK 샘플, 필수 파라미터 및 오류 처리 세부 정보가 포함됩니다."
weight: 32
---

## REST API

이 REST API는 여러 Excel 파일을 하나의 Excel 워크북으로 병합합니다.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 요청 파라미터

| 파라미터 이름   | 타입    | 위치       | 설명                                                                 | 필수 여부 |
| --------------- | ------- | ---------- | -------------------------------------------------------------------- | --------- |
| files[]         | file    | formData   | 병합할 하나 이상의 Excel 워크북. 요청 시 `file1`, `file2`, …를 사용합니다. | 예        |
| format          | string  | query      | 원하는 출력 형식(예: `xlsx`).                                          | 예        |
| mergeToOneSheet | boolean | query      | 모든 워크시트를 단일 시트로 통합하려면 `true`로 설정합니다. 기본값은 `false`입니다. | 아니요    |

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

| 코드 | 의미                        | 설명                                                      |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.       |
| 400  | 잘못된 요청(Bad Request)    | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식).   |
| 401  | 인증되지 않음(Unauthorized) | 잘못되거나 누락된 JWT 토큰.                                |
| 413  | 페이로드가 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과함.               |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류.                            |

## SDK를 사용하여 PostMerge API 사용하는 방법

### PostMerge API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64String--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}