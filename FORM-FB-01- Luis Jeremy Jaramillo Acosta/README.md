# FORM-FB-01 — Fichas Bibliográficas: Fundamentos de Sistemas Distribuidos y Arquitecturas Distribuidas

[![Asignatura](https://img.shields.io/badge/Asignatura-Aplicaciones%20Distribuidas%20(SOF--I--R)-007acc.svg)](#)
[![Nivel](https://img.shields.io/badge/Nivel-7mo%20Nivel%20--%20Paralelo%20A-brightgreen.svg)](#)
[![Modalidad](https://img.shields.io/badge/Modalidad-Individual%20--%20Formativa-orange.svg)](#)
[![Compilador](https://img.shields.io/badge/LaTeX-pdflatex%20%2B%20biber-blueviolet.svg)](#)

---

## 📌 1. Datos Informativos

- **Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Facultad:** Facultad de Ciencias de la Computación / Ciencias de la Ingeniería
- **Carrera:** Ingeniería de Software
- **Asignatura:** Aplicaciones Distribuidas (SOF-I-R)
- **Nivel / Paralelo:** 7mo Nivel — Paralelo "A"
- **Docente:** Dr. Gleiston Cicerón Guerrero Ulloa
- **Estudiante Responsable:** Luis Jeremy Jaramillo Acosta
- **Cédula de Identidad:** `1206898718`
- **Correo Institucional:** `ljaramilloa@uteq.edu.ec`
- **Código de Actividad:** FORM-FB-01
- **Período Académico:** Semana 2 (2 al 8 de noviembre de 2026)

---

## 🎯 2. Propósito de la Actividad

Esta actividad formativa individual prepara al estudiante para redactar el **Informe Académico Individual TA-IND-01** (*Análisis crítico de un sistema distribuido real*), correspondiente a la Semana 3. 

El presente compendio reúne cinco fuentes científicas rigurosamente verificadas (publicadas entre 2020 y 2023 en IEEE, Elsevier y editoriales reconocidas), que cubren comparativas empíricas entre arquitecturas monolíticas y de microservicios, revisiones sistemáticas de adopción en DevOps, marcos de evaluación de migración y fundamentos de escalabilidad y distribución.

---

## 📂 3. Estructura de Archivos del Espacio de Trabajo

```text
FORM-FB-01- Luis Jeremy Jaramillo Acosta/
│
├── main.tex                                           # Código fuente principal en LaTeX
├── referencias.bib                                    # Archivo unificado BibLaTeX con las 5 fuentes
├── main.pdf                                           # Documento PDF final compilado
├── README.md                                          # Documentación e instrucciones de compilación
│
└── Referencias (PDF)/                                 # Documentos fuente originales en formato PDF
    ├── [1] Monolithic_vs_Microservice_Architecture_A_Performa.pdf
    ├── [2] waseem2020sms.pdf
    ├── [3] Towards_a_migration_framework_for_Microservices.pdf
    ├── [4] Building Microservices Designing Fine-Grained Systems 2nd By Sam Newman.pdf
    └── [5] Distributed_Systems_4.pdf
```

---

## 📚 4. Fuentes Académicas Verificadas (5 Fichas)

| N° | Autores | Título | Revista / Editorial | Año | Identificador (DOI / ISBN) |
|:--:|:--------|:-------|:--------------------|:---:|:---------------------------|
| **1** | G. Blinowski, A. Ojdowska, A. Przybyłek | *Monolithic vs. Microservice Architecture: A Performance and Scalability Evaluation* | *IEEE Access* (IEEE) | 2022 | DOI: [10.1109/ACCESS.2022.3152803](https://doi.org/10.1109/ACCESS.2022.3152803) |
| **2** | M. Waseem, P. Liang, M. Shahin | *A Systematic Mapping Study on Microservices Architecture in DevOps* | *Journal of Systems and Software* (Elsevier) | 2020 | DOI: [10.1016/j.jss.2020.110798](https://doi.org/10.1016/j.jss.2020.110798) |
| **3** | F. Auer, V. Lenarduzzi, M. Felderer, D. Taibi | *From Monolithic Systems to Microservices: An Assessment Framework* | *Information and Software Technology* (Elsevier) | 2021 | DOI: [10.1016/j.infsof.2021.106600](https://doi.org/10.1016/j.infsof.2021.106600) |
| **4** | S. Newman | *Building Microservices: Designing Fine-Grained Systems* (2nd ed.) | O'Reilly Media | 2021 | ISBN: `978-1492034025` |
| **5** | M. van Steen, A. S. Tanenbaum | *Distributed Systems* (4th ed.) | Maarten van Steen | 2023 | ISBN: `978-9081540636` |

---

## 🛠️ 5. Instrucciones de Compilación (Requisitos de la Cátedra)

Conforme a las directrices de la actividad, a continuación se especifican el **compilador**, el **archivo principal**, el **orden de comandos** y las **dependencias** para compilar el documento de forma reproducible:

### 5.1. Compilador
- **Compilador Principal:** `pdflatex` (pdfTeX versión 3.141592653 o superior).
- **Motor Bibliográfico:** `biber` (versión 2.19 o superior compatible con `biblatex`).
- **Distribuciones Soportadas:** TeX Live (2023 o superior), MiKTeX (24.x o superior) o plataformas en la nube como Overleaf.

### 5.2. Archivo Principal y Base Bibliográfica
- **Archivo Fuente Principal:** `main.tex`
- **Archivo Bibliográfico Único:** `referencias.bib`
- **Salida Generada:** `main.pdf`

### 5.3. Orden Estricto de Comandos para Compilación
Para garantizar que se resuelvan adecuadamente los enlaces internos, las referencias cruzadas y la bibliografía en formato IEEE, ejecute la siguiente secuencia en la terminal:

```bash
# 1. Primera pasada para generar archivos auxiliares (.aux, .bcf)
pdflatex -interaction=nonstopmode main.tex

# 2. Procesamiento del archivo unificado de citas con Biber
biber main

# 3. Segunda pasada para incorporar las referencias generadas
pdflatex -interaction=nonstopmode main.tex

# 4. Tercera pasada para resolver numeración e hipervínculos definitivos
pdflatex -interaction=nonstopmode main.tex
```

### 5.4. Dependencias y Paquetes LaTeX Requeridos
El archivo `main.tex` utiliza los siguientes paquetes estándar del ecosistema LaTeX:
- `inputenc` (`[utf8]`): Codificación universal de caracteres y tildes.
- `babel` (`[spanish, es-tabla]`): Adaptación tipográfica y términos en español.
- `geometry` (`[margin=2.5cm]`): Dimensionamiento de márgenes de página.
- `xcolor`: Gestión de paleta de colores corporativos.
- `tcolorbox`: Cajas estructuradas para la diagramación de cada ficha bibliográfica.
- `csquotes`: Manejo semántico de citas textuales.
- `hyperref`: Enlaces activos a DOIs y navegación en el PDF.
- `biblatex` (`[backend=biber, style=ieee, sorting=none]`): Motor bibliográfico con formato oficial IEEE.

---

## 🤖 6. Declaración de Uso de Inteligencia Artificial

En cumplimiento estricto con las políticas de honestidad académica de la UTEQ:
- Se declara el uso de la herramienta **Gemini (Google)** exclusivamente para labores de **revisión ortográfica, control de acentuación (tildes) y ajuste de puntuación** sobre los borradores previamente redactados por el estudiante.
- No se utilizó IA generativa para la creación ni síntesis de los resúmenes, datos concretos ni notas de aplicación técnica.
- Todas las fuentes, cifras y citas fueron verificadas manualmente contra las publicaciones oficiales indexadas.
