---
tipo: nota
area: WSO2 API Manager
tema: TEMA — Diseño y Gestión de una API
subtema: SUB — Diseño de una API
creado: 21-04-2026
dominio: ⬜ sin revisar
tags:
  - nota
---

# 📄 Nota — Introducción

> Parte de: [[SUB — Diseño de una API]] → [[TEMA — Diseño y Gestión de una API]] → [[WSO2 API Manager]]

---

## 📖 Definición

> _Con tus propias palabras._

---

## 🧠 Analogía o ejemplo

---

## ⚙️ Detalle técnico

El ciclo de vida que involucra al desarrollo de una API está constituido por muchas fases. Con WSO2 API Manager podemos facilita el diseño de una API a través del Developer Portal.

![[Pasted image 20260421155004.png]]

La primer etapa, i.e. la más obvia, es la creación de la API. Crear una API en WSO2 API Manager consiste en implementar el backend de una API existente con el Publisher Portal de WSO2. Desde este punto es posible gestionar su ciclo de vida, seguridad, documentación, comunidad y suscripciones.

WSO2 API Manager es compatible con un gran número de diseños para APIs.
### API Rest
Existen dos maneras de publicar un API Rest:

- Crear el API directamente en el Publisher Portal vinculando el backend existente.
- Proporcionar la definición OpenAPI de la API, la cual ya incluye (o debería incluir) toda la información necesaria (nombre, descripción, endpoints, etc.).

### GraphQL API
GraphQL es un Data Querry Language para APIs. Cuando se usa este diseño el usuario puede especificar explicitamente que datos necesita de una API.

### Streaming API

Una API de transmisión (o streaming API) es una colección lógica de mensajes relacionados a través de los cuales los clientes pueden enviar y recibir eventos en un formato definido. Entro ellos se encuentra:

- API WebSocket
- API WebSub/WebHook
- Server Sent Events (SSE) API
- AsyncAPI

---

## 🃏 Flash cards relacionadas

- [[FC — Nota — Introducción]]

---

*← [[SUB — Diseño de una API]] | ↑ [[🏠 Inicio]]*
