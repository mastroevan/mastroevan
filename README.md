# Hey, I'm Evan 👋

## Full-Stack Software Engineer | React | TypeScript | Node.js | Power Platform

![Open to Work](https://img.shields.io/badge/Open%20to%20Work-Full--Stack%20Software%20Roles-2ea44f?style=for-the-badge)
![Available](https://img.shields.io/badge/Available-Immediate%20Start-blue?style=for-the-badge)
![Location](https://img.shields.io/badge/Location-Denver%20%7C%20Remote-lightgrey?style=for-the-badge)

I build practical, polished software that turns messy business problems into clean digital products. My work spans full-stack web apps, automation tools, cloud-based workflows, and AI-powered business solutions.

Currently focused on building scalable apps, improving user experiences, and shipping projects that are actually useful — wild concept, I know.

---

## 🚀 Tech Stack

![JavaScript](https://img.shields.io/badge/JavaScript-333333?style=for-the-badge&logo=javascript)
![TypeScript](https://img.shields.io/badge/TypeScript-333333?style=for-the-badge&logo=typescript)
![React](https://img.shields.io/badge/React-333333?style=for-the-badge&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-333333?style=for-the-badge&logo=node.js)
![Express](https://img.shields.io/badge/Express.js-333333?style=for-the-badge&logo=express)
![Python](https://img.shields.io/badge/Python-333333?style=for-the-badge&logo=python)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-333333?style=for-the-badge&logo=postgresql)
![Prisma](https://img.shields.io/badge/Prisma-333333?style=for-the-badge&logo=prisma)
![AWS](https://img.shields.io/badge/AWS-333333?style=for-the-badge&logo=amazon-aws)
![Git](https://img.shields.io/badge/Git-333333?style=for-the-badge&logo=git)
![GitHub](https://img.shields.io/badge/GitHub-333333?style=for-the-badge&logo=github)
![Power Platform](https://img.shields.io/badge/Power%20Platform-333333?style=for-the-badge&logo=microsoft)
![SharePoint](https://img.shields.io/badge/SharePoint-333333?style=for-the-badge&logo=microsoft-sharepoint)
![SAP BTP](https://img.shields.io/badge/SAP%20BTP-333333?style=for-the-badge&logo=sap)
![SAP CAP](https://img.shields.io/badge/SAP%20CAP-333333?style=for-the-badge&logo=sap)
![SAP HANA Cloud](https://img.shields.io/badge/SAP%20HANA%20Cloud-333333?style=for-the-badge&logo=sap)
![Cloud Foundry](https://img.shields.io/badge/Cloud%20Foundry-333333?style=for-the-badge&logo=cloudfoundry)
![MCP](https://img.shields.io/badge/MCP-333333?style=for-the-badge&logo=modelcontextprotocol)
![Next.js](https://img.shields.io/badge/Next.js-333333?style=for-the-badge&logo=nextdotjs)
![FastAPI](https://img.shields.io/badge/FastAPI-333333?style=for-the-badge&logo=fastapi)
![Jest](https://img.shields.io/badge/Jest-333333?style=for-the-badge&logo=jest)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-333333?style=for-the-badge&logo=githubactions)
![Claude Code](https://img.shields.io/badge/Claude%20Code-333333?style=for-the-badge&logo=claudecode)
![Docker](https://img.shields.io/badge/Docker-333333?style=for-the-badge&logo=docker)
![Fastify](https://img.shields.io/badge/Fastify-333333?style=for-the-badge&logo=fastify)
![GraphQL](https://img.shields.io/badge/GraphQL-333333?style=for-the-badge&logo=graphql)
![MongoDB](https://img.shields.io/badge/MongoDB-333333?style=for-the-badge&logo=mongodb)
![MySQL](https://img.shields.io/badge/MySQL-333333?style=for-the-badge&logo=mysql)
![Pytest](https://img.shields.io/badge/Pytest-333333?style=for-the-badge&logo=pytest)
![Postman](https://img.shields.io/badge/Postman-333333?style=for-the-badge&logo=postman)
![Linux](https://img.shields.io/badge/Linux-333333?style=for-the-badge&logo=linux)
![Bash](https://img.shields.io/badge/Bash-333333?style=for-the-badge&logo=gnubash)

---

## 🛠 Featured Projects

### [Developer Portfolio](https://emsoftwaresolutions.com)
My personal site: current projects, background, and resume in one place. Built with React, TypeScript, Vite, and Tailwind CSS, deployed on Vercel.

### [Shadow Trader](https://github.com/mastroevan/shadow-trader)
An AI market research agent for stocks and crypto. Enter a ticker and it gathers live quotes, recent headlines, and technical signals; a LangGraph agent turns that evidence into a structured thesis with a confidence score and a watchlist plan. A deterministic risk gate, not the model, decides whether a setup can become a paper trade.

**Key Features**
- Structured theses: strategy, timeframe, bias, confidence, and exactly two bullish and two bearish factors
- Watchlist plans with trigger, invalidation, entry zone, stop loss, take profit, and risk/reward
- Confidence routing: 75%+ setups join the watchlist automatically, 60–74% wait for manual review, and anything lower is rejected
- Risk gate before any paper trade opens: stop and target placement, risk/reward, volume, trend strength, and a cooldown after losses
- Separate Next.js, Node API, and Python agent services, with PostgreSQL via Prisma and a Dockerfile for each
- End-to-end proof script that requires a real agent response, then opens and closes a paper trade
- Tests across the API, web app, and agent, run in GitHub Actions on every push

**Built with** Next.js, React, TypeScript, Node.js, Python (FastAPI), LangGraph, OpenAI, PostgreSQL, Prisma, Docker, GitHub Actions

### [Countersign](https://github.com/mastroevan/countersign)
Checks a carrier's "delivered" scan against what the Ring doorbell camera actually sees. When a package is marked delivered, the backend opens a live view on the door camera, samples frames, and asks an Amazon Bedrock vision model what's in them. The model only reports observations; plain Python policy code turns them into Verified, Disputed, or Inconclusive, so every verdict is reproducible and auditable. Built for the Ring track of Amazon's Build, Ship, Shape developer hackathon.

**Key Features**
- Live-view frame sampling over WebRTC (WHEP), refusing any camera with end-to-end encryption enabled
- Bedrock Converse with forced tool use returns observations only (parcel visible, location, confidence, watermark time); `policy.py` decides the verdict
- Claim drafts and S3 evidence packets with SHA-256 manifests are built only after a named person approves
- Privacy safeguards: no people, faces, or vehicles are described
- MCP server (FastMCP, Streamable HTTP) so voice assistants can check a delivery, with deliberately no approval tool
- Live pipeline trace over Server-Sent Events
- 150+ tests and strict mypy in CI, plus an eval harness with precision and recall thresholds for the vision judge (so far run on synthetic frames)
- Runs fully offline in minutes with synthetic frames and a stand-in tracker

**Built with** Python (FastAPI, async), Amazon Bedrock, Amazon S3, Ring API, WebRTC (aiortc), EasyPost, MCP (FastMCP), Next.js, React, Tailwind

---

## 💼 What I Bring

- Full-stack development with React, TypeScript, Node.js, and REST APIs
- Experience building business-facing tools, dashboards, and workflow apps
- Strong focus on clean UI, practical architecture, and maintainable code
- Microsoft 365, SharePoint, and Power Platform development experience
- Cloud, automation, API integration, and technical problem-solving skills

---

## 📊 GitHub Stats

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=mastroevan&layout=compact&theme=github_dark&hide_border=true)

---

## 📫 Connect With Me

[![Portfolio](https://img.shields.io/badge/Portfolio-emsoftwaresolutions.com-000000?style=for-the-badge&logo=google-chrome&logoColor=white)](https://emsoftwaresolutions.com)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Evan%20Mastro-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mastroevan/)

[![Email](https://img.shields.io/badge/Email-evanmastro%40icloud.com-1A73E8?style=for-the-badge&logo=icloud&logoColor=white)](mailto:evanmastro@icloud.com)

---

Thanks for stopping by. Feel free to check out my projects or connect with me.
