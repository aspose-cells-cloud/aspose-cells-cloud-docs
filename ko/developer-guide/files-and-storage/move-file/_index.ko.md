---
title: "Aspose.Cells Cloud Move File API – 클라우드 내 파일 빠르게 이동을 위한 인터페이스"
second_title: "문서"
ArticleTitle: "클라우드 기반 Excel 파일 효율적 관리 솔루션 – 클라우드 내 파일 빠르게 이동을 위한 인터페이스"
linktype: "이동 파일"
type: docs
url: /ko/move-file/
keywords: "Aspose.Cells, Move File API, 클라우드 스토리지, Excel API, 파일 관리"
description: "Aspose.Cells Cloud 스토리지 내에서 폴더 간 파일을 이동하는 방법 – v4.0 Move File API의 엔드포인트, 매개변수, 예제 및 SDK 링크."
weight: 100
---

**moveFile** API는 Aspose.Cells Cloud 스토리지 내에서 파일을 한 위치에서 다른 위치로 이동시킵니다. 이를 통해 파일을 정리하고 스토리지를 효율적으로 관리할 수 있습니다.

## **Excel API: 파일 이동**

### 웹 API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **moveFile** API의 요청 매개변수는 다음과 같습니다.

| 매개변수 이름     | 유형   | 경로/쿼리 스트링/HTTP 본문 | 설명                                                   |
| ----------------- | ------ | -------------------------- | ------------------------------------------------------ |
| srcPath           | String | 경로                       | 이동할 원본 파일의 경로입니다.                         |
| destPath          | String | 쿼리                       | 파일이 이동될 대상 경로입니다.                         |
| srcStorageName    | String | 쿼리                       | 원본 스토리지 이름(해당하는 경우)입니다.               |
| destStorageName   | String | 쿼리                       | 대상 스토리지 이름(해당하는 경우)입니다.               |
| versionId         | String | 쿼리                       | 파일의 버전 ID(해당하는 경우)입니다.                   |

### **응답**

성공적인 요청은 빈 JSON 본문과 함께 **HTTP 200 OK** 상태 코드를 반환합니다.

```json
{}
```

**HTTP 상태 코드**

| HTTP 코드 | HTTP 상태               | 설명                                                         |
| --------- | ----------------------- | ------------------------------------------------------------ |
| 200       | OK                      | 웹 API가 성공적으로 호출되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400       | Bad Request             | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다. |
| 401       | Unauthorized            | 잘못되거나 누락된 JWT 토큰입니다.                            |
| 413       | Payload Too Large       | 업로드된 파일이 크기 제한을 초과했습니다.                    |
| 500       | Internal Server Error   | 예기치 않은 서버 오류입니다.                                 |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/FileController/MoveFile)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트의 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다.