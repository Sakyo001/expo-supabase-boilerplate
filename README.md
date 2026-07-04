# Expo Supabase Starter

A clean, production-ready starter for building mobile applications with **Expo**, **React Native**, and **Supabase**.

> Built with scalability, maintainability, and developer experience in mind.

---

## ✨ Features

- ⚡ Expo SDK 57
- 📱 React Native
- 🧭 Expo Router
- 🔐 Supabase Authentication
- 🗄️ Supabase Database
- 🔄 TanStack Query
- 🐻 Zustand
- 📝 React Hook Form
- ✅ Zod Validation
- 🎨 NativeWind
- 💾 MMKV Storage
- 🔒 Expo SecureStore
- 🌙 Dark Mode Ready
- 🧩 Feature-Based Architecture
- 📦 TypeScript
- 🚀 Production Ready

---

# Tech Stack

| Technology | Purpose |
|------------|---------|
| Expo | React Native Framework |
| Expo Router | File-based Routing |
| TypeScript | Type Safety |
| Supabase | Backend & Authentication |
| TanStack Query | Server State |
| Zustand | Global State |
| React Hook Form | Forms |
| Zod | Validation |
| NativeWind | Styling |
| MMKV | Local Storage |
| SecureStore | Secure Token Storage |

---

# Project Structure

```text
app/
├── (auth)/
├── (tabs)/
├── (onboarding)/
├── (modals)/
├── _layout.tsx
├── +not-found.tsx
└── index.tsx

assets/
├── fonts/
├── icons/
└── images/

src/
├── components/
├── config/
├── constants/
├── features/
├── hooks/
├── lib/
├── providers/
├── services/
├── store/
├── theme/
├── types/
├── utils/
└── validation/

supabase/
├── functions/
├── migrations/
├── config.toml
└── seed.sql
```

---

# Getting Started

## 1. Clone the repository

```bash
git clone https://github.com/yourusername/expo-supabase-starter.git

cd expo-supabase-starter
```

## 2. Install dependencies

```bash
npm install
```

or

```bash
yarn
```

or

```bash
pnpm install
```

---

## 3. Configure Environment Variables

Create a `.env` file.

```env
EXPO_PUBLIC_SUPABASE_URL=

EXPO_PUBLIC_SUPABASE_ANON_KEY=
```

---

## 4. Start the project

```bash
npx expo start
```

---

# Folder Guide

## app/

Contains all routes managed by Expo Router.

```text
(auth)         Authentication screens

(tabs)         Main application

(onboarding)   First-time user flow

(modals)       Modal screens
```

---

## src/features

Each feature owns its own business logic.

Example:

```text
profile/
├── components/
├── hooks/
├── services/
├── types/
└── index.ts
```

---

## src/components

Reusable UI components.

Example:

```text
Button

Input

Card

Avatar

Loader
```

---

## src/services

Application services.

```text
auth.ts

profile.ts

storage.ts
```

No screen should directly communicate with Supabase.

---

## src/store

Application state using Zustand.

Example:

```text
auth.ts

app.ts
```

---

## src/lib

Application configuration.

```text
supabase.ts

query-client.ts

env.ts
```

---

# Authentication

Supports:

- Email & Password
- Magic Link
- Google OAuth
- Apple Sign In (optional)

Authentication is handled by Supabase Auth.

---

# State Management

## Server State

TanStack Query

Used for:

- Profiles
- Posts
- Notifications
- Messages

---

## Client State

Zustand

Used for:

- User session
- Theme
- Preferences

---

# Styling

NativeWind

Example:

```tsx
<View className="flex-1 items-center justify-center">
    <Text>Hello World</Text>
</View>
```

---

# Database

Supabase

Recommended:

- Enable Row Level Security (RLS)
- Use Migrations
- Never expose service role keys

---

# Scripts

```bash
npm run start

npm run android

npm run ios

npm run web

npm run lint

npm run typecheck

npm run test
```

---

# Production Checklist

- [ ] Configure Supabase Authentication
- [ ] Enable Row Level Security
- [ ] Configure Deep Linking
- [ ] Configure Push Notifications
- [ ] Configure Error Monitoring
- [ ] Configure Analytics
- [ ] Configure EAS Build
- [ ] Configure EAS Update

---

# Recommended Packages

- Expo Router
- Supabase
- TanStack Query
- Zustand
- NativeWind
- React Hook Form
- Zod
- MMKV
- SecureStore
- Reanimated

---

## Architecture

For a detailed overview of the project structure and application flow, see:

📖 **[Architecture Guide](docs/architecture.md)**

## Contributing

Contributions are always welcome!

Please read **[CONTRIBUTING.md](CONTRIBUTING.md)** before opening an issue or submitting a pull request.



# License

MIT License.