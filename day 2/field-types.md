| Field turi            | Afzalligi                                                 |
| --------------------- | --------------------------------------------------------- |
| **String**            | Eng ko‘p ishlatiladi, qisqa matnlar uchun ideal           |
| **Text**              | Katta hajmdagi ma’lumotlar uchun qulay                    |
| **Integer / Decimal** | Hisob-kitob, raqamli qiymatlar uchun                      |
| **Boolean**           | Flag (ha/yo‘q) sifatida ishlatiladi                       |
| **Date / DateTime**   | Tizimdagi vaqtni kuzatish uchun zarur                     |
| **Email / URL**       | Avtomatik format tekshiruvi beradi                        |
| **JSON**              | Moslashuvchan, murakkab ma’lumotni bitta ustunda saqlaydi |


| Field Name          | Type            | Validation                                                                             | When to Use                                                             |
| ------------------- | --------------- | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| **text_field**      | String          | Maksimal uzunlik (odatda 255 ta belgi). Harflar, raqamlar, belgilarni kiritish mumkin. | Foydalanuvchi nomi, sarlavha, qisqa ma’lumotlar uchun.                  |
| **long_text_field** | Text            | Belgilar soni cheklanmagan. HTML yoki uzun matnni saqlay oladi.                        | Blog posti, izoh, tavsif (description) kabi uzun matnlar uchun.         |
| **number_field**    | Integer         | Faqat butun sonlar (0, -1, 5, 100).                                                    | Sanash, miqdor, ball, yosh, view soni uchun.                            |
| **decimal_field**   | Decimal / Float | Raqamli format, kasr sonlarni qabul qiladi (masalan 12.50).                            | Narxlar, reytinglar, o‘lchov birliklari uchun.                          |
| **boolean_field**   | Boolean         | Faqat ikki qiymat: `true` yoki `false`.                                                | Faollashtirilganmi, tasdiqlanganmi kabi holatlarni aniqlash uchun.      |
| **date_field**      | Date            | Faqat yil-oy-kun formatidagi sana (YYYY-MM-DD).                                        | Tug‘ilgan sana, post chiqqan sana, deadline uchun.                      |
| **datetime_field**  | DateTime        | Sana + vaqt (YYYY-MM-DD HH:MM:SS).                                                     | Yaratilgan vaqt, tahrirlangan vaqt, login time uchun.                   |
| **email_field**     | Email           | Kiritilgan qiymat email formatida bo‘lishi kerak (`@` belgisi bilan).                  | Foydalanuvchi emaili, kontakt uchun.                                    |
| **url_field**       | URL             | To‘liq veb manzil formatini tekshiradi (`https://...`).                                | Havolalar, rasm manzili, tashqi sayt linklari uchun.                    |
| **json_field**      | JSON            | Faqat JSON formatidagi tuzilma (key-value) qabul qiladi.                               | Qo‘shimcha ma’lumot, konfiguratsiya yoki moslashuvchan struktura uchun. |
