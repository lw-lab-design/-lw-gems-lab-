# Sustrato de Notas Técnicas — GOLD NODE · LW Gems

Documento de gobernanza interna del sistema de notas técnicas del laboratorio GOLD NODE.

Este archivo define el **sustrato obligatorio**, la **política de versionado** y las **reglas de evolución** de todas las notas técnicas publicadas en `/lab-notes/`.

---

## 1. Definición de sustrato

El **sustrato** es el conjunto mínimo, no negociable, de elementos técnicos y semánticos que una nota debe cumplir para ser considerada válida dentro del sistema.

Una nota que no cumple el sustrato **no se publica**.

---

## 2. Alcance

Este sustrato aplica a:

- Todas las notas técnicas actuales
- Todas las notas futuras
- Toda modificación, ampliación o corrección de notas existentes

No aplica al home del subdominio ni a páginas índice.

---

## 3. Sustrato obligatorio (v1.0)

Cada nota técnica DEBE incluir:

### 3.1 Estructura HTML base
- `<!doctype html>`
- `<html lang="es">`
- `<meta charset="utf-8">`
- `<meta name="viewport">`

---

### 3.2 SEO primario
- `<title>` técnico y único
- `<meta name="description">`
- `<meta name="robots" content="index, follow">`
- `<link rel="canonical">` absoluto

---

### 3.3 Identidad semántica (JSON-LD)
- `Article` JSON-LD completo
- `@id` propio (`URL#article`)
- `headline`
- `description`
- `inLanguage`
- `datePublished`
- `dateModified`
- `mainEntityOfPage`
- Conexión por `@id` a:
  - `WebSite`
  - `Organization`

---

### 3.4 Jerarquía de navegación
- `BreadcrumbList` JSON-LD:
  - Home
  - Lab Notes
  - Nota actual

---

### 3.5 Representación externa mínima
- Open Graph:
  - `og:type = article`
  - `og:title`
  - `og:description`
  - `og:url`
- Twitter:
  - `twitter:card = summary`
  - `twitter:title`
  - `twitter:description`

---

### 3.6 Presentación
- CSS único del sistema (`/assets/css/style.css`)
- Prohibido estilos inline en notas técnicas

---

### 3.7 Trazabilidad temporal
- `datePublished`
- `dateModified`

---

## 4. Elementos prohibidos

Queda expresamente prohibido:

- `author` persona física
- `BlogPosting`, `NewsArticle`
- `meta keywords`
- JSON-LD duplicados
- Scripts externos
- Tracking / analytics
- CTAs comerciales
- Contenido publicitario

---

## 5. Plantilla oficial

La única forma válida de crear una nueva nota es duplicando la plantilla:
