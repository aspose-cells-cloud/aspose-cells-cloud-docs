---
title: "Migrating Protection & Encryption to 4.0"
second_title: "Document"
ArticleTitle: "Migrating Protection & Encryption APIs from 3.0 to 4.0: What's Better, What's Missing, and How to Fill the Gaps"
linktitle: "Protection & Encryption Migration"
type: docs
weight: 100
keywords: "Aspose.Cells Cloud, Excel API, migration, spreadsheet conversion, merge Excel, split Excel, protect Excel, cloud spreadsheet SDK, REST API, Excel processing"
description: "How 10 Protection and Encryption endpoints collapse into 3 consolidated 4.0 routes, what the simplification costs you in fine-grained control, and how to work around it."
url: /cells/migrating-protection/
---

## Introduction

Aspose.Cells Cloud 4.0 simplifies the Protection API from 10 endpoints in version 3.0 down to **3 clean, unified endpoints**. The new API consolidates password protection, write protection, encryption, and digital signatures into a streamlined interface that's easier to use — but with a significant trade-off: **fine-grained control is reduced**.

This guide maps every 3.0 protection endpoint to its 4.0 replacement, explains what's been consolidated, identifies the gaps, and proposes concrete solutions for missing capabilities.

---

## What's Changed at a Glance

| Aspect | 3.0 | 4.0 |
|--------|-----|-----|
| **Total Endpoints** | 10 | 3 |
| **HTTP Methods** | POST + PUT + DELETE | PUT only |
| **Password Protection** | Dedicated endpoint | Unified with protection |
| **Write Protection** | Separate PUT/DELETE pair | Unified with protection |
| **Encryption** | Separate POST/DELETE pair | Unified with protection |
| **Digital Signature** | 1 endpoint | 1 endpoint |
| **Batch Lock/Unlock** | ✅ Yes (BatchController) | ❌ No |
| **Granular Protection Types** | ✅ Yes (All, Contents, etc.) | ✅ Yes |
| **Modify Password** | ✅ Yes | ✅ Yes |
| **Base Path** | `/v3.0/cells` | `/v4.0/cells` |

---

## Endpoint Mapping: 3.0 → 4.0

### ✅ Directly Mappable Endpoints

| # | 3.0 Endpoint | 4.0 Endpoint | Notes |
|---|-------------|-------------|-------|
| 1 | `POST /cells/{name}/digitalsignature` | `PUT /cells/digitalsignature/spreadsheet` | Path restructured |
| 2 | `POST /cells/{name}/protection` | `PUT /cells/protection/spreadsheet` | Consolidated |
| 3 | `DELETE /cells/{name}/protection` | `PUT /cells/unprotection/spreadsheet` | Method changed |
| 4 | `POST /cells/protect` | `PUT /cells/protection/spreadsheet` | Consolidated into unified endpoint |
| 5 | `POST /cells/lock` | `PUT /cells/protection/spreadsheet` | Consolidated into unified endpoint |
| 6 | `POST /cells/unlock` | `PUT /cells/unprotection/spreadsheet` | Consolidated into unified endpoint |

### ❌ Consolidated (No Dedicated Endpoint)

| # | 3.0 Endpoint | 4.0 Status | How to Achieve in 4.0 |
|---|-------------|-----------|----------------------|
| 7 | `POST /cells/{name}/encryption` | ❌ No dedicated endpoint | Pass `password` to `PUT /cells/protection/spreadsheet` |
| 8 | `DELETE /cells/{name}/encryption` | ❌ No dedicated endpoint | Pass `password` to `PUT /cells/unprotection/spreadsheet` |
| 9 | `PUT /cells/{name}/writeProtection` | ❌ No dedicated endpoint | Pass `modifyPassword` to `PUT /cells/protection/spreadsheet` |
| 10 | `DELETE /cells/{name}/writeProtection` | ❌ No dedicated endpoint | Pass `modifyPassword` to `PUT /cells/unprotection/spreadsheet` |

### 🆕 4.0 Exclusive

| Endpoint | Description |
|----------|-------------|
| *(None)* | 4.0 Protection API has **no new exclusive endpoints** — it's a pure consolidation |

---

## Why Migrate to 4.0?

### 1. 🔧 Unified API — One Endpoint for All Protection Types

In 3.0, you had to remember which endpoint to call for each protection type:

```
POST /cells/{name}/protection       → Sheet protection
POST /cells/{name}/encryption       → File encryption
PUT  /cells/{name}/writeProtection  → Write protection
POST /cells/protect                 → Batch protection
POST /cells/lock                    → Batch lock
```

In 4.0, **one endpoint handles everything**:

```
PUT /cells/protection/spreadsheet?password=xxx&modifyPassword=yyy
```

The API automatically determines the protection type based on the parameters you provide.

### 2. 🧹 Fewer Endpoints to Learn

3.0 had 10 protection endpoints. 4.0 has 3:

| Purpose | 4.0 Endpoint |
|---------|-------------|
| Protect a spreadsheet | `PUT /cells/protection/spreadsheet` |
| Unprotect a spreadsheet | `PUT /cells/unprotection/spreadsheet` |
| Add digital signature | `PUT /cells/digitalsignature/spreadsheet` |

