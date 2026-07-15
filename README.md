# 🍔 Online Food Ordering System — Software Requirements Specification

An **IEEE 830-1998 compliant SRS document** for a full-stack Online Food Ordering System (OFOS) — covering functional requirements, non-functional requirements, system architecture, and interface design for customers, restaurant staff, and administrators.

> Course Project | B.Tech Electronics & Computer Engineering | Guided by Mrs. Pinky M.S | September 2025

---

## 📖 Overview

The **Online Food Ordering System (OFOS)** is a web-based platform (extensible to mobile) that connects customers with local restaurants — enabling menu browsing, order placement, secure online payments, and real-time delivery tracking. This document specifies the complete system requirements for v1.0, following the **IEEE 830-1998** standard for Software Requirements Specifications.

## 🎯 Scope

**In Scope (v1.0):**
- User registration & authentication (Customer / Restaurant / Admin)
- Restaurant & menu management
- Cart management and order placement
- Secure payment processing (cards, UPI, wallets, cash-on-delivery)
- Real-time order tracking & status updates
- Notifications (email, SMS, push)
- Reviews & ratings
- Admin panel with reporting & analytics

**Out of Scope (v1.0):**
- Physical food delivery execution (tracking only, not fulfillment)
- Delivery agent live-tracking (future integration)
- AI-based recommendations
- Native mobile app (web-first, mobile-ready design)

## 👥 User Classes

| User Class | Role |
|---|---|
| **Customers** | Browse restaurants, place orders, make payments, track deliveries |
| **Restaurant Staff** | Manage menus, process orders, update statuses, view reports |
| **System Administrators** | Manage users, monitor performance, ensure smooth operations |
| **Delivery Personnel** *(future scope)* | Confirm and track deliveries |

## 🏗️ System Architecture

```
Customer/User <---> Web/Mobile App <---> Application (Core System)
                                                |
                          -------------------------------------
                          |                |                   |
                      Database          Admin Panel      External Services
                   (Orders, Menu,         (Staff)        (Payment, SMS, Email)
                       Users)
```

**Major Components:**
- **Customer Interface** — browsing, ordering, payments
- **Restaurant/Admin Panel** — menu & order management
- **System Database** — MySQL/PostgreSQL (3NF normalized)
- **External Interfaces** — Payment Gateway API, Notification Service API

## 🧩 Key System Features

| Feature | Priority |
|---|---|
| User Registration & Authentication | High |
| Browse Restaurants & Menus | High |
| Cart Management & Order Placement | High |
| Payment Processing | High |
| Order Processing & Status Tracking | High |
| Notifications & Alerts | Medium |
| Restaurant Admin Panel | High |
| Reviews & Ratings | Medium |
| Administration & Reporting | High |
| Coupons & Promotions | Medium |
| Security & Privacy (RBAC, encryption) | High |

Each feature includes fully traceable **functional requirements** (`FR-XX-NN`) with `[MUST] / [SHOULD] / [MAY]` priority tags and defined acceptance criteria.

## 🔐 Non-Functional Requirements Highlights

- **Performance:** ≥500 concurrent users (scalable to 2000); <2s page load; <5s checkout
- **Availability:** 99.5% uptime (monthly, excluding maintenance)
- **Security:** TLS 1.2+, PCI-DSS compliance, bcrypt password hashing, RBAC, SQL injection prevention
- **Scalability:** Horizontal scaling, Redis/Memcached caching for hot reads
- **Maintainability:** >60% test coverage, centralized logging & monitoring
- **Compliance:** GDPR-like data privacy practices, regional financial regulations

## 🛠️ Proposed Tech Stack

| Layer | Technology Options |
|---|---|
| **Frontend** | React / Angular, responsive design (HTML5, CSS3, JS ES6) |
| **Backend** | Java (Spring Boot), Python (Django), or Node.js (Express) |
| **Database** | MySQL 8.0 / PostgreSQL 14 |
| **Payment Gateways** | Razorpay, Stripe, PayPal |
| **Notifications** | Twilio SMS API, Firebase Cloud Messaging, SMTP (SendGrid) |
| **Auth** | OAuth 2.0, JWT, Google reCAPTCHA v3 |
| **Deployment** | Docker, CI/CD (GitHub Actions), AWS/GCP/Azure |

## 📄 Document Structure

1. Introduction (Purpose, Scope, Conventions, Audience)
2. Overall Description (Product Perspective, Functions, User Classes, Operating Environment, Constraints)
3. External Interface Requirements (User, Hardware, Software, Communication Interfaces)
4. System Features (11 feature areas with detailed FRs)
5. Non-Functional Requirements (Performance, Security, Scalability, Compliance)
6. Appendices (Glossary, Analysis Models, TBD List)

📎 Full document: [`SRS-Online-Food-Ordering-System.pdf`](./SRS-Online-Food-Ordering-System.pdf)

*Guided by Mrs. Pinky M.S*

## 📄 License

This project was developed as an academic course project and is shared for educational and portfolio purposes.
