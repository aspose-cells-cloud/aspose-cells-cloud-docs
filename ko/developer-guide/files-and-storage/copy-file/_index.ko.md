---
title: "Aspose.Cells Cloud 파일 복사 API - 클라우드에서 Excel 파일을 빠르게 복사하고 일괄 작업을 수행하기 위한 인터페이스"
second_title: "문서"
ArticleTitle: "클라우드 기반 Excel 파일 관리 솔루션 – Aspose.Cells 복사 파일 API의 일괄 복사 기능 상세 설명"
linktitle: "파일 복사"
type: docs
url: /ko/copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel 파일 복사, 클라우드 저장소, REST API"
description: "Aspose.Cells Cloud CopyFile API를 사용하여 Excel 파일을 효율적으로 복제하고 저장소 간에 관리하는 방법을 알아보세요."
weight: 100
---

**copyFile** API를 사용하면 지정된 소스 경로에서 대상 경로로 Excel 파일을 복사할 수 있으며, 다양한 저장소 옵션을 지원합니다.

## **Excel API: 파일 복사**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **copyFile** API의 요청 파라미터는 다음과 같습니다

| 파라미터 이름    | 유형   | 경로/쿼리 스트링/HTTP 본문 | 설명                                               |
| ---------------- | ------ | -------------------------- | -------------------------------------------------- |
| srcPath          | String | Path                       | 복사할 파일의 소스 경로                            |
| destPath         | String | Query                      | 파일이 저장될 대상 경로                            |
| srcStorageName   | String | Query                      | 소스 저장소 이름                                   |
| destStorageName  | String | Query                      | 대상 저장소 이름                                   |
| versionId        | String | Query                      | 복사할 파일의 선택적 버전 ID                       |

### **응답**

성공 시 이 작업은 콘텐츠를 반환하지 않습니다. 일반적인 HTTP 상태 코드는 다음과 같습니다:

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                         |
| ---- | --------------------- | ------------------------------------------------------------ |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함         |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식)    |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰                                 |
| 413  | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과함                         |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류                                     |

## SDK를 사용하여 복사 파일 API를 어떻게 사용하나요?

### 복사 파일 API 사양

[복사 파일 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 제공되는 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화해 최소한의 코드로 스프레드시트 테이블 데이터를 이미지로 변환할 수 있으므로 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

---