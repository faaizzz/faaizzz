<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=180&section=header&text=Faaiz%20K%20Rissad&fontColor=ffffff&fontSize=44&fontAlignY=38&desc=GenAI%20Platform%20Engineer&descAlignY=60" alt="Faaiz K Rissad, GenAI Platform Engineer"/>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=2C9CDB&center=true&vCenter=true&width=640&lines=I+build+governed+LLM+gateways;Azure+AI+Foundry+%C2%B7+AKS+%C2%B7+Terraform;Turning+news+feeds+into+AI+podcasts;Terraform+plans+the+contract%2C+the+gateway+enforces+it" alt="I build governed LLM gateways. Azure AI Foundry, AKS, Terraform. Turning news feeds into AI podcasts."/>
</p>

<p align="center">
  <a href="https://faaizzz.github.io"><img src="https://img.shields.io/badge/Website-faaizzz.github.io-2C9CDB?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website"/></a>
  <a href="https://www.linkedin.com/in/faaiz-rissad/"><img src="https://img.shields.io/badge/LinkedIn-faaiz--rissad-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
</p>

### `$ kubectl describe engineer faaiz`

Eleven years in, I spend my days on the plumbing that makes LLMs safe to hand to a whole company: gateways that decide who may call which model, what it costs, and what gets logged. If I were one of my own gateway's use cases, my onboarding file would look like this:

```yaml
# usecases/faaiz.yaml
metadata:
  id: faaiz-k-rissad
  role: GenAI Platform Engineer
  location: Mülheim an der Ruhr, Germany 🇩🇪
spec:
  modelRoutes: [azure-ai-foundry, azure-openai, amazon-bedrock, litellm]
  runtime: [aks, ecs-fargate, docker]
  provisioning: terraform        # never click-ops
  delivery: gitops               # argocd, merge to deploy
  observability:
    tier: everything             # langfuse traces, cost per call
  certifications: [azure-ai-engineer-associate]
  budget:
    coffee: unlimited            # ASSUMPTION, not an approved budget
```

---

## 🛡️ [AWS AI Gateway with LiteLLM](https://github.com/faaizzz/aws-ai-gateway-with-litellm-poc)

> A product team onboards an AI use case by editing **one YAML file** and opening a pull request.

Terraform turns that file into least-privilege IAM, an approved model route, a route-scoped gateway key and a budget. Bad requests never reach a model: a wrong route or data classification fails at `terraform plan`, and at runtime a model override, a bad key or an empty budget is refused.

```mermaid
flowchart LR
    A["📝 usecase.yaml<br/>(pull request)"] --> B["🏗️ Terraform<br/>IAM · key · budget"]
    B --> C["🚪 LiteLLM gateway<br/>ECS Fargate"]
    App["📱 App + gateway key"] --> C
    C -->|approved route only| D["🧠 Amazon Bedrock<br/>EU"]
    C -.->|traces| E["🔭 Langfuse"]
```

`Terraform` `LiteLLM` `Amazon Bedrock` `ECS Fargate` `Langfuse` `GitHub Actions` · 31 Terraform test runs, tflint and trivy on every PR

## 🎙️ [BYOP — Bring Your Own Podcast](https://github.com/faaizzz/Bring-Your-Own-Podcast-BYOP)

> **Your sources in, a podcast out.**

A self-hosted app that reads the feeds, pages and searches you care about and turns them into a scheduled, multi-speaker AI podcast with its own RSS feed, playable in Apple Podcasts or Spotify. Bring any LLM and voice provider, or run it all locally for free.

```mermaid
flowchart LR
    S["📰 RSS · pages<br/>web search"] --> R["🧹 collect, dedupe<br/>and rank stories"]
    R --> W["✍️ LLM writes<br/>a dialogue"]
    W --> V["🗣️ a voice<br/>per speaker"]
    V --> M["🎚️ ffmpeg mix<br/>-16 LUFS"]
    M --> F["📡 your RSS feed"]
```

`Python` `FastAPI` `Celery` `PostgreSQL` `React` `TypeScript` `Docker` · cost tracking per call, Langfuse tracing, Playwright end-to-end tests

---

## 🧰 Toolbox

<p align="center">
  <img src="https://skillicons.dev/icons?i=azure,aws,terraform,kubernetes,docker,python,fastapi,ts,react,postgres,redis,githubactions,cs,dotnet&perline=7" alt="Azure, AWS, Terraform, Kubernetes, Docker, Python, FastAPI, TypeScript, React, PostgreSQL, Redis, GitHub Actions, C#, .NET"/>
</p>

<p align="center"><sub>Also: Azure AI Foundry · Azure API Management · ArgoCD · LangChain / LangGraph · LiteLLM · Langfuse</sub></p>

## 🐍 Contributions, eaten daily

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/faaizzz/faaizzz/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/faaizzz/faaizzz/output/github-snake.svg"/>
  <img alt="A snake eating my contribution graph" src="https://raw.githubusercontent.com/faaizzz/faaizzz/output/github-snake.svg"/>
</picture>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=100&section=footer" alt=""/>
