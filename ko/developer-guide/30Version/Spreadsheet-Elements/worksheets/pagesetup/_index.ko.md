---
title: "워크시트 페이지 설정"
second_title: "문서"
linktitle: "페이지 설정"
type: docs
url: /ko/page-setup/
keywords: "Aspose.Cells, pageSetup, 워크시트, 인쇄 설정, 여백, 방향, 용지 크기, 머리글, 꼬리글, 배율"
description: "Aspose.Cells Cloud의 PageSetup 객체를 사용하여 Excel 워크시트 인쇄 레이아웃을 구성하는 방법을 알아보세요. 속성 목록, 기본값, 범위 및 C#, Java, Python용 코드 예제를 포함합니다."
weight: 20
ArticleTitle: "워크시트 페이지 설정 – Aspose.Cells Cloud로 인쇄 레이아웃 구성하기"
---

# **PageSetup**

Excel 인쇄 페이지 설정

## 개요

**PageSetup** 객체는 여백, 방향, 배율, 머리글, 꼬리글 및 기타 인쇄 관련 설정을 포함한 Excel 워크시트의 인쇄 레이아웃 옵션을 정의합니다. 이러한 속성을 구성하면 개발자가 원하는 외관과 페이지 분할을 갖는 인쇄 가능한 워크북을 생성할 수 있습니다.

아래는 Aspose.Cells Cloud SDK를 사용하여 일반적인 페이지 설정 속성을 설정하는 간단한 C# 예제입니다:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API 클라이언트 초기화 (자신의 자격 증명으로 대체하세요)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// PageSetup 설정 정의
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// 워크북의 첫 번째 워크시트에 설정 적용
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

이 코드 스니펫은 워크시트를 가로 방향으로 설정하고 A4 용지를 사용하며, 콘텐츠를 수직 및 수평 중앙 정렬하고 100% 배율을 적용합니다.

## 속성

| 속성 이름               | 속성 유형 | Null 허용 | 읽기 전용 | 기본값         | 설명                                                                 |
| ----------------------- | --------- | --------- | -------- | -------------- | -------------------------------------------------------------------- |
| BlackAndWhite           | bool      | false     | false    | false          | 워크시트를 흑백 모드로 인쇄합니다.                                   |
| BottomMargin            | float     | true      | false    | 2.54 cm        | 하단 여백의 크기(센미터 단위).                                        |
| CenterHorizontally      | bool      | false     | false    | false          | 인쇄 시 시트를 수평 방향으로 중앙 정렬합니다.                         |
| CenterVertically        | bool      | false     | false    | false          | 인쇄 시 시트를 수직 방향으로 중앙 정렬합니다.                         |
| FirstPageNumber         | int       | true      | false    | 1              | 시트 인쇄 시 사용되는 첫 번째 페이지 번호입니다.                    |
| FitToPagesTall          | int       | false     | false    | 1              | 워크시트가 배율 조정될 때 세로로 몇 페이지로 맞출지 설정합니다.     |
| FitToPagesWide          | int       | false     | false    | 1              | 워크시트가 배율 조정될 때 가로로 몇 페이지로 맞출지 설정합니다.     |
| FooterMargin            | float     | true      | false    | 2.54 cm        | 페이지 하단에서 꼬리글까지의 거리(센미터 단위).                     |
| HeaderMargin            | float     | true      | false    | 2.54 cm        | 페이지 상단에서 머리글까지의 거리(센미터 단위).                     |
| IsAutoFirstPageNumber   | bool      | false     | false    | false          | 자동으로 첫 번째 페이지 번호를 할당합니다.                          |
| IsHFAlignMargins        | bool      | false     | false    | true           | true일 경우 머리글/꼬리글 여백이 페이지 여백과 정렬됩니다.          |
| IsHFDiffFirst           | bool      | false     | false    | false          | 첫 번째 페이지의 머리글/꼬리글이 다른 페이지와 다름을 나타냅니다.   |
| IsHFDiffOddEven         | bool      | false     | false    | false          | 홀수 페이지와 짝수 페이지의 머리글/꼬리글이 다름을 나타냅니다.      |
| IsHFScaleWithDoc        | bool      | false     | false    | false          | 문서와 함께 머리글 및 꼬리글을 배율 조정합니다(Excel 2007 이상).    |
| IsPercentScale          | bool      | false     | false    | true           | false일 경우 `FitToPagesWide` 및 `FitToPagesTall`이 배율을 제어합니다. |
| LeftMargin              | float     | true      | false    | 2.54 cm        | 왼쪽 여백의 크기(센미터 단위).                                       |
| Order                   | string    | true      | false    | "DownThenOver" | 큰 워크시트를 인쇄할 때 Excel이 페이지 번호를 매기는 순서입니다.    |
| Orientation             | string    | false     | false    | "Portrait"     | 페이지 방향: **Landscape**(가로) 또는 **Portrait**(세로).          |
| PaperSize               | string    | true      | false    | "A4"           | 인쇄에 사용되는 용지 크기입니다.                                    |
| PrintArea               | string    | true      | false    | (없음)         | 인쇄할 셀 범위(예: `"A1:D20"`).                                      |
| PrintComments           | string    | true      | false    | "NoComments"   | 시트와 함께 주석을 인쇄하는 방식입니다.                             |
| PrintCopies             | int       | true      | false    | 1              | 인쇄할 부수입니다.                                                  |
| PrintDraft              | bool      | false     | false    | false          | 초안 모드로 워크시트를 인쇄합니다(그래픽 없음).                     |
| PrintErrors             | string    | true      | false    | "Display"      | 표시되는 인쇄 오류 유형입니다.                                      |
| PrintGridlines          | bool      | false     | false    | false          | 셀 격자선을 인쇄합니다.                                             |
| PrintHeadings           | bool      | false     | false    | false          | 행 및 열 제목을 인쇄합니다.                                         |
| PrintQuality            | int       | true      | false    | 600            | 인쇄 품질 설정(초당 도트 수, DPI).                                  |
| PrintTitleColumns       | string    | true      | false    | (없음)         | 인쇄된 각 페이지 왼쪽에 반복할 열입니다.                            |
| PrintTitleRows          | string    | true      | false    | (없음)         | 인쇄된 각 페이지 상단에 반복할 행입니다.                            |
| RightMargin             | float     | true      | false    | 2.54 cm        | 오른쪽 여백의 크기(센미터 단위).                                     |
| TopMargin               | float     | true      | false    | 2.54 cm        | 상단 여백의 크기(센미터 단위).                                       |
| Zoom                    | int       | false     | false    | 100            | 퍼센트 단위의 배율 인자(10 – 400%).                                 |
| Header                  | object    | true      | false    | (없음)         | 페이지 머리글 설정입니다.                                           |
| Footer                  | object    | true      | false    | (없음)         | 페이지 꼬리글 설정입니다.                                           |

## 관련 객체

- **Header** – 워크시트 머리글을 설정합니다.  
- **Footer** – 워크시트 꼬리글을 설정합니다.  
- **PrintOptions** – 페이지 나누기 및 인쇄 범위 등 추가 인쇄 관련 설정입니다.  
---