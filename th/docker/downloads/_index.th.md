---
title: "ดาวน์โหลดภาพ Docker ของ Aspose.Cells Cloud"  
second_title: "เอกสาร"  
ArticleTitle: "ดาวน์โหลดภาพ Docker ของ Aspose.Cells Cloud"  
linktype: "ดาวน์โหลดภาพ"  
type: docs  
url: /docker/downloads/  
description: "รับภาพ Docker ล่าสุดของ Aspose.Cells Cloud สำหรับ Windows Server 2016/2019 และ Linux ทำตามคำแนะนำแบบทีละขั้นตอน ข้อกำหนดเบื้องต้น และคำแนะนำด้านความปลอดภัยเพื่อเรียกใช้คอนเทนเนอร์ในเครื่องของคุณ"  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, container, image, download, Windows Server, Linux, REST API"  
---

## ภาพรวม  

`aspose/cells-cloud` – ภาพ Docker อย่างเป็นทางการที่ให้บริการ **Aspose.Cells Cloud** REST API ภาพนี้ช่วยให้คุณสามารถเรียกใช้เครื่องมือประมวลผลสเปรดชีตแบบเต็มรูปแบบภายในคอนเทนเนอร์ ทำให้สามารถปรับใช้งานแบบออฟไลน์หรือในคลาวด์ส่วนตัวได้โดยไม่ต้องพึ่งพาบริการคลาวด์สาธารณะของ Aspose  

**อัปเดตล่าสุด:** 2026‑06‑30  

**รายการตรวจสอบสำหรับการเริ่มต้นใช้งานอย่างรวดเร็ว**

- ตรวจสอบให้แน่ใจว่าเวอร์ชัน Docker Engine คือ 20.10 หรือใหม่กว่า  
- ดึงภาพที่เหมาะสมสำหรับระบบปฏิบัติการของคุณ (ดูหัวข้อด้านล่าง)  
- ตั้งค่าตัวแปรแวดล้อม `ASPOSE_CLIENT_ID` และ `ASPOSE_CLIENT_SECRET`  
- เรียกใช้คอนเทนเนอร์โดยแมปพอร์ต 8080 ไปยังพอร์ตภายใน 80  

---  

## ข้อกำหนดเบื้องต้น  

| ข้อกำหนด | รายละเอียด |
|----------|-----------|
| **Docker Engine** | ติดตั้ง Docker 20.10 หรือใหม่กว่าบนระบบปฏิบัติการเซิร์ฟเวอร์ |
| **ระบบปฏิบัติการ** | Windows Server 2016, Windows Server 2019 หรือการแจกจ่าย Linux รุ่นสมัยใหม่อื่นๆ |
| **การเข้าถึง Docker Hub** | บัญชี Docker Hub ที่ใช้งานอยู่ (ไม่บังคับ แต่แนะนำสำหรับภาพส่วนตัว) รันคำสั่ง `docker login` หากคุณต้องการดึงภาพจากที่เก็บส่วนตัว |
| **ข้อมูลรับรอง Aspose Cloud** | `ASPOSE_CLIENT_ID` และ `ASPOSE_CLIENT_SECRET` – รับจากแดชบอร์ด Aspose Cloud |

> **คำแนะนำ:** ตรวจสอบการติดตั้ง Docker โดยใช้ `docker --version`  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## การเรียกใช้คอนเทนเนอร์  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **ตัวแปรแวดล้อม** – `ASPOSE_CLIENT_ID` และ `ASPOSE_CLIENT_SECRET` ใช้จัดส่งข้อมูลรับรองที่ API ต้องการ  
* **การแมปพอร์ต** – คอนเทนเนอร์เปิดพอร์ต 80 ไว้; แมปไปยังพอร์ตของโฮสต์ (เช่น 8080) เพื่อเข้าถึงบริการ  
* **โหมดแยก (`-d`) **– เรียกใช้คอนเทนเนอร์ในเบื้องหลัง  

---  

## การเวอร์ชันและการอัปเดต  

| ระบบปฏิบัติการ | แท็ก | วันที่เผยแพร่ | วิธีรับเวอร์ชันล่าสุด |
|----------------|------|----------------|------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **หมายเหตุ:** แท็ก `21.9` คือเวอร์ชันที่เสถียรในปัจจุบัน ใช้แท็ก `latest` หรือตรวจสอบ[บันทึกการเผยแพร่ของ Aspose.Cells Cloud](/cells/release-notes/) เพื่อดูเวอร์ชันที่ใหม่กว่า  

---  

## การตรวจสอบและความปลอดภัย  

* **ตรวจสอบ Digest ของภาพ**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **สแกนช่องโหว่ **(แนะนำ)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **แนวทางปฏิบัติที่ดี** – อัปเดต Docker อย่างสม่ำเสมอ รันคอนเทนเนอร์ด้วยสิทธิ์ขั้นต่ำที่จำเป็น และสแกนภาพเป็นประจำเพื่อตรวจหา CVE ที่รู้จัก  

* **ตัวอย่างข้อมูลโครงสร้าง (JSON‑LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker Image",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## ปัญหาทั่วไปและการแก้ไขข้อขัดข้อง  

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ไข |
|-------|-------------------|-----------|
| `docker: command not found` | Docker ไม่ได้ติดตั้งหรือไม่ได้ตั้งค่า PATH | ติดตั้ง Docker และรีสตาร์ทเทอร์มินัล |
| ล้มเหลวในการยืนยันตัวตนเมื่อดึงภาพ | ไม่มีหรือ `docker login` ไม่ถูกต้อง | รัน `docker login` ด้วยข้อมูลรับรอง Docker Hub ที่ถูกต้อง |
| คอนเทนเนอร์หยุดทำงานทันที | ไม่มีตัวแปรแวดล้อมที่จำเป็น | ระบุ `ASPOSE_CLIENT_ID` และ `ASPOSE_CLIENT_SECRET` ดังที่แสดงในหัวข้อ **การเรียกใช้คอนเทนเนอร์** |
| พอร์ตขัดแย้งบนโฮสต์ | พอร์ตของโฮสต์ถูกใช้งานอยู่ | เลือกพอร์ตของโฮสต์อื่น (เช่น `-p 8081:80`) |

---  

## ดูเพิ่มเติม  

* [เอกสารประกอบ API Aspose.Cells Cloud](/cells/cloud/api/)  
* [บันทึกการเผยแพร่ Aspose.Cells Cloud](/cells/release-notes/) – บันทึกการเปลี่ยนแปลงโดยละเอียดสำหรับเวอร์ชัน 21.9 และใหม่กว่า  
* [คุณสมบัติของคอนเทนเนอร์ Aspose.Cells Docker](/cells/docker/features/)  
* [แท็กภาพ Docker Aspose.Cells](/cells/docker/tag-list/)  

---  

*เขียนโดยทีมวิศวกรของ Aspose Cloud*