---
icon: 
title: 4. สร้าง LINE LIFF
---

# สร้าง LINE LIFF

<iframe width="560" height="315" src="https://www.youtube.com/embed/jEnlP8l-GGY?si=_jyeN_XKKQ2w4SNq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**การตั้งค่า LINE LIFF Booking ใน Fox Connect**

---

### 1. กลับไปที่การตั้งค่าช่องทางใน Fox Connect  
- หลังจากเชื่อมต่อ *Line OA* เสร็จแล้ว (ดูคู่มือก่อนหน้า) ให้กลับไปที่ **Settings → Channels** ใน Fox Connect  
- เลื่อนลงจนพบส่วน **Line LIFF Booking** ซึ่งเป็นที่สำหรับกรอกรายละเอียดต่อไปนี้

---

### 2. สร้าง LINE Login Channel บน Developers Console  
1. เปิด **LINE Developers** console (`https://developers.line.biz/console/`) และเข้าสู่ระบบด้วยบัญชี LINE ของคุณ  
2. จากรายการ provider ให้เลือก provider ที่คุณสร้างไว้ก่อนหน้า  
3. คลิก **Create New Channel**  
4. ในป็อปอัป เลือก **LINE Login** เป็นประเภทช่องทาง  
5. ตั้ง **Service Region** เป็น *Thailand* และยืนยันประเทศของเจ้าของ (เช่น Thailand)  
6. กรอก **Channel Name** และ **Description**  
7. ทำเครื่องหมายที่ช่อง **Web App** และ **Mobile App** ทั้งสองช่อง  
8. ยอมรับ LINE Developer Agreement แล้วคลิก **Create**

---

### 3. กำหนดค่าแท็บ LIFF  
1. ภายในช่องทางที่สร้างใหม่ ค้นหาแท็บ **LIFF** แล้วคลิก **Add**  
2. กรอกชื่อที่อธิบายแอป LIFF ของคุณ  
3. ภายใต้ **Size** เลือก **Full**  
4. คัดลอก **Endpoint URL** จากบล็อก Line LIF ID for booking ใน Fox Connect (พบได้ในการตั้งค่าช่องทาง)  
5. วาง URL นี้ในช่อง **Endpoint URL** ในการตั้งค่า LIFF  
6. ทำเครื่องหมายในช่องสามช่องที่ปรากฏด้านล่าง URL และยืนยันป็อปอัปที่ตามมา  
7. สำหรับตัวเลือก **Add Friend** ให้ตั้งเป็น **On aggressive** (เพื่อเปิดใช้งานปุ่ม "Add friend" โดยอัตโนมัติ)  
8. คลิก **Add** เพื่อบันทึกการตั้งค่าแอป LIFF

---

### 4. เปิดใช้งาน Share Target Picker และเผยแพร่  
1. ในหน้าถัดไป สลับ **Share Target Picker** เป็น *On* และยืนยันกล่องโต้ตอบที่ปรากฏ  
2. ที่ด้านบนของหน้า คลิกป้ายกำกับ **Developing** และยืนยันเพื่อเผยแพร่ช่องทาง

---

### 5. ดึงและบันทึก LIFF ID  
1. หลังจากเผยแพร่แล้ว **LIFF ID** จะปรากฏที่ด้านล่างของหน้าจอ  
2. คัดลอก ID นี้และกลับไปที่การตั้งค่าช่องทางใน Fox Connect แล้ววางลงในช่อง **LIFF ID**  
3. คลิก **Save** เพื่อสรุปการตั้งค่า

---

### 6. เสร็จสมบูรณ์  
การเชื่อมต่อ LINE LIFF Booking ของคุณได้รับการตั้งค่าอย่างสมบูรณ์และพร้อมใช้งานแล้ว คุณสามารถดำเนินการในส่วนถัดไปของเอกสารหรือเริ่มทดสอบการจองได้เลย

---
