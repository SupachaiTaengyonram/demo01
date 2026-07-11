# Real E Gurus Prototype — Session Progress

อัปเดตล่าสุด: 11 กรกฎาคม 2026  
ไฟล์หลัก: `index.html`  
รูปแบบงาน: Single-file HTML/CSS/JavaScript prototype

## ภาพรวมงาน

ปรับปรุงเว็บไซต์ Real E Gurus จากแบบอ้างอิง PDF และไฟล์ DOCX ให้รวมทุกหน้าไว้ใน `index.html` เพียงไฟล์เดียว ใช้การนำทางแบบ hash route เช่น `#home`, `#for-sale` และ `#contact` โดยทุกหน้าใช้ Navbar, Footer, สี, typography, card, button และ animation ในแนวทางเดียวกับ Homepage

## หน้าที่รวมอยู่ใน Prototype

- Homepage
- For Sale
- For Rent
- Commercial
- Recently Sold
- Favorites
- Property Detail
- Agent Page
- Developer Page
- Foreign Buyer Page
- About Real E Gurus
- FAQs
- Related Services และหน้ารายละเอียดบริการ
- Contact Us
- User Profile
- Admin Dashboard
- Admin Listings, Add Listing และ Edit Listing
- Admin Users และ Edit User Access

## สิ่งที่ดำเนินการแล้ว

### 1. โครงสร้างเว็บไซต์และดีไซน์

- รวมทุกหน้าเป็น Single-page prototype ภายใน `index.html`
- ปรับดีไซน์ของแต่ละหน้าให้ใช้ระบบสีและ layout เดียวกับ Homepage
- นำรูปภาพจาก `images/homepage/` และ `images/pdf-assets/` มาใช้กับแต่ละ section
- เพิ่ม SVG icon สำหรับเมนู ปุ่ม ข้อมูลอสังหาริมทรัพย์ และ Admin UI
- เพิ่ม responsive layout สำหรับเดสก์ท็อป แท็บเล็ต และมือถือ
- เพิ่ม page fade, hover, dropdown และ button animation

### 2. Navbar และ Dropdown

- รวม Register และ Login เป็นปุ่ม `Register/Login`
- เพิ่ม hover/focus dropdown ให้เมนูหลัก
- แก้ปัญหา dropdown ของช่องค้นหาบน Homepage ถูกซ่อนอยู่ภายในกรอบสีขาว
- เพิ่ม dropdown หมวด FAQ บน Navbar ประกอบด้วย:
  - All Questions
  - Buyer FAQ
  - Foreign Buyer FAQ
  - Developer FAQ
  - Listings FAQ
  - Platform & Account FAQ
  - Payments & Fees FAQ
  - General FAQ
- เพิ่มหมวด `LISTINGS` ใน dropdown ของ For Sale และ For Rent:
  - All Listings
  - Land
  - House
  - Condo
- เมื่อเลือกหมวด Listing ระบบจะกรองการ์ดและเปลี่ยนหัวข้อ/จำนวนรายการให้ตรงกับประเภท
- คงเมนูเดิม Recently Sold, Property Detail และ Commercial ไว้ครบ

### 3. ระบบค้นหา Homepage

- มีแท็บ For Sale, For Rent, Land และ Commercial
- มี dropdown Area, Property Type และ Price
- Dropdown รองรับ hover, focus และ click
- ปุ่ม Search นำทางไปยังหน้ารายการตามแท็บที่เลือก

### 4. FAQs

- ปรับหน้า FAQ ให้มีหน้าตาและการใช้งานแบบเว็บไซต์สมัยใหม่
- เพิ่มช่องค้นหาคำถาม
- เพิ่มปุ่มกรองหมวดหมู่
- เพิ่ม Accordion เปิด/ปิดคำตอบ
- เชื่อมหมวด FAQ จาก Navbar ให้เปิดหมวดที่เลือกโดยตรง

### 5. Authentication, Favorites และ Profile

