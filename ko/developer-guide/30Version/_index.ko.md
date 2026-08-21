---
title: "Aspose.Cells Cloud 3.0 개발자 가이드"
ArticleTitle: "Aspose.Cells Cloud 3.0 REST API 개발자 가이드 – 엑셀 워크북 생성, 변환 및 서식 지정"
second_title: "문서"
type: docs
url: /developer-guide-3.0/
aliases: [/developer-guide/v3.0/,/developer-guide-v3.0/]
keywords: "Aspose.Cells Cloud, 엑셀 REST API, 워크북 변환, 차트 API, 데이터 가져오기, 내보내기, PDF, CSV, JSON, 개발자 가이드"
description: "Aspose.Cells Cloud 3.0 REST API를 사용하여 엑셀 워크북 생성, 변환, 서식 지정, 차트, 테이블 등을 다루는 방법을 알아보세요. 코드 예제와 모범 사례 팁이 포함되어 있습니다."
weight: 150
---

## Aspose.Cells Cloud REST API 사용하기

**Aspose.Cells Cloud 3.0 개발자 가이드**는 엑셀 워크북 및 워크시트와 관련하여 가장 자주 사용되는 REST API 작업에 대한 간결하고 검색 가능한 개요를 제공합니다. 이 가이드는 프로그래밍 방식으로 엑셀 파일을 생성, 수정, 변환 및 조작해야 하는 개발자를 대상으로 합니다. 아래 섹션을 사용하여 필요한 작업을 찾아보세요. 각 링크는 요청 구문, 매개변수 및 예제가 포함된 자세한 페이지로 연결됩니다. 이 허브 페이지는 **Aspose.Cells Cloud REST API** 참조를 한 곳에 모아 워크북 관련 엔드포인트, 차트 처리, 데이터 가져오기 및 내보내기 기능을 쉽게 찾을 수 있도록 도와줍니다.

**사전 요구 사항:** API를 사용하기 전에 유효한 Aspose Cloud 계정, API 키 및 비밀 키, 개발 환경에 맞는 적절한 SDK가 설치되어 있는지 확인하세요.

