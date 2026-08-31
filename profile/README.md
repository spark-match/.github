<div align="center">

# Spark Match

### Copiloto de Orientación Vocacional con IA Generativa

[![TFP](https://img.shields.io/badge/UNI-TFP-blueviolet)](https://github.com/spark-match)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![AWS](https://img.shields.io/badge/AWS-Terraform-orange)](https://github.com/spark-match/spark-match-02-infrastructure)

**Spark Match** es un proyecto académico del Trabajo de Fin de Programa (UNI — II Programa de Especialización en IA Generativa y Machine Learning Ops) que implementa un copiloto de orientación vocacional basado en IA Generativa y MLOps.

</div>

---

## 🎯 ¿Qué es Spark Match?

Una aplicación web que ayuda a estudiantes a descubrir carreras afines a su perfil mediante:

- 🧠 **IA Generativa** (Amazon Bedrock + Claude) para análisis de perfil y recomendaciones
- 📊 **MLOps** pipelines para entrenar y servir modelos de matching vocacional
- 🎨 **Frontend moderno** (Angular) con UX conversacional
- ⚙️ **Backend escalable** (FastAPI en ECS Fargate)
- 🗄️ **Storage y analytics** (RDS Aurora, S3, CloudFront)

---

## 📚 Repositorios

### 🔧 Core

| Repo | Descripción |
|---|---|
| [**spark-match-00-knowledge-base**](https://github.com/spark-match/spark-match-00-knowledge-base) | Base de conocimiento compartida (ADRs, SDDs, postmortems, onboarding) |
| [**spark-match-01-devops**](https://github.com/spark-match/spark-match-01-devops) | Pipelines reutilizables (Terraform + LaTeX) con OIDC, lint y security checks |
| [**spark-match-02-infrastructure**](https://github.com/spark-match/spark-match-02-infrastructure) | Infraestructura AWS como código (Terraform puro), backend S3 + OIDC |

### 💻 Aplicación

| Repo | Descripción |
|---|---|
| [**spark-match-03-backend**](https://github.com/spark-match/spark-match-03-backend) | API REST en FastAPI (servicios core, integración con IA) |
| [**spark-match-04-frontend**](https://github.com/spark-match/spark-match-04-frontend) | SPA en Angular con UI conversacional |
| [**spark-match-05-data-pipeline**](https://github.com/spark-match/spark-match-05-data-pipeline) | Pipelines ETL (procesamiento de datos vocacionales) |
| [**spark-match-07-deep-agent**](https://github.com/spark-match/spark-match-07-deep-agent) | Deep agent (LangChain + AG-UI + Bedrock) con memoria de estudiante (langmem) |

### 📝 Documentación

| Repo | Descripción |
|---|---|
| [**spark-match-06-article**](https://github.com/spark-match/spark-match-06-article) | Artículo académico LaTeX (TFP) con CI/CD automatizado |

---

## 👥 Equipos

| Team | Responsabilidad |
|---|---|
| **owners** | Propietarios de la organización |
| **product-owners** | Gestión de prioridades y aprobaciones finales |
| **devops** | Infraestructura AWS y Terraform |
| **backend-devs** | API REST en FastAPI, servicios core |
| **frontend-devs** | SPA en Angular |
| **ai-devs** | IA/ML: LangChain, prompts, embeddings, modelos |
| **qa** | Aseguramiento de calidad y testing |
| **article-authors** | Autores del artículo académico |

---

## 🛠️ Stack técnico

### Cloud & Infrastructure
- **AWS** (`us-east-1`) — Cloud principal
- **Terraform** >= 1.6.0 — Infrastructure as Code
- **S3 + Lockfile** — Backend state remoto (sin DynamoDB)
- **GitHub Actions + OIDC** — CI/CD sin access keys

### Backend & AI
- **FastAPI** — API REST en Python
- **Amazon Bedrock** — Modelos fundacionales (Claude)
- **LangChain** — Orquestación de LLMs
- **PostgreSQL (RDS Aurora)** — Base de datos transaccional

### Frontend
- **Angular** — SPA con TypeScript
- **CloudFront** — CDN
- **S3** — Hosting estático

### Data & ML
- **S3 + Glue/Athena** — Data lake
- **SageMaker / Bedrock** — Model training y serving
- **CloudWatch** — Monitoring y logs

### Documentación
- **LaTeX** — Artículo académico (TFP)
- **GitHub Releases** — Versionado automático del PDF

---

## 🔐 Seguridad

Todos los repos siguen estas prácticas:

- ✅ **Branch protection** estricta (1 review + CODEOWNERS + conv resolution)
- ✅ **CODEOWNERS** por equipo (cada cambio requiere aprobación del equipo responsable)
- ✅ **OIDC + IAM Roles** (no access keys de larga duración)
- ✅ **Roles separados** para plan (read-only) vs apply (write)
- ✅ **GitHub Environments** como approval gates para deploys a producción
- ✅ **CI lint checks** (actionlint, gitleaks, yamllint) como required status checks
- ✅ **enforce_admins** activado (admins no pueden bypasear protecciones)

---

## 📖 Cómo contribuir

1. **Elige un repo** de los listados arriba
2. **Lee el README** del repo para entender su estructura
3. **Crea una rama** con prefijo descriptivo: `feat/`, `fix/`, `refactor/`, `docs/`
4. **Desarrolla** siguiendo las convenciones del repo
5. **Abre un PR** — el CI correrá automáticamente
6. **Espera aprobación** de CODEOWNERS del equipo correspondiente
7. **Mergea** cuando el CI pase y tengas al menos 1 aprobación

---

## 📜 Licencia

MIT — ver [LICENSE](LICENSE).

---

<div align="center">

**Construido con 🧠 + ❤️ por el equipo Spark Match**

</div>