That's it. No more memorizing which HTTP method (POST/PUT/DELETE) to use for each operation.

### 3. 🔒 Simplified Request Model

**3.0 — Multiple request formats:**
```json
// Protection request
{ "ProtectionType": "All", "Password": "secret" }

// Encryption request  
{ "EncryptionType": "XOR", "Password": "secret", "KeyLength": 40 }

// Write protection request
{ "Password": "modify_secret" }
```

**4.0 — Single request format:**
```json
// All protection via one endpoint
{
  "password": "secret",
  "modifyPassword": "modify_secret",
  "protectionType": "All"
}
```

---

## Migration Examples

### Example 1: Protect a Spreadsheet with Password

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/report.xlsx/protection" \
  -H "Authorization: Bearer TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"ProtectionType": "All", "Password": "secret123"}'
```

**4.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?password=secret123" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@report.xlsx"
```

### Example 2: Encrypt a Workbook

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/report.xlsx/encryption" \
  -H "Authorization: Bearer TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"EncryptionType": "XOR", "Password": "secret123", "KeyLength": 40}'
```

**4.0:**
```bash
# Encryption is now part of the protection endpoint
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?password=secret123" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@report.xlsx"
```

> **Note:** The `EncryptionType` and `KeyLength` parameters are not yet exposed in the 4.0 API. The server applies default encryption settings. See "What's Missing" below.

### Example 3: Add Write Protection

**3.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/report.xlsx/writeProtection" \
  -H "Authorization: Bearer TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"Password": "modify_secret"}'
```

**4.0:**
```bash
# Write protection via modifyPassword parameter
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?modifyPassword=modify_secret" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@report.xlsx"
```

### Example 4: Remove All Protection

**3.0:**
```bash
# Three separate calls needed:
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/report.xlsx/protection" \
  -d '{"Password": "secret123"}'

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/report.xlsx/encryption" \
  -d '{"Password": "secret123"}'

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/report.xlsx/writeProtection"
```

**4.0:**
```bash
# One call removes all protection
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=secret123&modifyPassword=modify_secret" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@report.xlsx"
```

### Example 5: Add Digital Signature

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/report.xlsx/digitalsignature" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@report.xlsx" \
  -F "certificate=@cert.pfx" \
  -d "password=cert_password"
```

**4.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/digitalsignature/spreadsheet?password=cert_password" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@report.xlsx" \
  -F "certificate=@cert.pfx"
```

---

## C# SDK Migration

### 3.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Protect
await cellsApi.PostProtectWorkbook("report.xlsx", "All", "secret123");

// Encrypt
await cellsApi.PostEncryptWorkbook("report.xlsx", "XOR", "secret123", 40);

// Write protect
await cellsApi.PutDocumentProtectFromChanges("report.xlsx", "modify_secret");

// Unprotect (3 calls)
await cellsApi.DeleteUnProtectWorkbook("report.xlsx", "secret123");
await cellsApi.DeleteDecryptWorkbook("report.xlsx", "secret123");
await cellsApi.DeleteDocumentUnProtectFromChanges("report.xlsx");
```

### 4.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Protect (all-in-one)
using var stream = File.OpenRead("report.xlsx");
await cellsApi.ProtectSpreadsheet(stream, password: "secret123", modifyPassword: "modify_secret");

// Unprotect (all-in-one)
await cellsApi.UnprotectSpreadsheet(stream, password: "secret123", modifyPassword: "modify_secret");

// Digital signature
await cellsApi.SpreadsheetDigitalsignature(stream, certificateStream, password: "cert_password");
```

---

## ❌ What 4.0 Doesn't Support (Yet)

### Gap Analysis

| 3.0 Feature | 4.0 Status | Impact | Priority |
|-------------|-----------|--------|----------|
| **Encryption type selection** (XOR, RC4, AES) | ❌ Not configurable | 🟡 Medium — defaults to AES | Medium |
| **Key length selection** (40, 56, 128, 256 bit) | ❌ Not configurable | 🟡 Medium — defaults to 256 | Medium |
| **Protection type granular control** (Contents, Formatting, Columns, Rows) | ✅ Supported | 🟢 Low | — |
| **Batch lock/unlock** (BatchController) | ❌ Not available | 🟡 Medium | Medium |
| **Digital signature details** (X509, timestamp) | ❌ Not configurable | 🟡 Medium | Medium |
| **Unprotect without password** (if known) | ✅ Supported | 🟢 Low | — |

---

## 🔧 How to Add Missing Features

### Feature 1: Encryption Configuration

**Why it matters:** Different security requirements demand different encryption algorithms and key lengths. Government and financial sectors often require AES-256.

**Proposed endpoint enhancement:**
```
PUT /cells/protection/spreadsheet?password=xxx&encryptionType=AES&keyLength=256
```

**Implementation approach:**

