# Rizo Market — Mini Marketplace + AI

Foydalanuvchilar mahsulotlarni ko‘rishi, qidirishi va savatchaga qo‘shishi mumkin bo‘lgan web-platforma. AI yordamchi mahsulot tanlashda faqat katalogdagi ma’lumotlarga tayanib maslahat beradi.

**Sayt havolasi:** _(Vercel havolasini shu yerga qo‘ying)_

## Imkoniyatlar
- Bosh sahifa: tavsiya etilgan takliflar, kategoriyalar, eng yuqori baholanganlar
- Katalog: 58 ta mahsulot, 8 ta kategoriya (rasm, nom, narx, qisqa tavsif)
- Qidiruv va filtr: nom, kategoriya, narx, reyting bo‘yicha; saralash
- Mahsulot sahifasi: batafsil tavsif, narx, miqdor, savatchaga qo‘shish, sharhlar
- Savatcha: miqdorni o‘zgartirish, umumiy summa, promokod (`RIZO10`)
- Buyurtma: ism, telefon, manzil, to‘lov usuli, tasdiqlash
- AI yordamchi: oddiy tilda savol ("500 ming so‘mgacha sovg‘a"), javobda mahsulot nomi, narxi va nima uchun mosligi; katalogda yo‘q narsani o‘ylab topmaydi
- Qo‘shimcha: ro‘yxatdan o‘tish/kirish, profil, sevimlilar, taqqoslash, sotuvchi bo‘limi, qorong‘i/yorug‘ rejim

## Texnologiyalar
- Frontend: HTML, CSS, JavaScript (bitta fayl, kutubxonasiz)
- Ma’lumotlar bazasi va autentifikatsiya: Supabase
- AI: Gemini API, `api/chat.js` serverless funksiyasi orqali
- Joylashtirish: Vercel
- Vibe coding: Claude yordamida kod yaratildi va xatolar tuzatildi

## AI xavfsizligi
API kaliti frontend kodida **yo‘q**. U faqat serverda `GEMINI_API_KEY` muhit o‘zgaruvchisida saqlanadi. `/api/chat` ishlamasa, sayt katalog asosidagi zaxira mantiqqa o‘tadi.

## Ishga tushirish
1. Repozitoriyani Vercel'ga import qiling.
2. Environment Variables qo‘shing: `GEMINI_API_KEY`, `SUPABASE_ANON_KEY`.
3. Deploy qiling.

## Tuzilma
```
index.html     — butun frontend
api/chat.js    — AI maslahatchi (server tomoni)
```

## Rivojlantirish rejasi
Haqiqiy to‘lov tizimlari (Click, Payme), buyurtma holatini serverda yuritish, mahsulot rasmlarini Supabase Storage'ga ko‘chirish, ko‘p tillilik.
