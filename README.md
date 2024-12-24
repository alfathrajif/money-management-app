# Money Management App

This is a full-stack Money Management application designed to track income and expenses. Built with **Next.js** on the [client-side](https://github.com/alfathrajif/money-management-app-client/tree/c4427e5c8b1fadcd5ca6209ffd174f8ed4ab0c2e) and **NestJS** on the [server-side](https://github.com/alfathrajif/money-management-app-server/tree/cfe13660054d5df5af927ec6fe871dd19f623b9e), the app provides a seamless experience for managing personal finances.

## Features

- **Income & Expense Tracking**: Add, edit, and delete financial transactions with details like amount, category, and date.
- **Chart**: Income and expenses graph per category.
- **User Authentication**: Secure login and user management.
- **Responsive Design**: Optimized for use on both desktop and mobile devices.

## Technologies

- **Frontend**: Next.js (React, TypeScript)
- **Backend**: NestJS (TypeScript, Prisma)
- **Database**: MySQL
- **State Management**: React Context and Zustand
- **Authentication**: JWT, Cookies, etc.

## 📷 Screenshots

![Main Page](https://raw.githubusercontent.com/alfathrajif/money-management-app/refs/heads/main/docs/Expense-Tracker-12-25-2024_02_17_AM.png "Main Page")

---

## Running on Local

### Prerequisites

- Node.js (v14.x or later)
- npm or yarn
- MySQL database
- Environment setup for both Next.js and NestJS projects

### Clone the Repository

You have to clone the client-side and server-side one by one.

```bash
git clone https://github.com/alfathrajif/money-management-app-client.git
```

```bash
git clone https://github.com/alfathrajif/money-management-app-server.git
```

### Set Up Environment Variables

#### Install Frontend Dependencies (Next.js)

1. Navigate to the `client` folder (assumed structure for Next.js project).
2. Create a `.env.development.local` file with the following variables:

```env
NODE_ENV=development
NEXT_PUBLIC_API_URL=<NestJS_API_URL> 
NEXT_PUBLIC_AUTH_COOKIE_NAME=<JWT_SECRET>
```

#### Backend Setup (NestJS)

1. Go to the `server` folder (assumed structure for NestJS project).
2. Create a `.env.development.local` file with the following variables:

```env
DATABASE_URL="mysql://<username>:<password>@<host>:<port>/<database>"
JWT_SECRET=<JWT_SECRET>
PORT=5000
```

Ensure to replace `<username>`, `<password>`, `<host>`, `<port>`, `<database>`, and `<JWT_SECRET>` with your actual MySQL credentials and JWT secret key.

### Install Dependencies

#### Frontend

```bash
cd client
npm install
# or
yarn install
```

#### Backend

```bash
cd .../server
npm install
# or
yarn install
```

### Set Up Database (Prisma)

Run Prisma migrations to create the database tables.

```bash
npm run prisma:migrate:dev
```

Optionally, seed the database if there’s a seed file

```bash
npm run prisma:seed:dev
```

### Run the Application

#### Backend (NestJS)

In the `server` folder, start the backend server in development mode:

```bash
npm run start:dev
# or
yarn start:dev
```

#### Frontend (Next.js)

In the `client` folder, start the frontend app:

```bash
npm run dev
# or
yarn dev
```

### Access the Application

- **Frontend**: Visit `http://localhost:3000`:
- **Backend**: Visit `http://localhost:5000`:

## Additional Notes

- Ensure the database is running and accessible via the credentials in `.env.development.local`
- Both frontend and backend servers should be running concurrently for the application to work as expected.
