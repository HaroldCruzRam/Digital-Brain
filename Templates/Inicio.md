# 🏠 Inicio

> Tu base de operaciones. Navega por área o por tipo de nota.

---

## 🗺 Áreas de estudio

- [[🗺 MOC - Java & Spring Boot]]
- [[🗺 MOC - Matemáticas]]
- [[🗺 MOC - Python]]
- [[🗺 MOC - DevOps & Docker]]
- [[🗺 MOC - API]]

---

## 📅 Sesiones recientes

```dataview
TABLE fecha, area, duracion
FROM #sesion
SORT fecha DESC
LIMIT 7
```

---

## 💡 Conceptos recientes

```dataview
TABLE area, dominio
FROM #concepto
SORT file.mtime DESC
LIMIT 10
```

---

## 🃏 Flash cards para repasar

```dataview
TABLE area, nivel
FROM #flashcard
SORT file.mtime DESC
LIMIT 10
```

---

## 📋 Plantillas disponibles

| Plantilla | Uso |
|-----------|-----|
| [[TPL_MOC]] | Nuevo mapa de contenido |
| [[TPL_Concepto]] | Nueva nota de concepto |
| [[TPL_Sesion]] | Nueva sesión de estudio |
| [[TPL_FlashCard]] | Nueva tarjeta de repaso |

---

> 💬 _"Lo que no se escribe, se olvida. Lo que no se enlaza, se pierde."_
