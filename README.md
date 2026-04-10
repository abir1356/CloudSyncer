
# 🌩️ CloudSyncer – Plateforme GitOps Multi-Cloud

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/abir1356/cloudsyncer/ci.yml?branch=main)  
![Docker Pulls](https://img.shields.io/docker/pulls/<username>/cloudsyncer)  
![License](https://img.shields.io/github/license/<username>/cloudsyncer)  

---

## 🔹 Description

**CloudSyncer** est une plateforme DevOps avancée qui automatise le provisionnement d’infrastructure, le déploiement d’applications et la supervision multi-environnement et multi-cloud.  

Grâce à **Terraform**, **Docker**, **Kubernetes**, **Argo CD** et **GitHub Actions**, CloudSyncer permet de :  

- Créer et gérer automatiquement des clusters Kubernetes et l’infrastructure cloud.  
- Construire et stocker des images Docker dans une registry.  
- Déployer les applications automatiquement via GitOps.  
- Superviser les services avec **Prometheus** et **Grafana**.  
- Gérer plusieurs environnements : dev, staging, prod.  
- Préparer une approche multi-cloud réaliste (local + cloud).  

Ce projet démontre une approche de **plateforme DevOps complète**, allant de l’infrastructure à l’observabilité, et est conçu pour être **réaliste pour un étudiant motivé tout en impressionnant un jury**.  

---

## 🔹 Fonctionnalités principales

- Provisionnement automatisé de l’infrastructure avec Terraform (MVP).  
- Déploiement GitOps via Argo CD (MVP).  
- Gestion multi-environnement : dev, staging, prod (MVP).  
- CI/CD avec GitHub Actions : lint, tests, build Docker, push image, mise à jour GitOps (MVP).  
- Supervision avec Prometheus & Grafana (MVP).  
- Rollback automatique (Bonus).  
- Self-service deployment via templates ou dashboard interne (Bonus).  
- Multi-cloud AWS + Azure (Bonus).  

---

## 🔹 Architecture Globale

```mermaid
graph LR
    A[Code source App] --> B[GitHub Actions CI/CD]
    B --> C[Docker Registry]
    B --> D[GitOps Repo]
    D --> E[Argo CD]
    E --> F[Kubernetes Cluster]
    F --> G[Prometheus]
    F --> H[Grafana]
    F --> I[Users / Devs]
    

    ---

## 🔹 État actuel du projet

Le projet CloudSyncer est en cours de construction progressive selon une approche DevOps.

### ✔️ Implémenté (Bloc 2 – Environnement de test)
- Application FastAPI fonctionnelle
- Tests automatisés avec pytest
- Conteneurisation avec Docker
- Exécution dans un environnement isolé
- Validation via navigateur et tests HTTP

### 🚧 En cours
- Pipeline CI/CD avec GitHub Actions

### 🔜 À venir
- Déploiement Kubernetes
- GitOps avec Argo CD
- Monitoring avec Prometheus & Grafana
- Infrastructure as Code avec Terraform
- Multi-environnement et multi-cloud

---

## 🔹 Environnement de test

Un environnement de test conteneurisé a été mis en place afin de valider l'application.

### Objectifs
- Tester l'application avant déploiement
- Garantir un environnement reproductible
- Isoler l'exécution

### Lancer le projet

```bash
docker build -t cloudsyncer-app .
docker run -p 8000:8000 cloudsyncer-app