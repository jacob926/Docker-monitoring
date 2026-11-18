# Projet de Supervision et de Monitoring DevOps

Ce projet a été réalisé à titre de projet de fin d'année. Il met en place une infrastructure complète de supervision et de conteneurisation pour surveiller l'état de santé des services et remonter des alertes en temps réel.

---

##  Architecture & Stack Technologique

Le projet repose sur une architecture conteneurisée via **Docker** et **Docker Compose** :

* **Prometheus** : Collecte et stockage des métriques (Time-Series Database).
* **Alertmanager** : Gestion, groupage et routage des alertes vers les canaux de notification.
* **Grafana** : Visualisation des métriques à l'aide de tableaux de bord personnalisés.
* **Node-exporter** : Collecte des métriques système de la machine hôte.
* **cAdvisor** : Collecte des métriques d'utilisation des ressources par les conteneurs Docker.
* **Nginx** : Application cible ("cobaye") utilisée pour simuler des pannes et tester les alertes.
* **Discord** : Canal de réception des notifications d'alertes en temps réel (`firing` / `resolved`).

---

##  Guide d'installation et de lancement

### Prérequis
* Avoir **Docker** et **Docker Compose** installés sur votre machine.

### 1. Cloner le projet
```bash
git clone [https://github.com/jacob926/Docker-monitoring](https://github.com/jacob926/Docker-monitoring.git)
cd Docker-monitoring
