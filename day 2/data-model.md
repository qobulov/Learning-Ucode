# Data Model - Blog Platforma

## 📘 Umumiy ma’lumot
Bu ma’lumotlar bazasi blog tizimi uchun mo‘ljallangan bo‘lib, unda **mualliflar (authors)**, **postlar (blog_posts)**, **teglar (tags)**, **kategoriya (categories)** va **izohlar (comments)** o‘zaro bog‘langan.  
Model One-to-Many va Many-to-Many aloqalar orqali tuzilgan.

---

## 🧑‍💻 Jadval va ularning maqsadi

### 1. Authors (Mualliflar)
**Maqsadi:** Blog yozuvlarini yaratgan foydalanuvchilar haqidagi ma’lumotlarni saqlaydi.  
**Asosiy maydonlar:**
- `id`: muallifning noyob identifikatori  
- `first_name`, `last_name`: ism va familiya  
- `email`: yagona (unique) elektron pochta manzili  
- `bio`: qisqa tavsif  
- `active`: muallif faol yoki yo‘qligini bildiradi  

**Aloqa:**
- One-to-Many → `blog_posts`: bitta muallif ko‘p post yozishi mumkin

---

### 2. Blog_Posts (Postlar)
**Maqsadi:** Mualliflar yozgan blog maqolalarini saqlaydi.  
**Asosiy maydonlar:**
- `id`: post identifikatori  
- `title`: sarlavha  
- `content`: maqola matni  
- `views`: ko‘rishlar soni  
- `published`: e’lon qilingan yoki yo‘qligi  
- `published_date`: e’lon qilingan sana  
- `author_id`: postni kim yozganini bildiradi  
- `category_id`: post qaysi kategoriyaga tegishli  

**Aloqa:**
- Many-to-One → `authors`
- Many-to-One → `categories`
- Many-to-Many → `tags` (orqali `blog_posts_tags`)
- One-to-Many → `comments`

---

### 3. Tags 
**Maqsadi:** Blog postlarni mavzularga qarab belgilash uchun ishlatiladi.  
**Asosiy maydonlar:**
- `id`
- `name`: teg nomi (masalan: “Technology”, “Tutorial”)  
- `slug`: URL uchun qisqa nom  
- `color`: ixtiyoriy rang  

**Aloqa:**
- Many-to-Many → `blog_posts` (ko‘p postda bir xil teg bo‘lishi mumkin)

---

### 4. Categories 
**Maqsadi:** Postlarni umumiy yo‘nalish bo‘yicha guruhlash uchun ishlatiladi.  
**Asosiy maydonlar:**
- `id`
- `name`: kategoriya nomi (masalan: “Web Development”)  
- `description`: tavsif  

**Aloqa:**
- One-to-Many → `blog_posts` (bitta kategoriya ichida ko‘p postlar bo‘ladi)

---

### 5. Comments
**Maqsadi:** Foydalanuvchilar yozgan izohlarni saqlaydi.  
**Asosiy maydonlar:**
- `id`
- `blog_post_id`: qaysi postga yozilganini bildiradi  
- `author_name`, `author_email`: izoh egasi ma’lumoti  
- `content`: izoh matni  
- `created_at`: yozilgan vaqt  
- `approved`: tasdiqlangan yoki yo‘qligi  

**Aloqa:**
- Many-to-One → `blog_posts` (bitta postga ko‘p izoh)

---

### 6. Blog_Posts_Tags (Oraliq jadval - Junction Table)
**Maqsadi:** Postlar va teglar orasidagi Many-to-Many aloqani amalga oshiradi.  
**Asosiy maydonlar:**
- `id`
- `blog_post_id`  
- `tag_id`  

**Aloqa:**
- Many-to-One → `blog_posts`
- Many-to-One → `tags`

---
