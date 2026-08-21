---
title: "워크시트 배경 이미지 추가 또는 삭제 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "배경"
type: docs
url: /ko/worksheets/background/
keywords: "Aspose.Cells Cloud, 워크시트 배경, Excel API, 배경 이미지 추가, 워크시트 배경 삭제, SDK 예제"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 배경 이미지를 추가하거나 제거하는 방법을 알아보세요. 요청 구문, Java, .NET, Python, PHP용 SDK 예제 및 오류 처리를 포함합니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API로 워크시트 배경 이미지 추가 또는 삭제"
---

## Excel 워크시트의 배경 작업

**개요:** 워크시트 배경은 워크시트 셀 뒤에 나타나는 이미지로, 브랜딩이나 시각적 힌트 제공에 유용합니다. Aspose.Cells Cloud API를 사용하면 이 배경 이미지를 프로그래밍 방식으로 추가하거나 삭제할 수 있습니다.

**사전 요구 사항:**  
- 유효한 Aspose.Cells Cloud 액세스 토큰(OAuth 2.0)  
- 클라우드에 저장된 Excel 워크북  
- 배경으로 사용할 이미지 파일(PNG, JPEG, BMP)

- **배경 추가** – 워크시트에 배경 이미지를 설정합니다. 자세한 가이드는 [Excel 워크시트에 배경 설정하는 방법](/ko/cells/worksheets/background/add/)을 참조하세요.  
- **배경 삭제** – 워크시트에서 기존 배경 이미지를 제거합니다. 자세한 가이드는 [Excel 워크시트에서 배경 삭제하는 방법](/ko/cells/worksheets/background/delete/)을 참조하세요.

워크시트 배경을 사용하면 브랜딩을 강화하거나 중요한 섹션을 강조 표시하며 최종 사용자에게 시각적 힌트를 제공할 수 있습니다. Aspose.Cells Cloud API는 애플리케이션에서 이 배경 이미지를 직접 설정하거나 삭제하기 쉽게 제공합니다.

### API 참조

| 작업 | HTTP 메서드 | 엔드포인트 | 경로 매개변수 | 요청 본문 | 성공 응답 |
|-----------|-------------|----------|----------------|--------------|------------------|
| 배경 추가 | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – 워크북 파일 이름<br>`sheetName` – 대상 워크시트 | 이미지 파일(PNG, JPEG, BMP)을 multipart/form‑data로 | `200 OK` – 배경 적용됨 |
| 배경 삭제 | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – 워크북 파일 이름<br>`sheetName` – 대상 워크시트 | *없음* | `200 OK` – 배경 제거됨 |

#### 예제 (Java SDK)

```java
// 배경 이미지 추가
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// 배경 이미지 삭제
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### 예제 (Python SDK)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# 배경 추가
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# 배경 삭제
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

추가 언어(C#, PHP, Ruby)에 대한 예제는 SDK 문서를 참조하세요.

**관련 주제**  
- 일반적으로 워크시트를 관리하는 방법에 대해 자세히 알아보세요: [워크시트 개요](/ko/cells/worksheets/).  
- Aspose.Cells Cloud 인증 방법을 이해하세요: [API 인증 가이드](/ko/cells/authentication/).  
- 차트, 표, 수식 등 기타 스프레드시트 요소를 탐색하세요: [스프레드시트 요소 색인](/ko/cells/elements/).
---