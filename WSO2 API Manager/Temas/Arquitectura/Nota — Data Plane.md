---
tipo: nota
area: WSO2 API Manager
tema: TEMA — Arquitectura
subtema: SUB — Arquitectura General
creado: 21-04-2026
dominio: ⬜ sin revisar
tags:
  - nota
  - "{{area}}"
---

# 📄 Nota — Data Plane

> Parte de: [[SUB — Arquitectura General]] → [[TEMA — Arquitectura]] → [[WSO2 API Manager]]

---

## 📖 Definición

Componente de WSO2 API Manager encargado de exponer las APIs a los consumidores. Este actúa como un proxy entre el usuario y el backend.
Además se encarga de aplicar medidas de seguridad, aplicar políticas de rate limiting, mapear datos, entre otras funciones.

---

## 🧠 Analogía o ejemplo

---

## ⚙️ Detalle técnico

Es la capa donde se exponen las APIs creadas a los consumidores. Esta capa actúa como un Proxy para las llamadas de las APIs.  

Permite aplicar medidas de seguridad y rate limiting policies.

Esta compuesto por diversos Gateways:
- [[#Universal Gateway]]
- [[#Kubernetes Gateway]]
- [[#Inmutable Gateway]]

![[Pasted image 20260421101154.png]]

### Universal Gateway

WSO2 Universal Gateway actúa como el punto de acceso de un API request hecha a alguna API gestionada por WSO2 API Manager.

![[Pasted image 20260421114126.png]]

Como puede verse en la imagen, el flujo sigue los siguientes pasos:

1. Universal Gateway valida el JWT comprobando la firma, emisor, fecha de caducidad y suscripción. Esta última se válida usando un mapa en memoria el cual incluye, principalmente, la información de la API, la aplicación y la suscripción.

2. Se procesa el mensaje a un formato pre-configurado (JSON, XML, CSV, etc.).

3. Aplica las políticas de seguridad y de rate limiting, además de recopilar datos estadísticos usando los handlers.

4. En los mediadores se procesa el payload (la información útil, excluyendo cabeceras y meta-datos) y se formatean los datos a un formato pre configurado (JSON, XML, CSV, etc.) y se envía al backend.

>[!note]
>WSO2 Universal Gateway se puede integrar en entornos locales y en la nube.

### Kubernetes Gateway

Es la plataforma de gestión de APIs en la nube nativa de WSO2 diseñada para auxiliar en la creación, implementación y gestión de API en la nube.

Esta diseñada para ofrecer alta disponibilidad y gestionar grandes volúmenes de solicitudes de APIs gracias a funciones como failover automático (direccionamiento de tráfico a un servidor disponible) y el balance de carga.

Ofrece soporte para CI/CD.

### Inmutable Gateway

Es un Gateway para microservicios nativo de la nube, descentralizada y centrada en el desarrollador. Es utilizado para la seguridad de los mensajes, la seguridad del transporte y el enrutamiento, entro otras funciones relacionadas con la calidad del servicio.

---

## 🃏 Flash cards relacionadas

- [[FC — Nota — Data Plane]]

---

*← [[🔸 {{subtema}}]] | ↑ [[🏠 Inicio]]*
