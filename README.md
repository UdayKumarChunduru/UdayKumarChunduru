## Uday Kumar Chunduru

DevOps Engineer based in Hyderabad, India. I work on the infrastructure and automation side of software delivery: building CI/CD pipelines, containerising services onto Kubernetes, and provisioning cloud environments with Terraform so teams can deploy without manual steps.

My background is 2.4 years of enterprise DevOps work on a large-scale Java microservice platform for a US telecom client, where the day-to-day involved GitHub Actions pipelines, Amazon EKS cluster management, Argo CD GitOps deployments, Terraform IaC, and SonarQube and Trivy as security gates in the delivery pipeline.

Currently building personal projects across DevSecOps platform engineering, AWS-native CI/CD, AI-assisted cost optimization and Kubernetes troubleshooting, and working toward AWS certification.

---

### What I work with
**Cloud and Infrastructure**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)

**Containers and Orchestration**
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white)
![ArgoCD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=flat-square&logo=argo&logoColor=white)

**CI/CD and GitOps**
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)

**Security and DevSecOps**
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=flat-square&logo=sonarqube&logoColor=white)
![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat-square&logo=aqua&logoColor=white)
![Snyk](https://img.shields.io/badge/Snyk-4C4A73?style=flat-square&logo=snyk&logoColor=white)
![Falco](https://img.shields.io/badge/Falco-00ACD7?style=flat-square&logoColor=white)
![Kyverno](https://img.shields.io/badge/Kyverno-1A6078?style=flat-square&logoColor=white)

**Monitoring and Observability**
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

**AI and Automation**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![OpenRouter](https://img.shields.io/badge/Open_Router_API-000000?style=flat-square&logoColor=white)

**Scripting and OS**
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Version Control and Collaboration**
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=flat-square&logo=confluence&logoColor=white)

---

### Projects
**[Automated DevSecOps Security Gate for Kubernetes Deployments](https://github.com/udaykumarchunduru/devsecops-cicd-pipeline)**
Jenkins pipeline enforcing a zero-Critical policy across Gitleaks, SonarQube, Snyk and Trivy application scans, extended to Terraform and Ansible infrastructure code with Checkov, tflint and ansible-lint. Provisions EKS, Secrets Manager and EFS with Terraform and Ansible, enforces Kyverno admission policies and Falco runtime detection with SNS-triggered Lambda pod remediation, and secures all access through IRSA and SSM Session Manager, zero static credentials, zero SSH.

Stack: Jenkins · SonarQube · Snyk · Trivy · Gitleaks · Checkov · tflint · ansible-lint · Docker · Kubernetes (EKS) · Kyverno · Falco · Terraform · Ansible · AWS (EC2, IAM/IRSA, Secrets Manager, EFS, CodeBuild, SNS, Lambda, SSM) · GitHub Actions

---

**[AI-Assisted Kubernetes Troubleshooter](https://github.com/udaykumarchunduru/k8s-ai-troubleshooter)**
JWT-authenticated FastAPI agent that collects pod logs, events and deployment status through the Kubernetes API, detects 14 failure patterns including CrashLoopBackOff, OOMKilled and ImagePullBackOff, and generates root cause analysis with kubectl fix commands through a pluggable OpenRouter, Ollama and Bedrock LLM backend. Packaged as a Helm chart with least-privilege read-only RBAC, HPA and PDB, a Redis-backed job queue, and Prometheus and Grafana dashboards tracking investigation and LLM metrics.

Stack: Python · FastAPI · Kubernetes · Helm · Docker · Redis · Prometheus · Grafana · OpenRouter API · Ollama · AWS Bedrock · GitHub Actions

---

**[AI-Powered AWS Cost Optimizer](https://github.com/udaykumarchunduru/aws-cost-optimizer-ai)**
Plugin-based cost optimizer using boto3 and a thread pool to run 10 auto-discovered scanners in parallel across Cost Explorer-identified regions, flagging idle EC2, RDS, EBS, NAT Gateway and Secrets Manager waste. Generates AI remediation guidance via Bedrock and Ollama, automates nightly idle-shutdown and weekly SES cost-report Lambdas on EventBridge schedules, and caches AWS Pricing API lookups to avoid throttling across parallel regional scans.

Stack: Python · FastAPI · boto3 · Terraform · AWS Lambda · Bedrock · DynamoDB · CloudWatch · SES · EventBridge · GitHub Actions · Docker · Ollama

---

**[End-to-End CI/CD Pipeline for Flask Application on AWS Code Services](https://github.com/udaykumarchunduru/aws-codepipeline-terraform)**
Flask app deployed to an Auto Scaling Group behind a WAF-protected, HTTPS Application Load Balancer using CodePipeline, CodeBuild and CodeDeploy, with CloudWatch alarms triggering automatic rollback on failed traffic-controlled rollouts. Terraform changes ship through GitHub Actions using OIDC federation with zero stored AWS credentials, gating pull requests on fmt, validate and Checkov scans ahead of an approval-gated production apply.

Stack: AWS CodePipeline · CodeBuild · CodeDeploy · Auto Scaling · Application Load Balancer · WAF · IAM (OIDC) · S3 · DynamoDB · CloudWatch · SNS · Terraform · GitHub Actions · Checkov

---

### GitHub stats
<img src="metrics/stats.svg" alt="GitHub Stats" height="70%" width="70%">

---

### Languages
<img src="metrics/languages.svg" alt="Top Languages" height="70%" width="70%">

---

### Connect

[LinkedIn](https://www.linkedin.com/in/udaykumarchunduru) &nbsp;·&nbsp; [GitHub](https://github.com/udaykumarchunduru) &nbsp;·&nbsp; [Telegram](https://t.me/fortecipher)
