# Contributing

First off, thank you for considering contributing to Expo Supabase Boilerplate! 🎉

Whether you're fixing bugs, improving documentation, suggesting new features, or submitting code, your contributions are greatly appreciated.

---

# Before You Start

Please:

- Search existing issues before opening a new one.
- Keep pull requests focused on a single feature or fix.
- Be respectful and constructive.

---

# Development Setup

## 1. Fork the repository

Click the **Fork** button on GitHub.

## 2. Clone your fork

```bash
git clone https://github.com/Sakyo001/expo-supabase-boilerplate.git

cd expo-supabase-boilerplate
```

## 3. Install dependencies

```bash
npm install
```

## 4. Configure environment variables

Create a `.env` file.

```env
EXPO_PUBLIC_SUPABASE_URL=

EXPO_PUBLIC_SUPABASE_ANON_KEY=
```

## 5. Start the project

```bash
npm start
```

---

# Project Structure

```
app/            Expo Router screens
src/components  Shared UI components
src/features    Feature modules
src/services    Business logic
src/store       Zustand stores
src/lib         Supabase & shared libraries
supabase/       Database migrations
```

---

# Branch Naming

Please use descriptive branch names.

Examples:

```
feature/social-auth

feature/dark-mode

fix/login-validation

docs/readme-update

refactor/auth-provider
```

---

# Commit Messages

Use clear commit messages.

Examples:

```
feat: add Google authentication

fix: resolve login redirect issue

docs: improve README

refactor: simplify auth provider

chore: update dependencies
```

---

# Pull Requests

Before opening a PR, ensure:

- [ ] The project builds successfully
- [ ] TypeScript has no errors
- [ ] ESLint passes
- [ ] Existing tests pass
- [ ] Documentation is updated (if needed)

---

# Coding Guidelines

- Prefer TypeScript over JavaScript.
- Keep components small and reusable.
- Follow the existing folder structure.
- Avoid unnecessary dependencies.
- Write readable and maintainable code.

---

# Reporting Bugs

Please include:

- Expected behavior
- Actual behavior
- Steps to reproduce
- Device / Platform
- Expo SDK version

---

# Feature Requests

When proposing a feature:

- Explain the use case.
- Describe the expected behavior.
- Consider whether it fits the project's goals.

---

# Ways to Contribute

You don't have to write code!

You can also help by:

- Improving documentation
- Fixing typos
- Suggesting better architecture
- Reporting bugs
- Reviewing pull requests
- Sharing the project

---

# Questions?

Feel free to open a GitHub Discussion or create an Issue.

Thanks for helping improve Expo Supabase Boilerplate! 🚀