---
title: "Excel 워크시트에서 범위 콘텐츠 업데이트하는 방법"
second_title: "문서"
linktitle: "업데이트"
type: docs
url: /ranges/update/
keywords: "Excel, 범위 업데이트, Aspose.Cells Cloud, REST API, 스프레드시트, 범위 스타일, 범위 값, 행 높이, 열 너비"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 범위 콘텐츠를 업데이트합니다. 지원되는 SDK를 통해 스타일, 값, 행 높이, 열 너비를 수정합니다."
weight: 20
ArticleTitle: "Excel 워크시트에서 범위 콘텐츠 업데이트하는 방법 – Aspose.Cells Cloud 문서"
---

## Excel 워크시트에서 범위 콘텐츠 업데이트 작업

업데이트 작업을 사용하기 전에 유효한 Aspose.Cells Cloud API 토큰이 있고 대상 워크북이 클라우드 스토리지에 저장되어 있는지 확인하세요. 이 API는 Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift용 SDK를 통해 제공됩니다.

네 가지 주요 업데이트 작업에 대한 간략한 요약은 아래와 같습니다. 이 표는 개발자가 각 작업의 HTTP 메서드, 엔드포인트 패턴, 주요 매개변수, 일반적인 성공 응답을 빠르게 참조할 수 있도록 도와줍니다.

| 작업            | HTTP 메서드 | 엔드포인트 패턴                                                                                     | 주요 매개변수                | 200‑OK 응답               |
|-----------------|-------------|------------------------------------------------------------------------------------------------------|-------------------------------|------------------------------|
| 스타일 설정     | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | `style` 객체                | 업데이트된 범위 스타일          |
| 값 설정         | POST        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | `values` 배열                | 업데이트된 범위 값              |
| 행 높이 설정    | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | `height` 숫자               | 업데이트된 행 높이           |
| 열 너비 설정    | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | `width` 숫자                | 업데이트된 열 너비           |

이 페이지에서는 범위의 스타일 설정, 범위의 값 설정, 행 높이 조정, 열 너비 조정의 네 가지 주요 업데이트 작업에 대한 빠른 접근을 제공합니다.

- [Excel 워크시트에서 범위의 스타일을 설정하는 방법](/cells/ranges/update/style/)  
- [Excel 워크시트에서 범위의 값을 설정하는 방법](/cells/ranges/update/values/)  
- [Excel 워크시트에서 범위의 행 높이를 설정하는 방법](/cells/ranges/update/row-height/)  
- [Excel 워크시트에서 범위의 열 너비를 설정하는 방법](/cells/ranges/update/column-width/)  
---