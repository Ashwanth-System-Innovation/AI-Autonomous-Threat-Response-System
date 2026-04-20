<h1 align="center">🔐 Security Policy</h1>

<h3 align="center">ThreatSentinel AI — Ashwanth System & Innovation</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Maintained%20by-Ashwanth-8B5CF6?style=for-the-badge&logo=github&logoColor=white"/>
  <img src="https://img.shields.io/badge/Security-Enterprise%20Grade-ef4444?style=for-the-badge&logo=shield&logoColor=white"/>
  <img src="https://img.shields.io/badge/Response%20SLA-48%20Hours-22c55e?style=for-the-badge&logo=clockify&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scanning-Automated%20CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"/>
  <img src="https://img.shields.io/badge/Zero%20Trust-Architecture-0F3460?style=for-the-badge&logo=security&logoColor=white"/>
</p>

---

> 🛡️ This document defines the security policy for **ThreatSentinel AI**, engineered and maintained by **Ashwanth** at **Ashwanth System & Innovation**. We treat security as a first-class engineering concern — not an afterthought.
>
> 📬 Contact: `ashwanth@system-innovation.dev` | 🌐 [Ashwanth System & Innovation](https://sites.google.com/view/ashwanthtechsolution)

---

## 📌 Table of Contents

- [✅ Supported Versions](#-supported-versions)
- [🚨 Reporting a Vulnerability](#-reporting-a-vulnerability)
- [🔑 API Key Management](#-api-key-management)
- [🏗️ Deployment Security](#️-deployment-security)
- [🔒 Zero Trust Architecture](#-zero-trust-architecture)
- [🧬 Secure Development Lifecycle](#-secure-development-lifecycle)
- [🤖 LLM-Specific Security Controls](#-llm-specific-security-controls)
- [🛡️ Threat Model for ThreatSentinel AI Itself](#️-threat-model-for-threatsentinel-ai-itself)
- [🔍 Automated Security Scanning](#-automated-security-scanning)
- [📊 Vulnerability Severity Matrix](#-vulnerability-severity-matrix)
- [⚖️ Responsible Use Policy](#️-responsible-use-policy)
- [⚠️ Known Security Considerations](#️-known-security-considerations)
- [🔄 Security Update Policy](#-security-update-policy)
- [📚 Additional Resources](#-additional-resources)
- [🏆 Acknowledgments](#-acknowledgments)

---

## ✅ Supported Versions

Security updates are released and maintained by **Ashwanth System & Innovation** for the following versions:

| Version | Supported | Notes |
|---------|-----------|-------|
| `latest` (master branch) | ✅ Active — Full security patches | **Always recommended** |
| `0.15.x` | ✅ Active — Patch support | Current stable |
| `0.14.x` | ⚠️ Critical patches only | Upgrade strongly advised |
| `0.13.x` | ❌ End of Life | No further updates |
| `< 0.13` | ❌ End of Life | Unsupported — upgrade immediately |

> ⚡ **Ashwanth System & Innovation** strongly recommends always running the latest version of ThreatSentinel AI. Security patches are backported to the current stable only.

---

## 🚨 Reporting a Vulnerability

**Ashwanth System & Innovation** takes every security report seriously. We operate a responsible disclosure programme. Please follow these steps:

### Step 1 — Do NOT open a public issue ❌

Never disclose security vulnerabilities in public GitHub issues, discussions, social media, or forums. This puts users at risk before a patch is available.

### Step 2 — Report Privately ✅

Choose one of the following secure channels:

| Channel | Details |
|---|---|
| 🔒 **GitHub Security Advisory** | [Open a private advisory](https://github.com/Ashwanth/ThreatSentinel-AI/security/advisories/new) *(preferred)* |
| 📧 **Email** | `ashwanth@system-innovation.dev` — PGP key available on request |
| 🌐 **Website** | [Ashwanth System & Innovation — Contact](https://sites.google.com/view/ashwanthtechsolution) |

### Step 3 — Include the Following in Your Report

```
Title:          [Brief one-line description]
Reporter:       Your name / handle (for acknowledgment, if desired)
Severity:       Critical / High / Medium / Low
Affected:       Version(s) affected
Component:      Module / file / endpoint affected

Description:
  A clear explanation of the vulnerability and its root cause.

Steps to Reproduce:
  1. ...
  2. ...
  3. ...

Proof of Concept:
  [Code, payload, curl command, or screenshot — if available]

Potential Impact:
  What an attacker could achieve by exploiting this.

Suggested Fix:
  [Optional, but appreciated]

Environment:
  OS, Python version, deployment method (Docker/local/K8s)
```

### Step 4 — Coordinated Disclosure Timeline

| Milestone | SLA |
|---|---|
| 🕐 Acknowledgment of receipt | Within **48 hours** |
| 🔍 Initial triage & severity assessment | Within **5 business days** |
| 🛠️ Patch development begins | Within **10 business days** (Critical: immediate) |
| 🚀 Patch released | Within **30 days** (Critical: within 7 days) |
| 📢 Public disclosure | After patch release + 14-day adoption window |

> All reports are handled personally by **Ashwanth** at **Ashwanth System & Innovation**. We will keep you updated throughout the process.

---

## 🔑 API Key Management

ThreatSentinel AI integrates with multiple LLM providers. Protecting your credentials is critical.

### ✅ DO

```bash
# Store keys in .env — never in source code
cp .env.example .env
chmod 600 .env          # Restrict file permissions (Linux/macOS)

# Use OS-level secrets managers in production
# AWS Secrets Manager
aws secretsmanager create-secret \
  --name "threatsentinel/prod/openai-key" \
  --secret-string '{"OPENAI_API_KEY":"sk-..."}'

# HashiCorp Vault
vault kv put secret/threatsentinel \
  OPENAI_API_KEY="sk-..." \
  ANTHROPIC_API_KEY="sk-ant-..."

# Kubernetes Secret
kubectl create secret generic threatsentinel-secrets \
  --from-env-file=.env \
  --namespace=security-tools

# Rotate keys every 90 days
# Ashwanth System & Innovation recommends automated rotation
```

### ❌ DON'T

```bash
# ❌ Hardcode keys in source files
OPENAI_API_KEY = "sk-abc123..."       # NEVER

# ❌ Commit .env to git
git add .env                           # BLOCKED by .gitignore — do not override

# ❌ Log API keys
print(f"Using key: {api_key}")         # NEVER log credentials

# ❌ Share keys in Slack / email / screenshots
# ❌ Use the same key across dev, staging, production
# ❌ Skip spending limits on LLM provider dashboards
```

### 🔑 Key Scoping Best Practices

| Provider | Scope Recommendation |
|---|---|
| OpenAI | Create org-level keys with project-scoped permissions |
| Anthropic | Use workspace keys; enable usage policies |
| Google AI | Use service accounts with minimal IAM roles |
| GitHub | Use fine-grained PATs scoped to specific repos/orgs |
| Azure OpenAI | Use Managed Identity in Azure deployments — no key needed |

---

## 🏗️ Deployment Security

### 🌐 Network Security — Nginx Reverse Proxy

```nginx
# 🔒 Hardened Nginx config — Ashwanth System & Innovation
server {
    listen 443 ssl http2;
    server_name threatsentinel.yourdomain.com;

    ssl_certificate     /etc/ssl/certs/threatsentinel.crt;
    ssl_certificate_key /etc/ssl/private/threatsentinel.key;
    ssl_protocols       TLSv1.3;
    ssl_ciphers         TLS_AES_256_GCM_SHA384:TLS_CHACHA20_POLY1305_SHA256;
    ssl_stapling        on;
    ssl_stapling_verify on;

    # HSTS — force HTTPS for 1 year
    add_header Strict-Transport-Security "max-age=31536000; includeSubDomains; preload" always;
    add_header X-Frame-Options             "DENY" always;
    add_header X-Content-Type-Options      "nosniff" always;
    add_header X-XSS-Protection            "1; mode=block" always;
    add_header Referrer-Policy             "strict-origin-when-cross-origin" always;
    add_header Content-Security-Policy     "default-src 'self'; script-src 'self' 'unsafe-inline';" always;

    # Rate limiting — 30 req/min per IP
    limit_req_zone $binary_remote_addr zone=threatsentinel:10m rate=30r/m;
    limit_req zone=threatsentinel burst=10 nodelay;

    location / {
        proxy_pass         http://127.0.0.1:8501;
        proxy_http_version 1.1;
        proxy_set_header   Upgrade $http_upgrade;
        proxy_set_header   Connection "upgrade";
        proxy_set_header   Host $host;
        proxy_set_header   X-Real-IP $remote_addr;
        proxy_read_timeout 300s;
        auth_basic         "ThreatSentinel AI — Ashwanth System & Innovation";
        auth_basic_user_file /etc/nginx/.htpasswd;
    }
}
server {
    listen 80;
    server_name threatsentinel.yourdomain.com;
    return 301 https://$host$request_uri;
}
```

### 🐳 Docker Security

```dockerfile
# ✅ Hardened Dockerfile — Ashwanth System & Innovation
FROM python:3.11-slim-bookworm

# Run as non-root user
RUN groupadd --gid 10001 ashwanth \
 && useradd --uid 10001 --gid ashwanth --shell /bin/bash --create-home ashwanth

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt \
 && pip install pip-audit \
 && pip-audit --requirement requirements.txt

COPY --chown=ashwanth:ashwanth . .
USER ashwanth

EXPOSE 8501
HEALTHCHECK --interval=30s --timeout=10s --retries=3 \
  CMD curl -f http://localhost:8501/_stcore/health || exit 1

ENTRYPOINT ["streamlit", "run", "main.py", \
            "--server.address=0.0.0.0", \
            "--server.headless=true"]
```

```yaml
# 🔒 docker-compose.yml — Security hardened — Ashwanth System & Innovation
services:
  threatsentinel:
    image: ashwanth/threatsentinel-ai:latest
    user: "10001:10001"
    read_only: true
    tmpfs: [/tmp]
    security_opt:
      - no-new-privileges:true
      - seccomp:seccomp-profile.json
    cap_drop: [ALL]
    cap_add: [NET_BIND_SERVICE]
    mem_limit: 4g
    cpus: "2.0"
    restart: unless-stopped
    env_file: .env
    ports:
      - "127.0.0.1:8501:8501"
```

### ☸️ Kubernetes Security

```yaml
# 🔒 K8s SecurityContext — Ashwanth System & Innovation
apiVersion: apps/v1
kind: Deployment
metadata:
  name: threatsentinel-ai
  namespace: security-tools
  labels:
    app: threatsentinel-ai
    owner: ashwanth
    org: ashwanth-system-innovation
spec:
  replicas: 3
  template:
    spec:
      serviceAccountName: threatsentinel-sa
      automountServiceAccountToken: false
      securityContext:
        runAsNonRoot: true
        runAsUser: 10001
        runAsGroup: 10001
        fsGroup: 10001
        seccompProfile:
          type: RuntimeDefault
      containers:
        - name: threatsentinel-ai
          image: ashwanth/threatsentinel-ai:0.15
          securityContext:
            allowPrivilegeEscalation: false
            readOnlyRootFilesystem: true
            capabilities:
              drop: ["ALL"]
          resources:
            requests: { memory: "1Gi", cpu: "500m" }
            limits:   { memory: "4Gi", cpu: "2000m" }
          envFrom:
            - secretRef:
                name: threatsentinel-secrets
```

---

## 🔒 Zero Trust Architecture

**Ashwanth System & Innovation** implements Zero Trust principles throughout ThreatSentinel AI:

```
┌─────────────────────────────────────────────────────────────────┐
│              ZERO TRUST SECURITY MODEL                          │
│              Ashwanth System & Innovation                       │
├─────────────────────────────────────────────────────────────────┤
│  NEVER TRUST, ALWAYS VERIFY                                     │
│                                                                 │
│  1. Identity Verification   →  Every request authenticated      │
│  2. Least Privilege         →  Minimal permissions per service  │
│  3. Micro-segmentation      →  Network isolation per component  │
│  4. Continuous Monitoring   →  All actions logged & analysed    │
│  5. Assume Breach           →  Defence in depth at every layer  │
│                                                                 │
│  User → [MFA] → [SSO/OIDC] → [API Gateway] → [Service]        │
│                     ↓                ↓                          │
│               [Audit Log]     [Rate Limiter]                    │
│                     ↓                ↓                          │
│              [SIEM / ELK]    [WAF / DDoS Shield]               │
└─────────────────────────────────────────────────────────────────┘
```

- 🔐 All internal service communication uses **mTLS**
- 🎫 Short-lived tokens (**15-minute JWT expiry**) with refresh rotation
- 🔍 Every API call produces a **structured audit log** entry
- 🚧 Network policies enforce **deny-by-default** at the pod level
- 🧱 WAF rules block OWASP Top 10 attack patterns at ingress

---

## 🧬 Secure Development Lifecycle

**Ashwanth** follows a rigorous SDL at **Ashwanth System & Innovation**:

```
  Plan → Design → Develop → Test → Release → Monitor
    ↓       ↓        ↓        ↓       ↓          ↓
 Threat  STRIDE   SAST     DAST   Signed     Runtime
 Model   Review   Bandit   OWASP  Commits    Defence
                  CodeQL   ZAP    Trivy      SIEM
                  Semgrep         SBOM       Alerts
```

### 🔄 Pre-Commit Security Hooks

```bash
# Install pre-commit hooks — Ashwanth System & Innovation
pip install pre-commit
pre-commit install

# .pre-commit-config.yaml covers:
#   - detect-secrets     (blocks API key commits)
#   - bandit             (Python SAST)
#   - gitleaks           (git history secret scan)
#   - black + isort      (code formatting)
#   - check-json / check-yaml

# Run manually on all files
pre-commit run --all-files
```

### 📋 SBOM Generation

```bash
# Generate SBOM — Ashwanth System & Innovation
pip install cyclonedx-bom
cyclonedx-py --output bom.json --format json
cyclonedx-py --output bom.xml  --format xml

# Verify SBOM against known CVEs
grype sbom:bom.json --fail-on high
```

### 🔏 Signed Releases

```bash
# All releases signed with Sigstore cosign — Ashwanth System & Innovation
cosign sign --key cosign.key ashwanth/threatsentinel-ai:0.15

# Verify a release
cosign verify --key cosign.pub ashwanth/threatsentinel-ai:0.15
```

---

## 🤖 LLM-Specific Security Controls

As an AI-powered tool, **ThreatSentinel AI** addresses LLM-specific threats — built by **Ashwanth System & Innovation**:

### 🧠 Prompt Injection Defence (OWASP LLM01)

```python
# threatsentinel/security/prompt_guard.py
# Ashwanth System & Innovation — LLM Input Sanitisation

import re

INJECTION_PATTERNS = [
    r"ignore (all |previous |above )?instructions",
    r"you are now (a |an )?",
    r"disregard (your |all )?",
    r"act as (a |an )?",
    r"jailbreak",
    r"DAN mode",
    r"pretend (you are|to be)",
    r"system prompt",
    r"<\|.*?\|>",
    r"\[INST\].*?\[/INST\]",
]

def sanitise_input(user_input: str) -> tuple[str, bool]:
    """
    Sanitise user input against prompt injection patterns.
    Returns (sanitised_input, was_flagged).
    Built by Ashwanth — Ashwanth System & Innovation.
    """
    flagged = False
    sanitised = user_input.strip()

    for pattern in INJECTION_PATTERNS:
        if re.search(pattern, sanitised, re.IGNORECASE):
            flagged = True
            _log_security_event("PROMPT_INJECTION_ATTEMPT", sanitised)
            sanitised = re.sub(pattern, "[REDACTED]", sanitised, flags=re.IGNORECASE)

    # Enforce max input length (prevent token flooding)
    if len(sanitised) > 8000:
        sanitised = sanitised[:8000]
        flagged = True

    return sanitised, flagged

def _log_security_event(event_type: str, content: str) -> None:
    import structlog
    log = structlog.get_logger()
    log.warning(
        "security_event",
        event_type=event_type,
        content_preview=content[:200],
        org="Ashwanth System & Innovation"
    )
```

### 🔏 LLM Output Validation (OWASP LLM02)

```python
# threatsentinel/security/output_validator.py
# Ashwanth System & Innovation — LLM Output Sanitisation

import bleach
from pydantic import BaseModel, validator
from typing import Optional

class ThreatModelOutput(BaseModel):
    threats: list[dict]
    dread_scores: dict
    mitigations: list[str]
    attack_tree: Optional[str]

    @validator("attack_tree")
    def sanitise_mermaid(cls, v: Optional[str]) -> Optional[str]:
        """Strip any script injection from Mermaid diagram source."""
        if v is None:
            return v
        return bleach.clean(v, tags=[], strip=True)

    @validator("mitigations", each_item=True)
    def sanitise_mitigation(cls, v: str) -> str:
        return bleach.clean(v, tags=["strong", "em", "code"], strip=True)
```

### 🚦 Rate Limiting & Abuse Prevention

```python
# threatsentinel/security/rate_limiter.py
# Ashwanth System & Innovation — Token-bucket Rate Limiter

import time, redis
from functools import wraps

r = redis.Redis.from_url("redis://localhost:6379/0")

def rate_limit(max_calls: int, window_seconds: int):
    """
    Per-user rate limiter for LLM API calls.
    Prevents abuse and runaway API costs.
    Maintained by Ashwanth — Ashwanth System & Innovation.
    """
    def decorator(func):
        @wraps(func)
        def wrapper(*args, user_id: str, **kwargs):
            key = f"rate_limit:{user_id}:{func.__name__}"
            pipe = r.pipeline()
            now = time.time()
            pipe.zremrangebyscore(key, 0, now - window_seconds)
            pipe.zcard(key)
            pipe.zadd(key, {str(now): now})
            pipe.expire(key, window_seconds)
            _, call_count, *_ = pipe.execute()
            if call_count >= max_calls:
                raise RateLimitExceeded(
                    f"Rate limit: {max_calls} calls per {window_seconds}s. "
                    f"Contact Ashwanth System & Innovation."
                )
            return func(*args, user_id=user_id, **kwargs)
        return wrapper
    return decorator

class RateLimitExceeded(Exception):
    pass
```

### 🔍 PII Detection Before LLM Submission (OWASP LLM06)

```python
# threatsentinel/security/pii_detector.py
# Ashwanth System & Innovation — PII Scrubber

import re

PII_PATTERNS = {
    "email":       r"[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+",
    "ipv4":        r"\b(?:\d{1,3}\.){3}\d{1,3}\b",
    "api_key":     r"(sk-[a-zA-Z0-9]{32,}|sk-ant-[a-zA-Z0-9\-]{32,})",
    "aws_key":     r"AKIA[0-9A-Z]{16}",
    "credit_card": r"\b(?:\d[ -]?){13,16}\b",
    "phone":       r"\+?[\d\s\-().]{10,15}",
    "jwt":         r"eyJ[A-Za-z0-9_-]+\.eyJ[A-Za-z0-9_-]+\.[A-Za-z0-9_-]+",
}

def scrub_pii(text: str) -> tuple[str, list[str]]:
    """
    Detect and redact PII before sending to LLM providers.
    Built by Ashwanth — Ashwanth System & Innovation.
    """
    found_types = []
    scrubbed = text
    for pii_type, pattern in PII_PATTERNS.items():
        if re.search(pattern, scrubbed):
            found_types.append(pii_type)
            scrubbed = re.sub(pattern, f"[REDACTED_{pii_type.upper()}]", scrubbed)
    return scrubbed, found_types
```

---

## 🛡️ Threat Model for ThreatSentinel AI Itself

**Ashwanth System & Innovation** applies STRIDE analysis to ThreatSentinel AI's own architecture:

| STRIDE | Threat | Control |
|--------|--------|---------|
| **S** Spoofing | Attacker impersonates a valid user session | JWT + MFA + short-lived tokens |
| **T** Tampering | Malicious LLM prompt modifies threat report | Output validation + signed reports |
| **R** Repudiation | User denies submitting a malicious input | Structured audit log with user ID + timestamp |
| **I** Info Disclosure | API keys leaked via logs or error messages | Secrets scrubbing in all log outputs |
| **D** Denial of Service | Token flooding exhausts LLM API quota | Rate limiting + token budget caps |
| **E** Elevation of Privilege | Prompt injection grants admin capabilities | Input sanitisation + least-privilege system prompts |
| **LLM01** | Prompt injection via user input | Regex guard + semantic injection detection |
| **LLM02** | Insecure output rendered as HTML | Bleach sanitisation on all outputs |
| **LLM06** | Sensitive data exfiltration in prompts | PII detector before every API submission |
| **LLM08** | Excessive agency / autonomous actions | All LLM actions require human confirmation |

---

## 🔍 Automated Security Scanning

Every commit triggers the full **Ashwanth System & Innovation** security pipeline:

### CI/CD Security Gates

```yaml
# .github/workflows/security.yml
# Ashwanth System & Innovation — Automated Security Pipeline

name: 🔐 Security Scan — Ashwanth System & Innovation

on:
  push:
    branches: [master, develop]
  pull_request:
    branches: [master]
  schedule:
    - cron: "0 9 * * 1"   # Every Monday 09:00 UTC

jobs:
  sast-bandit:
    name: 🐍 Python SAST (Bandit)
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: pip install bandit[toml]
      - run: bandit -r . -ll -ii -f json -o bandit-report.json
      - uses: actions/upload-artifact@v4
        with: { name: bandit-report, path: bandit-report.json }

  codeql:
    name: 🔬 Semantic Analysis (CodeQL)
    runs-on: ubuntu-latest
    permissions: { security-events: write }
    steps:
      - uses: actions/checkout@v4
      - uses: github/codeql-action/init@v3
        with: { languages: python, queries: security-and-quality }
      - uses: github/codeql-action/analyze@v3

  dependency-audit:
    name: 📦 Dependency CVE Scan
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: pip install pip-audit safety
      - run: pip-audit --requirement requirements.txt --format json -o pip-audit.json
      - run: safety check --full-report -r requirements.txt

  secret-scan:
    name: 🔐 Secret Detection (Gitleaks)
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with: { fetch-depth: 0 }
      - uses: gitleaks/gitleaks-action@v2
        env: { GITHUB_TOKEN: "${{ secrets.GITHUB_TOKEN }}" }

  container-scan:
    name: 🐳 Container Scan (Trivy)
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: docker build -t ashwanth/threatsentinel-ai:test .
      - uses: aquasecurity/trivy-action@master
        with:
          image-ref: ashwanth/threatsentinel-ai:test
          format: sarif
          output: trivy-results.sarif
          severity: CRITICAL,HIGH
          exit-code: "1"

  semgrep:
    name: 🧬 Advanced SAST (Semgrep)
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: semgrep/semgrep-action@v1
        with:
          config: "p/python p/secrets p/owasp-top-ten"

  sbom:
    name: 📋 Generate SBOM (CycloneDX)
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: pip install cyclonedx-bom && cyclonedx-py --output bom.json
      - uses: actions/upload-artifact@v4
        with: { name: sbom-cyclonedx, path: bom.json }
```

### Running All Scans Locally

```bash
# 🔒 Full local security audit — Ashwanth System & Innovation

# 1. Python SAST
pip install bandit semgrep
bandit -r . -ll -ii -f txt
semgrep --config=p/owasp-top-ten .

# 2. Dependency CVE scan
pip install pip-audit safety
pip-audit --requirement requirements.txt
safety check -r requirements.txt --full-report

# 3. Secret scanning
brew install gitleaks
gitleaks detect --source . --verbose --report-format json

# 4. Container scanning
brew install trivy
trivy image ashwanth/threatsentinel-ai:latest --severity HIGH,CRITICAL
trivy fs . --security-checks vuln,secret,config

# 5. SBOM generation
pip install cyclonedx-bom
cyclonedx-py --output bom.json

# 6. Run all hooks at once
pip install pre-commit && pre-commit run --all-files
```

---

## 📊 Vulnerability Severity Matrix

**Ashwanth System & Innovation** follows this response matrix:

| Severity | CVSS Score | Response Time | Action |
|----------|-----------|---------------|--------|
| 🔴 **Critical** | 9.0–10.0 | Same day | Emergency patch + hotfix release |
| 🟠 **High** | 7.0–8.9 | Within 7 days | Patch release |
| 🟡 **Medium** | 4.0–6.9 | Next scheduled release | Evaluated and patched |
| 🟢 **Low** | 0.1–3.9 | Best effort | Reviewed; patched when feasible |
| ℹ️ **Informational** | N/A | Backlog | Documented; no immediate action |

---

## ⚖️ Responsible Use Policy

ThreatSentinel AI is developed by **Ashwanth System & Innovation** exclusively for **legitimate, defensive security purposes**. By using this software you agree to:

### ✅ Permitted Uses

- 🛡️ Threat modeling to improve application security posture
- 🏗️ Security architecture design and review
- 📊 Risk assessment and mitigation planning
- 🧪 Security testing of systems you own or have permission to test
- 📚 Security education and research

### ❌ Prohibited Uses

- 🚫 Using generated threat intelligence for offensive or malicious purposes
- 🚫 Targeting systems without explicit written authorization
- 🚫 Violating any local, national, or international law
- 🚫 Circumventing LLM safety controls or misusing the AI engine
- 🚫 Submitting real, sensitive production system details to third-party LLM APIs

> Violations may result in account suspension and legal action. Report misuse to `ashwanth@system-innovation.dev`.

---

## ⚠️ Known Security Considerations

### 1. 🤖 LLM Provider Data Sharing

Threat model inputs are sent to your chosen LLM provider (OpenAI, Anthropic, Google, etc.). These providers may log requests per their own data retention policies.

**Recommendation by Ashwanth System & Innovation:**
- Use sanitised / generic system descriptions — never real IP addresses, credentials, or internal hostnames
- For maximum privacy, use **local models via Ollama** — zero data leaves your network:

```bash
ollama pull llama3.3:70b
export OLLAMA_ENDPOINT=http://localhost:11434
streamlit run main.py
```

### 2. 🔒 Streamlit Session State

- Session data is stored in browser memory only
- Clear sensitive inputs when analysis is complete
- Close browser tabs after use in shared environments

### 3. 📄 Output Sensitivity

Generated threat models contain security-sensitive information about your system. **Ashwanth System & Innovation** recommends:
- Storing downloaded reports in encrypted storage
- Classifying outputs as **CONFIDENTIAL — INTERNAL USE ONLY**
- Restricting sharing to authorised security personnel

### 4. 🚦 Rate Limiting for Public Deployments

If exposing ThreatSentinel AI publicly, implement rate limiting:

```python
# Add to your deployment — Ashwanth System & Innovation
from slowapi import Limiter
from slowapi.util import get_remote_address

limiter = Limiter(key_func=get_remote_address)

@app.get("/analyze")
@limiter.limit("10/minute")
async def analyze(request: Request):
    ...
```

### 5. 🧬 AI-Generated Output Disclaimer

Threat models are AI-generated and must be reviewed by qualified security professionals. **Ashwanth System & Innovation** recommends using ThreatSentinel AI output as a starting point, not a complete or final security analysis.

---

## 🔄 Security Update Policy

Security updates from **Ashwanth System & Innovation** are released as patch versions and documented in the changelog. Stay protected:

```bash
# Watch for security advisories
gh repo watch Ashwanth/ThreatSentinel-AI

# Always update to latest
git pull origin master
pip install --upgrade -r requirements.txt

# Check your current version
python -c "import threatsentinel; print(threatsentinel.__version__)"
```

---

## 📚 Additional Resources

| Resource | Link |
|---|---|
| 🔟 OWASP Top 10 | [owasp.org/www-project-top-ten](https://owasp.org/www-project-top-ten/) |
| 🤖 OWASP LLM Top 10 | [owasp.org/www-project-top-10-for-large-language-model-applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) |
| 🧠 STRIDE Methodology | [Microsoft Threat Modeling](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats) |
| 🏗️ MITRE ATT&CK | [attack.mitre.org](https://attack.mitre.org/) |
| 🐳 Docker Security | [docs.docker.com/engine/security](https://docs.docker.com/engine/security/) |
| ☸️ K8s Security | [kubernetes.io/docs/concepts/security](https://kubernetes.io/docs/concepts/security/) |
| 🔐 Streamlit Security | [docs.streamlit.io](https://docs.streamlit.io/) |
| 🏛️ NIST Cybersecurity Framework | [nist.gov/cyberframework](https://www.nist.gov/cyberframework) |

---

## 🏆 Acknowledgments

**Ashwanth System & Innovation** gratefully acknowledges the security research community's efforts in responsibly disclosing vulnerabilities. Contributors who report valid security issues will be credited (with permission) in our security advisories.

Special thanks to all researchers who help make ThreatSentinel AI more secure for everyone.

---

<p align="center">
  <a href="https://sites.google.com/view/ashwanthtechsolution" target="_blank">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&text=Ashwanth%20System%20%26%20Innovation&fontSize=22&fontColor=ffffff&fontAlignY=65&desc=Built%20with%20precision.%20Secured%20by%20design.%20%F0%9F%94%92&descSize=13&descAlignY=85&animation=twinkling" width="100%"/>
  </a>
</p>
