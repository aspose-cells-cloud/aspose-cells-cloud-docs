---
title: "Excel 메타데이터 및 속성 다루기"
second_title: "문서"
linktype: "메타데이터 및 속성"
type: docs
url: /metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, Excel 메타데이터, 문서 속성 API, REST API, 메타데이터 조회, Excel 속성 업데이트, Excel 메타데이터 삭제"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일 메타데이터를 읽고, 추가하고, 업데이트하고, 삭제하는 방법을 알아보세요. Java, .NET, Python, Node.js 등 다양한 SDK 및 cURL 사용 예제가 포함되어 있습니다."
ArticleTitle: "Excel 메타데이터 및 문서 속성 다루기 – Aspose.Cells Cloud"
weight: 100
---

Excel 파일은 문서를 식별하고, 정리하며, 관리하는 데 도움이 되는 다양한 메타데이터를 저장할 수 있습니다. Aspose.Cells Cloud는 이러한 메타데이터를 읽고, 추가하고, 업데이트하고, 삭제할 수 있는 간단한 REST API를 제공하여 개발자가 문서 속성 관리를 애플리케이션에 통합할 수 있도록 지원합니다. 이 가이드에서는 표준 속성과 사용자 정의 속성이라는 두 가지 주요 속성 유형을 설명하고, 이를 다루는 방법을 안내하며, 관련 API 엔드포인트로 바로 연결하는 링크를 제공합니다. 또한 구현을 빠르게 진행할 수 있도록 요청 세부 정보를 담은 간결한 API 참조 표도 포함되어 있습니다.

**최종 업데이트:** 2026년 7월 8일  

**문서 속성 유형**

Aspose.Cells Cloud API를 사용하여 Excel 문서(메타데이터)의 문서 속성을 보고, 수정하고, 제거하는 방법을 배우기 전에, Excel 문서가 가질 수 있는 속성 종류를 명확히 알아보겠습니다.

- **표준 속성**은 Excel에서 공통적으로 사용되는 속성입니다. 제목, 주제, 작성자, 카테고리 등 기본 정보를 포함합니다. 이러한 속성에 사용자 정의 텍스트 값을 할당하여 파일을 더 쉽게 찾을 수 있도록 할 수 있습니다.

- **사용자 정의 속성**은 사용자가 정의한 속성입니다. Excel 문서에 추가 메타데이터를 삽입할 수 있습니다.

**Excel 파일의 문서 속성 다루기**

- [스토리지를 사용하여 특정 문서 속성 조회하기](/cells/document-properties/get/)
- [스토리지를 사용하지 않고 문서 속성 조회하기](/cells/metadata/get/)
- [스토리지를 사용하여 모든 문서 속성 조회하기](/cells/document-properties/get-all/)
- [스토리지를 사용하여 특정 문서 속성 업데이트하기](/cells/document-properties/update/)
- [스토리지를 사용하지 않고 특정 문서 속성 업데이트하기](/cells/metadata/update/)
- [스토리지를 사용하여 특정 문서 속성 삭제하기](/cells/document-properties/delete/)
- [스토리지를 사용하지 않고 문서 속성 삭제하기](/cells/metadata/delete/)
- [스토리지를 사용하여 모든 문서 속성 삭제하기](/cells/document-properties/clear/)

**API 참조(스토리지 미사용)**  

| 메서드 | 엔드포인트 | 설명 |
|--------|------------|------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | 클라우드에 저장된 워크북의 모든 문서 속성을 조회합니다. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | `propertyName`으로 식별되는 특정 속성(표준 또는 사용자 정의)의 값을 조회합니다. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | 기존 속성의 값을 업데이트합니다. 요청 본문에는 JSON 형식의 새 값이 포함됩니다. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | 워크북에서 특정 속성을 삭제합니다. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | 워크북에서 모든 사용자 정의 및 표준 속성을 삭제합니다. |

*모든 요청에는 OAuth 2.0 액세스 토큰이 필요하며, 특정 스토리지 위치를 사용할 경우 `storage` 및 `folder`와 같은 선택적 쿼리 매개변수를 포함할 수 있습니다.*
---