# 🔧 Fundi Chap Chap - Backend API

**Backend ya Fundi Chap Chap - App ya kutafuta mafundi waaminifu Tanzania!**

## 📋 Setup Instructions

### 1. Prerequisites
- Node.js 16+ installed
- Supabase account
- Git

### 2. Installation

```bash
cd backend
npm install
```

### 3. Environment Setup

```bash
cp .env.example .env
```

Edit `.env` na weka Supabase credentials:
```
SUPABASE_URL=your_project_url
SUPABASE_ANON_KEY=your_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
JWT_SECRET=generate_strong_secret_here
```

### 4. Database Setup

1. Go to **Supabase SQL Editor**
2. New Query
3. Copy & paste content ya `database/schema.sql`
4. Run

### 5. Start Server

```bash
npm run dev
```

Server itaanzisha: `http://localhost:3000`

---

## 📚 API Endpoints

### Auth
- `POST /api/auth/signup` - Register
- `POST /api/auth/login` - Login
- `POST /api/auth/logout` - Logout

### Fundi
- `POST /api/fundi/complete-kyc` - Complete KYC
- `GET /api/fundi/profile` - Get profile
- `POST /api/fundi/services` - Add service
- `GET /api/fundi/services` - Get services
- `GET /api/fundi/bookings` - Get bookings
- `POST /api/fundi/bookings/:id/accept` - Accept booking
- `POST /api/fundi/bookings/:id/complete` - Complete booking

### Client
- `GET /api/client/fundi/search` - Search fundi
- `GET /api/client/fundi/:id` - Get fundi details
- `POST /api/client/bookings` - Create booking
- `GET /api/client/bookings` - Get bookings
- `POST /api/client/reviews` - Submit review

### Payments
- `POST /api/payments/initiate` - Start payment
- `POST /api/payments/confirm` - Confirm payment
- `GET /api/payments/history` - Payment history

### Notifications
- `GET /api/notifications` - Get notifications
- `PATCH /api/notifications/:id/read` - Mark as read
- `DELETE /api/notifications/:id` - Delete

---

## 🔐 Authentication

All protected endpoints require JWT token:
```
Authorization: Bearer YOUR_JWT_TOKEN
```

---

## 📱 Frontend Integration (React)

```typescript
const API_BASE_URL = 'http://localhost:3000/api';

const api = axios.create({
  baseURL: API_BASE_URL,
  headers: {
    Authorization: `Bearer ${token}`
  }
});
```

---

## 🚀 Deployment

### Vercel
```bash
npm install -g vercel
vercel
```

### Render
1. Connect GitHub
2. Set environment variables
3. Deploy

---

**Made with ❤️ for Tanzania**
