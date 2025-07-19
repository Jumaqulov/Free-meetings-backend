# Free-Meetings Backend 🚀

Node.js + **Socket.IO** asosida yozilgan yengil signalizatsiya (signaling) xizmati. U **WebRTC** sesiyalarida brauzerlar o‘rtasidagi to‘g‘ridan-to‘g‘ri (peer-to-peer) aloqa uchun kerakli `offer/answer/ICE` paketlarini uzatadi va foydalanuvchilarni “xona” (room) ga birlashtiradi. Frontend: [https://free-meetings.vercel.app](https://free-meetings.vercel.app).

---

## 📒 Jadval ichidagilar
- [Xususiyatlar](#xususiyatlar)
- [Texnologiyalar](#texnologiyalar)
- [Talablar](#talablar)
- [O‘rnatish](#o‘rnatish)
- [Socket API](#socket-api)
- [Ish jarayoni](#ish-jarayoni)
- [Deploy (Production)](#deploy-production)
- [Hissa qo‘shish](#hissa-qo‘shish)
- [Litsenziya](#litsenziya)

---

## Xususiyatlar

| #   | Funksional imkoniyat                                      |
| --- | --------------------------------------------------------- |
| 1   | **Xona boshqaruvi** – `join-room`, xonaga kirish/chiqish  |
| 2   | **WebRTC signaling** – `signal` orqali offer/answer/ICE   |
| 3   | **Real-time xabarlar** – `user-joined`, `user-left` hodisalari |
| 4   | **CORS** – front domeni bilan aniq ruxsat (`free-meetings.vercel.app`) |
| 5   | **Nodemon** – dev rejimida issiq qayta yuklash            |
| 6   | 100% **TypeScript-siz**: minimal bog‘liqlik, oddiy mustaqil ishga tushirish |

---

## Texnologiyalar

- **Node.js (v18+)**
- **Express 5** – HTTP server sathi
- **Socket.IO v4** – WebSocket / fallback transportlari
- **cors** paketi – CORS sozlamalari
- **nodemon** (dev only) – Hot-reload

---

## Talablar

| Dastur        | Versiya            |
| ------------- | ------------------ |
| Node.js       | **≥ 18.x**         |
| npm (yoki pnpm)| **≥ 9.x**          |

---

## O‘rnatish

```bash
# 1. Reponi klon qiling
git clone https://github.com/your-org/free-meetings-backend.git
cd free-meetings-backend

# 2. Bog‘lamalarni o‘rnating
npm install      # yoki: pnpm install

# 3. Muhit o‘zgaruvchilari (.env)
cp .env.example .env
# .env tarkibi:
# PORT=5000
# CLIENT_ORIGIN=https://free-meetings.vercel.app

# 4. Ishga tushirish
npm run dev      # nodemon bilan (dev)
# yoki
npm start        # production
