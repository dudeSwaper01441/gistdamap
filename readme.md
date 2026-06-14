# 🗺️ GISTDA Map — Geohackathon 2025

> แผนที่เชิงโต้ตอบสำหรับแสดงข้อมูลภูมิสารสนเทศของประเทศไทย  
> พัฒนาด้วย **GISTDA Sphere Map API** สำหรับการแข่งขัน **GISTDA Geohackathon 2025**

---

## 🌐 Tech Stack

| Layer | เทคโนโลยี |
|-------|-----------|
| Map Engine | [GISTDA Sphere Map API](https://sphere.gistda.or.th) |
| Backend / Server | Node.js + Express 5 |
| Frontend | HTML5 / Vanilla JavaScript |
| Map Data | GISTDA Sphere (แผนที่ประเทศไทยความละเอียดสูง) |

---

## ✨ ฟีเจอร์

- 🗺️ **Fullscreen Interactive Map** — แผนที่ GISTDA Sphere ครอบคลุมทั่วประเทศไทย
- 🏫 **University Tag Layer** — แสดง Tag Label "มหาวิทยาลัย" บนแผนที่โดยอัตโนมัติ
- ⚡ **Renderer-ready Loading** — โหลด Layer หลัง Map Renderer พร้อมทำงานเพื่อป้องกัน Race Condition
- 📦 **Minimal Dependencies** — ใช้ Express เพียงตัวเดียวสำหรับ Static File Serving

---

## 🚀 วิธีติดตั้งและรันโปรเจกต์

### Prerequisites
- Node.js (v16 ขึ้นไป)
- GISTDA Sphere API Key — ขอได้ที่ [sphere.gistda.or.th](https://sphere.gistda.or.th)

### ขั้นตอน

```bash
# 1. Clone repository
git clone https://github.com/dudeSwaper01441/gistdamap.git
cd gistdamap

# 2. ติดตั้ง dependencies
npm install

# 3. รัน server
node index.js

# 4. เปิดเบราว์เซอร์
# http://localhost:3000
```

---

## 🔑 การตั้งค่า API Key

ใน `index.html` บรรทัดที่โหลด Sphere SDK:

```html
<script src="https://api.sphere.gistda.or.th/map/?key=YOUR_API_KEY_HERE"></script>
```

แทนที่ `YOUR_API_KEY_HERE` ด้วย API Key ของคุณ

> ⚠️ **หมายเหตุ:** อย่า Commit API Key จริงขึ้น GitHub  
> แนะนำให้ใช้ Environment Variable หรือ `.env` file แทน

---

## 📁 โครงสร้างไฟล์

```
gistdamap/
├── index.html        # Frontend — Sphere Map + Tag Layer
├── index.js          # Backend — Express Static File Server
├── package.json      # Node.js dependencies
└── readme.md         # ไฟล์นี้
```

---

## 🗺️ เกี่ยวกับ GISTDA Sphere Map API

**GISTDA Sphere** คือแพลตฟอร์มแผนที่ภูมิสารสนเทศของ **สำนักงานพัฒนาเทคโนโลยีอวกาศและภูมิสารสนเทศ (องค์การมหาชน)** หรือ GISTDA ประเทศไทย

ความสามารถหลักของ API ที่ใช้ในโปรเจกต์นี้:

| Feature | การใช้งาน |
|---------|-----------|
| `sphere.Map` | สร้าง Interactive Map เต็มหน้าจอ |
| `map.Renderer.on('load')` | รอ Renderer พร้อมก่อนเพิ่ม Layer |
| `map.Tags.set()` | แสดง Tag Label บนแผนที่ตาม Category |

📖 เอกสาร API เพิ่มเติม: [sphere.gistda.or.th/docs](https://sphere.gistda.or.th/docs/)

---

## 🏆 บริบทการพัฒนา

โปรเจกต์นี้พัฒนาขึ้นสำหรับ **GISTDA Geohackathon 2025** ซึ่งเป็นการแข่งขัน Hackathon ด้านภูมิสารสนเทศของประเทศไทย โดยมีเป้าหมายในการประยุกต์ใช้ข้อมูลและเครื่องมือเชิงภูมิสารสนเทศเพื่อแก้ปัญหาสังคมและสิ่งแวดล้อม

---

## 📄 License

โปรเจกต์นี้พัฒนาเพื่อการศึกษาและการแข่งขัน  
ข้อมูลแผนที่อยู่ภายใต้ข้อกำหนดการใช้งานของ [GISTDA Sphere Terms of Service](https://sphere.gistda.or.th/terms)

---

Made with ❤️ by **dudeSwaper01441** · GISTDA Geohackathon 2025