```csharp
[HttpPut]
[Route("protection/spreadsheet")]
public IActionResult ProtectSpreadsheet(
    string password,
    string modifyPassword = null,
    string protectionType = null,
    string encryptionType = "AES",  // NEW: XOR, RC4, AES
    int keyLength = 256)            // NEW: 40, 56, 128, 256
{
    return StreamsOperation(streams =>
    {
        var workbook = LoadWorkbookFromStreams(streams);
        
        // Apply sheet protection
        if (!string.IsNullOrEmpty(protectionType))
        {
            foreach (Worksheet sheet in workbook.Worksheets)
            {
                var protection = sheet.Protection;
                protection.Type = ParseProtectionType(protectionType);
                protection.Password = password;
            }
        }
        
        // Apply encryption
        if (!string.IsNullOrEmpty(password))
        {
            var encryptionOptions = new EncryptionOptions
            {
                EncryptionType = ParseEncryptionType(encryptionType),
                KeyLength = keyLength,
                Password = password
            };
            workbook.SetEncryptionOptions(encryptionOptions);
        }
        
        // Apply write protection
        if (!string.IsNullOrEmpty(modifyPassword))
        {
            workbook.Settings.WriteProtection.Password = modifyPassword;
        }
        
        return workbook.ToStream(SaveFormat.Xlsx);
    }, "ProtectSpreadsheet");
}
```

### Feature 2: Batch Protection Operations

**Why it matters:** When managing hundreds of files, batch operations are essential for efficiency.

**Proposed endpoint:**
```
PUT /cells/batch/protection/spreadsheet
```

**Implementation approach:**

```csharp
[HttpPut]
[Route("batch/protection/spreadsheet")]
public IActionResult BatchProtectSpreadsheets(
    string folder,
    string fileMatchExpression = null,
    string password = null,
    string modifyPassword = null,
    string action = "protect")  // protect, unprotect
{
    return StorageOperation(storage =>
    {
        var files = storage.ListFiles(folder);
        var matchingFiles = files
            .Where(f => f.IsFile && MatchesPattern(f.Name, fileMatchExpression))
            .ToList();
        
        var results = new List<BatchResult>();
        
        foreach (var file in matchingFiles)
        {
            try
            {
                using var stream = storage.ReadFile(file.FullName);
                var workbook = new Workbook(stream);
                
                if (action == "protect")
                {
                    ApplyProtection(workbook, password, modifyPassword);
                }
                else
                {
                    RemoveProtection(workbook, password, modifyPassword);
                }
                
                storage.WriteFile(file.FullName, workbook.ToStream(SaveFormat.Xlsx));
                results.Add(new BatchResult { File = file.Name, Status = "Success" });
            }
            catch (Exception ex)
            {
                results.Add(new BatchResult { File = file.Name, Status = "Failed", Error = ex.Message });
            }
        }
        
        return results;
    }, "BatchProtectSpreadsheets");
}
```

### Feature 3: Digital Signature Configuration

**Why it matters:** Advanced digital signature scenarios require control over signature algorithm, timestamp server, and certificate chain.

**Proposed endpoint enhancement:**
```
PUT /cells/digitalsignature/spreadsheet?password=xxx&timestampServer=https://timestamp.digicert.com
```

**Implementation approach:**

```csharp
[HttpPut]
[Route("digitalsignature/spreadsheet")]
public IActionResult SpreadsheetDigitalsignature(
    string password,
    string timestampServer = null,  // NEW
    string reason = null,           // NEW
    string location = null)         // NEW
{
    return StreamsOperation(streams =>
    {
        Stream certStream = null;
        Stream workbookStream = null;
        
        foreach (var stream in streams)
        {
            if (stream.Key.EndsWith(".pfx") || stream.Key.EndsWith(".p12"))
                certStream = stream.Value;
            else
                workbookStream = stream.Value;
        }
        
        var workbook = new Workbook(workbookStream);
        
        var signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(
            new X509Certificate2(certStream, password));
        
        signature.Comments = reason ?? "Signed via Aspose.Cells Cloud";
        signature.SignTime = DateTime.Now;
        
        if (!string.IsNullOrEmpty(timestampServer))
        {
            signature.TimeStamp = new TimeStamp(timestampServer, "", "");
        }
        
        workbook.AddDigitalSignature(signature);
        
        return workbook.ToStream(SaveFormat.Xlsx);
    }, "SpreadsheetDigitalsignature");
}
```

---

## Summary: Migration Decision Matrix

| Scenario | Migrate to 4.0? | Reason |
|----------|----------------|--------|
| Basic password protection | ✅ **Yes** | Simpler, unified API |
| Write protection | ✅ **Yes** | Unified with protection endpoint |
| Digital signatures | ✅ **Yes** | Direct mapping |
| Unprotect files | ✅ **Yes** | One call vs. three |
| Custom encryption (AES-128 vs AES-256) | ⚠️ **Wait** | Not configurable in 4.0 yet |
| Batch lock/unlock | ⚠️ **Wait** | Not in 4.0 — keep 3.0 or request feature |
| Advanced digital signature (timestamp) | ⚠️ **Wait** | Not configurable in 4.0 yet |
