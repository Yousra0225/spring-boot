# Spring Boot CheatSheet

- [Qu'est-ce que Spring](#1-quest-ce-que-spring-)
- [Qu'est-ce que Spring Boot](#2-quest-ce-que-spring-boot-)
- [Création d'un projet Spring Boot](#création-dun-projet-spring-boot)
- [Structure du projet](./Structure-de-projet.md)

## 1. Qu'est-ce que Spring ?

_C'est un **framework Java** très populaire qui permet de créer des applications robustes, modulaires et testables.  
Il est composé de plusieurs **modules** spécialisés :_

| Module          | Utilité principale                            |
| --------------- | --------------------------------------------- |
| Spring Core     | Injection de dépendances                      |
| Spring Web      | Développement d'API REST / site web           |
| Spring Data     | Accès aux bases de données (JPA, Mongo, etc.) |
| Spring Security | Sécurité (authentification, autorisation)     |

## 2. Qu'est-ce que Spring Boot ?

**Spring Boot** est une extension de Spring, une version simplifier qui facilite son utilisation grâce à l'autoconfiguration qu'il offre. Il fournit :
- de l'**auto-configuration**
- un **serveur intégré** (comme Tomcat)
- un système de **"starter"** (pour ajouter facilement des fonctionnalités)
- la possibilité de **lancer une app en 1 clic** (`main()`)
---

## Création d’un projet Spring Boot


##  1. Création manuelle

1. Création des dossiers à la main (`src/main/java`, `resources`...)
2. Création du fichier `pom.xml` ou `build.gradle`
3. Ajout des dépendances nécessaires (ex: `spring-boot-starter-web`..)
4. Création de la classe principale `@SpringBootApplication`
5. Organisation des dossiers (`controller`, `service`..)
---

## 2. Utiliser [Spring Initializr](https://start.spring.io/)

- Choix de la version de Spring Boot
- Choix de dépendances (Web, JPA, Security..)
- Personnalisation du projet (nom, package, langage...)
- Génère un projet prêt à être ouvert dans IntelliJ, Eclipse...

### Résultat :
- Un ZIP contenant toute la structure Spring Boot
- Projet avec `pom.xml` ou `build.gradle` déjà configuré

---

## 3. Depuis IntelliJ IDEA 

> IntelliJ Ultimate a un **plugin Spring Boot** intégré
1. `File` > `New` > `Project...`
2. Choisir **Spring Initializr**
3. Configurer :
   - Group / Artifact
   - Langage : Java, Kotlin, etc.
   - Version de Spring Boot
   - Dépendances : Web, JPA, etc.
4. IntelliJ télécharge et génère automatiquement le projet