- Favorites ต้องมีผู้ใช้ Login ก่อนจึงจะเข้าถึงได้
- ผู้ใช้ที่ยังไม่ Login จะเห็นหน้าต่าง Register/Login
- รองรับการจำลอง Register และ Login โดยไม่ต้องใช้ Backend
- Email ที่มีคำว่า `admin` จะจำลองเป็น Admin account
- ตั้งค่าเริ่มต้นเป็น Demo User บทบาท Customer
- เปิด URL `#admin` เพื่อเข้าสู่ Admin Demo และ Admin Dashboard
- สิทธิ์ Admin ถูกเก็บเฉพาะ session ขณะใช้งานหน้ากลุ่ม Admin และจะกลับเป็นผู้ใช้ปกติเมื่อออกสู่หน้าเว็บไซต์ทั่วไป
- เพิ่มปุ่มเพิ่ม/ลบ Favorite บน Property Card
- เพิ่มหน้า User Profile พร้อมแบบฟอร์มแก้ไข Name, Email, Phone และ Location

### 6. Admin Prototype

- เพิ่ม Admin Dashboard พร้อม metric cards, status chart, activity และ graph mockup
- เพิ่ม Admin Listings พร้อม Search, Filter, Pagination, Edit, View และ Delete mockup
- เพิ่มหน้า Add Listing และ Edit Listing
- เพิ่ม Admin Users และหน้า Edit User Access
- ปรับโทนสี Dashboard และส่วนประกอบให้ดูชัดเจนและเป็นระบบมากขึ้น

### 7. การนำทางภายในเว็บไซต์

- ปุ่ม Agent, Developer และ Foreign Buyer CTA เชื่อมไปหน้า Contact Us
- ซ่อนปุ่ม Back/Home เดิมที่ซ้ำในเนื้อหา
- รวมเมนูนำทางด่วนไว้ในปุ่มลอยมุมล่างขวา
- เมื่อ hover หรือคลิกปุ่มลอยจะแสดง:
  - Top
  - Back
  - Home
- ปุ่ม Top เลื่อนกลับไปบนสุดของหน้าแบบ smooth scroll
- เมนูลอยใช้งานได้ทั้งเดสก์ท็อปและมือถือ

### 8. LINE และ Email Mockup

- ปุ่ม Email เปิดหน้าต่าง Email Composer จำลอง
- ฟอร์ม Email มี From, To, Subject และ Message
- เมื่อกด Send จะแสดงข้อความ `Email sent successfully (mockup)`
- ปุ่ม LINE เปิดหน้าติดต่อ LINE จำลองพร้อม QR, LINE ID และปุ่ม Open LINE
- ปุ่ม Open LINE แสดงข้อความจำลองการเปิด Official Account
- เชื่อมปุ่ม Email/LINE จาก:
  - Contact Us
  - Property Detail
  - Related Services
  - Topbar และ Footer
  - Social LINE icon

### 9. Language Selector

- เพิ่ม hover/click dropdown สำหรับเลือก English และภาษาไทย
- ระบบเปลี่ยนข้อความที่กำหนดไว้ใน Navbar, Homepage และส่วน UI หลัก
- ตั้งค่า `lang` ของเอกสารตามภาษาที่เลือก
- เนื้อหาบางหน้าที่ยังเป็นภาษาอังกฤษทั้งหมดจะต้องเพิ่มคำแปลเมื่อพัฒนาเป็น Production

### 10. Logo

- ใช้โลโก้ `images/137118 1.png`
- ตรวจพบว่าไฟล์ต้นฉบับมี canvas ขนาด `1536 × 1024` และมีพื้นที่โปร่งใสรอบโลโก้มาก
- ขยายกรอบแสดงผลเพื่อชดเชยพื้นที่โปร่งใส ทำให้ตัวโลโก้จริงดูใหญ่ขึ้น
- ปรับตำแหน่งโลโก้ให้อยู่กึ่งกลาง Navbar ทั้งแกนแนวตั้งและแนวนอน
- ตรวจวัดแล้วแกนแนวนอนคลาดจากกึ่งกลางประมาณ `0.5px`
- ปรับขนาดแยกสำหรับเดสก์ท็อป แท็บเล็ต และมือถือ
- ตรวจแล้วไม่มี horizontal overflow

