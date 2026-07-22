<div align="center">

# Harshil Jain

**Software Engineer focused on backend systems and database architecture**

[kotaharshil2906@gmail.com](mailto:kotaharshil2906@gmail.com) · [LinkedIn](https://www.linkedin.com/in/harshil-jain-543940317/) · [Portfolio](https://harshiljain.online) · [GitHub](https://github.com/harshiljain2911)

</div>

---

## About Me

I'm a B.Tech Electronics & Communication Engineering student who builds backend systems the way I'd
want to defend them in an interview: with the design written down before the code, and the security
and correctness claims backed by tests rather than assumptions.

My work spans two directions that inform each other — a multi-tenant SaaS product where tenant
isolation is enforced by the database itself, and a continuous, publicly-committed practice record
in data structures and algorithms. I'd rather ship less and be able to explain every decision than
ship more and hand-wave the parts I didn't think through.

## Quick Snapshot

- B.Tech Electronics & Communication Engineering, LNMIIT Jaipur
- Building a multi-tenant SaaS product with database-enforced tenant isolation
- 550+ solved DSA problems across two long-running practice repositories
- Primary interests: backend architecture, PostgreSQL, and system design

## Featured Projects

### SupportPilot — Flagship Project

A multi-tenant SaaS platform where businesses train an AI support assistant on their own
documentation and embed it on their site via a cross-origin widget, billed only for the questions
it actually answers.

**Private flagship project — architecture walkthrough available on request.**

| Aspect | Detail |
|---|---|
| **Architecture** | Tenant isolation is enforced by PostgreSQL Row-Level Security — enabled and forced on all 14 tables — rather than by application-layer filtering. Background jobs are enqueued through `pg-boss` inside the same database transaction as the state change that triggers them, so a state change and its job either commit together or roll back together. |
| **Database security** | A four-actor access model (user, widget, worker, system) is checked inside the policies themselves, not just at the application boundary. Two tightly scoped `SECURITY DEFINER` functions handle the two cases where that boundary must be crossed; everywhere else, the absence of a policy is the enforcement. |
| **Testing** | The security-critical test suite runs as the actual least-privileged database role against a real PostgreSQL instance, not a mock. The repository has more test code than application code, and that suite has already caught and fixed two real policy gaps before they shipped. |
| **Process** | Built across eight milestones, each gated by a design document reviewed and approved before implementation starts. Thirty-one architecture decisions are recorded individually, each with the alternative that was rejected and why. |
| **Stack** | TypeScript, Next.js, PostgreSQL, Drizzle ORM, pg-boss |
| **Status** | Tenancy and authentication shipped; asynchronous ingestion pipeline in progress; chat, embeddable widget, and billing are designed and scheduled |

### Harshil-OS — Portfolio Platform

The platform this profile links to is not a static page — it's a small full-stack product I built
and maintain. Content is stored as schema-validated JSON and edited through a purpose-built admin
panel; an AI assistant answers questions about my work by retrieving from that same content, with
automatic fallback across providers if one is unavailable.

| Aspect | Detail |
|---|---|
| **Backend** | FastAPI with Pydantic-validated content models — the server will not boot on invalid data |
| **Frontend** | React, with route-level prerendering and a keyboard-driven interface |
| **Notable engineering** | A retrieval-grounded AI assistant with automatic multi-provider fallback; a production contact pipeline with rate limiting and a durable fallback path if email delivery fails |
| **Stack** | React, FastAPI, PostgreSQL/MongoDB, Tailwind CSS |
| **Status** | Deployed and live |

### Data Structures & Algorithms

Four repositories, not maintained for a single showcase-worthy number but as a continuous record of
practice. The value here is consistency over time, not any individual result.

| Repository | Focus | Verified scale |
|---|---|---|
| [DSA-CPP](https://github.com/harshiljain2911/DSA-CPP) | Daily C++ practice across arrays through graphs, with a dedicated dynamic-programming track | 300+ solutions, 90+ days |
| [DSA-CPP-STRIVER](https://github.com/harshiljain2911/DSA-CPP-STRIVER) | The Striver A2Z curriculum worked end to end | 250+ solutions, 60+ days |
| [DSA-LC-Weekly](https://github.com/harshiljain2911/DSA-LC-Weekly_Contests) | LeetCode Weekly Contest solutions | 5 consecutive contests |
| [DSA-LC-BiWeekly](https://github.com/harshiljain2911/DSA-LC-Bi-Weekly_Contests) | LeetCode Biweekly Contest solutions | 2 consecutive contests |

## Engineering Philosophy

- **Design precedes code.** SupportPilot's eight milestones each start with a written design that is
  reviewed before any implementation begins — deviations discovered while building are surfaced,
  not silently patched in.
- **Claims are backed by tests, not assumptions.** Database security is verified by a test suite
  that runs against a real database as the real runtime role; nothing about tenant isolation is
  taken on faith.
- **The naive solution is written down, not skipped.** Across the DSA repositories, the brute-force
  approach is kept alongside the optimized one, because the optimization is only meaningful once
  the baseline is explicit.
- **Decisions are recorded with their alternatives.** A design choice without the rejected option
  next to it isn't a defensible decision — it's a guess that happened to work.

## Skills

**Languages**

![C++](https://img.shields.io/badge/C%2B%2B-00599C?logo=cplusplus&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Drizzle ORM](https://img.shields.io/badge/Drizzle_ORM-C5F74F?logo=drizzle&logoColor=black)
![Zod](https://img.shields.io/badge/Zod-3E67B1?logo=zod&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwindcss&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?logo=postgresql&logoColor=white)

**Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?logo=railway&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)

**Tools**

![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![pnpm](https://img.shields.io/badge/pnpm-F69220?logo=pnpm&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest&logoColor=white)
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?logo=eslint&logoColor=white)

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=harshiljain2911&show_icons=true&theme=tokyonight&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=harshiljain2911&layout=compact&theme=tokyonight&hide_border=true)

</div>

## Contact

| | |
|---|---|
| Email | [kotaharshil2906@gmail.com](mailto:kotaharshil2906@gmail.com) |
| LinkedIn | [linkedin.com/in/harshil-jain-543940317](https://www.linkedin.com/in/harshil-jain-543940317/) |
| Portfolio | [harshiljain.online](https://harshiljain.online) |
| GitHub | [@harshiljain2911](https://github.com/harshiljain2911) |
