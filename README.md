
![toolxox com-enhanced-XArSH6gzj7Wt82PRCZFK9Tu4dV0EBy](https://github.com/user-attachments/assets/bbb8e304-636b-4cb9-9835-30c6936b068f)

<h1 align="center">🛡️ Ashwanth & System and Innovation</h1>

<h3 align="center">⚡ Engineered by <strong>Ashwanth</strong> · <a href="https://sites.google.com/view/ashwanthtechsolution">Ashwanth System & Innovation</a></h3>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/Version-0.15-blue?style=for-the-badge&logo=github&logoColor=white" alt="Version"/>
  <img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge&logo=statuspage&logoColor=white" alt="Status"/>
  <img src="https://img.shields.io/badge/Security-AI%20Powered-ef4444?style=for-the-badge&logo=shield&logoColor=white" alt="Security"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Supported-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Kubernetes-Orchestrated-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes"/>
  <img src="https://img.shields.io/badge/OpenAI-GPT--5.2-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI"/>
  <img src="https://img.shields.io/badge/Anthropic-Claude%204.5-FF6B35?style=for-the-badge&logo=anthropic&logoColor=white" alt="Anthropic"/>
  <img src="https://img.shields.io/badge/Google-Gemini%203-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MITRE-ATT%26CK-black?style=for-the-badge&logo=mitre&logoColor=white" alt="MITRE"/>
  <img src="https://img.shields.io/badge/STRIDE-Methodology-8B5CF6?style=for-the-badge&logo=security&logoColor=white" alt="STRIDE"/>
  <img src="https://img.shields.io/badge/OWASP-Top%2010-red?style=for-the-badge&logo=owasp&logoColor=white" alt="OWASP"/>
  <img src="https://img.shields.io/badge/DREAD-Risk%20Model-orange?style=for-the-badge&logo=danger&logoColor=white" alt="DREAD"/>
  <img src="https://img.shields.io/badge/Zero--Day-Detector-critical?style=for-the-badge&logo=radar&logoColor=white" alt="Zero-Day"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Kafka-Event%20Streaming-231F20?style=for-the-badge&logo=apachekafka&logoColor=white"/>
  <img src="https://img.shields.io/badge/Elasticsearch-Log%20Analysis-005571?style=for-the-badge&logo=elasticsearch&logoColor=white"/>
  <img src="https://img.shields.io/badge/Streamlit-UI%20Engine-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ollama-Local%20LLM-black?style=for-the-badge&logo=ollama&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
</p>

---

> 🛡️ **ThreatSentinel AI** is a next-generation, AI-powered cyber threat detection and autonomous response engine that leverages the most advanced Large Language Models — including **OpenAI GPT-5.2**, **Anthropic Claude 4.5**, and **Google Gemini 3** — to autonomously generate threat models, attack trees, STRIDE analyses, DREAD risk scores, and real-time defense protocols. Built with precision and secured by design by **Ashwanth** at **Ashwanth System & Innovation**.

---

## 📌 Table of Contents

- [🧠 System Architecture](#-system-architecture)
- [⚡ Features](#-features)
- [📦 Tech Stack](#-tech-stack)
- [🔧 Installation](#-installation)
  - [Option 1: Clone Repository](#option-1-cloning-the-repository)
  - [Option 2: Docker Container](#option-2-using-docker-container)
  - [Option 3: Kubernetes Deployment](#option-3-kubernetes-enterprise-deployment)
- [⚙️ Configuration & Environment Variables](#️-configuration--environment-variables)
- [🚀 Usage](#-usage)
  - [Streamlit App](#option-1-running-the-streamlit-app-locally)
  - [Docker Run](#option-2-using-docker-container)
  - [CLI Mode](#option-3-cli--headless-mode)
  - [REST API Mode](#option-4-rest-api-mode)
- [🧪 Advanced Usage & Commands](#-advanced-usage--commands)
- [🤖 AI Model Configuration](#-ai-model-configuration)
- [📊 Threat Analysis Pipeline](#-threat-analysis-pipeline)
- [🔐 Security Best Practices](#-security-best-practices)
- [🏢 Enterprise Deployment](#-enterprise-deployment)
- [🧬 STRIDE & OWASP Integration](#-stride--owasp-integration)
- [🗺️ Roadmap](#️-roadmap)
- [📋 Changelog](#-changelog)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🧠 System Architecture

```mermaid
flowchart TD
    A[🌐 Network Traffic Input] --> B[Real-Time Data Streamer\nApache Kafka]
    B --> C[Preprocessing Engine\nFeature Extraction & Normalisation]
    C --> D{🤖 AI Threat Classifier\nEnsemble LLM Engine}
    D -->|Known Attack Pattern| E[Pattern Matcher\nMITRE ATT&CK v15]
    D -->|Unknown Anomaly| F[Zero-Day Detector\nGraph Neural Network]
    D -->|GenAI/Agentic Risk| G[OWASP LLM Top 10\nASI Threat Analyser]
    E --> H[Threat Score Engine\nDREAD Model]
    F --> H
    G --> H
    H --> I{⚖️ Risk Level\nEvaluation}
    I -->|🔴 Critical| J[🚨 Auto Response\nDeploy Defense Protocol]
    I -->|🟠 High| K[🔔 Escalate to SOC\nPagerDuty / OpsGenie]
    I -->|🟡 Medium| L[⚠️ Alert Dashboard\nSOC Notification]
    I -->|🟢 Low| M[📊 Log & Monitor\nELK Stack]
    J --> N[Incident Report Generator]
    K --> N
    L --> N
    M --> N
    N --> O[📁 ThreatSentinel AI Output\nAshwanth System & Innovation]
    O --> P[📤 Export: PDF / Markdown / JSON]

    style A fill:#1a1a2e,color:#fff
    style D fill:#16213e,color:#fff
    style I fill:#0f3460,color:#fff
    style J fill:#e94560,color:#fff
    style O fill:#533483,color:#fff
    style P fill:#2d6a4f,color:#fff
```

---

## ⚡ Features

| 🔖 Feature | 📝 Description |
|---|---|
| 🖥️ **Intuitive UI** | Clean Streamlit interface, zero learning curve |
| 🔍 **STRIDE Engine** | Full STRIDE threat model generation per component |
| 🤖 **Agentic AI Support** | OWASP Top 10 for Agentic Applications (ASI01–ASI10) |
| 🧬 **GenAI Threat Modeling** | OWASP LLM Top 10 (LLM01–LLM10) integration |
| 🏗️ **Pattern Detection** | Auto-detects RAG, multi-agent, MCP, tool ecosystems |
| 🖼️ **Multi-Modal Input** | Upload architecture diagrams, flowcharts, screenshots |
| 🌳 **Attack Trees** | Visual attack path enumeration via Mermaid.js |
| 🛡️ **Mitigation Engine** | Contextual, actionable mitigation suggestions |
| 📊 **DREAD Scoring** | Quantitative risk scores for every identified threat |
| 🧪 **Gherkin Test Cases** | BDD test cases generated from threat data |
| 🐙 **GitHub Integration** | Analyze public/enterprise repos automatically |
| 🧠 **Multi-LLM Support** | GPT-5.2, Claude 4.5, Gemini 3, Mistral Magistral |
| 🔌 **LLM Provider Agnostic** | OpenAI, Anthropic, Google, Mistral, Groq, Ollama, LM Studio |
| 🔒 **Zero Data Storage** | Nothing persisted — your data stays yours |
| 🐳 **Containerized** | Full Docker + Kubernetes support |
| ⚙️ **Env Config** | `.env`-based secure secrets management |
| 📥 **Export Outputs** | Download as Markdown, PDF, or JSON |

---

## 📦 Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white"/>
  <img src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white"/>
  <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white"/>
  <img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white"/>
  <img src="https://img.shields.io/badge/Kibana-005571?style=flat-square&logo=kibana&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white"/>
  <img src="https://img.shields.io/badge/Anthropic-FF6B35?style=flat-square&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/Google%20Gemini-4285F4?style=flat-square&logo=google&logoColor=white"/>
  <img src="https://img.shields.io/badge/Mistral-black?style=flat-square&logo=mistral&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ollama-black?style=flat-square&logo=ollama&logoColor=white"/>
  <img src="https://img.shields.io/badge/Groq-F55036?style=flat-square&logo=groq&logoColor=white"/>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white"/>
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
  <img src="https://img.shields.io/badge/Trivy-1904DA?style=flat-square&logo=trivy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Bandit-FFD43B?style=flat-square&logo=python&logoColor=black"/>
  <img src="https://img.shields.io/badge/CodeQL-000000?style=flat-square&logo=github&logoColor=white"/>
</p>

---

## 🔧 Installation

### Option 1: Cloning the Repository

```bash
# 1️⃣ Clone the ThreatSentinel AI repository by Ashwanth
git clone https://github.com/Ashwanth/ThreatSentinel-AI.git

# 2️⃣ Navigate into the project directory
cd ThreatSentinel-AI

# 3️⃣ (Recommended) Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate        # Linux/macOS
# .venv\Scripts\activate.bat     # Windows CMD
# .venv\Scripts\Activate.ps1     # Windows PowerShell

# 4️⃣ Upgrade pip to the latest version
pip install --upgrade pip setuptools wheel

# 5️⃣ Install all required dependencies
pip install -r requirements.txt

# 6️⃣ (Optional) Install dev/test dependencies
pip install -r requirements-dev.txt

# 7️⃣ Set up your environment variables
cp .env.example .env
nano .env   # or: code .env / vim .env
```

### Option 2: Using Docker Container

```bash
# 🐳 Pull the latest ThreatSentinel AI image
docker pull ashwanth/threatsentinel-ai:latest

# 🚀 Run the container with your .env file
docker run -d \
  --name threatsentinel \
  -p 8501:8501 \
  --env-file .env \
  --restart unless-stopped \
  ashwanth/threatsentinel-ai:latest

# 📋 Check container logs
docker logs -f threatsentinel

# 🛑 Stop the container
docker stop threatsentinel && docker rm threatsentinel

# 🔨 Build from source
docker build -t ashwanth/threatsentinel-ai:dev .

# 🧹 Clean up old images
docker image prune -f
```

### Option 3: Kubernetes Enterprise Deployment

```bash
# ☸️ Add the Ashwanth System & Innovation Helm chart repository
helm repo add ashwanth-innovation https://charts.ashwanth-system.dev
helm repo update

# 🔍 Search available charts
helm search repo ashwanth-innovation

# 🚀 Install ThreatSentinel AI to your cluster
helm install threatsentinel ashwanth-innovation/threatsentinel-ai \
  --namespace security-tools \
  --create-namespace \
  --set replicaCount=3 \
  --set image.tag=0.15 \
  --set ingress.enabled=true \
  --set ingress.host=threatsentinel.yourdomain.com \
  --set secrets.openaiApiKey="$OPENAI_API_KEY" \
  --set secrets.anthropicApiKey="$ANTHROPIC_API_KEY" \
  --set secrets.googleApiKey="$GOOGLE_API_KEY"

# 📊 Check deployment status
kubectl get pods -n security-tools -l app=threatsentinel-ai
kubectl rollout status deployment/threatsentinel-ai -n security-tools

# 📋 View live logs
kubectl logs -f -n security-tools -l app=threatsentinel-ai

# 🔄 Upgrade to a new version
helm upgrade threatsentinel ashwanth-innovation/threatsentinel-ai \
  --namespace security-tools \
  --set image.tag=0.16

# 🧹 Uninstall
helm uninstall threatsentinel -n security-tools
```

---

## ⚙️ Configuration & Environment Variables

Copy `.env.example` to `.env` and populate all keys:

```env
# ============================================================
# 🔐 ThreatSentinel AI — Environment Configuration
#     Ashwanth System & Innovation
# ============================================================

# --- 🌐 LLM Provider API Keys ---
OPENAI_API_KEY=sk-your_openai_api_key_here
ANTHROPIC_API_KEY=sk-ant-your_anthropic_api_key_here
GOOGLE_API_KEY=your_google_ai_api_key_here
MISTRAL_API_KEY=your_mistral_api_key_here
GROQ_API_KEY=your_groq_api_key_here

# --- 🏢 Azure OpenAI (Enterprise) ---
AZURE_API_KEY=your_azure_openai_api_key
AZURE_API_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_DEPLOYMENT_NAME=gpt-5-deployment
AZURE_API_VERSION=2024-09-01-preview

# --- 🐙 GitHub Integration ---
GITHUB_API_KEY=ghp_your_github_personal_access_token

# --- 🤖 Local LLM Endpoints ---
OLLAMA_ENDPOINT=http://localhost:11434
LM_STUDIO_ENDPOINT=http://localhost:1234

# --- 🗄️ Database (Optional — Audit Logging) ---
POSTGRES_URL=postgresql://user:password@localhost:5432/threatsentinel_db
REDIS_URL=redis://localhost:6379/0

# --- 📡 Application Settings ---
APP_HOST=0.0.0.0
APP_PORT=8501
APP_ENV=production                # development | staging | production
LOG_LEVEL=INFO                    # DEBUG | INFO | WARNING | ERROR
MAX_TOKENS_STANDARD=32000
MAX_TOKENS_THINKING=48000

# --- 🔔 Alerting Integrations ---
SLACK_WEBHOOK_URL=https://hooks.slack.com/services/xxx/yyy/zzz
PAGERDUTY_API_KEY=your_pagerduty_api_key
OPSGENIE_API_KEY=your_opsgenie_api_key

# --- 📊 Observability ---
PROMETHEUS_ENABLED=true
GRAFANA_ADMIN_PASSWORD=your_grafana_password
ELASTICSEARCH_URL=http://localhost:9200

# ============================================================
# Built by Ashwanth — Ashwanth System & Innovation 🛡️
# ============================================================
```

---

## 🚀 Usage

### Option 1: Running the Streamlit App Locally

```bash
# 🌟 Launch ThreatSentinel AI UI
streamlit run main.py

# 🎨 Custom port and host
streamlit run main.py --server.port 8502 --server.address 0.0.0.0

# 🔇 Headless mode (no auto-browser)
streamlit run main.py --server.headless true

# 📈 Enable performance stats
streamlit run main.py --global.developmentMode false
```

Access at: **http://localhost:8501**

---

### Option 2: Using Docker Container

```bash
# ▶️ Standard run
docker run -p 8501:8501 --env-file .env ashwanth/threatsentinel-ai

# 🔁 Auto-restart production mode
docker run -d \
  --name ts-ai-prod \
  -p 8501:8501 \
  --env-file .env \
  --restart always \
  --memory="4g" \
  --cpus="2.0" \
  ashwanth/threatsentinel-ai:latest

# 🐳 Docker Compose (full stack)
docker compose up -d
docker compose logs -f threatsentinel
docker compose down --volumes
```

---

### Option 3: CLI / Headless Mode

```bash
# 🖥️ Run threat analysis from command line (no UI)
python cli.py \
  --mode stride \
  --input "Web app with OAuth2 login and PostgreSQL backend" \
  --model claude-opus-4-5 \
  --output report.md \
  --dread \
  --attack-tree

# 🔍 Analyze a GitHub repository
python cli.py \
  --mode github \
  --repo https://github.com/your-org/your-repo \
  --token $GITHUB_API_KEY \
  --model gpt-5-2 \
  --output repo_threat_model.md

# 📸 Multi-modal: analyze an architecture diagram image
python cli.py \
  --mode multimodal \
  --image ./diagrams/system-architecture.png \
  --model gemini-3-flash \
  --output vision_threat_model.md

# 🧪 Generate Gherkin test cases only
python cli.py \
  --mode gherkin \
  --threats ./threats.json \
  --output tests.feature
```

---

### Option 4: REST API Mode

```bash
# 🚀 Start the FastAPI server
uvicorn api.main:app --host 0.0.0.0 --port 8000 --workers 4

# Or with gunicorn for production
gunicorn api.main:app \
  -w 4 \
  -k uvicorn.workers.UvicornWorker \
  --bind 0.0.0.0:8000 \
  --timeout 120
```

```python
# 🐍 Python client example — Ashwanth System & Innovation
import httpx, json

client = httpx.Client(base_url="http://localhost:8000")

# POST /analyze — Full STRIDE threat model
response = client.post("/analyze", json={
    "description": "Microservice API with JWT auth, Redis cache, and PostgreSQL",
    "model": "claude-sonnet-4-5",
    "methodology": "STRIDE",
    "enable_dread": True,
    "enable_attack_tree": True,
    "enable_gherkin": True
})

result = response.json()
print(json.dumps(result["threat_model"], indent=2))
```

```bash
# 🌐 cURL example
curl -X POST http://localhost:8000/analyze \
  -H "Content-Type: application/json" \
  -H "X-API-Key: $THREATSENTINEL_API_KEY" \
  -d '{
    "description": "Cloud-native e-commerce app with Stripe payments",
    "model": "gpt-5-2",
    "methodology": "STRIDE",
    "enable_dread": true,
    "enable_attack_tree": true
  }' | jq .

# 📥 GET /health — Health check
curl http://localhost:8000/health

# 📊 GET /metrics — Prometheus metrics
curl http://localhost:8000/metrics
```

---

## 🧪 Advanced Usage & Commands

### 🔬 Running Security Scans Locally

```bash
# 🕵️ Static analysis with Bandit
bandit -r . -ll -ii -f json -o bandit-report.json
cat bandit-report.json | jq '.results[] | select(.issue_severity == "HIGH")'

# 🔍 Dependency vulnerability audit
pip-audit --requirement requirements.txt --format json > pip-audit-report.json
pip-audit --fix   # Auto-fix known vulnerabilities

# 🐳 Docker image scanning with Trivy
trivy image --severity HIGH,CRITICAL ashwanth/threatsentinel-ai:latest
trivy fs --security-checks vuln,secret,config .

# 🔐 Secret scanning with Gitleaks
gitleaks detect --source . --verbose --report-format json \
  --report-path gitleaks-report.json

# 🧬 CodeQL analysis (GitHub CLI)
gh codeql database create threatsentinel-db --language=python
gh codeql analyze threatsentinel-db \
  --format=sarif-latest \
  --output=codeql-results.sarif
```

### 🧪 Testing & Quality Assurance

```bash
# ✅ Run the full test suite
pytest tests/ -v --cov=src --cov-report=html --cov-report=term-missing

# 🏎️ Run tests in parallel
pytest tests/ -n auto --dist=loadbalance

# 🎯 Run only threat modeling unit tests
pytest tests/unit/test_threat_engine.py -v -k "stride or dread"

# 📸 Run integration tests (requires API keys)
pytest tests/integration/ -v --runintegration

# 🔁 Watch mode during development
ptw tests/ -- -v

# 📊 Generate coverage badge
coverage-badge -o coverage.svg -f

# 🎨 Code formatting & linting
black src/ tests/ --line-length 100
isort src/ tests/
flake8 src/ tests/ --max-line-length 100
mypy src/ --strict
```

### 📊 Benchmark Threat Analysis Performance

```bash
# ⏱️ Run performance benchmarks
python benchmarks/run_benchmarks.py \
  --models gpt-5-2,claude-opus-4-5,gemini-3-pro \
  --iterations 10 \
  --output benchmark_results.json

# 📈 Visualise benchmark results
python benchmarks/plot_results.py --input benchmark_results.json
```

### 🗄️ Database Management

```bash
# 🏗️ Initialize the database schema
python manage.py db init
python manage.py db migrate -m "Initial schema"
python manage.py db upgrade

# 📤 Export threat data
python manage.py export \
  --format json \
  --since 2025-01-01 \
  --output exports/threats_2025.json

# 🗑️ Purge old audit logs (older than 90 days)
python manage.py purge-logs --days 90

# 🔄 Backup database
pg_dump threatsentinel_db > backup_$(date +%Y%m%d).sql
```

---

## 🤖 AI Model Configuration

ThreatSentinel AI supports the following LLMs, curated by **Ashwanth System & Innovation**:

### 🟢 OpenAI Models

| Model | Context | Thinking | Use Case |
|---|---|---|---|
| `gpt-5-2` | 256k | ❌ | Fast general threat modeling |
| `gpt-5-2-reasoning` | 256k | ✅ | Deep chain-of-thought analysis |
| `o3` | 200k | ✅ | Complex multi-hop attack trees |
| `o4-mini` | 128k | ✅ | Cost-efficient at scale |

### 🟠 Anthropic Claude Models

| Model | Context | Thinking | Max Tokens |
|---|---|---|---|
| `claude-opus-4-5` | 200k | ✅ | 48k (thinking) |
| `claude-sonnet-4-5` | 200k | ✅ | 32k (standard) |
| `claude-haiku-4-5` | 200k | ❌ | 8k |

### 🔵 Google Gemini Models

| Model | Context | Thinking | Notes |
|---|---|---|---|
| `gemini-3-pro` | 1M | ✅ | Extended thinking preview |
| `gemini-3-flash` | 1M | ❌ | Ultra-fast, large diagram input |

### ⚫ Local / Self-Hosted

```bash
# 🦙 Pull and run models locally with Ollama
ollama pull llama3.3:70b
ollama pull mistral-large:latest
ollama pull codellama:34b
ollama pull deepseek-r1:70b

# 🏃 Serve Ollama
ollama serve

# 🔌 Configure ThreatSentinel to use Ollama
export OLLAMA_ENDPOINT=http://localhost:11434
export DEFAULT_MODEL=llama3.3:70b
streamlit run main.py
```

---

## 📊 Threat Analysis Pipeline

### 🔍 STRIDE Analysis — Python Example

```python
# threatsentinel/stride_analyzer.py
# Built by Ashwanth — Ashwanth System & Innovation 🛡️

from threatsentinel import ThreatSentinelAI, STRIDEModel, DREADScorer

# Initialize the engine
engine = ThreatSentinelAI(
    model="claude-opus-4-5",
    methodology="STRIDE",
    enable_thinking=True
)

# Define your system
system = STRIDEModel(
    name="Payment Gateway API",
    description="""
        RESTful API service handling payment processing.
        Uses OAuth2 + JWT for auth, PostgreSQL for storage,
        Redis for session management, deployed on AWS EKS.
    """,
    components=["API Gateway", "Auth Service", "Payment Processor",
                "Database", "Cache Layer", "Message Queue"],
    data_flows=["User → API", "API → DB", "API → Payment Provider"],
    trust_boundaries=["Internet → DMZ", "DMZ → Internal Network"]
)

# Run full analysis
result = engine.analyze(system)

# STRIDE threats
for threat in result.threats:
    print(f"[{threat.category}] {threat.title}")
    print(f"  Component: {threat.component}")
    print(f"  Description: {threat.description}")
    print(f"  DREAD Score: {threat.dread_score}/50")
    print(f"  Severity: {threat.severity}")
    print()

# DREAD scoring
scorer = DREADScorer()
scored = scorer.score_all(result.threats)
top_risks = sorted(scored, key=lambda t: t.dread_score, reverse=True)[:5]

print("🚨 Top 5 Critical Threats:")
for i, threat in enumerate(top_risks, 1):
    print(f"  {i}. {threat.title} — DREAD: {threat.dread_score}/50")

# Export
result.export("payment_gateway_threats.md", format="markdown")
result.export("payment_gateway_threats.json", format="json")
result.export("payment_gateway_threats.pdf", format="pdf")
```

### 🌳 Attack Tree — Python Example

```python
# Generate a visual attack tree
from threatsentinel import AttackTreeGenerator

generator = AttackTreeGenerator(model="gpt-5-2")

tree = generator.generate(
    goal="Gain unauthorized access to payment data",
    system_description="E-commerce platform with REST API and PostgreSQL",
    output_format="mermaid"  # or: 'json', 'graphviz', 'plantuml'
)

# Print Mermaid diagram source
print(tree.mermaid_source)

# Save to file
tree.save("attack_tree_payment.md")
```

### 🧪 Gherkin Test Generation

```python
# Generate BDD test cases from threats
from threatsentinel import GherkinTestGenerator

gen = GherkinTestGenerator(model="claude-sonnet-4-5")
tests = gen.generate_from_threats(result.threats)

for feature in tests.features:
    print(f"Feature: {feature.title}")
    for scenario in feature.scenarios:
        print(f"\n  Scenario: {scenario.title}")
        print(f"    Given {scenario.given}")
        print(f"    When {scenario.when}")
        print(f"    Then {scenario.then}")

# Save .feature file
tests.save("security_tests.feature")
```

---

## 🔐 Security Best Practices

### 🔑 Protecting Your API Keys

✅ **DO:**
- Enter API keys via the UI (session-scoped, never persisted to disk)
- Use `.env` files only on personal/developer machines
- Rotate API keys every 90 days
- Set strict spending limits in every LLM provider dashboard
- Use secrets management services (AWS Secrets Manager, HashiCorp Vault, Azure Key Vault) in production
- Enable MFA on all LLM provider accounts
- Regularly audit your API key usage logs

❌ **DON'T:**
- Commit `.env` files to version control (already in `.gitignore`)
- Share screenshots with API keys visible
- Log API keys in application logs
- Hardcode keys in source files — ever
- Use the same API key across development and production environments

---

### 🕵️ Data Privacy

When generating threat models, ThreatSentinel AI sends your application description to your chosen LLM provider. For highly sensitive systems or regulated environments:

```bash
# 🔒 Use local models via Ollama — zero data leaves your network
export OLLAMA_ENDPOINT=http://localhost:11434
export DEFAULT_MODEL=llama3.3:70b
streamlit run main.py --server.address 127.0.0.1
```

---

### 🏢 Team / Organization Deployments

```bash
# 🔒 Deploy behind Nginx reverse proxy with TLS
# /etc/nginx/sites-available/threatsentinel
server {
    listen 443 ssl;
    server_name threatsentinel.internal.yourcompany.com;
    ssl_certificate /etc/ssl/certs/threatsentinel.crt;
    ssl_certificate_key /etc/ssl/private/threatsentinel.key;
    ssl_protocols TLSv1.3;

    location / {
        proxy_pass http://127.0.0.1:8501;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_set_header Host $host;
        auth_basic "ThreatSentinel AI — Ashwanth System & Innovation";
        auth_basic_user_file /etc/nginx/.htpasswd;
    }
}
```

- 🔐 Add SSO authentication (Okta, Azure AD, Google Workspace)
- 🔑 Use a secrets manager (Vault, AWS Secrets Manager) for all API keys
- 🌐 Deploy behind internal VPN or Zero Trust Network Access (ZTNA)
- 📜 Review the [SECURITY.md](https://github.com/mrwadams/stride-gpt/blob/master/SECURITY.md) document

---

### 🔍 Dependency Security

```bash
# 🔎 Audit all Python dependencies
pip-audit --requirement requirements.txt

# 🔄 Check for outdated packages
pip list --outdated

# 🧬 Run SAST scan
bandit -r . -f html -o security_report.html

# 🐳 Scan Docker image
trivy image --severity CRITICAL,HIGH ashwanth/threatsentinel-ai:latest

# 🔐 Scan for exposed secrets
gitleaks detect --source . --verbose
```

- 🤖 Dependabot automatically opens PRs for dependency updates
- 🔄 Automated security scanning runs on every commit via GitHub Actions
- 🧪 SAST, SCA, container scanning, and secret detection all integrated in CI/CD

---

### 🚨 Reporting Security Issues

Found a vulnerability in ThreatSentinel AI? Please disclose responsibly:

1. **DO NOT** open a public GitHub issue for security vulnerabilities
2. Use GitHub's private [Security Advisory](https://github.com/Ashwanth/ThreatSentinel-AI/security/advisories) reporting feature
3. Email: `security@ashwanth-system.dev`
4. **Ashwanth** and the team at **Ashwanth System & Innovation** will acknowledge within **48 hours** and work with you on a coordinated disclosure

---

## 🏢 Enterprise Deployment

Want to customize ThreatSentinel AI for your organization? Check out the comprehensive [Operationalization Guide](https://github.com/mrwadams/stride-gpt/blob/master/docs/operationalization-guide.md) by **Ashwanth System & Innovation**:

- 🎯 Inject organizational security controls and compliance standards (ISO 27001, SOC 2, PCI DSS, HIPAA)
- 📋 Customize threat models with your specific regulatory requirements
- 🔧 Fork, brand, and deploy internally as your company's threat modeling platform
- 📊 Get context-aware, actionable threat models specific to your environment and tech stack
- 🔗 Integrate with JIRA, ServiceNow, Splunk, and other enterprise security tools
- 🏆 White-label licensing available — contact **Ashwanth** at [Ashwanth System & Innovation](https://sites.google.com/view/ashwanthtechsolution)

---

## 🧬 STRIDE & OWASP Integration

**ThreatSentinel AI** by **Ashwanth System & Innovation** covers the complete threat landscape:

### STRIDE Categories

| 🔤 Category | 📝 Description | 🎯 Examples |
|---|---|---|
| **S** — Spoofing | Impersonating a user or system | Stolen JWT, session hijacking |
| **T** — Tampering | Modifying data in transit or at rest | SQL injection, man-in-the-middle |
| **R** — Repudiation | Denying actions without proof | Missing audit logs |
| **I** — Info Disclosure | Exposing data to unauthorised parties | API key leaks, verbose errors |
| **D** — Denial of Service | Disrupting availability | DDoS, resource exhaustion |
| **E** — Elevation of Privilege | Gaining higher permissions | IDOR, privilege escalation |

### OWASP LLM Top 10 (GenAI)

| # | Threat | ThreatSentinel Coverage |
|---|---|---|
| LLM01 | Prompt Injection | ✅ Full detection + mitigations |
| LLM02 | Insecure Output Handling | ✅ |
| LLM03 | Training Data Poisoning | ✅ |
| LLM04 | Model Denial of Service | ✅ |
| LLM05 | Supply Chain Vulnerabilities | ✅ |
| LLM06 | Sensitive Information Disclosure | ✅ |
| LLM07 | Insecure Plugin Design | ✅ |
| LLM08 | Excessive Agency | ✅ |
| LLM09 | Overreliance | ✅ |
| LLM10 | Model Theft | ✅ |

---

## 🗺️ Roadmap

- [x] ✅ Multi-modal threat modelling (image/diagram input)
- [x] ✅ Auto-generate descriptions from GitHub README files
- [x] ✅ OWASP LLM Top 10 + Agentic ASI01–ASI10 support
- [x] ✅ Extended thinking mode (Claude 4.5, GPT-5.2, Gemini 3)
- [x] ✅ Automated CI/CD security scanning pipeline
- [ ] 🔄 Exportable reports — PDF, Word, including attack tree visuals
- [ ] 🔄 Helper wizard for writing effective application descriptions
- [ ] 🔄 Multi-language UI support (Tamil, Hindi, Spanish, French, German)
- [ ] 🔄 Native JIRA / ServiceNow ticket creation from threats
- [ ] 🔄 Real-time network packet analysis integration
- [ ] 🔄 VSCode extension — analyze code files directly in the editor
- [ ] 🔄 Mobile app — ThreatSentinel AI on iOS & Android

---

## 📋 Changelog

### 🏷️ Version 0.15 *(latest — Ashwanth System & Innovation)*

- **🤖 Agentic AI Application Support** — OWASP Top 10 for Agentic Applications (ASI01–ASI10)
- **🧬 Generative AI Application Support** — OWASP LLM Top 10 (LLM01–LLM10) integration
- **🏗️ MAESTRO-Inspired Architectural Pattern Detection** — RAG, multi-agent, MCP, memory, autonomous ops
  - RAG/Retrieval: vector store poisoning, embedding manipulation, cross-tenant leakage
  - Multi-Agent: impersonation, message tampering, cascading compromise
  - Code Execution: sandbox escape, container breakout, malicious code gen
  - Tool/MCP: rogue tool providers, supply chain attacks, confused deputy
  - Persistent Memory: memory poisoning, cross-session leakage, state manipulation
  - Autonomous Ops: rogue agent persistence, human oversight bypass, runaway loops
- **🔗 Cross-Layer Threat Analysis** — multi-component attack chain modeling
- **🟢 OpenAI GPT-5.2** — updated models with improved reasoning
- **🟠 Anthropic Claude 4.5** — Extended Thinking support; 32k/48k token limits
- **🔵 Google Gemini 3 Preview** — extended thinking mode enabled
- **⚫ Mistral Updates** — Large 3, Medium 3.1, Small 3.2, Magistral 1.2
- **🐛 Bug Fix** — threat model no longer disappears after download

### 🏷️ Version 0.14.1

- **🔒 Security Infrastructure** — GitHub Actions + Bandit + CodeQL + pip-audit + Gitleaks + Trivy
- **📖 Enterprise Operationalization Guide** — comprehensive org customization docs

### 🏷️ Version 0.14

- GPT-5 Series, Claude 4 Integration, GitHub Enterprise, DREAD Assessment Display improvements

### 🏷️ Version 0.13

- gpt-4.1, o3, o4-mini, Google GenAI SDK Migration, Enhanced Reasoning, Multi-Modal

### 🏷️ Version 0.12

- Claude 3.7 + thinking mode, GitHub repo analysis improvements, GPT-4.5 Preview

### 🏷️ Version 0.11

- LM Studio Server, Gemini attack trees, DeepSeek R1 via Groq, Dynamic Model Discovery

### 🏷️ Version 0.10

- GitHub Repository Analysis, Environment Variable support, UI enhancements

### 🏷️ Version 0.9

- Local model hosting via Ollama, Mistral Client v1.0 update

<details>
<summary>📜 Click to view earlier release notes (v0.1–v0.8.1)</summary>

### Version 0.8.1 — GPT4o mini, Gemini 1.5 Pro stable
### Version 0.8 — DREAD Risk Scoring, Gherkin Test Cases, UI Enhancements
### Version 0.7 — Multi-Modal Threat Modelling, Google AI / Gemini 1.5 Pro
### Version 0.6 — Mistral API Integration, Refined Prompts, Public Roadmap
### Version 0.5 — Docker Container Image on Docker Hub
### Version 0.4 — New GPT Models, Direct OpenAI API Calls, JSON Mode
### Version 0.3 — Threat Mitigations, Downloadable Output, Improved UI
### Version 0.2 — Attack Tree Generation, Mermaid.js Visualisation, GPT-4
### Version 0.1 — Initial release by **Ashwanth**, **Ashwanth System & Innovation**

</details>

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

```bash
# 🍴 Fork & clone
git clone https://github.com/YOUR_USERNAME/ThreatSentinel-AI.git
cd ThreatSentinel-AI

# 🌿 Create a feature branch
git checkout -b feature/your-feature-name

# 💾 Commit your changes
git add .
git commit -m "feat: add [your feature description]"

# 📤 Push and open a PR
git push origin feature/your-feature-name
```

> Please follow [Conventional Commits](https://www.conventionalcommits.org/) and ensure all tests pass (`pytest tests/`) before submitting.

Maintained by **Ashwanth** — [Ashwanth System & Innovation](https://sites.google.com/view/ashwanthtechsolution)

[![GitHub](https://img.shields.io/badge/GitHub-Ashwanth-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Ashwanth)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ashwanth-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/ashwanth)
[![Website](https://img.shields.io/badge/Website-Ashwanth%20System%20%26%20Innovation-8B5CF6?style=flat-square&logo=googlechrome&logoColor=white)](https://sites.google.com/view/ashwanthtechsolution)

---

## 📄 License

This project is available under multiple licenses depending on your use case:

| License | Use Case | Details |
|---------|----------|---------|
| [![MIT](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square&logo=opensourceinitiative&logoColor=white)](https://choosealicense.com/licenses/mit/) | Personal & Open Source | Free to use, modify, and distribute with attribution |
| [![Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-3B82F6?style=flat-square&logo=apache&logoColor=white)](https://choosealicense.com/licenses/apache-2.0/) | Commercial & Enterprise | Includes patent rights; requires NOTICE file preservation |
| [![CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-F97316?style=flat-square&logo=creativecommons&logoColor=white)](https://creativecommons.org/licenses/by-nc/4.0/) | Research & Academic | Non-commercial use with attribution |
| [![Proprietary](https://img.shields.io/badge/License-Proprietary%20%2F%20OEM-EF4444?style=flat-square&logo=key&logoColor=white)](mailto:ashwanth@system-innovation.dev) | White-Label / OEM | Contact **Ashwanth** for custom licensing terms |

> **Default:** Unless otherwise specified, this repository is distributed under the **MIT License**.
> For enterprise or OEM licensing, contact [Ashwanth System & Innovation](https://sites.google.com/view/ashwanthtechsolution).

---

<p align="center">
  <a href="https://sites.google.com/view/ashwanthtechsolution" target="_blank">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=140&section=footer&text=Ashwanth%20System%20%26%20Innovation&fontSize=24&fontColor=ffffff&fontAlignY=62&desc=Built%20with%20precision.%20Secured%20by%20design.%20%F0%9F%94%92&descSize=14&descAlignY=82&animation=twinkling"/>
      <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=140&section=footer&text=Ashwanth%20System%20%26%20Innovation&fontSize=24&fontColor=ffffff&fontAlignY=62&desc=Built%20with%20precision.%20Secured%20by%20design.%20%F0%9F%94%92&descSize=14&descAlignY=82&animation=twinkling" alt="Ashwanth System & Innovation" width="100%"/>
    </picture>
  </a>
</p>
