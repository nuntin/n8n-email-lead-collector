# Troubleshooting Guide — Email Lead Collector (n8n)

## ❓ Workflow ไม่รันต่อหลัง Request Website
**สาเหตุ:** เว็บไม่มีเนื้อหาหรือไม่คืนค่า HTML

**วิธีแก้:** เปิด Settings → ✅ Always Output Data

---

## ❓ Error: "This node is not currently installed"
**สาเหตุ:** ใช้ Node ที่ไม่รองรับกับ n8n เวอร์ชันปัจจุบัน

**วิธีแก้:** ใช้ Node แบบมาตรฐานเท่านั้น เช่น Function Node แทน Extract Email / Convert CSV

---

## ❓ Save File: "ENOENT: no such file or directory"
**สาเหตุ:** โฟลเดอร์ `/data/` ไม่อยู่ในระบบ

**วิธีแก้:** แก้ path เป็น `./emails.csv` และรันใน n8n desktop / docker ที่ให้สิทธิ์ save

---

## 🧪 Test URLs แนะนำ
