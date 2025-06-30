# Spring Boot CheatSheet

- [Qu'est-ce que Spring](#1-quest-ce-que-spring-)
- [Configuration de l'environement de travail]
- [Création d'un projet Spring Boot]
- [Structure du projet]

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

