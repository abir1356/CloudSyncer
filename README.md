# 🌩️ CloudSyncer – Plateforme GitOps Multi-Cloud

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/abir1356/CloudSyncer/ci.yml?branch=main)
![License](https://img.shields.io/github/license/abir1356/CloudSyncer)

---

## 🔹 Description

**CloudSyncer** est un projet DevOps évolutif visant à construire une plateforme capable d’automatiser le provisionnement d’infrastructure, le déploiement d’applications et la supervision multi-environnement.

Grâce à **Docker**, **GitHub Actions**, **Kubernetes**, **Argo CD**, **Terraform**, **Prometheus** et **Grafana**, CloudSyncer a pour objectif de permettre :

- la construction et le test automatisé d’une application ;
- la conteneurisation et l’exécution dans un environnement isolé ;
- le déploiement continu via GitOps ;
- la supervision des services ;
- la gestion de plusieurs environnements : `dev`, `staging`, `prod` ;
- une évolution progressive vers une architecture multi-cloud réaliste.

Ce projet est conçu comme une **plateforme DevOps complète**, construite progressivement, avec une approche réaliste et démontrable devant un jury.

---

## 🔹 Fonctionnalités principales

### MVP (actuel)
- Environnement de test local avec Docker
- Application FastAPI conteneurisée
- Tests automatisés avec pytest
- Exécution dans un environnement isolé

### 🚧 En cours
- Pipeline CI/CD avec GitHub Actions

### 🔜 À venir
- Déploiement GitOps via Argo CD
- Kubernetes
- Monitoring avec Prometheus & Grafana
- Infrastructure as Code avec Terraform
- Multi-environnement
- Multi-cloud

---

## 🔹 Architecture globale

```mermaid
graph LR
    A[Code source App] --> B[GitHub Actions CI/CD]
    B --> C[Docker Registry]
    B --> D[GitOps Repo]
    D --> E[Argo CD]
    E --> F[Kubernetes Cluster]
    F --> G[Prometheus]
    F --> H[Grafana]
    F --> I[Utilisateurs / Développeurs]