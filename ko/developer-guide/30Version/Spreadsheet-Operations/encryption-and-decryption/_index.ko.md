---
title: "Excel 파일 암호화, 복호화 및 디지털 서명"
second_title: "문서"
linktype: "보호 Excel"
type: docs
url: /ko/protect/
aliases: [  /ko/workbook/password/ ]
keywords: "Excel, 보호, 암호화, 복호화, 디지털 서명, Aspose.Cells Cloud, REST API, 비밀번호, 보안"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 보호, 암호화, 복호화 및 디지털 서명하는 방법을 배워보세요 – Android, C#, Java, Python 등 다양한 언어의 코드 예제 포함."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 파일 암호화, 복호화, 디지털 서명 및 보호"
weight: 36
---

## **Excel 파일 보호 및 보호 해제**

**Aspose.Cells Cloud에서 “보호”란 무엇인가요?**  
**보호**(Protect) 작업은 비밀번호를 적용하여 파일 열기, 편집 또는 구조 수정을 제한함으로써 Excel 워크북을 보호합니다. 이 API는 워크북 암호화, 복호화 및 위변조 방지를 위한 디지털 서명 추가도 지원합니다.

**API 참조**  

| HTTP 메서드 | 엔드포인트 | 필수 쿼리/본문 매개변수 | 샘플 요청 본문 | 일반적인 응답 |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName`(경로), `password`(쿼리) | `{ "password": "MySecret123" }` | `200 OK` – 보호 적용됨, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName`(경로), `password`(쿼리) | 없음 | `200 OK` – 보호 해제됨, 위와 동일한 오류 코드 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName`(경로), `password`(쿼리) | 없음 | `200 OK` – 파일 암호화됨 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName`(경로), `password`(쿼리) | 없음 | `200 OK` – 파일 복호화됨 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName`(경로) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – 디지털 서명 추가됨 |

**코드 예제(C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API 클라이언트 초기화
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// 워크북 보호
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**사전 요구사항**  
- 활성화된 Aspose.Cells Cloud 구독  
- 인증을 위한 `AppSid` 및 `AppKey`  

**인증**  
모든 요청은 Aspose Cloud 인증 엔드포인트에서 획득한 유효한 JWT 토큰을 포함하는 `Authorization` 헤더를 포함해야 합니다.

**오류 처리**  
응답 본문에 반환된 HTTP 상태 코드와 `Error` 개체를 확인하세요. 일반적인 오류로는 잘못된 비밀번호(`400`), 파일 누락(`404`), 인증 실패(`401`) 등이 있습니다.

**참고 사항**  
- 동일한 엔드포인트에서 액션 섹션(`/encrypt`, `/decrypt`)을 변경함으로써 **암호화** 또는 **복호화**를 수행할 수 있습니다.  
- 디지털 서명을 사용하려면 API에서 접근 가능한 유효한 인증서 파일이 필요합니다.

- [Aspose.Cells Cloud API로 Excel 파일 암호화](/cells/excel-file-encrypt/)
- [Aspose.Cells Cloud API로 Excel 파일 보호](/cells/protect-excel-file/)
- [Excel 파일에 디지털 서명 추가](/cells/excel-digital-signature/)
- [Excel 파일 보호 – 상세 가이드](/cells/protect-excel-files/)
- [Excel 파일 비밀번호 설정](/cells/workbook/password/modify/)
- [Excel 파일 복호화](/cells/excel-file-decrypt/)
- [Excel 파일 보호 해제](/cells/excel-file-unprotect/)
- [Excel 파일 잠금 해제](/cells/unlock-excel-files/)
- [Excel 파일 비밀번호 초기화](/cells/clear-excel-files-password/)
---