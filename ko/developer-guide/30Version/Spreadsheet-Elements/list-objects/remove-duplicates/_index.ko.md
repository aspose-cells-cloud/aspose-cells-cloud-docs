---
title: "목록 개체에서 중복 행 제거하기 – Aspose.Cells Cloud API 문서"
second_title: "문서"
linktitle: "중복 제거"
type: docs
keywords: "중복 제거, 목록 개체, Aspose.Cells Cloud API, Excel, REST"
url: /list-objects/remove-duplicates/
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 목록 개체에서 중복 행을 삭제하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증, 샘플 요청 및 응답이 포함됩니다."
weight: 20
---

이 REST API는 Excel 워크시트 내 **목록 개체(ListObject)**에서 중복 행을 제거합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **요청 매개변수**

| 매개변수 이름        | 타입     | 위치   | 설명                                                |
| ------------------- | ------- | ------ | --------------------------------------------------- |
| **name**            | String  | Path   | Excel 파일의 이름입니다.                            |
| **sheetName**       | String  | Path   | 목록 개체가 포함된 워크시트의 이름입니다.          |
| **listObjectIndex** | Integer | Path   | 처리할 목록 개체의 0부터 시작하는 인덱스입니다.     |
| **folder**          | String  | Query  | (선택 사항) 파일이 저장된 폴더 경로입니다.         |
| **storageName**     | String  | Query  | (선택 사항) 스토리지 서비스의 이름입니다.           |

### 샘플 요청(cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "중복 행이 성공적으로 제거되었습니다."
}
```

{{< /tab >}}
{{< /tabs >}}

### 응답

성공 시 서비스는 위 예시와 유사한 JSON 객체를 반환합니다. 필드는 다음과 같습니다:

- **Code** – HTTP 상태 코드(`200`은 성공을 의미함).
- **Status** – 상태에 대한 텍스트 설명.
- **DuplicateRowsRemoved** – 제거된 행의 수.
- **Message** – 작업에 대한 추가 정보.

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                  |
|------|------------------------------|-------------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰.                            |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함.                   |
| 500  | Internal Server Error        | 예기치 않은 서버 오류.                                 |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 GitHub 저장소를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}