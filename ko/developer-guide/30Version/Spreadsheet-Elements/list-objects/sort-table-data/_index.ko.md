---
title: "엑셀 워크시트에서 ListObject 데이터 정렬하기"
second_title: "Document"
linktitle: "Sort"
type: docs
url: /ko/list-objects/sort-data/
aliases: [  /ko/get-a-list-object-or-table-inside-the-worksheet/ , /ko/tables/sort-data/ ]
keywords: "Aspose.Cells Cloud, Excel, ListObject, 데이터 정렬, REST API, 워크시트"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 엑셀 워크시트 내 ListObject(테이블) 데이터를 정렬하는 방법을 배웁니다. 엔드포인트, 매개변수, 샘플 cURL 요청 및 SDK 예제가 포함되어 있습니다."
weight: 40
ArticleTitle: "엑셀 워크시트에서 ListObject 데이터 정렬하기 – Aspose.Cells Cloud API"
---

**사전 준비 사항**  
이 API를 호출하려면 유효한 Aspose Cloud JWT 액세스 토큰이 필요하며, 워크북을 Aspose Cloud 저장소에 업로드해야 합니다. 모든 요청에서 헤더 `Authorization: Bearer <jwt token>`을 포함해야 합니다.

이 REST API는 엑셀 워크시트 내 테이블 데이터를 정렬합니다.  
이 작업을 사용하려면 워크북 이름, 워크시트 이름 및 대상 ListObject의 인덱스를 제공하고, 정렬 기준을 정의하는 `dataSorter` JSON 본문을 함께 전달해야 합니다.

## PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수**

| 매개변수 이름     | 유형     | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                         |
| ---------------- | ------- | ------------------------- | ----------------------------------------------------------------------------------------------------------- |
| name             | string  | path                      | Aspose Cloud 저장소에 저장된 엑셀 파일의 이름.                                                               |
| sheetName        | string  | path                      | ListObject가 포함된 워크시트의 이름.                                                                         |
| listObjectIndex  | integer | path                      | 워크시트 내 ListObject(테이블)의 0부터 시작하는 인덱스.                                                      |
| dataSorter       | object  | body                      | 정렬 옵션을 지정하는 JSON 객체(예: `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`).             |
| folder           | string  | query                     | Excel 파일이 위치한 저장소 내 폴더 경로.                                                                     |
| storageName      | string  | query                     | Aspose Cloud 저장소의 이름.                                                                                  |

**참고 사항**  
요청 본문은 `dataSorter` 스키마와 일치하는 유효한 JSON 객체여야 합니다. 정렬 작업을 호출하기 전에 워크북, 워크시트 및 ListObject가 존재하는지 확인해야 합니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 상태 코드 | 설명                                         |
|----------|---------------------------------------------|
| 200      | OK – 정렬이 성공적으로 완료됨.               |
| 400      | Bad Request – 잘못된 매개변수.               |
| 401      | Unauthorized – 인증 실패.                    |
| 404      | Not Found – 워크북, 워크시트 또는 ListObject를 찾을 수 없음. |
| 500      | Internal Server Error – 서버 측 문제.        |

**응답 매개변수**

| 매개변수 | 유형    | 설명                                      |
|---------|--------|------------------------------------------|
| Code    | integer | API에서 반환된 HTTP 상태 코드.              |
| Status  | string  | 결과에 대한 텍스트 설명(예: "OK").          |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[목록 개요로 돌아가기](/list-objects/)