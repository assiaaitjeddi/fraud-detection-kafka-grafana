# Détection de Fraudes en Temps Réel avec Kafka Streams et Tableau de Bord Grafana



## 1. Introduction

Ce projet permet la détection de fraudes en temps réel à l'aide de Kafka Streams pour le traitement des flux de transactions et de Grafana pour la visualisation des alertes de fraudes dans une base de données InfluxDB.

## 2. Configuration des Topics Kafka

### 2.1. Création des Topics Kafka

Créer deux topics Kafka via la CLI :

- **transactions-input** : Ce topic contient les transactions brutes.
- **fraud-alerts** : Ce topic stocke les transactions suspectes.

### 2.2. Dépendances Maven

Ajoutez les dépendances suivantes dans votre `pom.xml` :

```xml
<dependencies>
    <dependency>
        <groupId>org.apache.kafka</groupId>
        <artifactId>kafka-streams</artifactId>
        <version>3.5.0</version>
    </dependency>
    <dependency>
        <groupId>com.fasterxml.jackson.core</groupId>
        <artifactId>jackson-databind</artifactId>
        <version>2.15.2</version>
    </dependency>
</dependencies>

```
s
