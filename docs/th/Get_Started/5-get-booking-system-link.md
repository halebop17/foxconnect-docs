---
icon: 
title: 5. รับลิงก์การจองของคุณ
---

# รับลิงก์การจองของคุณ

<iframe width="560" height="315" src="https://www.youtube.com/embed/M1zvIJBgArk?si=Ckwa9AMkYeabiqa-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**วิธีดึง LIFF URL สำหรับระบบการจองของคุณ**

LINE Developers console มีแท็บ "LIFF" เฉพาะสำหรับแต่ละช่องทาง จากแท็บนี้คุณสามารถคัดลอกลิงก์ถาวรที่ลูกค้าจะใช้เพื่อเข้าถึงหน้าจองของคุณ

1. **เข้าสู่ระบบ LINE Developers Console**
    - เปิด `developers.line.biz` และเข้าสู่ระบบด้วยบัญชี LINE ของคุณ
2. **เลือก Provider ที่ถูกต้อง**
    - ในรายการ "Providers" คลิก provider ที่คุณสร้างไว้ก่อนหน้า ซึ่งเป็นที่รวมของช่องทางทั้งหมดของคุณ
3. **เลือกช่องทางที่เกี่ยวข้อง**
    - ภายใน provider นั้น ค้นหาและคลิกช่องทางที่โฮสต์ระบบการจองของคุณ (โดยปกติจะมีเพียงช่องทางเดียว)

    ![LINE LIFF tab](../../assets/images/get-booking-link-1.png)

4. **เปิดแท็บ LIFF**
    - บนหน้าของช่องทาง คลิกแท็บ **LIFF** ส่วนนี้แสดงรายการแอปพลิเคชัน LIFF ทั้งหมดที่เชื่อมกับช่องทาง
5. **คัดลอก LIFF URL**
    - เลื่อนไปยังรายการที่ตรงกับแอปการจองของคุณ
    - คัดลอก **LIFF URL** ที่แสดง ซึ่งเป็นลิงก์ถาวรที่สามารถแชร์ให้ลูกค้าได้
  
    ![LINE LIFF tab](../../assets/images/get-booking-link-2.png)

6. **แชร์ลิงก์**
    - เผยแพร่ URL นี้ผ่านอีเมล เว็บไซต์ หรือช่องทางการสื่อสารอื่น ๆ เมื่อลูกค้าคลิก พวกเขาจะถูกนำไปยังระบบการจองโดยตรงภายในแอป LINE หรือเบราว์เซอร์ภายนอก

> LIFF URL จะตั้งค่าเริ่มต้นเป็น Universal Link ทำให้เปิดได้ทั้งในแอป LINE และเบราว์เซอร์ภายนอก ช่วยให้ผู้ใช้เริ่มต้นการจองได้สะดวกจากทุกที่

**ประเด็นสำคัญ**

- LIFF URL เป็นเอกลักษณ์เฉพาะช่องทางและแอป LIFF ที่คุณสร้างขึ้น  
- สามารถเข้าถึงได้จากแท็บ **LIFF** ใน LINE Developers console ภายใต้ช่องทางที่เลือก  
- การแชร์ลิงก์นี้ช่วยให้ลูกค้าเข้าสู่ระบบการจองได้อย่างราบรื่น

อย่าลืมวาง URL ที่คัดลอกมาในการตั้งค่าช่องทาง Fox Connect ภายใต้ "Line LIFF Booking" เพื่อให้ลูกค้าสามารถเริ่มจองได้โดยตรงจากลิงก์
