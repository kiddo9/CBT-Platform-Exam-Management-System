# CBT Platform & Exam Management System

## 📘 Project Description

A comprehensive, full-stack web application designed to manage and streamline the administration of Computer-Based Tests (CBT). This system provides a secure, user-friendly, and scalable solution for question bank management, administrative oversight, and real-world examination simulations.

## ✨ Key Features

- ✅ CAPTCHA Validation – Prevents bots from accessing sensitive endpoints

- 🔐 One-Time Password (OTP) Authorization – Adds a second layer of verification

- 🔁 Forgotten Password & Reset Flow – Secure user recovery system

- 👤 Admin User Management – Create and manage admin-level users

- 📝 Question Management – Create, edit, and manage CBT questions

- 👀 CBT Question Review System – Review and approve test questions before publishing

- 🎮 CBT Simulation – Mimics real CBT environments for practice and testing

- 📊 Detailed User Interaction Logging – For audit and debugging

## 🛠️ Tech Stack

**Frontend:**

- React.js

- Tailwind CSS

**Backend:**

- Node.js

- Express.js

- Sequelize ORM

- MySQL

**DevOps & Deployment:**

- Git & GitHub

- CI/CD with GitHub Actions

- Docker (Containerization)

- Nginx (Web Server, Reverse Proxy, load balancer)

- AWS EC2 (Deployment Infrastructure)

## 🔧 Other Engineering Practices

- 🌐 RESTful API Architecture

- ⏱️ Cron Jobs for scheduled tasks

- 🧩 Data Modeling using Sequelize

- 📁 MVC Folder Structure for clean separation of concerns

- 🛡️ JWT Authentication & Authorization

## Set up Instructions

## Prerequisities

Ensure you have the following installed:

- **Node and npm** (`22.0` or later) -> [Download node](https://nodejs.org/en/download)

- **Git** [Download git](https://git-scm.com/downloads)

- **Docker** [Download Docker](https://www.docker.com)

- **Nginx** [Download nginx](https://nginx.org/en/download.html) OR using nginx image from docker **(Recommended)**

```sh
    docker pull nginx
```

- **mysql & phpmyadmin**

## installation and configuration

1. ### clone repo

```sh
git clone https://github.com/kiddo9/nct_question_Back.git

```

2. ### open the directory

```sh
cd nct_question_Back
```

navigate to the nginx.conf file and comment the production mode and uncomment the development mode

3. ### DB creation, migrations and seeders

navigate to the server folder and
create your .env file, your database and update your env file with your database credencials. navigate to the config folder and click on the config.json. update development with your database credencials and then run migrations

**run migrations**

```sh
 npx sequelize-cli db:migrate
```

navigate to the seeders folder click on users and update the email to the one you will use for getting OTP an then seed

**run seeders**

```sh
 npx sequelize-cli db:seed:all
```

**note**
ensure you include your email server details in your env file as it will be used to send emails to users
