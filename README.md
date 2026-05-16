[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1200&color=58A6FF&background=0D111700&center=false&vCenter=true&width=580&lines=Studian+Engineer+with+Product+Ownership;DB+Optimization+%7C+AWS+Infrastructure+%7C+OCI;Hanyang+Univ.+%E2%80%94+Summa+Cum+Laude)](https://git.io/typing-svg)

# 정진영(Jerry Jung)

---

## About

Seoul-based backend engineer. Graduated **Hanyang University** (창업융합전공 · 정보시스템) with **Summa Cum Laude**, GPA 4.22 / 4.5 — top 1% of department (한양학업최우수상).

I work across NestJS API development, PostgreSQL query tuning, and AWS infrastructure. Core interest is measurable performance improvement — not just code that works, but code that's demonstrably faster and cheaper to run.

Currently building ClassDay 2.0 at **Superlearning** as a backend engineer, serving military obligation as 산업기능요원. Working on NestJS modular architecture, SMS / 알림톡 dispatch systems, and Flutter-based attendance app backend.

---

## Currently

### ClassDay 2.0 — Superlearning

`BACKEND ENGINEER` &nbsp;·&nbsp; `산업기능요원` &nbsp;·&nbsp; 2026.02 –

NestJS modular monolith for academy management SaaS. Building **Text Sender module** (KT XRoShot SMS + MnWise 알림톡), **Attendance App v2** backend (OTP-based auth, course/session structure), and CI/CD pipeline with Codemagic + Play Store.

### eoullim — 외국인 유학생 전용 커뮤니티

`PERSONAL PROJECT` &nbsp;·&nbsp; 2025.10 – 2025.12

Foreign student community platform built end-to-end. NestJS + TypeORM + PostgreSQL + Redis on AWS EC2/RDS. Achieved **41.2% API response time improvement** via Promise.all parallel processing + composite index tuning.

### Hanyang University

`UNDERGRADUATE` &nbsp;·&nbsp; 2020.03 – 2025.02 &nbsp;·&nbsp; Graduated

창업융합전공 + 정보시스템 부전공. GPA 4.22 / 4.5 (4.5 scale). Summa Cum Laude — 한양학업최우수상 (top 1% by cumulative GPA). 총장상.

---

## Featured Work

### Backend

| Project | Stack | Description |
|---|---|---|
| [eoullim](https://github.com/Playinc-Project/eoullim_representative) | NestJS · TypeORM · PostgreSQL · Redis · AWS | Foreign student community MVP. JWT auth, Promise.all optimization, composite indexing. |
| classday-office *(private)* | NestJS · MySQL · OCI · Supabase Realtime | Academy management SaaS. Text Sender module, real-time dashboard, attendance system. |

### Full-Stack & Side Projects

| Project | Stack | Description |
|---|---|---|
| [eoullim-web](https://github.com/Playinc-Project/eoullim_representative) | Next.js · AWS S3 · CloudFront | Frontend for eoullim. Static deployment via S3 + CloudFront CDN. |
| bigsignal | React · Python | Crypto auto-trading performance analyzer. |
| naver-keyword-recommender | React · Node.js | User text input → Naver ad keyword suggestion engine. |

---

## Case Study

**"41.2% API Response Time Improvement via Promise.all + Composite Index"**

Single comment-creation endpoint generating 4 sequential SQL queries. Post and User lookups were independent but executed serially — identified full table scan on FK validation in Comments table as compounding bottleneck.

**Two-axis fix:** Promise.all for parallel Post/User lookup + composite index `idx_comments_post_user` on `(post_id, user_id)`.

| Scenario | Avg Response (ms) | vs Baseline |
|---|---|---|
| Sequential, no index (baseline) | 120.86 ms | — |
| Promise.all only | 114.80 ms | −5.0% |
| Composite index only | 83.07 ms | −31.3% |
| **Promise.all + Composite index** | **71.15 ms** | **−41.2%** |

*30-trial average per scenario. Measured with TypeORM query logging + `performance.now()` automation script.*

Key finding: index optimization contributed more than application-level parallelism (31% vs 5%), but combining both achieved the maximum 41% gain.

→ [Full writeup & sequence diagrams](https://github.com/Playinc-Project/eoullim_representative)

---

## Background

| Period | — |
|---|---|
| 2026 – | Backend Engineer, Superlearning · ClassDay 2.0 (산업기능요원) |
| 2025.10 – 2025.12 | eoullim — personal project, full-stack MVP |
| 2025.07 – 2025.09 | Salesforce Developer Intern, DKBMC(주) |
| 2022 – 2025 | Founder & Tech Lead, Wihan · ₩20M in grants (SK · 홍천군청 등) |
| 2020 – 2025 | Hanyang University, 창업융합전공 + 정보시스템 |

### Publications & Recognition

- **AAICON 2024** — *AI-Based Learner Engagement Measurement System in Online Education* (제2저자)
- **전자책** *"개발 프로젝트 그거 어떻게 하는데?"* — 공동 1저자, 리디북스 IT 분야 1위 (2개월)
- **위니브 × 모두의연구소** 파이썬 백엔드 부트캠프 최종 프로젝트 장려상 (with Sim2real)
- **SQLD** · 컴퓨터 활용능력 2급 · 워드프로세서

---

## Tech Stack

![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)

---

<br/>

[![GitHub Streak](https://streak-stats.demolab.com?user=najasinis&theme=dark&hide_border=true&background=0D1117&stroke=0D1117&ring=ffffff&fire=ffffff&currStreakNum=ffffff&sideNums=9e9e9e&currStreakLabel=9e9e9e&sideLabels=9e9e9e&dates=9e9e9e)](https://git.io/streak-stats)


<!--
**najasinis/najasinis** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
