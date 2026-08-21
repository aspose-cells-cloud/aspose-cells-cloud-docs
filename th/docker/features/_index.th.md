---
title: "ฟังก์ชันหลักของ Aspose.Cells Cloud Docker: การแปลงสเปรดชีต การผสาน การแยก การป้องกัน การประมวลผลข้อมูล และอื่นๆ"
second_title: "เอกสาร"
ArticleTitle: "ฟังก์ชันหลักของ Aspose.Cells Cloud Docker"
linktype: "คุณสมบัติ"
type: docs
url: /docker-container-features/
description: "เรียกใช้ API ของ Aspose.Cells Cloud แบบโลคัลด้วย Aspose.Cells Cloud Docker Container—a บริการที่บรรจุอยู่ในคอนเทนเนอร์แบบ Docker ซึ่งให้ความสามารถในการประมวลผลสเปรดชีตแบบเต็มรูปแบบ ความเป็นส่วนตัว และการทำงานแบบออฟไลน์ โดยไม่ต้องใช้คลาวด์สาธารณะของ Aspose"
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - การแปลงสเปรดชีต
  - การประมวลผล Excel
  - การส่งออกเป็น PDF
  - การจัดการ CSV
  - REST API
  - บริการที่บรรจุในคอนเทนเนอร์
  - คลาวด์ส่วนตัว
  - การประมวลผลแบบออฟไลน์
---

## Aspose.Cells Cloud Docker Container คืออะไร?

Aspose.Cells Cloud Docker Container คือ บริการที่บรรจุในคอนเทนเนอร์ซึ่งจัดทำโดย Aspose โดยอ้างอิงจาก Docker ช่วยให้คุณสามารถปรับใช้ฟังก์ชันของ Aspose.Cells Cloud API ในสภาพแวดล้อมแบบโลคัลหรือคลาวด์ส่วนตัว โดยไม่ต้องพึ่งพาบริการคลาวด์สาธารณะของ Aspose

## ทำไมจึงควรใช้ Aspose.Cells Cloud Docker Container?

Aspose.Cells Cloud Docker Container คือ คอนเทนเนอร์ของบริการประมวลผลสเปรดชีตที่ทรงพลัง ซึ่งรองรับ:

### คุณสมบัติหลัก

- อ่านและเขียนไฟล์ Excel (XLS, XLSX, CSV, ODS เป็นต้น)
- การคำนวณสูตร กราฟ การจัดรูปแบบแบบมีเงื่อนไข ตาราง.pivot เป็นต้น
- การแปลงรูปแบบ (เช่น Excel เป็น PDF HTML รูปภาพ เป็นต้น)
- การจัดการเซลล์ การตั้งค่ารูปแบบ การจัดการเวิร์กชีต เป็นต้น

Aspose.Cells Cloud Docker Container ห่อหุ้มคุณสมบัติเหล่านี้ไว้ในรูปแบบ RESTful API และบรรจุลงใน Docker image ช่วยให้คุณสามารถรันบนโครงสร้างพื้นฐานของตนเองได้

### ข้อได้เปรียบหลัก

| ข้อดี                          | คำอธิบาย                                                                 |
| ------------------------------ | ------------------------------------------------------------------------ |
| ความเป็นส่วนตัวและความปลอดภัยของข้อมูล | การประมวลผลไฟล์ทั้งหมดดำเนินการภายในเครือข่ายส่วนตัวของคุณ ไม่จำเป็นต้องอัปโหลดไปยังคลาวด์ของบุคคลที่สาม |
| ความพร้อมใช้งานแบบออฟไลน์    | ไม่พึ่งพาคลาวด์สาธารณะของ Aspose เหมาะสำหรับสภาพแวดล้อมในเครือข่ายภายในหรือแบบแยกisolated |
| ความยืดหยุ่นในการปรับขนาด     | ปรับขนาดแบบกระจายได้ง่ายผ่าน Docker/Kubernetes                         |
| API ที่สอดคล้องกัน             | สอดคล้องกับ Aspose.Cells Cloud public API ทั้งหมด ไม่จำเป็นต้องแก้ไขโค้ด |
| การควบคุมใบอนุญาต             | รองรับการยืนยันตัวตนสองรูปแบบ เลือกแบบที่เหมาะสมกับสถานการณ์ของคุณ |

## วิธีการใช้ Aspose.Cells Cloud Docker Container

อ้างอิงคู่มือผู้ใช้ — [วิธีการใช้ Aspose.Cells Cloud Docker Container](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container)

**ข้อกำหนดเบื้องต้น**

- Docker Engine เวอร์ชัน 20.10 หรือใหม่กว่าติดตั้งอยู่บนเครื่องโฮสต์  
- หน่วยความจำ RAM อย่างน้อย 2 GB และ CPU อย่างน้อย 2 คอร์ จัดสรรให้กับคอนเทนเนอร์สำหรับภาระงานทั่วไป  
- ไฟล์ใบอนุญาต Aspose.Cells Cloud ที่ถูกต้อง (หรือ access token) วางไว้ในไดเรกทอรีที่จะถูก mount ลงในคอนเทนเนอร์  

**เริ่มต้นอย่างรวดเร็ว**

1. ดึง Docker image: `docker pull aspose/cells-cloud`  
2. รันคอนเทนเนอร์ โดย mount ไดเรกทอรีใบอนุญาตและข้อมูล เช่น:  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. เข้าถึง REST API ที่ `http://localhost:8080/v3.0/` สำหรับการใช้งาน API แบบละเอียด ดูที่ [เอกสารอ้างอิง Aspose.Cells Cloud API](https://docs.aspose.cloud/cells/api-reference/)

## เอกสารอ้างอิง

- [วิธีการตั้งค่าการจัดเก็บข้อมูลของ Aspose.Cells Cloud Docker Container](https://docs.aspose.cloud/cells/docker/storage/)  
---