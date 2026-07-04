# Architecture

The project follows a **feature-based architecture** while separating navigation, business logic, and reusable UI.

```text
expo-supabase-boilerplate
│
├── app/
│   │
│   ├── (auth)
│   ├── (tabs)
│   ├── (onboarding)
│   ├── (modals)
│   │
│   ├── _layout.tsx
│   └── +not-found.tsx
│
├── src/
│   │
│   ├── components/
│   │     Shared UI components
│   │
│   ├── features/
│   │     Business features
│   │
│   ├── services/
│   │     Business logic
│   │
│   ├── lib/
│   │     Supabase, Query Client, Environment
│   │
│   ├── store/
│   │     Zustand stores
│   │
│   ├── hooks/
│   │
│   ├── providers/
│   │
│   ├── theme/
│   │
│   ├── utils/
│   │
│   └── constants/
│
└── supabase/
    │
    ├── migrations/
    └── functions/
```

---

# Application Flow

```text
                User
                  │
                  ▼
          Expo Router (app/)
                  │
                  ▼
          Screen Components
                  │
                  ▼
        Feature Business Logic
                  │
                  ▼
          Service Layer
                  │
                  ▼
      Supabase Client (lib/)
                  │
                  ▼
             Supabase API
```

---

# State Management

```
                 UI
                  │
     ┌────────────┴────────────┐
     │                         │
     ▼                         ▼
Zustand                 TanStack Query
(Client State)          (Server State)

Theme                   Profiles
Session                 Posts
Settings                Notifications
```

---

# Authentication Flow

```text
App Launch
     │
     ▼
Restore Session
     │
     ▼
Authenticated?
     │
 ┌───┴────┐
 │        │
 ▼        ▼
Yes       No
 │         │
 ▼         ▼
Tabs      Login
```

---

# Layer Responsibilities

## app/

Navigation only.

Avoid placing business logic here.

---

## features/

Each feature owns its own:

- Components
- Hooks
- Services
- Types

---

## services/

Responsible for:

- Database operations
- Authentication
- Storage
- External APIs

Screens should **never** communicate directly with Supabase.

---

## lib/

Contains shared infrastructure.

Examples:

- Supabase client
- Query Client
- Environment configuration

---

## store/

Stores global client state.

Do **not** store API responses here.

Use TanStack Query for server state.

---

# Design Principles

- Feature-first architecture
- Separation of concerns
- Reusable UI components
- Strong typing with TypeScript
- Scalable folder organization
- Simple over clever
- Minimal dependencies
- Production-ready defaults