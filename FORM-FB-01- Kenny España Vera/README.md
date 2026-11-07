# FORM-FB-01 — Fichas Bibliográficas: Fundamentos de Sistemas Distribuidos y Arquitecturas Distribuidas

[![Asignatura](https://img.shields.io/badge/Asignatura-Aplicaciones%20Distribuidas%20(SOF--I--R)-000000.svg)](#)
[![Nivel](https://img.shields.io/badge/Nivel-7mo%20Nivel%20--%20Paralelo%20A-000000.svg)](#)
[![Modalidad](https://img.shields.io/badge/Modalidad-Individual%20--%20Formativa-000000.svg)](#)
[![Compilador](https://img.shields.io/badge/LaTeX-pdflatex%20%2B%20biber-000000.svg)](#)

---

## 📌 1. Datos Informativos

- **Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Facultad:** Facultad de Ciencias de la Computación / Ciencias de la Ingeniería
- **Carrera:** Ingeniería de Software
- **Asignatura:** Aplicaciones Distribuidas (SOF-I-R)
- **Nivel / Paralelo:** 7mo Nivel — Paralelo "A"
- **Docente:** Dr. Gleiston Cicerón Guerrero Ulloa
- **Estudiante Responsable:** Kenny Isaías España Vera
- **Correo Institucional:** `kespanav@uteq.edu.ec`

---

## 🎯 2. Propósito y Alcance de la Actividad

Esta actividad formativa individual prepara al estudiante para redactar el **Informe Académico Individual TA-IND-01** (*Análisis crítico de un sistema distribuido real*), correspondiente a la Semana 3. 

El presente compendio sistematiza cinco fuentes científicas primarias de alto impacto (publicadas entre 2023 y 2024 en revistas y congresos internacionales indexados en Scopus Q1, Web of Science e IEEE Xplore).

---

## 📚 3. Fuentes Académicas Analizadas y Verificadas (5 Artículos Indexados)

| N° | Autores | Título del Artículo | Revista / Congreso | Indexación / Cuartil | Año | DOI Verificado |
|:--:|:--------|:--------------------|:-------------------|:--------------------:|:---:|:--------------:|
| **1** | V. Velepucha, P. Flores | *A Survey on Microservices Architecture: Principles, Patterns and Migration Challenges* | *IEEE Access* (IEEE) | Q1 Scopus / WoS | 2023 | [10.1109/ACCESS.2023.3305687](https://doi.org/10.1109/ACCESS.2023.3305687) |
| **2** | W. K. G. Assunção, J. Krüger, S. Mosser, S. Selaoui | *How do microservices evolve? An empirical analysis of changes in open-source microservice repositories* | *Journal of Systems and Software* (Elsevier) | Q1 Scopus / WoS | 2023 | [10.1016/j.jss.2023.111788](https://doi.org/10.1016/j.jss.2023.111788) |
| **3** | W. Meijer, C. Trubiani, A. Aleti | *Experimental evaluation of architectural software performance design patterns in microservices* | *Journal of Systems and Software* (Elsevier) | Q1 Scopus / WoS | 2024 | [10.1016/j.jss.2024.112183](https://doi.org/10.1016/j.jss.2024.112183) |
| **4** | R. Pinciroli, A. Aleti, C. Trubiani | *Performance Modeling and Analysis of Design Patterns for Microservice Systems* | *2023 IEEE 20th International Conference on Software Architecture (ICSA)* | Conferencia Indexada / WoS / Scopus | 2023 | [10.1109/ICSA56044.2023.00012](https://doi.org/10.1109/ICSA56044.2023.00012) |
| **5** | G. Parker, S. Kim, A. Al Maruf, T. Cerny, K. Frajtak, P. Tisnovsky, D. Taibi | *Visualizing Anti-Patterns in Microservices at Runtime: A Systematic Mapping Study* | *IEEE Access* (IEEE) | Q1 Scopus / WoS | 2023 | [10.1109/ACCESS.2023.3236165](https://doi.org/10.1109/ACCESS.2023.3236165) |

---

## 🛠️ 4. Instrucciones de Compilación (Requisitos de la Tarea)

De acuerdo con las instrucciones de la actividad académica, a continuación se detallan de forma explícita el **compilador**, el **archivo principal**, el **orden de comandos** y las **dependencias** requeridas para la compilación reproducible del documento:

### 4.1. Compilador
- **Compilador Principal:** `pdflatex` (pdfTeX versión 3.141592653 o superior).
- **Motor Bibliográfico:** `biber` (versión 2.19 o superior compatible con el paquete `biblatex`).
- **Distribución LaTeX Soportada:** MiKTeX (versión 24.x o superior) o TeX Live (2023 o superior) en sistemas Windows, Linux y macOS.

### 4.2. Archivo Principal
- **Documento Principal (5 fichas en tablas tipo Word, 7 páginas):** `main.tex` (genera `main.pdf`).
- **Base de Datos Bibliográfica:** `referencias.bib` (archivo unificado en estándar BibLaTeX / IEEE con 5 entradas verificadas).

### 4.3. Orden de Comandos
Para compilar el documento principal resolviendo correctamente las tablas, las citas en formato IEEE, la base bibliográfica, los enlaces y las referencias cruzadas, ejecute la siguiente secuencia estricta de 4 comandos en la terminal:

```bash
# Paso 1: Primera pasada para registrar estructura, tablas y generar archivos auxiliares (.aux, .bcf)
pdflatex -interaction=nonstopmode main.tex

# Paso 2: Ejecución del motor Biber para procesar el archivo de bibliografía (referencias.bib)
biber main

# Paso 3: Segunda pasada para incorporar las referencias formateadas en estándar IEEE
pdflatex -interaction=nonstopmode main.tex

# Paso 4: Tercera pasada para resolver numeración definitiva, hipervínculos y total de páginas
pdflatex -interaction=nonstopmode main.tex
```

### 4.4. Dependencias (Paquetes LaTeX Requeridos)
El documento hace uso exclusivo de paquetes estándar incluidos en cualquier instalación completa de MiKTeX o TeX Live:
- `babel` (con opciones `spanish, es-tabla`): localización tipográfica y textos predefinidos en español.
- `inputenc` (con codificación `utf8`): soporte integral para caracteres latinos, tildes y eñes.
- `geometry`: configuración geométrica de márgenes (2.0 cm superior/inferior, 2.0 cm izquierdo/derecho).
- `microtype`: optimización microtipográfica de espaciado y justificación.
- `booktabs`: formateo profesional de líneas horizontales para tablas (`\toprule`, `\midrule`, `\bottomrule`).
- `tabularx`: estructuración de tablas tipo Word con cálculo responsivo de ancho de columna.
- `array`: alineación avanzada y control dimensional de celdas en tablas.
- `enumitem`: listas y viñetas compactas con espaciado controlado.
- `csquotes`: manejo avanzado de entrecomillado tipográfico según normas bibliográficas.
- `amsmath`: operadores matemáticos y símbolos técnicos formales.
- `biblatex` (con opciones `backend=biber`, `style=ieee`, `sorting=none`): generación automatizada de citas y bibliografía en norma IEEE.
- `hyperref` (con opción `hidelinks`): enlaces clicables limpios para DOIs y referencias sin alterar la estética académica en blanco y negro.
- `titlesec`: diseño compacto y jerárquico de títulos de sección.

---

## 📂 5. Estructura de Archivos de esta Carpeta

```text
FORM-FB-01- Kenny España Vera/
│
├── README.md                                          # Documentación técnica, tabla de fuentes y guía de compilación
├── main.tex                                           # Código fuente LaTeX principal (5 fichas en tablas tipo Word, IEEE)
├── main.pdf                                           # PDF compilado final del informe completo (7 páginas exactas)
│
├── Referencia (PDF)/                                  # Archivos PDF originales de las fuentes académicas
│   ├── 2023-ICSA-DesignPatterns-Performance.pdf
│   ├── A Survey on Microservices Architecture Principles, Patterns and Migration Challenges.pdf
│   ├── Experimental evaluation of architectural software performance design.pdf
│   ├── How do microservices evolve An empirical analysis of changes in.pdf
│   └── Visualizing_Anti-Patterns_in_Microservices_at_Runtime_A_Systematic_Mapping_Study.pdf
│
└── Referencia (.BIB)/                                 # Archivos BibTeX individuales originales
    ├── A Survey on Microservices Architecture Principles, Patterns and Migration Challenges.bib
    ├── How do microservices evolve An empirical analysis of changes in.bib
    ├── Meijer2024Microservices.bib
    ├── Performance Modeling and Analysis of Design Patterns for Microservice Systems.bib
    └── Visualizing Anti-Patterns in Microservices at Runtime A Systematic Mapping Study.bib
```