### 목차
- [파일 작업](#file-operations)
- [홈 (셀 서식 및 행/열 관리)](#home-cell-formatting--rowcolumn-management)
- [삽입 (차트, 테이블 및 OLE 개체)](#insert-charts-tables--ole-objects)
- [페이지 레이아웃 (페이지 나누기 및 설정)](#page-layout-page-breaks--setup)
- [수식 (계산 및 이름 관리)](#formulas-calculate--names)
- [데이터 (개요, 필터 및 가져오기)](#data-outline-filter--import)
- [검토 (주석 및 보호)](#review-comments--protection)
- [보기 (창 및 확대/축소 제어)](#view-window--zoom-controls)

### 빠른 API 요약

| API 그룹 | 샘플 엔드포인트 | 주요 동작 |
|-----------|----------------|----------------|
| **워크북 생성** | `POST /cells/workbook` | 빈 엑셀 워크북 생성 |
| **워크북 변환** | `PUT /cells/workbook/convert` | 엑셀 파일을 PDF, CSV, JSON 등으로 변환 |
| **차트 추가** | `POST /cells/worksheets/{sheetName}/charts` | 워크시트에 새 차트 삽입 |
| **테이블 관리** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | 목록 개체(테이블) 업데이트 또는 삭제 |
| **데이터 가져오기** | `POST /cells/worksheets/{sheetName}/import` | CSV, JSON, 이미지 또는 배열을 워크시트로 가져오기 |
| **수식 계산** | `POST /cells/workbook/calculate` | 워크북의 모든 수식 재계산 |
| **필터 적용** | `POST /cells/worksheets/{sheetName}/filters` | 자동 필터 기준 추가 또는 제거 |
| **워크북 보호** | `POST /cells/workbook/protect` | 워크북에 암호 보호 적용 |

이러한 고빈도 작업은 **Aspose.Cells Cloud 엑셀 REST API**의 핵심 기능을 다루며, 자세한 문서 페이지로 직접 연결됩니다.

빠른 API 요약 테이블의 PDF 버전을 다운로드하여 오프라인 참조용으로 사용할 수 있습니다.

{{< tabs tabTotal="8" tabID="1" tabName1="파일" tabName2="홈" tabName3="삽입" tabName4="페이지 레이아웃" tabName5="수식" tabName6="데이터" tabName7="검토" tabName8="보기" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>워크북: 새로 만들기, 변환, 다른 이름으로 저장</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="API를 통해 빈 엑셀 워크북 생성" rel="noopener">빈 엑셀 워크북 생성.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="템플릿 파일에서 워크북 생성" rel="noopener">템플릿 파일에서 엑셀 워크북 생성.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="SmartMarker 템플릿에서 워크북 생성" rel="noopener">SmartMarker 템플릿에서 엑셀 워크북 생성.</a></li>
            <li><a href="/cells/convert/" title="워크북을 다른 형식으로 변환" rel="noopener">엑셀 워크북을 다양한 파일 형식으로 변환.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="워크북을 다른 형식으로 저장" rel="noopener">엑셀 워크북을 다양한 파일 형식으로 저장.</a></li>
        </ul>
        <p>검색 및 바꾸기</p>
        <ul>
            <li><a href="/cells/search/" title="엑셀 파일에서 텍스트 검색" rel="noopener">엑셀 파일에서 텍스트 검색.</a></li>
            <li><a href="/cells/replace/" title="엑셀 파일에서 값 바꾸기" rel="noopener">엑셀 파일에서 기존 값을 새 값으로 바꾸기.</a></li>
        </ul>
        <p>압축</p>
        <ul>
            <li><a href="/cells/compress/" title="엑셀 파일 압축" rel="noopener">엑셀 파일 압축.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>워크북: 병합, 분할</p>
        <ul>
            <li><a href="/cells/merge/" title="여러 엑셀 워크북 병합" rel="noopener">엑셀 워크북 병합.</a></li>
            <li><a href="/cells/split/" title="워크북을 개별 파일로 분할" rel="noopener">엑셀 워크북 분할.</a></li>
        </ul>
        <p>워터마크</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="워크북에 배경 이미지 추가" rel="noopener">워크북에 배경 추가.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="워크북 배경 이미지 삭제" rel="noopener">워크북에서 배경 삭제.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="워크시트에 배경 또는 워터마크 설정" rel="noopener">엑셀 워크시트에 배경 또는 워터마크 설정.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="워크시트 배경 또는 워터마크 삭제" rel="noopener">엑셀 워크시트에서 배경 또는 워터마크 삭제.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>셀 글꼴, 스타일, 조건부 서식 및 값</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="워크시트에서 셀 스타일 가져오기" rel="noopener">엑셀 워크시트에서 셀 스타일 가져오기.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="여러 셀 스타일 업데이트" rel="noopener">엑셀 워크시트에서 여러 셀 스타일 업데이트.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="단일 셀 스타일 변경" rel="noopener">엑셀 워크시트에서 셀 스타일 업데이트.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title=" Rich Text 서식을 셀에 적용" rel="noopener">엑셀 워크시트에서 셀에 리치 텍스트 서식 설정.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="셀 내용 및 스타일 지우기" rel="noopener">엑셀 워크시트에서 셀 내용 및 스타일 지우기.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="조건부 서식 규칙 관리" rel="noopener">엑셀 워크시트에서 조건부 서식 추가, 삭제 및 업데이트.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="셀 값 설정" rel="noopener">엑셀 워크시트에서 셀 값 설정.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>행/열: 삽입, 삭제, 복사, 숨기기 및 자동 맞춤</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="워크시트에 빈 행 삽입" rel="noopener">엑셀 워크시트에 빈 행 추가.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="워크시트에서 행 삭제" rel="noopener">엑셀 워크시트에서 행 삭제.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="워크시트 내 행 복사" rel="noopener">엑셀 워크시트에서 행 복사.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="워크시트에서 행 숨기기" rel="noopener">엑셀 워크시트에서 행 숨기기.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="워크북에서 행 자동 맞춤" rel="noopener">엑셀 워크북에서 행 자동 맞춤.</a></li>
            <li><a href="/cells/columns/add/" title="워크시트에 빈 열 삽입" rel="noopener">엑셀 워크시트에 빈 열 추가.</a></li>
            <li><a href="/cells/columns/delete/" title="워크시트에서 열 삭제" rel="noopener">엑셀 워크시트에서 열 삭제.</a></li>
            <li><a href="/cells/columns/copy/" title="워크시트 내 열 복사" rel="noopener">엑셀 워크시트에서 열 복사.</a></li>
            <li><a href="/cells/columns/hide/" title="워크시트에서 열 숨기기" rel="noopener">엑셀 워크시트에서 열 숨기기.</a></li>
            <li><a href="/cells/columns/autofit/" title="워크북에서 열 자동 맞춤" rel="noopener">엑셀 워크북에서 열 자동 맞춤.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>차트</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="워크시트에 차트 추가" rel="noopener">엑셀 워크시트에 차트 추가.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="워크시트에서 차트 삭제" rel="noopener">엑셀 워크시트에서 차트 삭제.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="워크시트에서 모든 차트 삭제" rel="noopener">엑셀 워크시트에서 모든 차트 삭제.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="차트를 이미지 파일로 변환" rel="noopener">차트를 이미지로 변환.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="차트 범례 숨기기" rel="noopener">엑셀 워크시트에서 차트 범례 숨기기.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="차트 제목 업데이트" rel="noopener">엑셀 워크시트에서 차트 제목 업데이트.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="차트 제목 삭제" rel="noopener">워크시트에서 차트 제목 삭제.</a></li>
        </ul>
        <p>테이블</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="워크시트에 테이블(목록 개체) 추가" rel="noopener">엑셀 워크시트에 목록 개체 추가.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="워크시트의 테이블 업데이트" rel="noopener">엑셀 워크시트에서 목록 개체 업데이트.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="테이블을 범위로 변환" rel="noopener">목록 개체를 범위로 변환.</a></li>
            <li><a href="/cells/sort-table-data/" title="테이블 내 데이터 정렬" rel="noopener">테이블 데이터 정렬.</a></li>
        </ul>
        <p>OleObject</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="워크시트에 OLE 개체 추가" rel="noopener">엑셀 워크시트에 OLE 개체 추가.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="특정 OLE 개체 업데이트" rel="noopener">엑셀 워크시트에서 특정 OLE 개체 업데이트.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="OLE 개체를 이미지로 변환" rel="noopener">OLE 개체를 이미지로 변환.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="워크시트에서 모든 OLE 개체 삭제" rel="noopener">엑셀 워크시트에서 모든 OLE 개체 삭제.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="특정 OLE 개체 삭제" rel="noopener">엑셀 워크시트에서 특정 OLE 개체 삭제.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>도형</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="워크시트에 도형 추가" rel="noopener">엑셀 워크시트에 도형 추가.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="워크시트에서 모든 도형 삭제" rel="noopener">엑셀 워크시트에서 모든 도형 삭제.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="색인으로 도형 삭제" rel="noopener">엑셀 워크시트에서 색인으로 도형 삭제.</a></li>
        </ul>
        <p>피벗 테이블</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="워크시트에 피벗 테이블 추가" rel="noopener">엑셀 워크시트에 피벗 테이블 추가.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="워크시트에서 모든 피벗 테이블 삭제" rel="noopener">엑셀 워크시트에서 모든 피벗 테이블 삭제.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="색인으로 피벗 테이블 삭제" rel="noopener">엑셀 워크시트에서 색인으로 피벗 테이블 삭제.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="피벗 테이블의 셀 스타일 업데이트" rel="noopener">엑셀 워크시트에서 피벗 테이블의 셀 스타일 업데이트.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="피벗 테이블 전체 스타일 업데이트" rel="noopener">엑셀 워크시트에서 피벗 테이블 스타일 업데이트.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="피벗 테이블 필터 사용" rel="noopener">엑셀 워크시트에서 피벗 필터 사용.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="피벗 필드 항목 숨기기" rel="noopener">엑셀 워크시트에서 피벗 필드 항목 숨기기.</a></li>
            <li><a href="/cells/move-pivot-table/" title="워크시트 내 피벗 테이블 이동" rel="noopener">엑셀 워크시트에서 피벗 테이블 이동.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>페이지 나누기</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="가로 페이지 나누기 삽입" rel="noopener">엑셀 워크시트에 가로 페이지 나누기 삽입.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="세로 페이지 나누기 삽입" rel="noopener">엑셀 워크시트에 세로 페이지 나누기 삽입.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="가로 페이지 나누기 삭제" rel="noopener">엑셀 워크시트에서 가로 페이지 나누기 삭제.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="세로 페이지 나누기 삭제" rel="noopener">엑셀 워크시트에서 세로 페이지 나누기 삭제.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>페이지 설정</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>계산</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="워크북의 모든 수식 계산" rel="noopener">엑셀 워크북에서 모든 수식 계산.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="특정 셀의 수식 계산" rel="noopener">엑셀 워크북에서 셀 수식 계산.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="워크시트의 수식 계산" rel="noopener">엑셀 워크시트에서 수식 계산.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>이름</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>개요</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="워크시트에서 행 그룹화" rel="noopener">엑셀 워크시트에서 행 그룹화.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="워크시트에서 행 그룹 해제" rel="noopener">엑셀 워크시트에서 행 그룹 해제.</a></li>
        </ul>
        <p>필터</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="열에 필터 추가" rel="noopener">엑셀 워크시트에서 열에 필터 추가.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="열 필터 삭제" rel="noopener">엑셀 워크시트에서 열 필터 삭제.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="날짜 필터 제거" rel="noopener">엑셀 워크시트에서 날짜 필터 제거.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="아이콘 필터 추가" rel="noopener">엑셀 워크시트에 아이콘 필터 추가.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="날짜 필터 추가" rel="noopener">엑셀 워크시트에 날짜 필터 추가.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="자동 필터로 데이터 필터링" rel="noopener">엑셀 워크시트에서 자동 필터로 데이터 필터링.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="상위 10개 항목 필터링" rel="noopener">엑셀 워크시트에서 목록의 상위 10개 항목 필터링.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="모든 빈 셀 일치" rel="noopener">엑셀 워크시트에서 목록의 모든 빈 셀 일치.</a></li>
        </ul>
        <p>정렬</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="워크시트 데이터 정렬" rel="noopener">엑셀 워크시트에서 데이터 정렬.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>데이터 가져오기</p>
        <ul>
            <li><a href="/cells/import/" title="엑셀 파일에 데이터 가져오기" rel="noopener">엑셀 파일에 데이터 가져오기.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="워크시트에 CSV 데이터 가져오기" rel="noopener">엑셀 워크시트에 CSV 데이터 가져오기.</a></li>
            <li><a href="/cells/import/picture/" title="워크시트에 그림 가져오기" rel="noopener">엑셀 워크시트에 그림 가져오기.</a></li>
            <li><a href="/cells/import/double-array/" title="워크시트에 double 배열 가져오기" rel="noopener">엑셀 워크시트에 double 배열 가져오기.</a></li>
            <li><a href="/cells/import/integer-array/" title="워크시트에 정수 배열 가져오기" rel="noopener">엑셀 워크시트에 정수 배열 가져오기.</a></li>
            <li><a href="/cells/import/string-array/" title="워크시트에 문자열 배열 가져오기" rel="noopener">엑셀 워크시트에 문자열 배열 가져오기.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="스토리지 사용하여 데이터 가져오기" rel="noopener">스토리지를 사용하여 엑셀 워크시트에 데이터 가져오기.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="스토리지 미사용하여 데이터 가져오기" rel="noopener">스토리지를 사용하지 않고 엑셀 워크시트에 데이터 가져오기.</a></li>
        </ul>
        <p>어셈블리</p>
        <ul>
            <li><a href="/cells/assembly/" title="엑셀 파일에 데이터 어셈블리" rel="noopener">엑셀 파일에 데이터 어셈블리.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>주석</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="셀에 주석 추가" rel="noopener">엑셀 워크시트에서 셀에 주석 추가.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="셀 주석 업데이트" rel="noopener">엑셀 워크시트에서 주석 업데이트.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="워크시트의 모든 주석 삭제" rel="noopener">엑셀 워크시트에서 모든 주석 삭제.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>변경 사항</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="엑셀 워크북 보호" rel="noopener">엑셀 워크북 보호.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="엑셀 워크북 보호 해제" rel="noopener">엑셀 워크북 보호 해제.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>창</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="워크시트에서 창 고정" rel="noopener">엑셀 워크시트에서 창 고정.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="워크시트에서 창 고정 해제" rel="noopener">엑셀 워크시트에서 창 고정 해제.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="워크시트 숨기기" rel="noopener">엑셀 워크시트 숨기기.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="워크시트 숨기기 해제" rel="noopener">엑셀 워크시트 숨기기 해제.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>확대/축소</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="워크시트 확대/축소 수준 설정" rel="noopener">엑셀 워크시트에서 확대/축소 설정.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}