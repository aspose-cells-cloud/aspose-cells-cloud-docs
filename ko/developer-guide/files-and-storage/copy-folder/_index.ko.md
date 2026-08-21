---
title: "Aspose.Cells Cloud 폴더 복사 API – 클라우드에서 폴더를 빠르게 복사"
secondtitle: "문서"
articletitle: "클라우드 기반 엑셀 파일 관리 솔루션 – Aspose.Cells 폴더 복사 API의 일괄 복사 기능 상세 설명"
linktitle: "폴더 복사"
type: docs
url: /copy-folder/
keywords: "폴더 복사, Aspose.Cells Cloud, REST API, 클라우드 스토리지, 스프레드시트 관리"
description: "단일 REST 호출로 Aspose.Cells Cloud 스토리지 내 폴더를 복사하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 요청, 오류 코드, SDK 예제가 포함됩니다."
weight: 100
---

**CopyFolder** API는 Aspose.Cells Cloud 스토리지 내 기존 폴더를 복제합니다. 이 기능은 백업 생성, 데이터 재조직화, 또는 수동 파일 이동 없이 추가 처리를 위해 폴더 계층 구조를 준비할 때 유용합니다.

## **엑셀 API: 폴더 복사**

### 웹 API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### CopyFolder API는 다음과 같은 매개변수를 수신합니다

| 매개변수 이름       | 필수 여부 | 유형   | 위치(경로/쿼리) | 설명                                                               |
| ----------------- | -------- | ------ | ---------------- | ------------------------------------------------------------------ |
| `srcPath`         | 예       | 문자열 | 경로               | 복사할 원본 폴더의 경로입니다.                                      |
| `destPath`        | 예       | 문자열 | 쿼리             | 새로 생성될 폴더의 경로입니다.                                      |
| `srcStorageName`  | 아니요   | 문자열 | 쿼리             | 원본 폴더가 포함된 스토리지의 이름입니다.                          |
| `destStorageName` | 아니요   | 문자열 | 쿼리             | 폴더를 복사할 대상 스토리지의 이름입니다.                          |

### 샘플 응답

성공적인 호출은 빈 JSON 본문과 함께 **HTTP 200**을 반환합니다:

```json
{}
```

**샘플 cURL 요청**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                             |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됩니다.  |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.    |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰입니다.                                 |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과했습니다.                         |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                      |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해 주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}