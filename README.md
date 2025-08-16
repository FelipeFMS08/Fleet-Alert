![Logo do projeto](./web/public/logo.png)

## FleetAlert: Fleet Management System with Geofencing Technology
This repository contains the source code for FleetAlert, a comprehensive fleet management system developed as a Final Project for the Analysis and Systems Development undergraduate course.

The main goal of this project is to provide an effective and integrated solution for companies to monitor and manage their vehicle fleets in real-time, leveraging geofencing technology to enhance security and operational efficiency.

### Table of Contents
- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Repository Structure](#repository-structure)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
- [Authors](#authors)

<a id="about-the-project"></a>
### About the Project
FleetAlert is designed to address the challenges faced by transportation and logistics companies. By defining virtual geographic boundaries (geofences), the system allows managers to receive automatic alerts when a vehicle enters or exits a designated area, ensuring routes are followed correctly and preventing unauthorized usage. The platform provides a complete overview of the fleet's performance through a web dashboard, while drivers use a mobile application to follow their assigned routes.

<a id="key-features"></a>
### Key Features
- Real-Time Vehicle Tracking: Monitor the exact location of all vehicles in real-time on an interactive map.
- Geofencing: Create custom virtual perimeters and receive instant alerts for any boundary violations.
- Route Management: Define, assign, and monitor vehicle routes from start to finish.
- User & Vehicle Management: Easily add, update, and manage drivers, managers, and vehicles in the system.
- Role-Based Access Control (RBAC): Three levels of access (Admin, Manager, and Member) to ensure users only see relevant information.
- Detailed Reports: Generate and export performance reports in PDF format to analyze fleet efficiency and operational costs.
- Secure Authentication: User authentication is handled securely using JSON Web Tokens (JWT) and password hashing with bcrypt.

<a id="repository-structure"></a>
### Repository Structure
This repository is a monorepo containing three distinct projects:

| Project   | Description                                                                                                                              |
| :-------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| **`/web`**| The main dashboard for fleet managers. Built with Next.js, it's where users can manage vehicles, drivers, routes, and view analytics.      |
| **`/server`** | The backend API that powers both the web and mobile applications. It handles business logic, database interactions, and real-time communication. |
| **`/mobile`** | The React Native application for drivers. It allows them to view assigned routes and its location is tracked to be monitored by managers. |

<a id="technology-stack"></a>
### Technology Stack
This project was built using a modern and robust stack to ensure scalability, performance, and a great user experience.

#### Web (Client)
- Framework: Next.js
- Language: TypeScript
- Styling: Tailwind CSS
- Mapping: React-Leaflet & Leaflet
- Charts: Recharts & Chart.js
- Authentication: NextAuth.js
- Real-time Communication: Socket.IO Client
- Schema Validation: Zod
- PDF Generation: React-PDF

#### Server (Backend)
- Framework: Express.js
- Language: TypeScript
- ORM: Prisma
- Authentication: JSON Web Token (JWT) & Bcrypt
- Real-time Communication: Socket.IO
- Security & Hashing: Crypto-JS
- Email Service: Nodemailer
- Core Logic: Geofencing algorithms

#### Mobile (Client)
- Framework: React Native (with Expo)
- Language: TypeScript
- TTP Client: Axios
- Mapping: React Native Maps
- Location Services: Expo Location
- Real-time Communication: Socket.IO Client
- Authentication: JWT Management

#### Database
- Database: PostgreSQL

<a id="getting-started"></a>
### Getting Started
To get a local copy up and running, please follow these simple steps.

#### Prerequisites
- Node.js (v18 or later)
- npm / yarn / pnpm
- A running instance of PostgreSQL
- Expo CLI (for the mobile project)

#### Installation
1. #### Clone the repository:
```sh
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

2. #### Setup the Server:
```sh
# Navigate to the server directory
cd server

# Install dependencies
npm install

# Create a .env file from the example
cp .env.example .env

# Add your database connection string and JWT secrets to the .env file
# DATABASE_URL="..."
# JWT_SECRET="..."

# Run database migrations
npx prisma migrate dev

# Start the server
npm run dev
```
3. #### Setup the Web Application:
```sh
# Navigate to the web directory from the root
cd web

# Install dependencies
npm install

# Create a .env.local file and add the API URL
# NEXT_PUBLIC_API_URL=http://localhost:3333

# Start the web application
npm run dev
```
4. #### Setup the Mobile Application:
```sh
# Navigate to the mobile directory from the root
cd mobile

# Install dependencies
npm install

# Start the mobile application with Expo
npx expo start
```
<a id="authors"></a>
### Authors
- Felipe Messias Silva
- Gabriel Maciel dos Santos
