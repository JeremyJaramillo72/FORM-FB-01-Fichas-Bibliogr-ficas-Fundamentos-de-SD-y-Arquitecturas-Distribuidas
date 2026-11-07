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
- **Estudiante Responsable:** Heiner Ariel Zambrano Ronquillo
- **Correo Institucional:** `hzambranor@uteq.edu.ec`

---

## 🎯 2. Propósito y Alcance de la Actividad

El objetivo central de este trabajo formativo radica en consolidar una base teórica y empírica rigurosa que sirva de sustento para la elaboración del informe individual **TA-IND-01**. En dicha entrega sumativa se evaluará el comportamiento, la tolerancia a fallos y los patrones arquitectónicos de una plataforma distribuida en producción.

A través de esta recopilación se analizan a fondo cinco publicaciones académicas indexadas (2021 a 2024), seleccionadas desde repositorios de primer nivel como IEEE Xplore, ACM Digital Library, Elsevier y Springer Nature. La investigación se orienta a esclarecer los desafíos de seguridad perimetral, la identificación de causa raíz en caídas del sistema y los compromisos reales entre escalabilidad y latencia en entornos de microservicios.

---

## 📚 3. Fuentes Académicas Analizadas y Verificadas (5 Artículos Indexados)

| N° | Autores | Título del Artículo | Revista / Editorial | Cuartil / Indexación | Año | DOI Verificado |
|:--:|:--------|:--------------------|:--------------------|:--------------------:|:---:|:--------------:|
| **1** | P. Haindl, P. Kochberger, M. Sveggen | *A Systematic Literature Review of Inter-Service Security Threats and Mitigation Strategies in Microservice Architectures* | *IEEE Access* (IEEE) | Q1 Scopus / WoS | 2024 | [10.1109/ACCESS.2024.3406500](https://doi.org/10.1109/ACCESS.2024.3406500) |
| **2** | J. Soldani, A. Brogi | *Anomaly Detection and Failure Root Cause Analysis in (Micro) Service-Based Cloud Applications: A Survey* | *ACM Computing Surveys* (ACM) | Q1 Scopus / WoS | 2022 | [10.1145/3501297](https://doi.org/10.1145/3501297) |
| **3** | A. Pereira-Vale, E. B. Fernandez, R. Monge, H. Astudillo, G. Márquez | *Security in microservice-based systems: A Multivocal literature review* | *Computers & Security* (Elsevier) | Q1 Scopus / WoS | 2021 | [10.1016/j.cose.2021.102200](https://doi.org/10.1016/j.cose.2021.102200) |
| **4** | S. Li, H. Zhang, Z. Jia, C. Zhong, C. Zhang, Z. Shan, J. Shen, M. A. Babar | *Understanding and addressing quality attributes of microservices architecture: A Systematic literature review* | *Information and Software Technology* (Elsevier) | Q1 Scopus / WoS | 2021 | [10.1016/j.infsof.2020.106449](https://doi.org/10.1016/j.infsof.2020.106449) |
| **5** | M. Sildatke, H. Karwanni, B. Kraft, A. Zündorf | *A Distributed Microservice Architecture Pattern for the Automated Generation of Information Extraction Pipelines* | *SN Computer Science* (Springer Nature) | Indexada / WoS | 2023 | [10.1007/s42979-023-02256-4](https://doi.org/10.1007/s42979-023-02256-4) |

---

## 🛠️ 4. Instrucciones de Compilación (Requisitos de la Tarea)

De acuerdo con las instrucciones de la actividad académica, a continuación se detallan de forma explícita el **compilador**, el **archivo principal**, el **orden de comandos** y las **dependencias** requeridas para la compilación reproducible del documento:

### 4.1. Compilador
- **Compilador Principal:** `pdflatex` (pdfTeX versión 3.141592653 o superior).
- **Motor Bibliográfico:** `biber` (versión 2.19 o superior compatible con el paquete `biblatex`).
- **Distribución LaTeX Soportada:** MiKTeX (versión 24.x o superior) o TeX Live (2023 o superior) en sistemas Windows, Linux y macOS.

### 4.2. Archivo Principal
- **Documento Principal (5 fichas completas, 7 páginas):** `main.tex` (genera `main.pdf`).
- **Base de Datos Bibliográfica:** `referencias.bib` (archivo unificado en estándar BibLaTeX / IEEE con 5 entradas verificadas).

### 4.3. Orden de Comandos
Para compilar el documento principal resolviendo correctamente las citas en formato IEEE, la base bibliográfica, los enlaces y las referencias cruzadas, ejecute la siguiente secuencia estricta de 4 comandos en la terminal:

```bash
# Paso 1: Primera pasada para registrar citas y generar archivos auxiliares (.aux, .bcf)
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
- `microtype`: optimización microtipográfica de justificación y reducción de cortes de palabra.
- `booktabs`: formateo profesional de líneas horizontales para tablas académicas (`\toprule`, `\midrule`, `\bottomrule`).
- `tabularx`: tablas con cálculo responsivo de ancho de columna.
- `enumitem`: listas numeradas y de viñetas con espaciado compacto y alineación controlada.
- `csquotes`: manejo avanzado de entrecomillado tipográfico según estándares de citas.
- `biblatex` (con opciones `backend=biber`, `style=ieee`, `sorting=none`): generación automatizada de citas y bibliografía en norma IEEE.
- `hyperref` (con opción `hidelinks`): enlaces clicables limpios para DOIs y referencias sin alterar la estética académica en blanco y negro.
- `titlesec`: formateo compacto y uniforme de encabezados de secciones y subsecciones.

---

## 📂 5. Estructura de Archivos de esta Carpeta

```text
FORM-FB-01- Zambrano Ronquillo Heiner/
│
├── README.md                                          # Documentación técnica y guía de compilación
├── main.tex                                           # Código fuente LaTeX principal (5 fichas, resumen, dato concreto, IEEE)
├── main.pdf                                           # PDF compilado final del informe completo (7 páginas)
├── referencias.bib                                    # Base de datos BibTeX unificada y verificada (claves IEEE)
│
├── Referencia (PDF)/                                  # Documentos primarios científicos originales en formato PDF
│   ├── A Distributed Microservice Architecture Pattern for the Automated Generation of Information Extraction Pipelines.pdf
│   ├── A_Systematic_Literature_Review_of_Inter-Service_Se.pdf
│   ├── Anomaly Detection and Failure Root Cause Analysis in(Micro) Service-Based Cloud Applications A Survey.pdf
│   ├── Security in microservice-based systems A Multivocal literature review.pdf
│   └── Understanding and addressing quality attributes of microservices architecture A Systematic literature review.pdf
│
└── Referencias (.bib)/                                # Citas BibTeX individuales descargadas de las editoriales
    ├── A Distributed Microservice Architecture Pattern for the Automated Generation of Information Extraction Pipelines.bib
    ├── Anomaly Detection and Failure Root Cause Analysis in(Micro) Service-Based Cloud Applications A Survey.bib
    ├── Haindl2024MicroserviceSecurity.bib
    ├── Security in microservice-based systems A Multivocal literature review.bib
    └── Understanding and addressing quality attributes of microservices architecture A Systematic literature review.bib
```