### 11. Social Media และ TikTok

- ใช้ไฟล์ icon จากโฟลเดอร์ `images/` สำหรับ:
  - Facebook
  - Instagram
  - LinkedIn
  - YouTube
  - TikTok
  - LINE
- เพิ่ม Social TikTok ทั้ง Topbar และ Footer
- ใช้ไฟล์ `images/tiktok-svgrepo-com.svg`
- เปลี่ยนตัวอักษรโน้ตเพลงใน Video Tour เป็นโลโก้ TikTok จริง
- ปรับพื้นหลังและขอบของ TikTok badge ให้โลโก้สีดำมองเห็นชัด
- แก้ครบทั้ง Homepage และ Property Detail

## การตรวจสอบที่ดำเนินการแล้ว

- ตรวจ JavaScript syntax ด้วย Node.js แล้วผ่าน
- ทดสอบการนำทางด้วย hash route
- ทดสอบ Navbar และ FAQ dropdown
- ทดสอบ For Sale > Land และ For Rent > Condo แล้วกรองรายการถูกต้อง
- ทดสอบ Favorites/Login และ Admin navigation
- ทดสอบ Quick Navigation: Top, Back และ Home
- ทดสอบ Email mockup ตั้งแต่เปิดฟอร์ม กรอกข้อความ และส่ง
- ทดสอบ LINE mockup และปุ่ม Open LINE
- ทดสอบตำแหน่ง Logo บนเดสก์ท็อปและมือถือ
- ทดสอบ TikTok social icon และ TikTok logo ใน Video Tour
- ตรวจ responsive layout และ horizontal overflow

## สถานะที่ยังเป็น Mockup

- ไม่มี Backend หรือ Database
- ข้อมูล Login, Profile, Favorites และ Admin จะไม่ถูกบันทึกถาวรหลัง Reload
- Email และ Contact Form ไม่ได้ส่งข้อความจริง
- LINE ยังไม่ได้เชื่อม Official Account URL จริง
- Social media อื่นยังไม่ได้ใส่ URL บัญชีทางการ
- Video Tour ยังแสดงข้อความ Prototype เมื่อกด ยังไม่ได้เปิดวิดีโอจริง
- Property Listing, ราคา, Agent, Dashboard graph และ Pagination เป็นข้อมูลตัวอย่าง
- Search และ Sort บางส่วนเป็น UI prototype
- QR LINE เป็นภาพจำลอง ไม่ใช่ QR Code ที่สแกนใช้งานจริง

## ไฟล์สำคัญ

- `index.html` — เว็บไซต์ทั้งหมด
- `images/137118 1.png` — โลโก้หลัก
- `images/tiktok-svgrepo-com.svg` — TikTok icon
- `images/2023_Facebook_icon.svg` — Facebook icon
- `images/instagram-icon.svg` — Instagram icon
- `images/linkedin-tile.svg` — LinkedIn icon
- `images/youtube-icon.svg` — YouTube icon
- `images/line-icon.svg` — LINE icon
- `images/homepage/` — รูปภาพ Homepage และ Property Card
- `images/pdf-assets/` — รูปภาพสำหรับหน้าภายในและบริการ

## ขั้นตอนแนะนำก่อนนำขึ้น Production

1. แยก CSS และ JavaScript ออกจาก `index.html` หากเริ่มพัฒนาระบบจริง
2. เชื่อม Backend, Database และระบบ Authentication จริง
3. เปลี่ยนข้อมูล Property และ Admin จาก mock data เป็น API
4. ใส่ URL Social media, LINE Official Account และ Video จริง
5. เชื่อม Email service หรือ Contact API
6. สร้าง QR Code LINE ที่สแกนได้จริง
7. เพิ่มคำแปลให้ครบทุกหน้า
8. เพิ่ม validation, security, SEO และ accessibility audit ก่อนเผยแพร่
