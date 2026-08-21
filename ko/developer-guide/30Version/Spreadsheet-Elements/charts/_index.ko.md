---
title: "Excel 차트 작업하기"
second_title: "문서"
linktitle: "차트"
type: docs
url: /ko/charts/
aliases: [  /ko/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, chart, API, REST, Cloud, spreadsheet"
description: "Aspose.Cells Cloud API를 사용하여 Excel 차트를 관리하는 방법을 배워보세요. 차트 검색, 추가, 수정, 삭제 및 이미지 형식으로 변환을 위한 단계별 가이드, 코드 예제 및 오류 처리 방법을 제공합니다."
weight: 100
ArticleTitle: "Excel 차트 작업하기 – Aspose.Cells Cloud 문서"
---

## Excel 파일의 차트 작업하기

**최종 업데이트:** 2026년 7월  

Excel 차트는 데이터의 시각적 표현으로, 사용자가 추세와 패턴을 빠르게 파악할 수 있도록 도와줍니다.  
Aspose.Cells Cloud API를 사용하면 클라우드에 저장된 Excel 워크북 내부의 차트를 프로그래밍 방식으로 작업할 수 있습니다. API를 통해 기존 차트를 검색하거나 새 차트를 추가하고, 제목, 축, 범례 등의 속성을 수정하거나 불필요한 차트를 삭제할 수 있으며, 보고서 작성 또는 후속 처리를 위해 차트를 이미지 형식으로 변환할 수도 있습니다. 다음 링크를 클릭하면 각 지원되는 차트 관련 작업에 대한 자세한 작업 페이지로 바로 이동할 수 있습니다.

### 빠른 참고 자료

| 작업 | HTTP 메서드 | 엔드포인트(템플릿) | 문서 |
|------|-------------|-------------------|------|
| 차트 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [워크시트에서 차트 가져오기](/cells/get-chart-from-a-worksheet/) |
| 차트 추가 | POST | `/cells/{file}/worksheets/{sheet}/charts` | [워크시트에 차트 추가하기](/cells/add-a-chart-in-a-worksheet/) |
| 모든 차트 삭제 | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [워크시트에서 모든 차트 삭제하기](/cells/delete-all-charts-from-a-worksheet/) |
| 차트 삭제 | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [워크시트에서 차트 삭제하기](/cells/delete-a-chart-from-a-worksheet/) |
| 차트를 이미지로 변환 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [차트를 이미지로 변환하기](/cells/convert-chart-to-image/) |
| 차트 영역 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [워크시트에서 차트 영역 가져오기](/cells/get-chart-area-from-a-worksheet/) |
| 채우기 서식 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [워크시트에서 차트 영역의 채우기 서식 가져오기](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| 범례 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [워크시트에서 차트 범례 가져오기](/cells/get-chart-legend-from-a-worksheet/) |
| 범례 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [워크시트에서 차트 범례 업데이트하기](/cells/update-chart-legend-in-a-worksheet/) |
| 범례 표시 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [워크시트에서 차트 범례 표시하기](/cells/show-chart-legend-in-a-worksheet/) |
| 범례 숨기기 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [워크시트에서 차트 범례 숨기기](/cells/hide-chart-legend-in-a-worksheet/) |
| 제목 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [워크시트에서 차트 제목 가져오기](/cells/get-chart-title-from-a-worksheet/) |
| 제목 설정 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Excel 워크시트에서 차트 제목 설정하기](/cells/set-chart-title-in-excel-worksheet/) |
| 제목 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Excel 워크시트에서 차트 제목 업데이트하기](/cells/update-chart-title-in-excel-worksheet/) |
| 제목 삭제 | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [워크시트에서 차트 제목 삭제하기](/cells/delete-chart-title-in-a-worksheet/) |
| 차트 속성 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [차트 속성 업데이트하기](/cells/charts/properties/update/) |
| 범주 축 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [차트 범주 축 가져오기](/cells/charts/category-axis/get/) |
| 값 축 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [차트 값 축 가져오기](/cells/charts/value-axis/get/) |
| 2차 범주 축 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [차트 2차 범주 축 가져오기](/cells/charts/second-category-axis/get/) |
| 2차 값 축 가져오기 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [차트 2차 값 축 가져오기](/cells/charts/second-value-axis/get/) |
| 범주 축 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [차트 범주 축 업데이트하기](/cells/charts/category-axis/update/) |
| 값 축 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [차트 값 축 업데이트하기](/cells/charts/value-axis/update/) |
| 2차 범주 축 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [차트 2차 범주 축 업데이트하기](/cells/charts/second-category-axis/update/) |
| 2차 값 축 업데이트 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [차트 2차 값 축 업데이트하기](/cells/charts/second-value-axis/update/) |

- [워크시트에서 차트 가져오기](/cells/get-chart-from-a-worksheet/)
- [워크시트에 차트 추가하기](/cells/add-a-chart-in-a-worksheet/)
- [워크시트에서 모든 차트 삭제하기](/cells/delete-all-charts-from-a-worksheet/)
- [워크시트에서 차트 삭제하기](/cells/delete-a-chart-from-a-worksheet/)
- [차트를 이미지로 변환하기](/cells/convert-chart-to-image/)
- [워크시트에서 차트 영역 가져오기](/cells/get-chart-area-from-a-worksheet/)
- [워크시트에서 차트 영역의 채우기 서식 가져오기](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [워크시트에서 차트 범례 가져오기](/cells/get-chart-legend-from-a-worksheet/)
- [워크시트에서 차트 범례 업데이트하기](/cells/update-chart-legend-in-a-worksheet/)
- [워크시트에서 차트 범례 표시하기](/cells/show-chart-legend-in-a-worksheet/)
- [워크시트에서 차트 범례 숨기기](/cells/hide-chart-legend-in-a-worksheet/)
- [워크시트에서 차트 제목 가져오기](/cells/get-chart-title-from-a-worksheet/)
- [Excel 워크시트에서 차트 제목 설정하기](/cells/set-chart-title-in-excel-worksheet/)
- [Excel 워크시트에서 차트 제목 업데이트하기](/cells/update-chart-title-in-excel-worksheet/)
- [워크시트에서 차트 제목 삭제하기](/cells/delete-chart-title-in-a-worksheet/)
- [차트 속성 업데이트하기](/cells/charts/properties/update/)
- [차트 범주 축 가져오기](/cells/charts/category-axis/get/)
- [차트 값 축 가져오기](/cells/charts/value-axis/get/)
- [차트 2차 범주 축 가져오기](/cells/charts/second-category-axis/get/)
- [차트 2차 값 축 가져오기](/cells/charts/second-value-axis/get/)
- [차트 범주 축 업데이트하기](/cells/charts/category-axis/update/)
- [차트 값 축 업데이트하기](/cells/charts/value-axis/update/)
- [차트 2차 범주 축 업데이트하기](/cells/charts/second-category-axis/update/)
- [차트 2차 값 축 업데이트하기](/cells/charts/second-value-axis/update/)