---
title: "Aspose.Cells Cloud AI – 用户任务分解 API（v4.0）｜SMART 任务规划"
second_title: "文档"
ArticleTitle: "如何使用 Aspose.Cells Cloud AI 任务分解 API 将用户目标转换为顺序行动方案"
linktype: "docs"
url: /zh/decompose-user-task/
keywords: "Aspose.Cells AI, 任务分解 API, SMART 任务规划, Redmine 导入, 项目自动化"
description: "借助 Aspose.Cells Cloud AI，将自由格式的目标转换为符合 SMART 原则、含时间估算的顺序任务列表。通过一次 PUT 请求，即可获得适用于 Redmine、Jira 或 Azure DevOps 的 CSV/XLSX 格式输出。"
weight: 100
---

**DecomposeUserTask**（分解用户任务）端点提供一个 REST 接口，可将自由格式的任务描述转换为详细的、按顺序排列的行动方案，且符合 SMART 原则。该服务自动分配以小时为单位的时间估算，并将输出格式化为与 Redmine 兼容的导入格式，同时创建项目里程碑节点。只需提供原始任务列表及可选的时间估算，API 即可返回一个可直接导入项目管理工具的就绪文件（如 CSV、XLSX 等），从而自动化任务拆解，减少人工操作。

## **分解用户任务 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名           | 类型   | 位置 | 必填/可选 | 描述                                                                                                                                                                                                                              |
| :--------------- | :----- | :--- | :-------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription  | string | Body | 必填      | 用户整体目标的纯文本描述。服务会解析该描述并生成独立的任务项。示例："为第三季度启动营销活动，包括内容创作、电子邮件群发及社交媒体广告。"                                                                                             |

### **响应**

成功响应（200 OK）  
Content‑Type: `application/octet-stream`（二进制文件流）

响应头：

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <字节数>`

XLSX/ODS 格式使用相同结构，各列置于第一个工作表中。

**HTTP 状态码**

| 状态码 | 含义             | 说明                         |
| ------ | ---------------- | ---------------------------- |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。            |
| 413    | Payload Too Large（请求实体过大） | 上传文件超过大小限制。         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。           |

**错误响应示例（400 Bad Request）**

```json
{
  "code": "InvalidParameter",
  "message": "字段 'TaskDescription' 为必填项，且不能为空。"
}
```

**示例请求体（JSON）**

```json
{
  "TaskDescription": "为现有系统开发一个任务拆分功能的 Web API。"
}
```

**示例响应**  
API 返回包含生成文件的二进制流。若需预览 CSV 响应的前几行，可解码该流并查看标题行，例如：

```
ID,Subject,Trucker,Estimated Duration,Description
1	任务拆分 API 需求收集	业务分析师	8	收集新任务拆分端点的功能性与非功能性需求、用户故事及验收标准。
2	API 规范（OpenAPI）	业务分析师	6	定义 POST /tasks/split 的 OpenAPI 合约，包括请求模式、响应格式、错误代码及安全要求。
3	拆分算法与数据模型设计	解决方案架构师	5	设计核心算法，将父任务拆分为子任务；并扩展数据模型（数据库表/实体），以存储层级结构与元数据。
4	架构集成评审	解决方案架构师	4	分析对现有服务、事件流及数据库迁移的影响；制定集成方案。
...
```

## 应在何处使用分解用户任务 API？

- **项目启动阶段**：将高层次项目简介转换为与 Redmine 兼容的任务列表（含时间估算），支持立即开展冲刺规划。
- **营销自动化**：将活动目标拆解为可执行步骤，导出为 CSV 并导入任务管理工具，实现跨团队协作。
- **资源分配**：为每个子任务生成基于小时的估算，使管理者可在项目启动前合理分配团队工作量。
- **里程碑跟踪**：自动生成可与甘特图工具同步的里程碑节点，确保每个阶段都有明确交付成果。

## 为何应使用分解用户任务 API？

- **符合 SMART 原则的输出**：确保每个生成的任务均满足“具体（Specific）、可衡量（Measurable）、可实现（Achievable）、相关性（Relevant）、时限性（Time-bound）”标准。
- **内置小时级时间估算**：免除手动计算，提升预测准确性。
- **即用型导入格式**（CSV、XLSX 等）：便于与 Redmine、Jira、Azure DevOps 及其他项目管理平台集成。
- **单请求自动化**：通过一次请求即可完成任务拆解，加速项目启动并减少人工干预。

## 如何使用 SDK 调用分解用户任务 API

### 分解用户任务 API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">分解用户任务 API 规范</a> 提供了公开可访问的编程接口，支持直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，让您能以简洁代码调用 DecomposeUserTask 端点。  
请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。  
以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务进行交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}