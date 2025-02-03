# Détection de Fraudes en Temps Réel avec Kafka Streams et Tableau de Bord Grafana


## 1. Introduction

Ce projet permet la détection de fraudes en temps réel à l'aide de Kafka Streams pour le traitement des flux de transactions et de Grafana pour la visualisation des alertes de fraudes dans une base de données InfluxDB.

## 2. Configuration des Topics Kafka

### 2.1. Création des Topics Kafka

Créer deux topics Kafka via la CLI :

- **transactions-input** : Ce topic contient les transactions brutes.
- **fraud-alerts** : Ce topic stocke les transactions suspectes.

```bash
kafka-topics --create --topic transactions-input --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
kafka-topics --create --topic fraud-alerts --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
```
s
