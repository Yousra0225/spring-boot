# Spring Boot CheatSheet

- [Qu'est-ce que Spring Boot](#quest-ce-que-spring-boot-)
- [Création d'un projet Spring Boot](#création-dun-projet-spring-boot)
  - [Création manuelle](#1-création-manuelle)
  - [Utilisation de Spring initialzr](#2-utiliser-spring-initializr)
  - [Via IntelliJ](#3-depuis-intellij-idea)
- [Structure du projet](./Structure-de-projet.md)
- [Gestion de dependances](#spring-boot--gestion-des-dépendances)
  - [Les outils](#outils-utilisés)
  - [Emplacement des dependances](#où-mettre-les-dépendances-)
  - [Dépendances pré-configurées de Spring Boot (Starters)](#dependances-préconfigurer-de-spring-boot)
  - [Centralisation des version](#parent-spring-boot-centralisation-des-versions)

## Qu'est-ce que Spring Boot ?

**Spring Boot** est une extension de Spring, une version simplifier qui facilite son utilisation grâce à l'autoconfiguration qu'il offre. Il fournit :
- de l'**auto-configuration**
- un **serveur intégré** (comme Tomcat)
- un système de **"starter"** (pour ajouter facilement des fonctionnalités)
- la possibilité de **lancer une app en 1 clic** (`main()`)
---

## Création d’un projet Spring Boot

###  1. Création manuelle

1. Création des dossiers à la main (`src/main/java`, `resources`...)
2. Création du fichier `pom.xml` ou `build.gradle`
3. Ajout des dépendances nécessaires (ex: `spring-boot-starter-web`..)
4. Création de la classe principale `@SpringBootApplication`
5. Organisation des dossiers (`controller`, `service`..)
---

### 2. Utiliser [Spring Initializr](https://start.spring.io/)

- Choix de la version de Spring Boot
- Choix de dépendances (Web, JPA, Security..)
- Personnalisation du projet (nom, package, langage...)
- Génère un projet prêt à être ouvert dans IntelliJ, Eclipse...

> Résultat :
- Un ZIP contenant toute la structure Spring Boot
- Projet avec `pom.xml` ou `build.gradle` déjà configuré

---

### 3. Depuis IntelliJ IDEA 

> IntelliJ Ultimate a un **plugin Spring Boot** intégré
1. `File` > `New` > `Project...`
2. Choisir **Spring Initializr**
3. Configurer :
   - Group / Artifact
   - Langage : Java, Kotlin, etc.
   - Version de Spring Boot
   - Dépendances : Web, JPA, etc.
4. IntelliJ télécharge et génère automatiquement le projet
--- 

## Spring Boot – Gestion des dépendances

###  Outils utilisés
- **Maven** : `pom.xml` (outil de build + gestion de dépendances)
- **Gradle** : `build.gradle` (alternative)
- Spring Initializr : https://start.spring.io
- IntelliJ Ultimate (plugin Spring Boot)

### Où mettre les dépendances ?

Dans `pom.xml`, section `<dependencies>` :

```xml
<dependencies>
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
  </dependency>
</dependencies>
```

### Dependances préconfigurer de spring Boot

| Starter                          | Utilité principale                          |
|----------------------------------|---------------------------------------------|
| `spring-boot-starter-web`        | Web MVC + Tomcat + JSON (Jackson)           |
| `spring-boot-starter-data-jpa`   | JPA + Hibernate + Spring Data               |
| `spring-boot-starter-security`   | Authentification + Sécurité HTTP            |
| `spring-boot-starter-thymeleaf`  | Moteur de template HTML                     |
| `spring-boot-starter-test`       | JUnit + Mockito + Spring Test               |

### Parent Spring Boot (centralisation des versions)

*Le Parent Spring Boot est une configuration centralisée (dans le pom.xml) qui gère automatiquement les versions des dépendances, plugins, et paramètres de build. Il simplifie le projet et permet d’ajouter des dépendances sans spécifier manuellement leurs versions.*
```xml
<parent>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-parent</artifactId>
  <version>3.2.0</version>
</parent>
```