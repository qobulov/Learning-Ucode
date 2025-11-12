self-assessment.md

### 1. One-to-Many va Many-to-Many farqi nima?

**One-to-Many:** Bitta yozuv ko‘p yozuvga ega bo'ladi (masalan, bitta muallif → ko`p blog postlar).

**Many-to-Many:** Har ikkala tomon bir-biriga ko`p bog`lanishga ega (masalan, postlar ↔ teglar).

### 2. Nega Many-to-Many uchun junction table kerak?

Chunki har bir post bir nechta tegga ega bo`lishi va har bir teg bir nechta postga tegishli bo`lishi mumkin.

Shuning uchun oraliq jadval (blog_posts_tags) bu bog`lanishni saqlab turadi:

| post_id | tag_id |
| --------+--------|
| 1 | 2 |
| 1 | 3 |
| 2 | 1 |

### 3. Qachon maydon required, qachon optional bo`ladi?

**Required:** Muhim va har doim kerak bo`lgan ma`lumot (masalan, title, author_id)

**Optional:** Ba`zan bo`lishi mumkin, ba`zan yo`q (masalan, published_date, color, category_id)

### 4. Blog postning “featured image” maydoni uchun qaysi field type ishlatiladi?

**String** (agar URL saqlansa)
yoki

**File / Image** (agar haqiqiy fayl sifatida yuklansa)

### 5. Postda bitta asosiy muallif va bir nechta hammualliflar bo`lsa, qanday model qilinadi?

**Asosiy muallif:** author_id (One-to-Many)

**Hammualliflar:** alohida Many-to-Many jadval orqali (post_coauthors)

| blog_post_id | author_id |
| --------------+-----------|
| 1 | 3 |
| 1 | 4 |
