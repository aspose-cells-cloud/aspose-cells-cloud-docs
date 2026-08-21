---
title: "Excel 데이터 유효성 검사 사용하기"
second_title: "문서"
linktitle: "유효성 검사"
type: docs
url: /ko/validations/ko/
keywords: "Excel 데이터 유효성 검사, Aspose.Cells Cloud, REST API, 스프레드시트, Office Cloud"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 데이터 유효성 검사 규칙을 프로그래밍 방식으로 추가, 조회, 업데이트, 삭제 및 지우는 방법을 배워보세요. .NET, Java, Python, PHP 예제를 포함합니다."
weight: 100
ArticleTitle: "Excel 데이터 유효성 검사 사용하기 - Aspose.Cells Cloud API 문서"
---

Excel 데이터 유효성 검사는 Microsoft Excel에서 워크시트의 셀에 사용자가 입력할 수 있는 내용을 제어하는 데 사용되는 기능입니다. 특정 날짜 범위, 정수만 입력하도록 제한하거나, 공간을 절약하고 단일 셀에 값을 드롭다운 목록으로 표시할 수도 있습니다. 또한 사용자가 잘못된 값이나 잘못된 형식을 입력할 때 나타나는 사용자 정의 메시지를 정의할 수도 있습니다.

예를 들어, 사용자는 오전 9시부터 오후 6시까지로 예정된 회의를 지정할 수 있습니다.

데이터 유효성 검사는 값이 양수인지, 월의 15일에서 30일 사이의 날짜인지, 앞으로 30일 이내에 발생하는 날짜인지, 25자 미만의 텍스트를 입력하는지 등을 확인하는 데 사용할 수 있습니다.

### API 개요

| 작업 | HTTP 메서드 | 엔드포인트 | 설명 |
|------|-------------|-----------|------|
| 추가 | POST | `/cells/{file}/worksheets/{sheet}/validations` | 유효성 검사 규칙 생성 |
| 조회 | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 특정 규칙 조회 |
| 전체 조회 | GET | `/cells/{file}/worksheets/{sheet}/validations` | 모든 규칙 목록 조회 |
| 업데이트 | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 규칙 수정 |
| 삭제 | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | 규칙 제거 |
| 모두 지우기 | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | 모든 규칙 제거 |

## Excel 파일에서 유효성 검사 사용하기

- [Excel 워크시트에 유효성 검사 규칙 추가하는 방법](/cells/validations/add/)
- [Excel 워크시트에서 유효성 검사 규칙 조회하는 방법](/cells/validations/get/)
- [Excel 워크시트에서 모든 유효성 검사 규칙 조회하는 방법](/cells/validations/get-all/)
- [Excel 워크시트에서 유효성 검사 규칙 삭제하는 방법](/cells/validations/delete/)
- [Excel 워크시트에서 모든 유효성 검사 규칙을 지우는 방법](/cells/validations/clear/)
- [Excel 워크시트의 유효성 검사 규칙 업데이트하는 방법](/cells/validations/update/)
---