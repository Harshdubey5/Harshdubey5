<h1 align="center">Hey, I'm Harsh 👋</h1>

<p align="center">
  <a href="https://readme-typing-svg.demolab.com">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1200&color=2F81F7&center=true&vCenter=true&width=620&lines=Full-stack+developer+from+India;I+like+owning+a+feature+from+DB+to+screen;Currently+building+DevBoard" alt="Typing intro" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open%20to-Full--Stack%20%26%20Backend%20roles-2ea44f?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Based%20in-India-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Remote%20%26%20Relocation-Open-orange?style=for-the-badge" />
</p>

---

### 🚀 Currently building

**[DevBoard](https://github.com/Harshdubey5/devboard)**: a project management platform I'm building from scratch.

| | |
|---|---|
| ✅ **Done** | Session auth (Argon2, Postgres-backed sessions), owner-only project access, project CRUD, migrations, API tests for cross-user isolation |
| 🚧 **Now** | Frontend tests, security checks (CSRF, CORS, cookies), UI polish, deployment |
| 🗺️ **Next** | Tasks, assignments, comments, then Redis, Docker, AWS and CI/CD |

---

### 🧰 Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=react,ts,nodejs,express,postgres,python,fastapi,flutter,dart,aws,firebase,git" />
</p>

---

### 🛠️ Things I've built

| Project | What it does | Tech |
|---|---|---|
| [**DevBoard**](https://github.com/Harshdubey5/devboard) | Full-stack project management app | React, TypeScript, Node, Postgres |
| [**Ticket Classification API**](https://github.com/Harshdubey5/REPO-NAME) | Triages support tickets across 6 categories | FastAPI, SQLAlchemy |
| [**Stripe in Flutter**](https://github.com/Harshdubey5/REPO-NAME) | Tokenized payments, no raw card data touched | Flutter, Dart, Stripe |
| [**Human Activity Prediction**](https://github.com/Harshdubey5/REPO-NAME) | LSTM model for activity recognition | Python, TensorFlow, Keras |

---

### 💼 Experience

- **Software Developer Intern, Technovalogy LLP.** Flutter modules across 8 clinical workflows (OPD, ICU, Prescriptions, Payments and more), led a 2-person team
- **Mobile Developer Intern, SpeezyIT.** S3 presigned uploads, AWS Cognito and Firebase Auth

---

<details>
<summary><b>🔐 Things I've been digging into</b></summary>
<br>

How session auth really works (cookies, regeneration, storage), cross-user access control and how to test it, and JWT and OAuth2 flows from first principles.

</details>

### 📫 Let's talk

<p align="center">
  <a href="https://www.linkedin.com/in/harsh-dubey-a19165256/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:harshdubey8689@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<h1 align="center">DevBoard</h1>
<p align="center">A full-stack project management platform, built from scratch to learn how a real product fits together, from database to UI.</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white" />
</p>

<p align="center"><a href="LIVE-LINK">Live demo</a> · <a href="#architecture">Architecture</a> · <a href="#security">Security</a> · <a href="#run-locally">Run locally</a></p>

![DevBoard dashboard](docs/dashboard.png)

## Status

| Area | State |
|---|---|
| Registration, login, logout, session restore | ✅ Done |
| Owner-only project CRUD | ✅ Done |
| API tests (anonymous access, cross-user isolation) | ✅ Done |
| Frontend tests, CSRF/CORS review, UI polish | 🚧 In progress |
| Deployment | 🚧 In progress |
| Tasks, assignments, comments | 🗺️ Next |
| Redis, Docker, AWS, CI/CD | 🗺️ Planned |

## Architecture

Request → **routes** → **controllers** → **services** (business logic) → **data access** → PostgreSQL

Keeping these layers separate means routing never touches SQL and business rules can be tested without HTTP.

## Security

- Passwords hashed with **Argon2**
- **Server-side sessions** stored in PostgreSQL, regenerated on login, with secure cookie settings
- **Owner-only authorization**: projects belong to the authenticated user, and update and delete check both project ID and owner ID
- **Tests** cover anonymous access and one user trying to read or change another's projects

## Tech

React, TypeScript, Vite · Node.js, Express · PostgreSQL with migrations · Input validation and centralized error handling

## Run locally

```bash
git clone https://github.com/Harshdubey5/devboard.git
cd devboard
# install, set up .env from .env.example, run migrations, start API and web
```
