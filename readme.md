# 🔐 Locker API

API REST principale du système Locker, développée avec **Spring Boot 3.5+** et **Java 21**.  
Elle centralise la logique métier, la gestion des utilisateurs, des machines, des armoires, des casiers, des produits, ainsi que les contraintes spécifiques (froid, vente, traçabilité, etc).

---

## 🚀 Stack technique

- **Java 21**
- **Spring Boot 3.5+**
- **Spring Web / Security / Data JPA**
- **MySQL / MariaDB**
- **Maven**
- **Validation (Jakarta Bean Validation)**
- **RESTful API** avec gestion des erreurs, statuts, etc.
- **WebSocket** ou **MQTT** (prévu)
- Prêt pour l’authentification par **JWT**

---

## 📁 Structure du projet (à venir)

```bash
locker-api/
├── src/
│   ├── main/
│   │   ├── java/com/locker/api/
│   │   │   ├── controller/
│   │   │   ├── model/
│   │   │   ├── repository/
│   │   │   ├── service/
│   │   │   └── config/
│   │   └── resources/
│   │       ├── application.properties
│   │       └── ...
├── pom.xml
└── README.md
```

---

## ⚙️ Configuration (local dev)

Créer la base de données :

```sql
CREATE DATABASE locker_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

Extrait de `application.properties` :

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/locker_db
spring.datasource.username=root
spring.datasource.password=ton_mot_de_passe
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## ▶️ Lancer l’application

```bash
mvn spring-boot:run
```

Ou construire le `.jar` :

```bash
mvn clean package
java -jar target/locker-api-0.0.1-SNAPSHOT.jar
```

---

## 📌 Endpoints de test

```http
GET /api/test -> "API Locker OK 🚀"
```

---

## 📄 Documentation associée

- [`locker-docs/api-design.md`](https://github.com/ThomasGossuin/locker-docs/blob/master/architecture/api-design.md)
- [`locker-docs/machine-architecture.md`](https://github.com/ThomasGossuin/locker-docs/blob/master/architecture/machine-architecture.md)
- [`locker-docs/service-web-structure.md`](https://github.com/ThomasGossuin/locker-docs/blob/master/architecture/service-web-structure.md)

---

## ✅ TODO

- [ ] Authentification JWT
- [ ] Gestion utilisateur + rôles
- [ ] Casiers, produits, armoires, températures
- [ ] Communication machine via WebSocket/MQTT

---

## 👨‍💻 Auteur

Thomas Gossuin — Projet personnel open source, évolutif sur plusieurs technos
