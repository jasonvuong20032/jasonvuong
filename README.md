# 👋 Hi, I'm Vuong Quang Tuan

🎓 Computing Graduate (UK Honours Degree, 2:2) | 💼 Former Intern at FPT Software | 🔎 Seeking a .NET / Web Developer Internship

---

## 🔗 Quick Links

| | Links |
|---|---|
| 💼 **Experience** | [Internship at FPT Software](#-experience) |
| 🚀 **VQT Japanese Food** (featured project) | [Source code](https://github.com/jasonvuong20032/vqt-japanese-food) · [Project write-up](projects/vqt-japanese-food.md) |
| 📚 **Project documentation** | [ERD](https://github.com/jasonvuong20032/vqt-japanese-food/blob/main/docs/erd.md) · [Sequence diagrams](https://github.com/jasonvuong20032/vqt-japanese-food/blob/main/docs/sequence-diagrams.md) · [Use cases](https://github.com/jasonvuong20032/vqt-japanese-food/blob/main/docs/use-cases.md) · [Architecture](https://github.com/jasonvuong20032/vqt-japanese-food/blob/main/docs/architecture.md) · [Admin guide](https://github.com/jasonvuong20032/vqt-japanese-food/blob/main/docs/admin-guide.md) |
| 🏅 **Certificate portfolio** | [All certificates with descriptions](https://github.com/jasonvuong20032/certificate-portfolio) |
| 📜 **Certificates** | [CS50P (Harvard)](https://github.com/jasonvuong20032/certificate-portfolio#1-cs50s-introduction-to-programming-with-python-cs50p) · [SQL (Intermediate)](https://github.com/jasonvuong20032/certificate-portfolio#2-sql-intermediate) · [SQL (Basic)](https://github.com/jasonvuong20032/certificate-portfolio#3-sql-basic) · [JavaScript (Intermediate)](https://github.com/jasonvuong20032/certificate-portfolio#4-javascript-intermediate) · [JavaScript (Basic)](https://github.com/jasonvuong20032/certificate-portfolio#5-javascript-basic) |

---

## 👨‍💻 About Me

I'm a **Computing graduate** with a UK honours degree (**Second-Class Honours, Lower Division – 2:2**) and a strong focus on **web development with .NET**.

I completed an **internship at FPT Software**, where I worked on a team building an e-commerce and online-auction platform as **.NET 8 microservices**. I was the main developer of the **User Service** (authentication, roles and privileges, seller verification and a reputation system) and also contributed to the **Commerce** and **Auction** services.

Outside of work I build full-stack projects, such as [VQT Japanese Food](#-featured-project-vqt-japanese-food) (ASP.NET Core + React), and verify my skills with certificates from Harvard's CS50 and HackerRank.

I'm now looking for my **next internship** as a **.NET backend or full-stack web developer**, where I can keep learning and contribute to real products.

---

## 🎯 Career Objective

- .NET Backend Developer Intern
- Full-stack Web Developer Intern (.NET + React)
- Open to **internship** positions

---

## 🛠️ Tech Stack

### Programming Languages
- C#
- JavaScript (ES6+) / TypeScript
- SQL
- Python

### Backend
- ASP.NET Core Web API (.NET 8 / .NET 9), ASP.NET MVC
- Entity Framework Core (code-first migrations)
- REST APIs, gRPC, SignalR (real-time)
- Microservices and event-driven messaging: RabbitMQ (MassTransit), transactional outbox pattern
- Authentication and authorisation: JWT, role- and privilege-based access control (RBAC)
- Redis caching

### Frontend
- React, TypeScript, Vite
- Tailwind CSS, HTML5, CSS3, responsive web design
- TanStack Query, i18next (multilingual UI)

### Database
- SQL Server: schema design, relationships, migrations, reporting queries

### Testing & Quality
- xUnit, Moq, integration tests against a real SQL Server
- Vitest
- SonarQube, code coverage

### Tools & Environment
- Docker, Docker Compose
- Git, GitHub, GitLab (merge-request workflow)
- Visual Studio, VS Code, Postman

---

## 💼 Experience

### Intern · FPT Software · Jun 2026 – Aug 2026

**Team project:** an e-commerce and online-auction marketplace built as **.NET 8 microservices** (user, catalog, commerce, auction, fulfilment and notification services behind an API gateway).
**Tech:** ASP.NET Core 8 · EF Core 8 · SQL Server · Redis · RabbitMQ (MassTransit) · gRPC · SignalR · Docker · xUnit · SonarQube · GitLab

**User Service** (main developer)
- Built authentication and authorisation: JWT with a token blacklist, a privilege catalog with role–privilege management endpoints, admin user-management and audit-log APIs, and login rate limiting scoped to IP address and account.
- Implemented seller registration with KYC as a state machine, and Vietnamese citizen-ID (CCCD) identity verification with an admin review workflow and concurrency control.
- Rewrote the reputation system in five phases: a scoring formula engine, one-time verification and seller-approval bonuses, a ratings pipeline with weekly aggregation, inactivity decay, and cross-service events that award or penalise reputation.
- Connected the service to the rest of the platform with the transactional outbox pattern, RabbitMQ consumers with dead-lettering, and a gRPC API that exposes user and reputation snapshots to other services.
- Raised test coverage with unit tests (for example the authentication service from 0% to about 90%, and the infrastructure layer from 0% to 89%) and added integration tests against a real SQL Server to prove idempotency.

**Commerce Service**
- Implemented the cart APIs and price calculation, checkout-to-order creation with order-management APIs and RBAC, inventory reservation through the outbox pattern and gRPC, and an idempotent payment-callback handler with cancel and refund.

**Auction Service**
- Built the auction lifecycle API and state machine, the place-bid API with optimistic concurrency, real-time bidding with SignalR, payment deadlines and payment synchronisation, and a reputation-based bidding eligibility check with caching and a resilience fallback.

**Way of working:** feature branches and GitLab merge requests into a shared `develop` branch, API contracts agreed in shared design documents, services run together locally with Docker Compose.

---

## 🚀 Featured Project: VQT Japanese Food

A full-stack e-commerce web application for a Japanese food store in Vietnam, rebuilt from a classic ASP.NET MVC site into a **React single-page app** on an **ASP.NET Core 9 Web API** (personal project, 2026).

- Layered architecture (controllers → service layer → EF Core → SQL Server) with a 24-table database: order lines that snapshot prices, order status history, and translation tables for five languages.
- Secure checkout: prices and totals are recalculated on the server, and stock is reserved with conditional updates inside a transaction so the last item can never be sold twice.
- Authentication with JWT in HttpOnly cookies, rotating refresh tokens with reuse detection, role-based access for staff and administrators, and rate limiting on sign-in and checkout.
- Back office with a revenue dashboard, an order workflow that emails customers in their own language, dish and photo management, coupons, review moderation and staff management.
- 5 languages (Vietnamese, English, Japanese, Korean, French) and 4 colour themes.
- 84 backend tests (xUnit) and 48 frontend tests (Vitest), plus documentation: ERD, sequence diagrams and use case specifications.

**Tech:** C# · .NET 9 · ASP.NET Core Web API · EF Core 9 · SQL Server · React 19 · TypeScript · Vite · Tailwind CSS 4 · TanStack Query · i18next · xUnit · Vitest

💻 **Source code:** [github.com/jasonvuong20032/vqt-japanese-food](https://github.com/jasonvuong20032/vqt-japanese-food)  
📄 **How it works, how to run it, tech stack and diagrams:** [projects/vqt-japanese-food.md](projects/vqt-japanese-food.md)

---

## 🏅 Certifications

📜 **Full certificate portfolio:** [github.com/jasonvuong20032/certificate-portfolio](https://github.com/jasonvuong20032/certificate-portfolio): every certificate with what it covers, why it matters and a verification link.

| Certificate | Issuer | Date | Verify |
|---|---|---|---|
| [CS50's Introduction to Programming with Python](https://github.com/jasonvuong20032/certificate-portfolio#1-cs50s-introduction-to-programming-with-python-cs50p) | Harvard University (CS50) | 2026 | [Verify](https://cs50.harvard.edu/certificates/a8743d2b-c34a-4c6c-b58d-bf0da919654f) |
| [SQL (Intermediate)](https://github.com/jasonvuong20032/certificate-portfolio#2-sql-intermediate) | HackerRank | 29 Mar 2026 | [Verify](https://www.hackerrank.com/certificates/f6708c1d8d4b) |
| [SQL (Basic)](https://github.com/jasonvuong20032/certificate-portfolio#3-sql-basic) | HackerRank | 29 Mar 2026 | [Verify](https://www.hackerrank.com/certificates/f2cf09ae31e4) |
| [JavaScript (Intermediate)](https://github.com/jasonvuong20032/certificate-portfolio#4-javascript-intermediate) | HackerRank | 27 Oct 2025 | [Verify](https://www.hackerrank.com/certificates/e31f1c72abbd) |
| [JavaScript (Basic)](https://github.com/jasonvuong20032/certificate-portfolio#5-javascript-basic) | HackerRank | 25 Oct 2025 | [Verify](https://www.hackerrank.com/certificates/2911fc05a883) |

---

## 📂 Other Projects

### 🌐 Web Application using .NET Framework
**Tech:** ASP.NET MVC, C#, SQL Server, HTML, CSS, JavaScript  
- Developed a full-stack web application with server-side rendering
- Implemented CRUD features and form validation
- Worked with SQL Server for data storage and querying
- Applied MVC architecture and clean code practices

### 🧠 Python Project
**Tech:** Python  
- Built small applications to practice logic, data handling, and problem-solving
- Focused on writing readable and maintainable code

### 🎨 Frontend Web Project
**Tech:** HTML, CSS, JavaScript  
- Created responsive web pages from scratch
- Focused on layout, styling, and basic interactivity

---

## 📚 Currently Learning

- Microservice architecture and distributed-system patterns
- Modern JavaScript / TypeScript patterns
- Web security fundamentals
- Clean architecture & best practices

---

## 🤝 Soft Skills

- Strong self-learning ability
- Responsibility & discipline
- Willing to receive feedback
- Team collaboration mindset

---

## 📫 Contact Me

- GitHub: [github.com/jasonvuong20032](https://github.com/jasonvuong20032)
- Email: [jasonvuong1512@gmail.com](mailto:jasonvuong1512@gmail.com)

---

⭐ Feel free to explore my repositories and contact me if you'd like to collaborate or learn together!
