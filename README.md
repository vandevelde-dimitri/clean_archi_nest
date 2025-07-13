# 🐺 Nest Clean Architecture Template

A starter project for building scalable and maintainable [NestJS](https://nestjs.com/) applications using **Clean Architecture** principles.

---

## 🚀 Getting Started

To create a new project based on this template, run:

```bash
git clone https://github.com/vandevelde-dimitri/clean_archi_nest.git
```

This will automatically clone the template into a new directory named my-app and install all dependencies.

---

## 📦 Features

- 🐾 Clean and modular folder structure
- 🌲 Separation of concerns via Domain, Application, Infrastructure, and Interface layers
- 🔗 Ready for Dependency Injection and SOLID principles
- ✨ Minimal, unopinionated starting point
- 🦊 ESLint + Prettier setup with custom rules included
- 🐘 Prisma setup for easy database integration

---

## 🛠️ Tech Stack

🐺 NestJS
🦊 TypeScript
⚡ ESLint
📝 Prettier
🐘 Prisma for database management

---

## 🗂️ Project Structure

```
src/
├── application/                        # Use cases (business logic orchestration)
│   └── use-cases/
├── controllers/                        # Interface layer (e.g. HTTP entrypoints)
├── domain/                             # Core domain logic
│   ├── entities/
│   ├── repositories/                   # Abstract interfaces
│   └── services/
├── infrastructure/                     # Implementations (DB, external APIs, etc.)
│   ├── services/
│   └── repositories/
│       └── prisma
│            └── .config
│                ├── schema.prisma
│                └── migrations
├── shared/                             # Common mappers, DTOs, and utilities
│   ├── dtos/
│   └── mappers/
├── app.module.ts                       # Root module
├── main.ts                             # App bootstrap
│.env.example                           # Environment config sample
```

---

## 🐘 Prisma Setup

This template includes Prisma for database interaction. After creating your project, follow these steps:

1. Set up your database by configuring the `DATABASE_URL` in the `.env` file.
2. Run the following command to generate Prisma client:

```bash
npx prisma generate
```

3. If you need to run database migrations, use the following command:

```bash
npx prisma migrate dev --name init
```

4. Now, you can use Prisma in your application to interact with your database!

To start your project, run:

```bash
npm run start:dev
```

## 🧠 Clean Architecture Overview

This template is inspired by Robert C. Martin (Uncle Bob)'s Clean Architecture principles.

The goal is to:

Isolate business logic (domain + use cases)
Keep infrastructure replaceable (DB, HTTP, etc.)
Promote testability and scalability

## 📄 License

MIT – feel free to use and modify!
