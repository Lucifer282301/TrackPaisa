# TrackPaisa 💰

**Every Rupee. Under Control.**

TrackPaisa is a personal finance and expense-tracking application designed to help users manage daily spending, track income, organize transactions, set budgets, and understand their financial habits.

With a simple and intuitive mobile experience, TrackPaisa helps users record expenses, manage multiple wallets, monitor budgets, review financial reports, and generate invoices. It makes managing money easier and helps users develop better financial habits.

## ✨ Features

### Authentication & Onboarding
- User registration and login.
- Secure authentication and session management.
- Personalized user profiles.
- User onboarding and currency preferences.

### Expense & Income Management
- Add, edit, and delete transactions.
- Track daily expenses and income.
- Organize transactions by category.
- Add descriptions, dates, and notes.
- Filter transactions by category, wallet, and date.
- View transaction history.

### Wallet Management
- Create and manage multiple wallets.
- Support cash, bank, credit, and mobile wallets.
- Set a default wallet.
- Monitor wallet balances.

### Budget Management
- Create and manage budgets.
- Monitor spending against budgets.
- Track spending limits.
- Review financial spending patterns.

### Dashboard & Reports
- View total balances.
- Monitor monthly income and expenses.
- Review spending summaries.
- Visualize financial activity.
- Analyze personal spending habits.

### Invoice Management
- Create and manage invoices.
- Add client information and invoice items.
- Update invoice statuses.
- Generate and export invoice PDFs.
- Share invoices.

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Mobile Application | React Native CLI |
| Language | TypeScript |
| Navigation | React Navigation |
| Backend Runtime | Bun |
| Backend Framework | Hono |
| Authentication | Better Auth |
| Database | PostgreSQL |
| ORM | Drizzle ORM |
| Validation | Zod |
| API Communication | Hono RPC |
| Data Fetching | TanStack Query |
| Forms | React Hook Form |
| UI | React Native |
| Monorepo | Turborepo |

## 🏗️ Project Architecture

TrackPaisa follows a modular monorepo architecture with separate mobile and backend applications.

```text
mobile/
├── android/
├── ios/
├── src/
│   ├── app/
│   ├── components/
│   ├── navigation/
│   ├── features/
│   │   ├── auth/
│   │   ├── dashboard/
│   │   ├── wallets/
│   │   ├── transactions/
│   │   ├── budgets/
│   │   ├── reports/
│   │   ├── invoices/
│   │   └── profile/
│   ├── services/
│   ├── hooks/
│   ├── store/
│   ├── theme/
│   ├── utils/
│   └── types/
├── .github/workflows/
├── package.json
└── README.md

backend/
├── src/
│   ├── config/
│   ├── database/
│   ├── modules/
│   │   ├── auth/
│   │   ├── users/
│   │   ├── wallets/
│   │   ├── categories/
│   │   ├── transactions/
│   │   ├── budgets/
│   │   ├── reports/
│   │   ├── invoices/
│   │   └── notifications/
│   ├── middleware/
│   ├── common/
│   ├── routes/
│   ├── utils/
│   ├── app.ts
│   └── server.ts
├── prisma/
│   ├── schema.prisma
│   └── migrations/
├── tests/
├── .github/workflows/
├── package.json
└── README.md
```

## ⚙️ Prerequisites

Install the following tools before starting development:

- Node.js
- Bun 1.2.19 or newer
- PostgreSQL
- Git
- Android Studio and Android SDK
- Java Development Kit (JDK)
- Xcode (for iOS development on macOS)
- React Native CLI development environment

React Native environment setup: https://reactnative.dev/docs/set-up-your-environment

## 🚀 Installation & Setup

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd trackpaisa
```

### 2. Install dependencies

```bash
bun install
```

### 3. Configure environment variables

Create `apps/server/.env`:

```env
DATABASE_URL=postgresql://postgres:postgres@localhost:5432/trackpaisa

BETTER_AUTH_SECRET=your-secret-key-at-least-32-characters-long

BETTER_AUTH_URL=http://localhost:3000

CORS_ORIGIN=http://localhost:8081

NODE_ENV=development
```

Configure the mobile API base URL in your React Native environment configuration.

For example:

```env
API_BASE_URL=http://localhost:3000
```

For a physical Android device, use your development machine's LAN IP address instead of localhost.

### 4. Create the database

```sql
CREATE DATABASE trackpaisa;
```

Push the database schema:

```bash
bun run db:push
```

### 5. Start the backend

```bash
bun run dev:server
```

### 6. Start Metro

From the mobile application directory:

```bash
cd apps/mobile
bun start
```

### 7. Run the Android application

```bash
bun run android
```

Or run directly through React Native CLI:

```bash
npx react-native run-android
```

### 8. Run the iOS application

On macOS:

```bash
cd apps/mobile/ios
pod install
cd ..
npx react-native run-ios
```

### 9. Type checking

From the project root:

```bash
bun run check-types
```

## 🔐 Authentication

TrackPaisa uses Better Auth for authentication and session management.

- Email and password authentication.
- Secure session handling.
- PostgreSQL-backed authentication.
- Authenticated API requests.
- Server-side session validation.

**Note:** Bare React Native does not automatically provide Expo authentication storage or Expo-specific integrations. Authentication storage and native integrations must be configured for the React Native CLI environment.

## 🔌 API Endpoints

| Endpoint | Description |
|---|---|
| `/api/auth/*` | Authentication |
| `/api/category` | Category management |
| `/api/wallet` | Wallet management |
| `/api/budget` | Budget management |
| `/api/transaction` | Transaction management |
| `/api/invoice` | Invoice management |
| `/api/notification` | Notifications |

## 🔄 Application Workflow

1. Register or sign in.
2. Complete user onboarding.
3. Create wallets.
4. Set up income and expense categories.
5. Record daily transactions.
6. Create and monitor budgets.
7. Review financial reports.
8. Create and export invoices.

## 🧑‍💻 Development Guidelines

- Follow modular architecture.
- Maintain separation between frontend and backend.
- Use TypeScript throughout the project.
- Build reusable React Native components.
- Keep business logic separate from UI components.
- Use shared schemas for request validation.
- Follow consistent naming conventions.
- Implement centralized error handling.
- Keep environment variables secure.
- Write maintainable and scalable code.

## 🗺️ Future Improvements

- AI-powered expense categorization.
- Receipt scanning and automatic transaction extraction.
- Smart spending insights.
- Recurring expense tracking.
- Budget alerts and notifications.
- Advanced financial analytics.
- CSV and Excel exports.
- Multi-currency support.

These are potential future enhancements, not necessarily implemented features.

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch.
3. Install dependencies.
4. Configure the development environment.
5. Implement your changes.
6. Run type checks.
7. Submit a pull request.

## 📄 License

No license has been added yet. Until a license is provided, all rights are reserved.

---

<p align="center">

**TrackPaisa**

*Every Rupee. Under Control.*

Made with ❤️ for smarter money management.

</p>
