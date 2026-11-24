# 🛒 Products — Angular & Spring Boot

**Mini application full-stack de gestion de produits : un front Angular qui consomme une API REST Spring Boot.**

![Angular](https://img.shields.io/badge/Angular-21-DD0031?logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.0-6DB33F?logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap_Icons-7952B3?logo=bootstrap&logoColor=white)

Travail pratique du module **Développement web full-stack** — Génie informatique, Université Mundiapolis.

---

## ✨ Fonctionnalités

- Affichage de la liste des produits (nom, prix, sélectionné ou non)
- Suppression d'un produit depuis l'interface
- Validation côté serveur (`@NotEmpty` sur le nom, `@Min(0)` sur le prix)
- Front Angular récent : composants *standalone*, nouveau *control flow* (`@if`, `@for`), `HttpClient`

## 🏗️ Architecture

```
┌────────────────────────┐   GET / DELETE   ┌───────────────────────────────────┐
│  angular-app  (:4200)  │ ───────────────▶ │  backend-app  (:8080)  /api/...   │
│  Home · Products       │                  │  web → services → JPA → H2        │
└────────────────────────┘                  └───────────────────────────────────┘
```

| Méthode | Endpoint | Description |
|---|---|---|
| `GET` | `/api/products` | Liste des produits |
| `GET` | `/api/products/{id}` | Détail d'un produit |
| `DELETE` | `/api/products/{id}` | Supprimer un produit |

## 🚀 Lancer le projet

**Prérequis :** Java 17, Node.js 20+ et Angular CLI.

```bash
# 1. Backend
cd angular-app/backend-app
./mvnw spring-boot:run        # http://localhost:8080  (console H2 : /h2-console)

# 2. Frontend
cd angular-app/angular-app
npm install
ng serve                       # http://localhost:4200
```

## 📁 Structure

```
angular-app/
├── angular-app/     # Front Angular (pages Home et Products, ProductService)
└── backend-app/     # API Spring Boot (entities, repositories, services, web)
```

---

👤 **Saad Sabir Idrissi** — Élève ingénieur Data & IA · [Portfolio](https://saad-sabir-idrissi.vercel.app) · [LinkedIn](https://www.linkedin.com/in/saad-sabir-idrissi)
