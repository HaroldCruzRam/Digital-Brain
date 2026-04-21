---
tipo: nota
area: WSO2 API Manager
tema: TEMA — Arquitectura
subtema: SUB — Arquitectura General
creado: 21-04-2026
dominio: ⬜ sin revisar
tags:
  - nota
---

# 📄 Nota — Traffic Manager

> Parte de: [[SUB — Arquitectura General]] → [[TEMA — Arquitectura]] → [[WSO2 API Manager]]

---

## 📖 Definición

> _Con tus propias palabras._

---

## 🧠 Analogía o ejemplo

---

## ⚙️ Detalle técnico

Traffic Manager es un componente que permite regular el tráfico hacia una API, disponer de ellas en diferentes niveles de un servicio y protegerlas contra ataques de seguridad.

Permite limitar el tráfico en tiempo real gracias a que cuenta con un motor de limitación dinámica.

![[Pasted image 20260421135819.png]]

Por último, se encarga de actualizar el mapa en memoria del Universal Gateway mediante un tema JMS. Esto se logra ya que el Traffic Manager publica eventos de actualización de artefactos (API/Aplicación) recibidos del Publisher Portal y del Developer Portal usando JMS. El Universal Gateway recibe estos eventos a través de JMS y actualiza el mapa en memoria

>[!info]
>**JMS** es una API estándar para enviar y recibir mensajes. Permite a los componentes basados en Java™ Platform, Enterprise Edition (Java EE) crear, enviar, recibir y leer mensajes.

---

## 🃏 Flash cards relacionadas

- [[FC — Nota — Traffic Manager]]

---

*← [[SUB — Arquitectura General]] | ↑ [[🏠 Inicio]]*
