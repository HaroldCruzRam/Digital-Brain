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

# 📄 Nota — API Control Plane

> Parte de: [[SUB — Arquitectura General]] → [[TEMA — Arquitectura]] → [[WSO2 API Manager]]

---

## 📖 Definición

Componente de WSO2 API Manager encargado de la creación y administración de APIs. Está constituido por:

- Publisher Portal
- Developer Portal
- Service Catalog

Además integra un Key Manager para las validaciones de seguridad y generación/revocación de tokens.

---

## 🧠 Analogía o ejemplo

---

## Nota

Esta constituido por los portales **[[#API Publisher]]**, **[[#API Developer Portal]]** y **[[#Service Catalog]]**.

Permite crear, administrar, implementar rate limiting policies, monitorear y monetizar APIs.

También provee un conjunto de APIs para interactuar con herramientas externas como API Controller además de paneles de análisis de APIs con datos relevantes para el negocio.

![[Pasted image 20260421101154.png|535]]

### API Publisher

Portal diseñado para los creadores de APIs para desarrollar, documentar, asegurar, probar y versionar APIs con facilidad. También permite publicar, monetizar y aplicar rate limiting policies.

### API Developer Portal

Portal diseñado para que los creadores alojar y publicar sus APIs. Además permite a otros usuarios explorar, evaluar, suscribirse y usar las APIs publicadas de forma segura y rápida.

### Service Catalog

Catalogo donde los desarrolladores registran sus servicios en forma RESTful. Es a través de estos catálogos que los servicios se hacen visibles para la capa de API Management, de modo que se pueden crear proxies de APIs directamente a partir de ellos.

### Key Manager

Actua como un Servicio de Tokens Seguros (Secure Token Service ó STS). El API Control Plane soporta OAuth 2.0, Basic Auth, Mutual SSL y mecanismos de autenticación basados en API Keys.

![[Pasted image 20260421104612.png]]

El Key Manager proporciona una API para generar o revocar tokens de acceso. Estos tokens pueden ser utilizados por los clientes para utilizar las APIs expuestas por WSO2 API Control Plane.

Se pueden generar tokens de acceso OAuth 2.0 invocando la API directamente o utilizando del Developer Portal. Además, se pueden generar API Keys (tokens JWT auto-firmados) a través del Developer Portal sin usar el Key Manager.

Cuando un usuario invoca una API con un token AOuth 2.0 o con una API Key, el Gateway valida el token usando su firma de validación y su suscripción.

El Key Manager también realiza la validación de alcance y (si se configura) puede generar tokens JWT para enviar los atributos del usuario al servidor.

>[!note]
>Es posible integrar proveedores de identidad de terceros, como Okta, Auth0, KeyCloak, etc., al API Control Plane.



---

## 🃏 Flash cards relacionadas

- [[FC — Nota — API Control Plane]]

---

*← [[SUB — Arquitectura General]] | ↑ [[🏠 Inicio]]*
