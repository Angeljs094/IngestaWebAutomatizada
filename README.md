# Ingesta Web Automatizada 📚⚙️

Proyecto final orientado a la **automatización de ingesta y procesamiento de datos web** hacia una base de datos relacional.  
El flujo implementa técnicas de **web scraping, limpieza de datos, reglas de negocio y carga estructurada con SQLAlchemy**, garantizando un proceso **escalable y profesional**.

---

## 🎯 Objetivo

Desarrollar un flujo completo que:
- Extraiga información desde una fuente web pública.
- Procese y limpie los datos aplicando reglas de negocio.
- Cargue los resultados en una base de datos relacional mediante **SQLAlchemy ORM**.

---

## 🌐 Contexto del Proyecto

La empresa requiere obtener información estructurada de libros del género **Fantasy** disponibles en el portal [Books to Scrape](https://books.toscrape.com).  
El objetivo es extraer esta información, procesarla según reglas definidas y almacenarla en una base de datos corporativa.

---

## 📋 Requerimiento Principal

Extraer todos los libros del género **Fantasy** y cargarlos en la base de datos cumpliendo las siguientes reglas:

- **Tabla final:** `books_for_sale`
- **Campos requeridos:**
  - `book_code`: Código único e incremental.
  - `book_name`: Nombre del libro (sin el contenido entre paréntesis).
  - `book_detail`: Texto extraído de los paréntesis del nombre (si aplica).
  - `book_price`: Precio del libro (tipo numérico).

---

## 🔄 Flujo del Proceso

1. Navegar a la categoría *Fantasy*.  
2. Capturar al menos 3 atributos de cada libro.  
3. Extraer información de todos los libros de la primera página.  
4. Extender la extracción a todas las páginas de la categoría.  
5. Crear la tabla `books_for_sale` con SQLAlchemy ORM.  
6. Aplicar reglas de negocio al cargar los datos.  
7. Implementar concurrencia en la carga hacia la base de datos.  

**Evaluaciones adicionales:**
- No incluir librerías innecesarias.  
- Cerrar el navegador correctamente al terminar el scrapeo.  

**Bonos:**
- Desarrollo modular (todo en funciones).  
- Uso de `WebDriverWait` para sincronización eficiente.  

---

## 📂 Estructura del Proyecto

- DATABASE/        # Contiene la base de datos SQLite (books.db)
- DOCS/            # Documentación del proyecto (adp_proyecto.pdf)
- NOTEBOOKS/       # Jupyter Notebooks para análisis y desarrollo

---

## 🚀 Tecnologías utilizadas

- **Python 3.x**
- **Jupyter Notebook**
- **SQLite + SQLAlchemy ORM**
- Librerías de scraping: `requests`, `BeautifulSoup4`, `selenium`
- Librerías de análisis: `pandas`, `numpy`

---

## ⚙️ Instalación y uso

1. Clona el repositorio:
   ```bash
   git clone https://github.com/Angeljs094/IngestaWebAutomatizada.git
   cd IngestaWebAutomatizada

