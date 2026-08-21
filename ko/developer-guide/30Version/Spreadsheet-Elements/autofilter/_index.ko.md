---
title: "Excel AutoFilter 사용하기"
second_title: "문서"
linktitle: "AutoFilter"
type: docs
url: /autofilter/
aliases: [/working-with-autofilter/]
keywords: "AutoFilter, Aspose.Cells Cloud, Excel 필터, 색상 필터, 날짜 필터, 동적 필터, 숫자 필터, 텍스트 필터, 빈 셀 필터, 사용자 정의 필터"
description: "Aspose.Cells Cloud API를 사용하여 Excel AutoFilter(색상, 날짜, 동적, 숫자, 텍스트, 빈 셀)를 추가, 편집 및 삭제하는 방법을 알아보세요. 여러 언어로 제공되는 코드 예제."
weight: 100
ArticleTitle: "Excel AutoFilter 사용하기 – Aspose.Cells Cloud 문서"
---

AutoFilter는 워크시트에서 필요한 항목만 빠르게 표시할 수 있는 가장 빠른 방법입니다. AutoFilter 기능을 사용하면 텍스트, 숫자 또는 날짜를 기준으로 지정된 조건에 따라 목록을 필터링할 수 있습니다.

**다양한 필터 유형**

Aspose.Cells Cloud는 색상 필터, 날짜 필터, 숫자 필터, 텍스트 필터, 빈 셀 필터, 비어 있지 않은 셀 필터 등 다양한 필터 유형을 적용할 수 있는 여러 API를 제공합니다.

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>채우기 색상</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud는 셀의 채우기 색상 속성에 따라 데이터를 필터링할 수 있도록 <a href="/cells/autofilter/add-color-filter/">채우기 색상 필터 추가 API</a>를 제공합니다.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>날짜</strong></td>
    <td class="col-md-10">
      <p>2018년 1월의 날짜를 가진 행을 필터링하는 등 다양한 날짜 필터를 적용할 수 있습니다. 날짜 필터를 추가하려면 <a href="/cells/autofilter/add-date-filter/">날짜 필터 추가 API</a>를 사용하세요.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>동적 날짜</strong></td>
    <td class="col-md-10">
      <p>동적 날짜 필터를 사용하면 연도와 관계없이 특정 월에 속한 셀을 필터링할 수 있습니다(예: 모든 1월 날짜). 자세한 내용은 <a href="/cells/autofilter/add-dynamic-filter/">동적 필터 API</a>를 참조하세요.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>숫자</strong></td>
    <td class="col-md-10">
      <p><a href="/cells/autofilter/add-filter/">사용자 정의 필터 API</a>를 사용하여 숫자 값이 주어진 범위 내에 있는 셀을 필터링할 수 있습니다.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>텍스트</strong></td>
    <td class="col-md-10">
      <p>열에 텍스트가 포함된 경우, <a href="/cells/autofilter/add-filter/">필터 추가 API</a>를 사용하여 특정 문자열을 포함하는 셀을 선택할 수 있습니다.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>빈 셀</strong></td>
    <td class="col-md-10">
      <p>열이 비어 있는 행을 검색하려면 <a href="/cells/autofilter/match-all-blank/">모든 빈 셀 일치 API</a>를 사용하세요.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>비어 있지 않은 셀</strong></td>
    <td class="col-md-10">
      <p>열에 빈 셀이 아닌 값이 포함된 행을 필터링하려면 <a href="/cells/autofilter/match-all-non-blank/">모든 비어 있지 않은 셀 일치 API</a>를 사용하세요.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>사용자 정의 필터</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud는 특정 하위 문자열을 포함하거나 특정 문자열로 시작/종료하는 행을 필터링하는 등 고급 시나리오를 위해 <a href="/cells/autofilter/add-custom-filter/">사용자 정의 필터 API</a>를 제공합니다.</p>
    </td>
  </tr>
</table>

**AutoFilter 작업**

- [Excel 워크시트에 색상 필터 추가하는 방법](/cells/autofilter/add-color-filter/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/add-color-filter/`
- [Excel 워크시트에 사용자 정의 필터 추가하는 방법](/cells/autofilter/add-custom-filter/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/add-custom-filter/`
- [Excel 워크시트에 날짜 필터 추가하는 방법](/cells/autofilter/add-date-filter/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/add-date-filter/`
- [Excel 워크시트에 동적 필터 추가하는 방법](/cells/autofilter/add-dynamic-filter/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/add-dynamic-filter/`
- [Excel 워크시트에 필터 추가하는 방법](/cells/autofilter/add-filter/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/add-filter/`
- [Excel 워크시트에 아이콘 필터 추가하는 방법](/cells/autofilter/add-icon-filter/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/add-icon-filter/`
- [Excel 워크시트에서 날짜 필터 삭제하는 방법](/cells/autofilter/delete-a-date-filter/) – **메서드:** DELETE, **엔드포인트:** `/cells/autofilter/delete-a-date-filter/`
- [Excel 워크시트에서 필터 삭제하는 방법](/cells/delete-filter/) – **메서드:** DELETE, **엔드포인트:** `/cells/delete-filter/`
- [Excel 워크시트에서 AutoFilter 설명 가져오기](/cells/autofilter/get/) – **메서드:** GET, **엔드포인트:** `/cells/autofilter/get/`
- [Excel 워크시트에서 모든 빈 셀 일치시키기](/cells/autofilter/match-all-blank/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/match-all-blank/`
- [Excel 워크시트에서 모든 비어 있지 않은 셀 일치시키기](/cells/autofilter/match-all-non-blank/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/match-all-non-blank/`
- [Excel 워크시트에서 AutoFilter 새로 고침](/cells/autofilter/refresh/) – **메서드:** POST, **엔드포인트:** `/cells/autofilter/refresh/`
---