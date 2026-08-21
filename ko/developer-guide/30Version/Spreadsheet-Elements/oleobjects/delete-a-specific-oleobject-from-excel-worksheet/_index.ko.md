---
title: "Excel 워크시트에서 OLE 개체 삭제하기"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /ko/oleobjects/delete/
aliases: [/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, 클라우드, 삭제, OLE, 개체, Excel, 워크시트, REST, API, SDK"
description: "Aspose.Cells Cloud REST API(v4.0)를 사용하여 Excel 워크시트에서 OLE 개체를 삭제하는 방법을 배웁니다. HTTPS 엔드포인트, 인증 절차, cURL 예제, SDK 코드 스니펫, 오류 처리 가이드, 다음 단계 링크가 포함됩니다."
weight: 50
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 OLE 개체 삭제하기"
---

이 페이지에서는 **Aspose.Cells Cloud**를 사용하여 Excel 워크북의 워크시트에서 특정 OLE 개체를 삭제하는 방법을 설명합니다. OLE 개체는 연결된 이미지, 차트 또는 Excel이 별도 엔티티로 저장하는 임의의 임베디드 개체일 수 있습니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안을 위해 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)을 요구합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### 요청 매개변수

| 매개변수 이름     | 유형     | 위치   | 설명                                                |
| ----------------- | -------- | ------ | --------------------------------------------------- |
| name              | string   | path   | 워크북 이름.                                        |
| sheetName         | string   | path   | 워크시트 이름.                                      |
| oleObjectIndex    | integer  | path   | 삭제할 OLE 개체의 인덱스.                           |
| folder            | string   | query  | 워크북이 포함된 폴더. (선택 사항)                  |
| storageName       | string   | query  | 스토리지 서비스 이름. (선택 사항)                  |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL 명령줄 도구**를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 요청을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### 응답 세부사항

| HTTP 상태 코드       | 설명                                                               | 예시 JSON                                                         |
| -------------------- | ------------------------------------------------------------------ | ----------------------------------------------------------------- |
| **200 OK**           | OLE 개체가 성공적으로 삭제되었습니다.                              | `{ "Code": 200, "Status": "OK" }`                                 |
| **401 Unauthorized** | JWT 토큰이 누락되었거나 유효하지 않습니다.                           | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | 지정된 워크북, 워크시트 또는 OLE 개체 인덱스가 존재하지 않습니다.    | `{ "Code": 404, "Message": "OLE object index out of range." }`    |
| **400 Bad Request**  | 필수 매개변수가 누락되었거나 잘못된 형식입니다.                    | `{ "Code": 400, "Message": "Invalid request parameters." }`       |

응용 프로그램에서 상태 코드를 확인하고 관련 메시지를 표시하여 이러한 응답을 처리하세요.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}