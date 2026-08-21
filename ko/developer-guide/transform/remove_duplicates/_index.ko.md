---
title: "중복 제거"
ArticleTitle: "중복 제거 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /ko/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, 중복 제거, API"
description: "워크시트, 범위 또는 테이블에서 중복 값을 제거합니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 중복 제거 기능

워크시트, 범위 또는 테이블에서 중복 값을 제거합니다. 이 메서드는 지정된 열에서 동일한 값을 가진 행을 대상 범위에서 검색하여 중복을 확인합니다. 각 중복 그룹에 대해 첫 번째 발생 항목을 제외한 나머지 중복 항목이 제거됩니다. 비교는 일반적으로 대소문자를 구분하며, 셀 값과 정확히 일치합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 유형   | 경로/쿼리 스트링/HTTP 본문 | 설명 |
|---------------|--------|-----------------------------|------|
| Spreadsheet   | 파일   | FormData                    | 업로드할 스프레드시트 파일입니다. |
| worksheet     | 문자열 | 쿼리                        | 워크시트 이름입니다. (선택 사항) |
| range         | 문자열 | 쿼리                        | 중복 제거가 필요한 범위 이름입니다. (선택 사항) |
| table         | 문자열 | 쿼리                        | 중복 제거가 필요한 테이블 이름입니다. (선택 사항) |
| outPath       | 문자열 | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로입니다. 기본값은 null입니다. |
| outStorageName| 문자열 | 쿼리                        | 출력 파일의 저장소 이름입니다. |
| region        | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱, 로케일 관련 동작에 영향을 줍니다. |
| password      | 문자열 | 쿼리                        | 스프레드시트 파일을 열기 위한 암호입니다. |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **응답**

```json
{
  "File": "결과 스프레드시트의 바이너리 스트림 (예: .xlsx)"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 중복이 제거된 결과 스프레드시트가 파일 스트림으로 반환됩니다. |
| 400 | 잘못된 요청 | 요청 파라미터가 잘못되었거나 URL 형식이 올바르지 않습니다. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 413 | 페이로드가 너무 큼 | 업로드한 파일이 허용된 최대 크기 제한을 초과합니다. |
| 500 | 내부 서버 오류 | 데이터를 가져오는 동안 스프레드시트에 이상이 발생하거나 기타 서버 측 오류가 발생했습니다. |

## SDK를 사용한 중복 제거 방법

### 중복 제거 사양

[중복 제거 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates})은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청하는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "결과 스프레드시트의 바이너리 스트림 (예: .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:

```csharp
// C#용 SDK 예제 코드
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Java용 SDK 예제 코드
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Python용 SDK 예제 코드
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---