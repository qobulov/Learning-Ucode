## One-to-Many (Bitta → Ko‘p) : Authors → Blog Posts

### Ta’rif
- **Bitta muallif (author)** bir nechta **blog postlar** yozishi mumkin.  
- Har bir **blog post** faqat **bitta muallifga** tegishli bo‘ladi.  
- Bu aloqa `blog_posts` jadvalidagi `author_id` orqali bog‘lanadi.

### Many-to-Many nima?
Bu shunday aloqa turi, unda **bitta obyekt** bir nechta boshqa obyekt bilan bog‘lanadi va **aksincha** — har biri ham bir nechta bilan bog‘lanishi mumkin.  
Masalan, **bitta blog posti**da bir nechta **teg (tag)** bo‘ladi, va bitta **teg** bir nechta **blog postga** tegishli bo‘lishi mumkin.

### Misollar:
1. O‘quvchilar ↔ Kurslar (bitta o‘quvchi bir nechta kursga yoziladi, kursda ko‘p o‘quvchi bo‘ladi)  
2. Film ↔ Aktyorlar (filmda ko‘p aktyor bo‘ladi, aktyor bir nechta filmda o‘ynaydi)

### Nega junction table kerak?
Chunki ma’lumotlar to‘g‘ridan-to‘g‘ri bog‘lanmaydi — ular o‘rtasida **oraliq jadval** (junction table) bo‘lishi kerak, u faqat **ikkala jadvaldagi ID larni** saqlaydi.  
Bu jadval orqali biz bilamiz, qaysi postga qaysi tag biriktirilgan.