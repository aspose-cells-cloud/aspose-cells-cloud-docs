---
title: "엑셀 워크시트에서 여러 열 자동 맞춤"
second_title: "문서"
linktitle: "열"
type: docs
url: /ko/worksheets/autofit/columns/
aliases: [  /ko/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, 열 자동 맞춤, Excel API, 클라우드 스프레드시트, REST"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 엑셀 워크시트에서 여러 열을 자동 맞춤하는 방법을 알아보세요. 엔드포인트, 매개변수, cURL 예제, 오류 처리, C#, Java, Python 등 다양한 언어의 SDK 코드 스니펫이 포함됩니다."
weight: 20
---

이 REST API는 엑셀 워크시트에서 **여러 열**을 자동 맞춤합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **요청 매개변수**

| 매개변수 이름         | 유형     | 위치   | 설명                                                                                                                              |
| --------------------- | ------- | ------ | --------------------------------------------------------------------------------------------------------------------------------- |
| name                  | string  | path   | 파일 이름.                                                                                                                        |
| sheetName             | string  | path   | 워크시트 이름.                                                                                                                    |
| firstColumn           | integer | query  | 시작 열 인덱스.                                                                                                                   |
| lastColumn            | integer | query  | 끝 열 인덱스.                                                                                                                     |
| autoFitterOptions\*   | object  | body   | 자동 맞춤 옵션([자동 맞춤 옵션](/ko/cells/auto-fitter-options/) 참조). `AutoFitMergedCells`, `IgnoreHidden`, `OnlyAuto` 포함. |
| firstRow              | integer | query  | 자동 맞춤 시작 행 인덱스(**선택 사항**).                                                                                          |
| lastRow               | integer | query  | 자동 맞춤 끝 행 인덱스(**선택 사항**).                                                                                            |
| folder              | string  | query  | 스토리지 내 폴더 경로(**선택 사항**).                                                                                             |
| storageName           | string  | query  | 스토리지 이름(**선택 사항**).                                                                                                      |

\* 매개변수 이름은 관련 문서로 연결된 링크로 표시됩니다.

[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 가장 좋은 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}