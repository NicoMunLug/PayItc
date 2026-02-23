# 📘 PayItc - Microservicio de Pasarela de Pagos

## 📌 Descripción

PayItc es una pasarela de pagos basada en microservicios que simula el funcionamiento de PayU. Permite la integración con:

* Ecommerce externo
* PSE
* Callbacks firmados
* Seguridad avanzada con JWT y HMAC

---

## 🏗 Arquitectura

* Java 21
* Spring Boot 3
* MySQL 8
* Docker
* Microservicios
* Clean Architecture
* JWT Authentication
* HMAC Signature Validation

---

## 📂 Microservicios

### 🔐 Auth Service

* Registro de merchants
* Generación API_KEY
* JWT
* Seguridad

### 💳 Payment Service

* Creación de transacciones
* Integración con PSE
* Webhooks
* Estados de pago

---

## 🗄 Base de Datos

Motor: MySQL 8
Diseñada inicialmente en MySQL Workbench.

Tablas principales:

* merchants
* api_credentials
* transactions
* payment_methods
* transaction_logs
* webhook_events

---

## 🔐 Seguridad Implementada

* JWT
* HMAC SHA256
* Idempotency Key
* Firma digital de callbacks
* Protección contra replay attack

---

## 🔄 Flujo de Pago

1. Ecommerce envía solicitud de pago.
2. PayItc valida firma.
3. Se crea transacción.
4. Se redirige a PSE.
5. PSE responde callback.
6. PayItc notifica al ecommerce.

---
# 🧱 FASE 1 — DISEÑO DE BASE DE DATOS MySQL

Esta BD está pensada para:

* Manejar múltiples comercios (ecommerce externos)
* Manejar transacciones
* Soportar múltiples métodos de pago (ej: PSE)
* Permitir auditoría
* Ser segura y escalable
* Soportar idempotencia
* Permitir callbacks firmados

---

# 🐳 FASE 2 — DOCKERIZACIÓN COMPLETA

## ¿Cómo ejecutar los contenedores?

### 1️⃣ Construir

```bash
docker-compose up --build
```

### 2️⃣ Iniciar contenedores

```bash
docker-compose up -d
```

### 3️⃣ Parar contenedores

```bash
docker-compose down
```

---

## 👨‍🎓 Creadores

*Universidad:* Escuela Tecnológica Instituto Técnico Central

*Curso:* Ingeniería de Software 1

*Autores:* Nicolás Fernando Muñoz, Juan Sebastián Donato, Hector Fabián Linares, Daniel Eduardo Sanchez