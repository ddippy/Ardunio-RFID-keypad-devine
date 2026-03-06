=== Arduino RFID & Keypad Door Lock System 1.0 ===

ระบบล็อกประตูด้วย RFID Card + Keypad Password
ใช้ Arduino ควบคุมการเปิด-ปิดประตูผ่าน Servo พร้อมจอ LCD แสดงสถานะ

// Features

- เปิดประตูด้วย RFID Card
- เปิดประตูด้วย Password จาก Keypad
- เพิ่มรหัสผ่านใหม่ได้
- ลบรหัสผ่านได้
- แสดงรายการรหัสผ่านทั้งหมด
- ลบรหัสผ่านทั้งหมดได้
- บันทึกรหัสผ่านใน EEPROM (ไม่หายเมื่อปิดเครื่อง)
- มี เสียง Buzzer แจ้งสถานะ

// Hardware
- Arduino Uno	1
- RFID RC522 1
- Keypad 4x4 1
- PCF8574 (I2C Expander) 1
- LCD 16x2 I2C 1
- Servo Motor	1 pin 8
- Buzzer 1 pin 3

---------------------------------

// Admin Mode - เข้าโดยพิมพ์ CD000
- ปุ่ม A : Add Password
- ปุ่ม B : Exit
- ปุ่ม # : List Password
- ปุ่ม C : Clear All Password (ลบ Password ทั้งหมดใน EEPROM ยกเว้น Default Password)

// ลบ Password ที่ต้องการ - เข้าโดยพิมพ์ D000
- พิมพ์ได้แค่เลข 0-9
- กด * เพื่อลบ
- กด B เพื่อยกเลิกและกลับหน้าหลัก

---------------------------------

** ข้อจำกัดของระบบ
- รองรับรหัสผ่านสูงสุด 10 รหัส
- ความยาวรหัสผ่าน 6 ตัว
