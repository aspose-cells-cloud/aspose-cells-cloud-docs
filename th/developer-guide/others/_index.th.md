---
title: "Aspise.Cells Cloud Web API – คุณสมบัติอื่นๆ: การตรวจสอบสุขภาพของระบบ, การรับคีย์สาธารณะ"
linktitle: "คุณสมบัติอื่นๆ"
ArticleTitle: "คุณสมบัติอื่นๆ: การตรวจสอบสุขภาพของระบบ, การรับคีย์สาธารณะ"
second_title: "เอกสาร"
type: docs
url: /th/other-features/
keywords: "Aspose.Cells, Cloud API, การตรวจสอบสุขภาพของระบบ, คีย์สาธารณะ, access token, Excel, REST"
description: "สำรวจคุณสมบัติอื่นๆ ของ Aspose.Cells Cloud: endpoint สำหรับการตรวจสอบสุขภาพของระบบ, การรับคีย์สาธารณะ และการสร้าง access token เพื่อความปลอดภัยในการผสานรวม API Excel ของคุณ"
weight: 180
---

**ข้อกำหนดเบื้องต้น** – เพื่อใช้งานคุณสมบัติที่ระบุไว้ด้านล่าง คุณต้องมีการสมัครใช้งาน Aspose Cloud ที่ถูกต้องและคู่ค่า **Client ID** / **Client Secret** ที่ใช้งานอยู่สำหรับการยืนยันตัวตน

คุณสมบัติ “คุณสมบัติอื่นๆ” เหล่านี้จัดเตรียมการดำเนินการสนับสนุนที่จำเป็นสำหรับ Aspose.Cells Cloud API เช่น การยืนยันความพร้อมใช้งานของบริการ การรับคีย์เชิงเข้ารหัส และการรับ access token โดยทั่วไปจะเรียกใช้ก่อนการทำงานกับ endpoint ที่เกี่ยวข้องกับเวิร์กบุ๊ก

- **[การตรวจสอบสุขภาพของบริการ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  ตรวจสอบว่าบริการ Aspose.Cells Cloud สามารถเข้าถึงได้และทำงานได้อย่างถูกต้องหรือไม่ การเรียกใช้งานที่สำเร็จจะส่งกลับ **HTTP 200** พร้อม JSON `{ "status": "OK" }` ใช้ endpoint นี้ในช่วงต้นของกระบวนการทำงานเพื่อหลีกเลี่ยงข้อผิดพลาดที่ไม่จำเป็น  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">อ่านเพิ่มเติม</a>

- **[รับสถานะการทำงานของ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  รับสถานะการทำงานปัจจุบันของบริการ โดยคำตอบจะระบุว่า API นั้นทำงานได้อย่างเต็มประสิทธิภาพอยู่หรือไม่ อยู่ในโหมดการบำรุงรักษา หรือกำลังประสบปัญหา  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">อ่านเพิ่มเติม</a>

- **[รับคีย์สาธารณะ](https://docs.aspose.cloud/cells/get-public-key/)**  
  รับคีย์สาธารณะ RSA (รูปแบบ PEM) ที่ใช้ยืนยันความถูกต้องของ JWT token ที่ออกโดย Aspose.Cells Cloud คีย์นี้จำเป็นเมื่อคุณยืนยันความถูกต้องของ token บนฝั่งเซิร์ฟเวอร์ของคุณ  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">อ่านเพิ่มเติม</a>

- **[รับ Access Token ด้วย Client ID และ Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  สร้าง access token แบบ OAuth 2.0 โดยใช้ grant type **client_credentials** ใส่ **Client ID** และ **Client Secret** ของคุณในเนื้อหาคำขอ คำตอบจะประกอบด้วย `access_token`, `token_type` และ `expires_in` access token นี้ต้องถูกส่งไปใน header `Authorization` สำหรับ API call ทั้งหมดที่ตามมา  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">อ่านเพิ่มเติม</a>

---