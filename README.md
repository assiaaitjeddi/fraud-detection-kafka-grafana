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

## 3. Application Kafka Streams
### 3.1. Produire les Transactions Financières
Le producteur génère des transactions aléatoires et les envoie au topic transactions-input.

### 3.2. Filtrer les Transactions Suspectes
Ce processeur Kafka Streams filtre les transactions suspectes, définies par un seuil d'amplitude de 10 000.

### 3.3. Consommer les Transactions Suspectes
Les transactions suspectes sont envoyées à InfluxDB pour stockage et analyse.

## 4. Stocker les Transactions Suspectes dans InfluxDB
Les alertes de fraude sont stockées directement dans InfluxDB avec les informations suivantes :

    - userId
    
    - amount
    
    - timestamp
    
## 5. Tableau de Bord Grafana
### 5.1. Configuration de Grafana
Connectez Grafana à InfluxDB et créez un tableau de bord pour visualiser les transactions suspectes.

## 6. Visualisations 
![Tableau de bord Grafana](./pictures/1.png)
![Tableau de bord Grafana](./pictures/2.png)
![Tableau de bord Grafana](./pictures/3.png)
![Tableau de bord Grafana](./pictures/4.png)
![Tableau de bord Grafana](./pictures/5.png)
![Tableau de bord Grafana](./pictures/6.png)
![Tableau de bord Grafana](./pictures/7.png)


