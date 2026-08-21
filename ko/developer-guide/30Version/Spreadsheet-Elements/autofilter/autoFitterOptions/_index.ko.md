---
title: "AutoFitterOptions – 속성 및 사용 가이드 | Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "AutoFitterOptions"
type: docs
url: /ko/auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, 엑셀 자동 맞춤, 행 높이, 병합 셀, API"
description: "Aspose.Cells Cloud API에서 AutoFitterOptions 객체를 사용하여 행 높이 자동 맞춤, 병합 셀 처리, 숨김 행/열 처리, 언어 설정 및 렌더링 옵션을 제어하는 방법을 알아보세요."
weight: 79
ArticleTitle: "AutoFitterOptions – Aspose.Cells Cloud용 속성 및 사용 가이드"
---

# AutoFitterOptions 속성

`AutoFitterOptions` 객체를 사용하면 Aspose.Cells Cloud에서 수행되는 자동 행 높이 조정을 세밀하게 조정할 수 있습니다. 병합 셀 처리, 숨김 행/열 처리, 언어별 서식 지정 또는 렌더링 관련 동작에 정밀한 제어가 필요한 경우 유용합니다.

**사전 요구 사항** – 이러한 옵션을 사용하려면 **Cells.ReadWrite** 범위를 포함하는 유효한 OAuth 2.0 액세스 토큰으로 인증되어 있어야 합니다. 이 요청은 v3.0 API를 지원하는 모든 SDK 버전과 함께 작동합니다.

| 이름                       | 유형        | 설명                                                                                     | 참고                                                                                                       |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | 병합 셀의 자동 맞춤 방식을 결정합니다.                                                    | 허용되는 값: `All`, `First`, `None`. 기본값: `All`. 샘플 JSON: `"AutoFitMergedCellsType":"All"`       |
| **IgnoreHidden**           | **boolean** | **true**인 경우, 자동 맞춤 과정에서 숨김 행 및 열을 무시합니다.                 | 기본값: `false`. 샘플 JSON: `"IgnoreHidden":false`                                                       |
| **OnlyAuto**               | **boolean** | 수동으로 높이를 조정하지 않은 행만 자동 맞춤할지 여부를 나타냅니다.    | 기본값: `false`. 샘플 JSON: `"OnlyAuto":false`                                                           |
| **DefaultEditLanguage**    | **string**  | 워크북의 기본 편집 언어를 설정합니다.                                             | 기본값: 시스템 언어(예: `"en-US"`). 샘플 JSON: `"DefaultEditLanguage":"en-US"`                    |
| **MaxRowHeight**           | **double**  | 행을 자동 맞춤할 때 적용되는 최대 행 높이(포인트 단위). **0**은 제한 없음을 의미합니다. | 기본값: `0`. 샘플 JSON: `"MaxRowHeight":0`                                                               |
| **AutoFitWrappedTextType** | **string**  | 셀 내에서 줄 바꿈된 텍스트의 자동 맞춤 방식을 제어합니다.                                          | 허용되는 값: `All`, `OnlyWrapped`, `None`. 기본값: `All`. 샘플 JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | 자동 맞춤 작업 중 사용되는 서식 전략을 지정합니다.                           | 일반적인 값: `AutoFit`, `PreserveExisting`. 기본값: `AutoFit`. 샘플 JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | 렌더링 목적(예: PDF, 이미지)을 위해 자동 맞춤을 수행할지 여부를 나타냅니다.   | 허용되는 값: `True`, `False`. 기본값: `False`. 샘플 JSON: `"ForRendering":"False"`                    |

아래는 `AutoFitterOptions`를 구성할 때 API로 전송할 수 있는 일반적인 JSON 페이로드 예시입니다.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

이 옵션을 워크북에 적용하는 샘플 `cURL` 요청:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**엔드포인트 참조**

| 메서드 | URL | 필수 매개변수 | 설명 |
|--------|-----|---------------------|-------------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions`(JSON 본문) | 지정된 `AutoFitterOptions`를 대상 워크북에 적용합니다. |
| GET    | `/cells/workbook/autoFitter` | *없음* | 워크북의 현재 `AutoFitterOptions` 설정을 가져옵니다. |

**PUT 엔드포인트의 요청 매개변수**

| 매개변수                 | 유형    | 필수 여부 | 설명 |
|--------------------------|---------|----------|-------------|
| AutoFitMergedCellsType   | string  | 예       | 병합 셀 자동 맞춤 방식(`All`, `First`, `None`). |
| IgnoreHidden             | boolean | 아니요   | 숨김 행/열을 무시할지 여부. |
| OnlyAuto                 | boolean | 아니요   | 수동 높이 설정이 없는 행만 맞춤. |
| DefaultEditLanguage      | string  | 아니요   | 편집 언어(예: `en-US`). |
| MaxRowHeight             | double  | 아니요   | 최대 행 높이(포인트); `0` = 무제한. |
| AutoFitWrappedTextType   | string  | 아니요   | 줄 바꿈 텍스트 처리 방식(`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | 아니요   | 서식 전략(`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | 아니요   | 렌더링용 자동 맞춤 적용(`True`, `False`). |

일반적인 응답 코드:

- **200 OK** – 작업이 성공적으로 완료되었습니다.  
- **400 Bad Request** – 유효하지 않은 JSON 페이로드 또는 지원되지 않는 값입니다.  
- **401 Unauthorized** – 인증 토큰이 누락되었거나 유효하지 않습니다.  
- **500 Internal Server Error** – 예기치 않은 서버 오류입니다.

**샘플 GET 응답**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

이 예시는 Aspose.Cells Cloud API 내에서 `AutoFitterOptions` 모델을 구성하고 호출하는 방법을 보여줍니다.
---