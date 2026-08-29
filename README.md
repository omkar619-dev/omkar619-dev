<h1 align="center">Hi 👋, I'm Omkar Shendge</h1>
<h3 align="center">Backend engineer @ Staple AI · building toward distributed systems & AI infrastructure</h3>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=omkar619-dev&label=Profile%20views&color=0e75b6&style=flat" alt="profile views" />
</p>

---

Backend engineer based in India 🇮🇳. I learn by building **production-grade systems end to end** — writing the service, containerizing it, wiring the CI/CD, deploying it, load-testing it, and keeping it observable. Right now I'm pushing deeper into **distributed systems**, **platform / SRE**, and **AI infrastructure / agentic engineering**.

### 🌱 Open source

I contribute to the infrastructure I run. Merged upstream:

- **[Grafana Mimir](https://github.com/grafana/mimir/pull/16338)** — store-gateway leaked one TCP connection per `get_range` because `loadChunks` closed the bucket range reader without draining it, so `net/http` discarded the connection instead of pooling it. Root-caused from a user's connection-exhaustion report and fixed by draining before close.
- **[Traefik](https://github.com/traefik/traefik/pull/13691)** — documented the Redis keyspace-notifications requirement that silently breaks the Redis provider when unset.

Currently open across **[KubeRay](https://github.com/ray-project/kuberay/pulls/omkar619-dev)**, **[Argo CD](https://github.com/argoproj/argo-cd/pulls/omkar619-dev)**, **[KEDA](https://github.com/kedacore/keda/pulls/omkar619-dev)**, **[Envoy Gateway](https://github.com/envoyproxy/gateway/pulls/omkar619-dev)** and **[Traefik](https://github.com/traefik/traefik/pulls/omkar619-dev)** — deprecation cleanups, a `singleflight` fix for concurrent auth-token lookups, circuit-breaker metrics, and an ingress-nginx annotation-translation bug.

### 🧱 What I've built

**[chat-go](https://github.com/omkar619-dev/chat-go)** — real-time chat in Go. WebSocket gateway with Redis pub/sub fan-out, **Kafka as the durable log** feeding three independent consumer groups (history, pgvector search indexing, local-LLM RAG bot), Postgres + pgvector, and streaming catch-up summaries over the socket. Includes a hardening write-up and a documented scaling limit I left in deliberately.

**[news-feed-go](https://github.com/omkar619-dev/news-feed-go)** — production-grade news feed in Go: auth, post CRUD, a follow graph, **hybrid push/pull fan-out**, ranking, Redis cache-aside, **pgvector** semantic search, notifications and full observability. Built as a real system rather than a toy MVP.

**[StudentSystemGo](https://github.com/omkar619-dev/StudentSystemGo)** — a Go REST API layered all the way up to production as a system-design playground:
- Multi-stage **Docker** build · **GitHub Actions** CI/CD to **AWS EC2**, later redeployed on **K3s**
- **Nginx** load balancer across multiple app instances with circuit breaking
- **MySQL primary + replica** with read/write split · **Redis** rate limiting + cache-aside
- **S3 + CloudFront** media storage provisioned with **Terraform**
- **RabbitMQ** worker queue · **Prometheus** metrics · **k6** load tests
- Deep-dive docs covering architecture, deployment, observability & load testing

### 🔭 What I'm building right now

- **[GitOps homelab on K3s + ArgoCD](https://github.com/omkar619-dev/omkar-homelab-gitops)** — moving my self-hosted services to declarative, Git-driven deployments.
- **Distributed systems via MIT 6.5840** — MapReduce ✅ · KV server + lock ✅ · **Raft** in progress.
- **chat-go, next phase** — presence and multi-gateway coordination, then **WebRTC** for voice/video.

### 🛣️ Where I'm headed

Backend today → **platform / SRE** and **AI-infrastructure / agentic** engineering. Same throughline everywhere: own systems end-to-end, and bring that rigor to the infrastructure that runs AI. Next on the roadmap — an **LLM agent** in TypeScript with **LangGraph** and a proper eval harness.

### 🛠️ Tech I work with

**Languages**

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)

**Backend & Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat&logo=postgresql&logoColor=white)
![MySQL / MariaDB](https://img.shields.io/badge/MySQL%20%2F%20MariaDB-4479A1?style=flat&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat&logo=rabbitmq&logoColor=white)

**Infra & DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![K3s](https://img.shields.io/badge/K3s-FFC61C?style=flat&logo=k3s&logoColor=black)
![Argo CD](https://img.shields.io/badge/Argo%20CD-EF7B4D?style=flat&logo=argo&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white)

**Observability & Testing**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat&logo=k6&logoColor=white)

### 📊 GitHub stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=omkar619-dev&show_icons=true&locale=en&theme=tokyonight" alt="Omkar's GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs?username=omkar619-dev&layout=compact&locale=en&theme=tokyonight" alt="Top languages" />
</p>

### 📫 Connect with me
- 💼 LinkedIn — [omkar-shendge](https://www.linkedin.com/in/omkar-shendge-43784612b/)
- 📧 Email — omkarshendge619@gmail.com
- 🐦 X / Twitter — [@p0pobeast](https://twitter.com/p0pobeast)
