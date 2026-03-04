
# next-expo-monorepo

Monorepo setup for **Next.js + Expo (React Native Web)** applications, managed with **pnpm**.

Created from `npx create-turbo@latest -e with-react-native-web`.
Fixed the `@types/minimatch` issue by installing `minimatch` and added custom packages.

---

## Packages

This monorepo includes the following packages:

- **ui** – Custom React/React Native components and design system.
- **typescript-config** – Centralized TypeScript configuration for all apps and packages.
- **constants** – Shared constants across apps and packages.
- **hooks** – Custom React hooks for reusable logic.
- **storage** – Zustand-based state management and storage utilities.
- **types** – Shared TypeScript types.

---

## Installation & Development

Install dependencies and start development servers:

```bash
pnpm i
pnpm run dev
```


## Build

To build the apps: `pnpm run build`

## Struckture

---
## Monorepo Structure

```text
next-expo-monorepo/
├─ apps/
│  ├─ web/         # Next.js app
│  └─ mobile/      # Expo / React Native app
├─ packages/
│  ├─ ui/          # Custom React / React Native components
│  ├─ hooks/       # Custom React hooks
│  ├─ types/       # Shared TypeScript types
│  ├─ constants/   # Shared constants
│  ├─ storage/     # Zustand storage and state management
│  └─ typescript-config/ # Central TS config
├─ pnpm-workspace.yaml
└─ package.json
---
---

## Path Aliases (TypeScript)

This monorepo uses central path aliases for easier imports:

```
import { Button } from '@ui/Button';
import { useAuth } from '@hooks/useAuth';
import { API_URL } from '@constants/api';
import { UserType } from '@types/user';
import { useStore } from '@storage/store';
```
