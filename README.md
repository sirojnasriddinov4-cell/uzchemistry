# UzChemistry — 2-bosqich (darslar interfeysi)

Ushbu bosqich 1-bosqichdagi Google orqali kirish, API va PostgreSQL tuzilmasini saqlaydi. Web interfeysiga o'zbek tilidagi kimyo mavzulari katalogi qo'shildi.

## Yangi imkoniyatlar
- 12 ta boshlang'ich kimyo darsi: nazariya, formula, misol va mustaqil mashq.
- Mavzu nomi va tavsifi bo'yicha qidiruv.
- Kategoriya bo'yicha saralash.
- Darsni ochish oynasi va mavzu o'rganilganini belgilash (hozircha brauzer sessiyasida; serverga saqlanmaydi).
- Telefon va kompyuter ekranlariga moslashuvchan interfeys.

## Ishga tushirish
Oldingi 1-bosqich sozlamalari o'z kuchida:

```bash
cp .env.example .env
# .env ichida GOOGLE_CLIENT_ID va JWT_SECRET ni sozlang
echo "VITE_GOOGLE_CLIENT_ID=SIZNING_CLIENT_ID" > apps/web/.env
npm install
docker compose up -d db
npm run migrate -w @uzchemistry/api
npm run dev:api
# ikkinchi terminalda:
npm run dev:web
```

Web: http://localhost:5173
API health: http://localhost:4000/api/health

## Hali bajariladigan ishlar
Bu 2-bosqich prototipi. Darslar hozircha interfeys ichida saqlangan; admin orqali dars qo'shish, progressni bazaga saqlash, testlar, AI API va mobil paketlash keyingi bosqichlarda qilinadi. AI API kalitini frontendga joylamang; u server tomonda saqlanishi kerak.
