# FORM-FB-01 — Fichas Bibliográficas: Fundamentos de Sistemas Distribuidos y Arquitecturas Distribuidas

[![Materia](https://img.shields.io/badge/Materia-Aplicaciones%20Distribuidas%20(SOF--I--R)-007acc.svg)](#)
[![Nivel](https://img.shields.io/badge/Nivel-7mo%20Nivel%20--%20Paralelo%20A-brightgreen.svg)](#)
[![Carácter](https://img.shields.io/badge/Car%C3%A1cter-Formativa%20(FORM--FB--01)-orange.svg)](#)
[![Compilación](https://img.shields.io/badge/LaTeX-BibLaTeX%20%7C%20IEEE-blue.svg)](#)

---

## 📌 Datos Informativos de la Actividad

- **Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Facultad:** Facultad de Ciencias de la Ingeniería / Ciencias de la Computación
- **Carrera:** Ingeniería de Software
- **Asignatura:** Aplicaciones Distribuidas (SOF-I-R)
- **Nivel / Paralelo:** 7mo Nivel — Paralelo "A"
- **Docente:** Dr. Gleiston Cicerón Guerrero Ulloa
- **Estudiante Responsable:** Luis Alberto Paca Pilataza
- **C.I.:** `1251252225`
- **Correo Institucional:** `lpacap@uteq.edu.ec`
- **Código de Actividad:** `FORM-FB-01`
- **Propósito Formativo:** Preparación de la base bibliográfica y análisis conceptual previo para el **Informe Académico Individual TA-IND-01** (Semana 3).

---

## 📂 Estructura de la Carpeta Individual

```text
FORMULARIO-FB-01- Luis Alberto Paca Pilataza/
│
├── main.tex                                    # Documento principal en LaTeX con las 5 fichas y bibliografía
├── Referencias.bib                             # Archivo de citas BibLaTeX en estándar IEEE
├── main.pdf                                    # Documento compilado final en formato PDF
├── Entrega_SGA_Luis_Alberto_Paca.tex           # Fuente LaTeX de la carátula de 1 sola página para el SGA
├── Entrega_SGA_Luis_Alberto_Paca.pdf           # PDF de 1 página listo para subir al SGA
├── README.md                                   # Documentación completa y manual de compilación
│
├── Referencias PDF/                            # Artículos y libros fuente originales íntegros
│   ├── Abgaz_et_al_2023_Decomposition_Monolith_Microservices.pdf
│   ├── Ford_Richards_Sadalage_Dehghani_Software_Architecture_The_Hard_Parts_Modern_Trade_Off_Analyses_for_Distributed_Architectures.pdf
│   ├── Oumoussa_Saidi_Evolution_of_Microservices_Identification_in_Monolith_Decomposition_IEEE_Access_2024.pdf
│   ├── Revista_de_Arquitectura_de_Sistemas_Journal_of_Systems_Architecture_Vol_118.pdf
│   └── Zhang_2023_Robust_Failure_Diagnosis.pdf
│
└── Referencias .bib/                           # Archivos BibTeX individuales originales de descarga
    ├── IEEE Xplore Citation BibTeX Download 2026.11.6.0.57.28.bib
    ├── IEEE Xplore Citation BibTeX Download 2026.11.6.1.22.52.bib
    ├── IEEE Xplore Citation BibTeX Download 2026.11.6.18.57.35.bib
    ├── S1383762121001442.bib
    └── SoftwareArchitecture.bib
```

---

## 🛠️ Instrucciones de Compilación del Documento LaTeX

El documento principal (`main.tex`) está configurado con **BibLaTeX** y el motor de bibliografía **Biber** utilizando la norma **IEEE**. Puede ser compilado localmente en cualquier entorno LaTeX estándar o mediante motores modernos de un solo paso.

### 1. Dependencias y Paquetes Requeridos
Asegúrese de contar con una distribución estándar de LaTeX (**TeX Live 2022+**, **MiKTeX 22+** o **MacTeX**):
- `geometry`, `inputenc` (utf8), `fontenc` (T1), `babel` (spanish).
- `lmodern`, `microtype`, `csquotes`, `amsmath`, `booktabs`.
- `tcolorbox` (con la librería `skins` y `breakable`).
- `biblatex` (con estilo `ieee`).
- `hyperref`, `xcolor`, `fancyhdr`.

### 2. Secuencia Clásica de Comandos (TeX Live / MiKTeX)
Para resolver correctamente las referencias cruzadas y la bibliografía de BibLaTeX:

```bash
# 1. Primera pasada para generar archivos auxiliares
pdflatex main.tex

# 2. Procesamiento de la bibliografía con Biber
biber main

# 3. Segunda pasada para incorporar citas
pdflatex main.tex

# 4. Tercera pasada para asentar numeraciones y enlaces cruzados
pdflatex main.tex
```

Alternativamente, si dispone de `latexmk`:
```bash
latexmk -pdf main.tex
```

### 3. Compilación Rápida con Tectonic (Motor Rust Autónomo)
Tectonic resuelve automáticamente las pasadas de compilación y descarga paquetes faltantes sin intervención manual:
```bash
tectonic main.tex
```

### 4. Compilación del Documento SGA (Hoja Única de Entrega)
Para generar el archivo de una página requerido por la plataforma institucional LMS SGA:
```bash
pdflatex Entrega_SGA_Luis_Alberto_Paca.tex
# o bien:
tectonic Entrega_SGA_Luis_Alberto_Paca.tex
```

---

## 📑 Sistematización de las Fichas Bibliográficas

A continuación se presentan las 5 fichas académicas desarrolladas a partir de la lectura exhaustiva y verificación directa de los documentos locales:

---

### Ficha N° 1: Descomposición de Monolitos hacia Arquitecturas de Microservicios

- **Referencia IEEE:**  
  Y. Abgaz *et al.*, "Decomposition of Monolith Applications Into Microservices Architectures: A Systematic Review," *IEEE Transactions on Software Engineering*, vol. 49, no. 8, pp. 4213–4242, Aug. 2023, doi: `10.1109/TSE.2023.3287297`.
- **DOI Verificado:** [10.1109/TSE.2023.3287297](https://doi.org/10.1109/TSE.2023.3287297) *(Revista Indexada: IEEE TSE — Scopus Q1)*.
- **Resumen Técnico Contextualizado (98 palabras):**  
  El artículo aborda la complejidad de migrar aplicaciones monolíticas legadas hacia arquitecturas de microservicios sin comprometer la continuidad operativa. Para ordenar el estado del arte, los autores ejecutaron una revisión sistemática de literatura (SLR) y un proceso de snowballing, filtrando 5,022 publicaciones hasta seleccionar 35 estudios primarios rigurosos. Como resultado fundamental, presentan el marco M2MDF (Monolith to Microservices Decomposition Framework), el cual clasifica las estrategias según el tipo de datos analizados (código estático, trazas de ejecución y modelos de dominio) y su madurez. Demuestran que la descomposición puramente automatizada fracasa sin la participación directa de expertos de dominio.
- **Dato Concreto y Verificable:**  
  *Sección IV-A, pág. 4214 y pág. 4222 (Fig. 4):* De un total de 5,022 resultados iniciales de búsqueda en bases de datos científicas, únicamente 35 investigaciones superaron las 4 fases de filtrado y análisis de inclusión. Adicionalmente, en la *Sección V, pág. 4235*, los autores demuestran que las herramientas de particionamiento totalmente automatizadas son incapaces de capturar la semántica contextual del negocio, ratificando la necesidad de la intervención de ingenieros de dominio.
- **Nota Personal y Articulación con TA-IND-01:**  
  Esta investigación me permitió comprender que la descomposición de un sistema monolítico distribuido no es un mero procedimiento algorítmico de agrupamiento de código fuente o clases, sino una decisión que debe reflejar fielmente las fronteras funcionales del negocio para evitar acoplamientos destructivos. En mi informe **TA-IND-01**, emplearé el marco M2MDF dentro de la sección *"Metodología de Descomposición y Análisis Estático/Dinámico"*, sustentando técnicamente cómo balancear el análisis de trazas de ejecución dinámicas con los modelos de dominio para justificar los límites de los microservicios en el caso práctico asignado.

---

### Ficha N° 2: Evolución y Retos en la Identificación de Microservicios

- **Referencia IEEE:**  
  I. Oumoussa and R. Saidi, "Evolution of Microservices Identification in Monolith Decomposition: A Systematic Review," *IEEE Access*, vol. 12, pp. 23389–23405, 2024, doi: `10.1109/ACCESS.2024.3365079`.
- **DOI Verificado:** [10.1109/ACCESS.2024.3365079](https://doi.org/10.1109/ACCESS.2024.3365079) *(Revista Indexada: IEEE Access — Scopus Q1-Q2)*.
- **Resumen Técnico Contextualizado (99 palabras):**  
  Los autores investigan la falta de estandarización en las técnicas de identificación de microservicios durante la modernización de monolitos. Con este fin, desarrollaron una revisión sistemática exhaustiva sobre 168 investigaciones primarias extraídas de múltiples repositorios científicos, examinando tendencias temporales, tipos de contribución y herramientas propuestas. Los hallazgos revelan que la disciplina enfrenta barreras críticas: escasez de comparaciones empíricas directas entre métodos, ausencia de métricas de calidad universales para validar los límites de los servicios y un sesgo desproporcionado hacia aplicaciones escritas en Java, lo cual limita la transferibilidad práctica de los resultados hacia ecosistemas empresariales heterogéneos.
- **Dato Concreto y Verificable:**  
  *Sección III-C, pág. 23392:* La selección metodológica final consolidó formalmente 168 artículos primarios (partiendo de 35 identificados inicialmente y añadiendo 133 mediante rastreo exhaustivo de referencias). En la *Sección VI-B, pág. 23401*, se comprueba que la gran mayoría de la literatura restringe sus validaciones experimentales a sistemas monolíticos desarrollados en Java, omitiendo arquitecturas políglotas.
- **Nota Personal y Articulación con TA-IND-01:**  
  El estudio de Oumoussa y Saidi me alertó sobre los riesgos de evaluar la calidad de los microservicios únicamente mediante métricas tradicionales de orientación a objetos (cohesión y acoplamiento sintáctico), sin considerar la sobrecarga inducida en la red distribuida. En el informe **TA-IND-01**, incorporaré estas conclusiones en la sección de *"Evaluación de Fronteras de Servicio y Deuda Técnica"*, evaluando críticamente las compensaciones entre granularidad fina y el incremento de llamadas inter-servicio en el diseño de la arquitectura.

---

### Ficha N° 3: Diagnóstico Robusto de Fallas con Datos Multimodales en Microservicios

- **Referencia IEEE:**  
  S. Zhang *et al.*, "Robust Failure Diagnosis of Microservice System Through Multimodal Data," *IEEE Transactions on Services Computing*, vol. 16, no. 6, pp. 3851–3864, Nov.-Dec. 2023, doi: `10.1109/TSC.2023.3290018`.
- **DOI Verificado:** [10.1109/TSC.2023.3290018](https://doi.org/10.1109/TSC.2023.3290018) *(Revista Indexada: IEEE TSC — Scopus Q1)*.
- **Resumen Técnico Contextualizado (101 palabras):**  
  La investigación aborda el desafío de diagnosticar averías en sistemas de microservicios donde las fallas en cascada degradan rápidamente la disponibilidad global. Los autores identifican que las soluciones tradicionales fracasan al depender de fuentes de telemetría aisladas. Para solucionarlo, llevaron a cabo un estudio empírico con fallas reales y diseñaron DiagFusion, un marco que integra métricas temporales, registros textuales y trazas distribuidas. Mediante técnicas de incrustación multimodal, grafos de dependencia topológica y redes neuronales de grafos (GNN), el sistema localiza la instancia causante y categoriza la anomalía, superando sustancialmente a los métodos basados en reglas o datos monomodales.
- **Dato Concreto y Verificable:**  
  *Resumen y Sección I, pág. 3851; Sección VII, pág. 3862 (Tabla VII):* Las evaluaciones empíricas sobre sistemas industriales demuestran que DiagFusion supera a las técnicas representativas del estado del arte, logrando mejoras del **20.9% al 368%** en la localización precisa de la instancia raíz causante y del **11.0% al 169%** en la determinación del tipo de falla.
- **Nota Personal y Articulación con TA-IND-01:**  
  Este artículo transformó mi comprensión práctica sobre la observabilidad distribuida. Comprobé que inspeccionar métricas aisladas como el uso de memoria o revisar logs independientes resulta ineficaz cuando un error se propaga en cadena entre decenas de nodos. En **TA-IND-01**, utilizaré los fundamentos de DiagFusion en la sección *"Confiabilidad Sistémica, Tolerancia a Fallos y Observabilidad Telemétrica"*, argumentando por qué es indispensable correlacionar trazas de extremo a extremo con telemetría multimodal para aislar averías en sistemas de alta disponibilidad.

---

### Ficha N° 4: Identificación Multi-Modelo Basada en Procesos de Negocio

- **Referencia IEEE:**  
  M. Daoud, A. El Mezouari, N. Faci, D. Benslimane, Z. Maamar, and A. El Fazziki, "A multi-model based microservices identification approach," *Journal of Systems Architecture*, vol. 118, p. 102200, Sept. 2021, doi: `10.1016/j.sysarc.2021.102200`.
- **DOI Verificado:** [10.1016/j.sysarc.2021.102200](https://doi.org/10.1016/j.sysarc.2021.102200) *(Revista Indexada: Elsevier JSA — Scopus Q1)*.
- **Resumen Técnico Contextualizado (102 palabras):**  
  El trabajo plantea que la partición de sistemas monolíticos debe responder a los flujos organizacionales y no solo a la sintaxis del código fuente. Los autores formulan un método de identificación sustentado en modelos de procesos de negocio (BPMN) que extrae dependencias de control, intercambio de datos y proximidad semántica respaldada por ontologías OWL. Mediante un algoritmo de agrupamiento jerárquico aglomerativo colaborativo (cHAC), la metodología particiona las actividades empresariales en servicios autónomos. Los experimentos en el sistema de bicicletas compartidas Bicing evidenciaron una reducción notable del acoplamiento inter-servicios y un incremento en la cohesión relacional frente a técnicas de clustering tradicionales.
- **Dato Concreto y Verificable:**  
  *Sección 4.4, págs. 19–21 (Fig. 8, Fig. 9, Tabla 13):* Al aplicar el algoritmo cHAC sobre el caso de estudio *Bicing*, la combinación de dependencias de control, datos y semántica fragment-driven redujo el acoplamiento aferente (AC) y eferente (EC) a valores óptimos en servicios clave como *RequestHandling* (AC=1, EC=2, Cohesión Relacional RC=0.88), superando holgadamente a esquemas basados únicamente en grafos sintácticos.
- **Nota Personal y Articulación con TA-IND-01:**  
  La investigación me convenció de que al estructurar un sistema distribuido, las fronteras de los microservicios deben alinearse estrictamente con los procesos del negocio y los modelos ontológicos de dominio. En el informe **TA-IND-01**, aplicaré este artículo en la sección *"Diseño Arquitectónico Guiado por Procesos de Negocio"*, justificando la modularización del sistema caso de estudio a partir del intercambio de artefactos de datos y la eliminación de dependencias circulares.

---

### Ficha N° 5: Análisis de Compensaciones en Arquitecturas Distribuidas

- **Referencia IEEE:**  
  N. Ford, M. Richards, P. Sadalage, and Z. Dehghani, *Software Architecture: The Hard Parts: Modern Trade-Off Analyses for Distributed Architectures*, 1st ed. Sebastopol, CA, USA: O'Reilly Media, 2021, ISBN: `978-1-492-08689-5`.
- **ISBN Verificado:** `978-1-492-08689-5` *(Libro científico-técnico de referencia internacional, O'Reilly Media)*.
- **Resumen Técnico Contextualizado (100 palabras):**  
  El libro examina los dilemas críticos que emergen al abandonar los monolitos en favor de arquitecturas distribuidas, demostrando que no existen soluciones universales sino compensaciones constantes (trade-offs). Los autores estructuran un marco analítico riguroso donde formalizan el concepto de quantum arquitectónico como la unidad mínima con capacidad de despliegue independiente, alta cohesión y acoplamiento dinámico síncrono. Asimismo, analizan los mecanismos para descomponer datos operacionales mediante impulsores de integración y desintegración, contrastando además la orquestación centralizada con la coreografía reactiva en sagas distribuidas, brindando criterios de decisión esenciales para balancear escalabilidad, consistencia y tolerancia a fallos.
- **Dato Concreto y Verificable:**  
  *Capítulo 2, pág. 29 (pág. 46 del PDF):* Define formalmente el concepto de *Architecture Quantum*: *"An architecture quantum is an independently deployable artifact with high functional cohesion, high static coupling, and synchronous dynamic coupling"*. En el *Capítulo 6 (págs. 132–146)*, formaliza los 'Data Disintegrators' (fuerzas para segregar bases de datos) frente a los 'Data Integrators' (consistencia ACID que exige unificarlas).
- **Nota Personal y Articulación con TA-IND-01:**  
  Esta obra me proporcionó una mentalidad crítica fundamental: en la ingeniería de software distribuida nunca existen "mejores prácticas" absolutas, sino únicamente compensaciones entre atributos de calidad. Entendí con precisión que si dos microservicios comparten una misma base de datos relacional, pertenecen fácticamente al mismo quantum arquitectónico y pierden su independencia de despliegue. En **TA-IND-01**, este libro será el pilar rector de la sección *"Análisis Crítico de Compensaciones (Trade-Offs), Transacciones Distribuidas y Descomposición de Datos"*.

---

## 🛡️ Declaración de Uso Ético de Inteligencia Artificial

- **Herramienta empleada:** Gemini (Google).
- **Finalidad:** Apoyo auxiliar exclusivamente para la corrección de ortografía, puntuación (comas y tildes), estilo gramatical y revisión de sintaxis del código fuente en LaTeX (`main.tex`). En ningún momento se empleó para generar automáticamente el contenido técnico.
- **Verificación y Autoría Humana:** Todos los resúmenes, síntesis conceptuales, datos numéricos y notas de reflexión técnica fueron extraídos, analizados y redactados directamente por el estudiante a partir de la lectura exhaustiva de los 5 documentos PDF locales adjuntos a la carpeta. Se verificó manualmente cada DOI, ISBN, volumen, autores y páginas en las publicaciones originales.

---

## 👤 Información del Autor
**Luis Alberto Paca Pilataza**  
Estudiante del 7mo Nivel — Paralelo "A"  
Carrera de Ingeniería de Software  
Universidad Técnica Estatal de Quevedo (UTEQ)  
Correo: `lpacap@uteq.edu.ec`
