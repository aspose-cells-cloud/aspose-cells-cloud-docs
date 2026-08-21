---
title: "Excel 범위 작업하기"
second_title: "문서"
linktype: "범위"
type: docs
url: /ko/ranges/
aliases: [  /ko/working-with-ranges/ ]
keywords: "Aspose.Cells, Excel 범위, REST API, SDK, .NET, Java, Python, 셀 병합, 범위 복사, 범위 값 설정"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 범위를 검색, 수정, 스타일 지정, 병합, 이동 및 복사하는 방법을 배워보세요. .NET, Java, Python 등에 대한 SDK 코드 예제가 포함되어 있습니다."
weight: 100
ArticleTitle: "Excel 범위 작업하기 – Aspose.Cells Cloud 문서"
---

**범위**(range)는 단일 셀, 전체 행, 전체 열, 연속된 셀 블록 또는 여러 워크시트에 걸친 3차원(3‑D) 범위를 나타냅니다.

## Excel 파일의 범위 작업하기

Aspose.Cells Cloud REST API는 각 범위 작업에 특화된 엔드포인트를 제공합니다. 다음 목록은 각 항목에 대한 상세 사용 예제 링크와 함께 빠른 참고를 위한 HTTP 메서드 및 엔드포인트를 제공합니다.

- [워크북 내부의 이름 있는 범위 가져오기](/cells/get-named-ranges-inside-the-workbook/) – 워크북에 정의된 모든 이름 있는 범위를 검색하여 해당 주소와 범위를 반환합니다. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [이름 있는 범위 기반 셀 데이터 가져오기](/cells/get-cells-data-based-on-named-range/) – 지정된 이름 있는 범위에 속한 셀의 값을 반환합니다. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [범위 내 행 높이 변경하기](/cells/cells/change-heights-of-rows-inside-the-range/) – 주어진 범위에 포함된 각 행의 높이를 조정합니다. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [범위 내 열 너비 변경하기](/cells/cells/change-widths-of-columns-inside-the-range/) – 범위와 교차하는 모든 열의 열 너비를 수정합니다. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [범위의 셀들을 하나의 셀로 병합하기](/cells/combines-a-range-of-cells-into-a-single-cell/) – 선택한 셀들을 하나의 셀로 병합하며, 좌상단 셀의 값을 보존합니다. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [워크시트 내 범위 복사 및 붙여넣기 옵션 사용하기](/cells/copy-range-in-a-worksheet-with-paste-options/) – 소스 범위를 대상 범위로 복사하며, 선택적 붙여넣기 유형(값, 서식, 수식 등)을 지정할 수 있습니다. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [범위 스타일 설정하기](/cells/set-the-style-of-the-range/) – 폰트, 채우기, 테두리, 정렬 스타일을 범위 내 모든 셀에 적용합니다. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [범위의 병합된 셀 해제하기](/cells/unmerge-merged-cells-of-the-range/) – 이전 병합 작업을 되돌려 원래 개별 셀들을 복원합니다. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Excel 워크시트와 함께 이름 있는 범위 이동하기](/cells/move-a-named-ranged-with-a-excel-worksheet/) – 이름 있는 범위를 동일 워크시트 내 다른 주소로 또는 다른 워크시트로 이동합니다. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Excel 워크시트에서 범위 값 설정하기](/cells/ranges/set-value/) – 지정된 범위에 단일 값 또는 값 배열을 기록합니다. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

모든 요청 및 응답은 JSON 형식으로 처리됩니다. 인증을 위해 `Authorization` 헤더에 액세스 토큰을 포함해야 합니다.