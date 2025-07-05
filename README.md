# 🕵️‍♂️ CMS Dirbusting Wordlists for Burp Suite

Una colección de diccionarios personalizados para realizar **dirbusting** (descubrimiento de directorios y archivos ocultos) en sitios web y detectar qué **CMS (Content Management System)** están siendo utilizados.

Este repositorio está diseñado para usarse con herramientas como **Burp Suite (Intruder)**.

---

## 🎯 Objetivo

Detectar automáticamente la presencia de CMS comunes mediante rutas específicas de cada uno, usando ataques dirigidos de fuerza bruta a URLs.

---

## 📚 CMS Soportados

- 🟦 WordPress
- 🟨 Joomla
- 🟥 Drupal
- 🟪 Magento
- 🟫 PrestaShop
- 🟩 Typo3

---

## 🚀 ¿Cómo Usarlo en Burp Suite?

### 🔹 Opción 1: Usando Intruder

1. Intercepta una solicitud `GET / HTTP/1.1` desde tu objetivo.
2. Envíala a **Intruder**.
3. En la pestaña **Positions**, reemplaza la ruta con `§FUZZ§`.
4. Carga uno de los archivos `.txt` como payload.
5. Inicia el ataque y analiza las respuestas:
   - `200 OK`: archivo o carpeta existe.
   - `302 Found`: redirección útil (login, admin).
   - `403 Forbidden`: acceso denegado pero ruta válida.

👁 https://github.com/fuzzdb-project/fuzzdb


