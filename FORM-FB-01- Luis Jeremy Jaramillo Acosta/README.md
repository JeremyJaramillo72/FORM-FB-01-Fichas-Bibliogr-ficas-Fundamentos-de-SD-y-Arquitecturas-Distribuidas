# FICHA BIBLIOGRÁFICA: FORM-FB-01
## Fundamentos de Sistemas Distribuidos y Arquitecturas Distribuidas

---

### 📌 Datos Informativos
- **Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)
- **Facultad:** Facultad de Ciencias de la Computación / Ciencias de la Ingeniería
- **Carrera:** Ingeniería de Software
- **Asignatura:** Aplicaciones Distribuidas (SOF-I-R)
- **Nivel / Paralelo:** 7mo Nivel — Paralelo "A"
- **Docente:** Dr. Gleiston Cicerón Guerrero Ulloa
- **Estudiante Responsable:** Luis Jeremy Jaramillo Acosta
- **C.I.:** 1206898718
- **Correo Institucional:** `ljaramilloa@uteq.edu.ec`
- **Código de Actividad:** FORM-FB-01

---

### 📖 Referencia Principal Analizada

#### Formato IEEE:
> A. Avizienis, J.-C. Laprie, B. Randell, and C. Landwehr, "Basic concepts and taxonomy of dependable and secure computing," *IEEE Transactions on Dependable and Secure Computing*, vol. 1, no. 1, pp. 11–33, Jan.–Mar. 2004, doi: [10.1109/TDSC.2004.2](https://doi.org/10.1109/TDSC.2004.2).

#### Formato APA (7.ª edición):
> Avizienis, A., Laprie, J.-C., Randell, B., & Landwehr, C. (2004). Basic concepts and taxonomy of dependable and secure computing. *IEEE Transactions on Dependable and Secure Computing*, 1(1), 11–33. https://doi.org/10.1109/TDSC.2004.2

---

### 📂 Estructura de esta Carpeta

```text
FORM-FB-01- Luis Jeremy Jaramillo Acosta/
│
├── README.md                                          # Ficha bibliográfica detallada del estudiante
├── Referencia (PDF)/                                 # Documentos y artículos fuente en formato PDF
│   ├── Basic_concepts_and_taxonomy_of_dependable_and_secu.pdf
│   └── R. Vitillo, Understanding Distributed Systems What Every Developer Should Know About Large Distributed Applications, 2nd ed. London.pdf
│
└── Referencias (.bib)/                                # Citas estructuradas en formato BibTeX
    ├── Avizienis2004Dependable.bib
    └── Vitillo2022DistributedSystems.bib
```

---

### 📑 Contenido de la Ficha Bibliográfica

#### 1. Resumen Ejecutivo
El artículo presenta un marco conceptual unificado y una taxonomía exhaustiva para la confiabilidad (*dependability*) y la seguridad en sistemas computacionales, con especial aplicación en arquitecturas y sistemas distribuidos. Los autores integran conceptos previamente fragmentados entre las comunidades de tolerancia a fallos y seguridad de la información. Se definen formalmente las amenazas (fallas, errores y averías), los atributos de la confiabilidad (disponibilidad, confiabilidad operativa, seguridad frente a catástrofes, integridad y mantenibilidad) y los medios para alcanzarla (prevención, tolerancia, eliminación y pronóstico de fallas).

#### 2. Palabras Clave
- *Dependability* (Confiabilidad sistémica)
- *Fault Tolerance* (Tolerancia a fallos)
- *Availability* (Disponibilidad)
- *Fault-Error-Failure Chain* (Cadena Falla-Error-Avería)
- *Distributed Systems Security* (Seguridad en Sistemas Distribuidos)
- *System Taxonomy* (Taxonomía de Sistemas)

#### 3. Cadena Fundamental de Causación: Falla $\rightarrow$ Error $\rightarrow$ Avería
1. **Falla (*Fault*):** La causa interna o externa que da origen a un estado anómalo (ejemplo: caída de un nodo en el clúster, cable de red desconectado o bug en el código).
2. **Error (*Error*):** La manifestación del estado anómalo dentro del sistema que puede llevar a una falla visible (ejemplo: inconsistencia en la memoria o retraso de mensajes en la cola).
3. **Avería / Fracaso (*Failure*):** La desviación del servicio entregado respecto a las especificaciones o expectativas del usuario (ejemplo: respuesta 503 Service Unavailable, datos corruptos entregados al cliente).

#### 4. Medios para Garantizar la Confiabilidad en Arquitecturas Distribuidas
- **Prevención de Fallas (*Fault Prevention*):** Prácticas de diseño riguroso y arquitecturas defensivas.
- **Tolerancia a Fallos (*Fault Tolerance*):** Detección de errores y recuperación del sistema (enmascaramiento mediante replicación, consenso distribuido como Raft/Paxos).
- **Eliminación de Fallas (*Fault Removal*):** Pruebas de integración, verificación formal y depuración continua.
- **Pronóstico de Fallas (*Fault Forecasting*):** Monitoreo telemétrico, métricas de confiabilidad (MTTF, MTBF, MTTR).

#### 5. Aplicabilidad en Sistemas Distribuidos Modernos
En entornos distribuidos modernos (microservicios, nube y sistemas basados en red), los nodos individuales son inherentemente propensos a fallar de manera independiente (*partial failures*). Esta taxonomía establece la justificación teórica para implementar patrones arquitectónicos como:
- **Circuit Breaker** (aislamiento de fallas en cascada).
- **Replicación activa y pasiva** (redundancia de información y de procesamiento).
- **Consenso distribuido** (acuerdo sobre estados globales a pesar de fallas bizantinas o por parada).

#### 6. Conclusión y Valoración Crítica
El trabajo de Avizienis et al. es la referencia canónica indispensable para cualquier estudio sobre sistemas distribuidos. Demuestra que la confiabilidad no es una propiedad añadida a posteriori, sino una propiedad emergente del diseño arquitectónico global. En aplicaciones distribuidas, asumir que la red es confiable es la primera falacia; diseñar tolerando averías parciales es el principio fundamental.
