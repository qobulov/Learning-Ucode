### 1. One-to-Many va Many-to-Many qachon ishlatiladi?

**One-to-Many (One-to-Many):** Bitta yozuv ko‘p marta bog‘langan yozuvlarga ega bo‘lsa (masalan, bitta muallif → ko`p blog postlar).

**Many-to-Many (Many-to-Many):** Har ikkala tomon ham bir nechta bog`langanishga ega bo`lsa (masalan, postlar ↔ teglar — bitta postda ko`p teg bo`ladi, va bitta teg ko`p postga tegishli bo`ladi).

#### 2. Jadval nomlarini qanday berish kerak (singular yoki plural)?

Eng yaxshi amaliyot — ko‘plikda (plural) yozish:

✅ authors, blog_posts, categories, tags

Chunki jadval ichida ko‘p yozuvlar bo‘ladi, va bu nomlashni intuitiv qiladi.

### 3. Qachon alohida jadval yaratish, qachon maydon qo'shish kerak?

Agar qiymatlar takrorlanib ko'p joyda ishlatilsa — alohida jadval yaratiladi.
Masalan: categories, tags.

Agar qiymat faqat bitta ob'ektga xos bo'lsa — maydon sifatida qo'shiladi.
Masalan: title, views, published_date.

### 4. Ixtiyoriy (optional) bog'lanishlar bilan qanday ishlash kerak?

Agar ma'lumot doim mavjud bo'lmasligi mumkin bo'lsa (masalan, category hali tanlanmagan),
u holda NULL ruxsat etiladi yoki optional belgilanadi.

Bu foydalanuvchiga ma'lumotni keyinroq to'ldirish imkonini beradi.

### 5. Yaxshi Primary Key qanday bo'ladi?

Har bir yozuvni noyob identifikatsiya qiluvchi maydon bo'lishi kerak.

Tavsiya etiladi:

id — UUID yoki AUTO_INCREMENT

O'zgarmas, qisqa, va takrorlanmaydigan qiymat

Masalan: id uuid yoki id serial
