---
title: "Excel 워크북에서 행 자동 맞춤"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/autofit-rows-on-an-excel-file/
aliases: [  /ko/auto-fit-rows-in-excel-workbooks/ , /ko/workbook/autofit/rows/ ]
keywords: "행 자동 맞춤, Excel 워크북, Aspose.Cells Cloud, REST API, 자동 맞춤 옵션"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 행 높이를 자동으로 조정하는 방법을 알아보세요. 엔드포인트, 매개변수, cURL 예제, C#, Java, Python 등 다양한 언어의 SDK 스니펫이 포함되어 있습니다."
weight: 90
ArticleTitle: "Excel 워크북에서 행 자동 맞춤 – Aspose.Cells Cloud API"
---

**사전 요구 사항**  
API를 호출하기 전에 Aspose 인증 서비스에서 유효한 Bearer JWT 토큰을 획득하고, 대상 워크북이 지원되는 저장소 위치(기본 저장소 또는 구성한 사용자 정의 저장소)에 저장되어 있는지 확인해야 합니다.

이 REST API는 Excel 워크북에서 **행 자동 맞춤**을 수행할 수 있도록 해 주며, 데이터 삽입 또는 수정 후 행 높이를 자동으로 조정합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름       | 유형              | 위치   | 설명                                                                                  |
| ------------------- | ----------------- | ------ | ------------------------------------------------------------------------------------- |
| name                | string            | path   | 워크북 파일 이름.                                                                     |
| autoFitterOptions   | AutoFitterOptions | body   | 자동 맞춤 동작을 제어하는 옵션.                                                       |
| startRow            | integer           | query  | 자동 맞춤할 첫 번째 행의 인덱스.                                                      |
| endRow              | integer           | query  | 자동 맞춤할 마지막 행의 인덱스.                                                       |
| firstColumn         | integer           | query  | 자동 맞춤 시 고려할 첫 번째 열의 인덱스.                                              |
| lastColumn          | integer           | query  | 자동 맞춤 시 고려할 마지막 열의 인덱스.                                               |
| onlyAuto            | boolean           | query  | **true**인 경우 자동 맞춤 플래그가 설정된 행만 처리합니다(기본값: **false**).         |
| folder              | string            | query  | 워크북이 저장된 폴더 경로.                                                            |
| storageName         | string            | query  | 저장소 서비스 이름.                                                                   |

**AutoFitterOptions**는 자동 맞춤 작업 동작을 지정하는 객체입니다(예: `AutoFitMergedCells`, `IgnoreHidden`).

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                                       |
|------|------------------------|------------------------------------------------------------|
| 200  | OK(성공)               | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request(잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | Unauthorized(인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large(페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과했습니다.              |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다.                   |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. `<jwt token>`을 Aspose 인증 서비스에서 획득한 유효한 Bearer JWT 토큰으로 대체하세요.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*예시 오류 응답(예: 워크북 누락 시):*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "지정된 워크북 'myWorkbook.xlsx'가 존재하지 않습니다."
}
```

{{< /tab >}}

{{< /tabs >}}

**참고 사항**  
- `AutoFitMergedCells`를 **true**로 설정하면 병합된 셀이 자동 맞춤 작업 시 단일 엔티티로 간주됩니다.  
- `IgnoreHidden`을 **true**로 설정하면 숨겨진 행과 열은 건너뛰며, 현재 치수를 유지합니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 개발에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}