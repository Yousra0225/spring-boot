# Structure d’un projet Spring Boot avec Spring Initializr

```bash
mon-projet/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── exemple/
│   │   │           └── monprojet/
│   │   │               ├── MonProjetApplication.java
│   │   │               └── controllers/
│   │   │               └── services/
│   │   │               └── models/
│   │   │               └── repositories/
│   │   └── resources/
│   │       ├── application.properties
│   │       ├── static/
│   │       └── templates/
│   └── test/
│       └── java/
│           └── com/
│               └── exemple/
│                   └── monprojet/
│                       └── MonProjetApplicationTests.java
├── pom.xml (ou build.gradle)
```

# Structure détaillée

| Dossier/Fichier                      | Contenu / Rôle principal                                              |
| ------------------------------------ | --------------------------------------------------------------------- |
| `src/main/java/`                     | Code source principal en Java                                         |
| ├── `MonProjetApplication.java`      | Point d’entrée (`@SpringBootApplication`)                             |
| ├── `controllers/`                   | Contrôleurs REST (`@RestController`)                                  |
| ├── `services/`                      | Logique métier (services, traitements)                                |
| ├── `models/`                        | Entités JPA, classes métier, DTO                                      |
| └── `repositories/`                  | Interfaces JPA (DAO) avec Spring Data                                 |
| `src/main/resources/`                | Fichiers de configuration et fichiers non java (js, html..)           |
| ├── `application.properties/yml`     | Configuration globale (BDD, port, etc.)                               |
| ├── `static/`                        | Ressources statiques (CSS, JS, images)                                |
| └── `templates/`                     | Templates HTML (Thymeleaf, etc.)                                      |
| `src/test/java/`                     | Code de test (unitaires et intégration)                               |
| └── `MonProjetApplicationTests.java` | Classe de test de l'application                                       |
| `pom.xml` ou `build.gradle`          | Fichier de configuration Maven ou Gradle (dépendances, plugins, etc.) |
