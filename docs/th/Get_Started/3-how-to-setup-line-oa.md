---
icon: 
title: 3. ตั้งค่า LINE OA
---

# ตั้งค่า LINE OA

<iframe width="560" height="315" src="https://www.youtube.com/embed/c6YIIMPAFk4?si=3TPcEqDh_QMpLVxe" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**การตั้งค่า LINE Official Account (OA) ใน Fox Connect**

---

### 1. เข้าถึง Fox Connect และเริ่มสร้างช่องทาง  
- เปิด **Fox Connect** → ไปที่ **Settings**  
- เลือกแท็บ **Channels** จากนั้นคลิก **Add Channel**  
- เลือก **Connect Line OA account** เป็นประเภทช่องทาง  

> *ต้องกรอกข้อมูลในฟิลด์ที่จำเป็นทั้งหมดเพื่อให้ระบบการจองทำงานได้อย่างถูกต้อง*

---

### 2. เปิดใช้งาน Messaging API บน LINE OA Manager  
- ไปที่เว็บไซต์ **LINE OA Manager** และเข้าสู่ระบบด้วยบัญชี LINE ของคุณ  
- คลิก **Settings** → **Messaging API** (เมนูด้านซ้าย)  
- กด **Enable Messaging API**  
- ในป็อปอัป ให้สร้าง provider ใหม่:
  - ตั้งชื่อ (ชื่อใดก็ได้ตามต้องการ)  
  - เพิ่ม URL สำหรับ **Privacy Policy** และ **Terms of Use** (หรือข้ามหากยังไม่พร้อม)  
  - ยืนยันโดยคลิก **OK**  

> *การเปิดใช้งาน Messaging API เป็นข้อกำหนดเบื้องต้นแรกสำหรับการเชื่อมต่อ*

---

### 3. ดึงข้อมูล Credentials จาก LINE Developers Console  
| รายการ | วิธีการรับ | ตำแหน่งที่วางใน Fox Connect |
|------|---------------|------------------------------|
| **Channel ID** | ในเว็บไซต์ LINE Developers เปิด provider ของคุณ → เลือกบัญชี OA ของคุณ ภายใต้ **Basic settings** ให้คัดลอก *Channel ID* | วางในฟิลด์ที่สอดคล้องกันใน Fox Connect |
| **Channel Secret** | เลื่อนลงภายใต้ **Basic settings** คัดลอก *Channel Secret* | วางใน Fox Connect |
| **Access Token** | ไปที่แท็บ **Messaging API** เลื่อนลงด้านล่างสุดแล้วคลิก **Issue** คัดลอก token ที่สร้างขึ้น | วางใน Fox Connect |
| **Bot Basic ID** | ที่ด้านบนของแท็บ **Messaging API** คัดลอก *Bot Basic ID* | วางใน Fox Connect |

> *ข้อมูล credentials เหล่านี้ช่วยให้ Fox Connect สามารถยืนยันตัวตนและโต้ตอบกับ LINE Messaging API ได้*

---

### 4. สรุปการตั้งค่าช่องทางใน Fox Connect  
- หลังจากวางข้อมูล credentials ทั้งหมดแล้ว ให้ **Save** การตั้งค่า  
- ฟิลด์ใหม่ควรปรากฏโดยอัตโนมัติ (เช่น Webhook URL)  

---

### 5. ตรวจสอบและเปิดใช้งาน Webhook  
- กลับไปที่แท็บ **Messaging API** ใน LINE Developers  
- ค้นหาฟิลด์ **Webhook URL** และคลิก **Verify** เพื่อตรวจสอบว่าเข้าถึงได้  
- สลับ **Use Webhook** เป็น "On"  

> *การเปิดใช้งาน webhook จะทำให้การตั้งค่าช่องทางสมบูรณ์ ช่วยให้ส่งข้อความได้แบบ real-time*

---

### รายการตรวจสอบสรุป  

- [ ] เปิดใช้งาน Messaging API บน LINE OA Manager แล้ว  
- [ ] สร้าง provider และบันทึก URL แล้ว (หากมี)  
- [ ] คัดลอก **Channel ID**, **Channel Secret**, **Access Token** และ **Bot Basic ID** แล้ว  
- [ ] วาง credentials ใน Fox Connect และบันทึกแล้ว  
- [ ] ตรวจสอบ Webhook URL และเปิดใช้งาน webhook แล้ว
