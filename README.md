Day 1 — Box Model (Block vs Inline vs Inline-block)
🔑 Qızıl qayda

Inline elementlər mətn axını üçündür, qutu (box) deyil.

Block və inline-block elementlər qutu sayılır.

📌 Inline (display: inline)

Yalnız text / inline content üçün nəzərdə tutulub

width ❌ işləməz

height ❌ işləməz

padding → left/right ✅, top/bottom ⚠️

margin → left/right ✅, top/bottom ❌

Block-level elementləri (div, p, h1–h6) qutu kimi əhatə edə bilməz

Nəticə:
Inline parent daxilində block elementlər varsa, parent “kart” kimi davranmır və background gözlənildiyi kimi görünmür.

📌 Block (display: block)

Həmişə yeni sətirdən başlayır

Tam qutu yaradır

width, height, padding, margin, background → hamısı işləyir

📌 Inline-block (display: inline-block)

Yan-yana düzülür (inline kimi)

Tam qutu yaradır (block kimi)

width, height, padding, margin, background → hamısı işləyir

❓ Niyə display: inline olan div-də background görünmür?

div inline edildikdə, daxilindəki h2, p kimi block elementləri qutu kimi sarıya bilmir

Inline element “container box” yaratmaq üçün nəzərdə tutulmayıb

Buna görə parent-in background/padding-i kart (box) kimi render olunmur

✅ Düzgün yanaşma

Text üçün → inline

Kart / box / component üçün → inline-block və ya block

div-i inline etmək → real layout-larda istifadə olunmamalıdır

🧠 1 cümləlik yekun

Inline element mətn üçündür, qutu deyil; qutu lazım olanda block və ya inline-block istifadə olunmalıdır.
inline text üçün, block\inline-block isə box sayılır. Yəni bir div elementinə display: inline verdikdə onun daxilində block level element-in bir çox xüsussiyyəti sıfırlanır. 
Kodda inline olan div içində 2 dənə block level element var, amma parent yəni div inline olduğu üçün bu elementlər box-a yerləşmir və onların box-modeli 0 olur. 
Buna görədə biz background, width, height padding verdikdə görsənmir. Amma inline olan div-in içində inline element varsa, (span, a və s.) onlara uyğun görünəcək:

<img width="1443" height="392" alt="image" src="https://github.com/user-attachments/assets/0574b539-5975-472b-8d6d-a603e5e69eeb" />
<img width="1924" height="402" alt="image" src="https://github.com/user-attachments/assets/b34d91d3-9ec5-4fb2-8c81-b1e3d6d67aa6" />
Amma div içində inline element olduqda:
<img width="832" height="121" alt="image" src="https://github.com/user-attachments/assets/901c6669-27ae-4f57-ae89-d97918a8029d" />
<img width="1912" height="407" alt="image" src="https://github.com/user-attachments/assets/4e4f8c22-c789-47d7-88fd-413e8bcf2dc1" />
