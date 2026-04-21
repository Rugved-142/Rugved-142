# 👋 Hi, I'm Rugved Gundawar

🎓 **MS Information Systems @ Northeastern University** (GPA: 3.7) | Boston, MA  
🚀 **Software Engineer** — Backend, Distributed Systems & Cloud Infrastructure  
💼 **2+ years** building enterprise-grade auth & IAM systems at Miniorange

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white&style=flat-square)](https://linkedin.com/in/rugved-gundawar)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?logo=vercel&logoColor=white&style=flat-square)](https://rugved-portfolio.vercel.app)
[![Email](https://img.shields.io/badge/Email-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:rgundawar1402@gmail.com)

---

## ⚡ Tech Stack

### 💻 Languages & Frameworks
![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-43853D?logo=node.js&logoColor=white)

### ☁️ Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?logo=apachekafka&logoColor=white)

### 🗄️ Databases & Messaging
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?logo=elasticsearch&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)

### 🔐 Security & Auth
![OAuth2](https://img.shields.io/badge/OAuth2-3C873A?logo=auth0&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?logo=jsonwebtokens&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?logo=springsecurity&logoColor=white)

### 🧪 Testing & Monitoring
![JUnit5](https://img.shields.io/badge/JUnit5-25A162?logo=junit5&logoColor=white)
![Mockito](https://img.shields.io/badge/Mockito-78A641?logoColor=white)
![Gatling](https://img.shields.io/badge/Gatling-FF9E2A?logo=gatling&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?logo=selenium&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)

---

## 🛠️ Featured Projects

### 🚦 [RateLimitX — Distributed Rate Limiting Service](https://github.com/Rugved-142/RateLimitX)
> Production-grade distributed rate limiter with **p95 latency of 11ms** at **4,500+ req/sec**

- **3 algorithms**: Token Bucket, Sliding Window Counter, Fixed Window — switchable at runtime via atomic Redis Lua scripts
- **JWT auth** with role-based tiered limits: USER (10), PREMIUM (100), ADMIN (1000) req/min via Spring Security 6
- **Circuit Breaker** pattern (CLOSED → OPEN → HALF_OPEN) with automatic failover to in-memory rate limiting — **99.9% availability**
- **Event-driven analytics** via Apache Kafka (3 partitions, async publishing) decoupled from rate-limit decisions
- **Real-time observability**: Prometheus metrics + auto-provisioned Grafana dashboards
- **7 services** orchestrated via Docker Compose + Kubernetes; load tested with Gatling

**Tech:** Java · Spring Boot · Redis · Kafka · PostgreSQL · Prometheus · Grafana · Docker · Kubernetes · Gatling

---

### ☁️ [Cloud-Native Web Application & Infrastructure](https://github.com/orgs/CSYE6225-Rugved/repositories)
> Full AWS infrastructure provisioned with Terraform IaC — zero manual steps from code to production

- Automated **VPC, EC2, ALB, ASG, RDS, Lambda, SNS, SES, S3, IAM** with least-privilege principles and zero hardcoded credentials
- **CI/CD pipeline** via GitHub Actions: Docker build → Amazon ECR → auto-deploy on every push to main
- **CloudWatch alarms** for ALB unhealthy hosts, EC2 CPU, Lambda errors, and 5XX responses with real-time SNS alerting
- S3 profile image uploads using IAM role-based access

**Tech:** AWS · Terraform · Node.js · Docker · GitHub Actions · CloudWatch · SNS · SES

---

### 📊 [Big Data Indexing — Medical Insurance Plan API](https://github.com/Rugved-142/INFO_7255_Big_Data_Indexing)
> RESTful API with advanced search indexing, async messaging, and OAuth2 security

- **Decomposed Redis** key-value storage with parent-child relationships (7 keys per plan object) + cascaded deletes
- **Elasticsearch** parent-child indexing — 4-level hierarchy (plan → membercostshare → planservice → linkedservice) with routing keys for same-shard co-location
- **RabbitMQ** async pipeline: API → Queue → Consumer → Elasticsearch, decoupling writes from search index updates
- Full CRUD + JSON Schema validation (RFC 7386 Merge Patch) + ETag-based conditional reads/writes (304, 412)
- Secured with **Google IDP OAuth2 RS256 JWT** via Spring Security

**Tech:** Java 17 · Spring Boot · Redis · Elasticsearch · RabbitMQ · Kibana · OAuth2 · Docker

---

### 🛡️ [AI Phishing Detector — Chrome Extension](https://github.com/Rugved-142/AI-Phishing-Detector)
> Hybrid AI + traditional threat detection with **71 passing tests** across 5 test suites

- **Hybrid scoring**: 20+ traditional risk factors (URL analysis, DOM structure, brand impersonation) + Google Gemini 2.5 Flash NLP (60% traditional + 40% AI)
- **Two-layer protection**: pre-loading URL screening blocks high-risk sites before content loads + deep content analysis
- **<100ms detection time** with color-coded risk badges (Low 0–30 / Medium 31–60 / High 61–100)
- Optional **Node.js/Express.js/MongoDB** backend exposing `/api/threats`, `/api/reports`, `/api/analytics`
- 71 tests across 5 Jest suites: AI integration, detection engine, service worker, UI components, end-to-end

**Tech:** JavaScript · Manifest V3 · Google Gemini API · Node.js · Express.js · MongoDB · Jest

---

### 🤝 [Community Connect — Enterprise Charitable Operations Platform](https://github.com/Rugved-142/Community_Connect)
> Multi-tenant Java desktop app reducing administrative overhead by **60%**

- **4-tier hierarchy**: Network → Enterprise → Organization → Users with 8 specialized RBAC roles
- Real-time donation processing, automated volunteer task assignment, priority-based aid distribution
- **Twilio SMS SDK** for event-driven notifications; JavaFaker for 150+ realistic test user profiles
- 130+ Java classes across layered architecture — Repository, Factory, Observer, MVC patterns; boots in <3s

**Tech:** Java 21 · Swing GUI · Maven · Twilio SDK · JavaFaker · MVC

---

### 🧪 [Selenium Test Automation — NEU Web Applications](https://github.com/Rugved-142/selenium-automation)
> End-to-end automated test suite for NEU web apps with Microsoft SSO + Duo 2FA handling

- **Page Object Model** pattern with data-driven testing via Apache POI Excel reader
- 5 scenarios: Canvas calendar events, Snell Library room booking, academic calendar, negative test (dataset download)
- **ExtentReports** HTML reporting with per-scenario screenshots before/after each step
- Dynamic 60s wait strategy for Duo 2FA push approval — reliable execution across authenticated apps

**Tech:** Java 11 · Selenium WebDriver 4 · TestNG · Maven · Apache POI · ExtentReports

---

## 💼 Work Experience Highlights

| Company | Role | Impact |
|---|---|---|
| **Miniorange Software Securities** | Software Developer Engineer | 60,000+ users · $50K contract · $40K revenue · 3hr→30min deployments |
| **IMATMI** | Full Stack Developer Intern | 85% match accuracy · 100ms→20ms latency · 75% faster reports |
| **InfoSpeed Services** | Software Developer Intern | 15,000 daily scans · 63% defect reduction · 91% test coverage |

---

## 📊 GitHub Stats

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Rugved-142&layout=compact&theme=tokyonight)

---

*"Build systems that are secure, observable, and built to last."*
