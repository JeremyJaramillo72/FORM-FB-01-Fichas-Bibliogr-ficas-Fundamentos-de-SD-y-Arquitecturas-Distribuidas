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
- **Estudiante Responsable:** Heiner Ariel Zambrano Ronquillo
- **C.I.:** 0957140346
- **Correo Institucional:** `hzambranor@uteq.edu.ec`
- **Código de Actividad:** FORM-FB-01

---

### 📖 Referencia Principal Analizada

#### Formato IEEE:
> P. Haindl, P. Kochberger, and M. Sveggen, "A Systematic Literature Review of Inter-Service Security Threats and Mitigation Strategies in Microservice Architectures," *IEEE Access*, vol. 12, pp. 83820–83856, 2024, doi: [10.1109/ACCESS.2024.3406500](https://doi.org/10.1109/ACCESS.2024.3406500).

#### Formato APA (7.ª edición):
> Haindl, P., Kochberger, P., & Sveggen, M. (2024). A Systematic Literature Review of Inter-Service Security Threats and Mitigation Strategies in Microservice Architectures. *IEEE Access*, 12, 83820–83856. https://doi.org/10.1109/ACCESS.2024.3406500

---

### 📂 Estructura de esta Carpeta

```text
FORM-FB-01- Zambrano Ronquillo Heiner/
│
├── README.md                                          # Ficha bibliográfica detallada del estudiante
├── Referencia (PDF)/                                 # Documento de investigación en formato PDF
│   └── A_Systematic_Literature_Review_of_Inter-Service_Se.pdf
│
└── Referencias (.bib)/                                # Cita estructurada en formato BibTeX
    └── Haindl2024MicroserviceSecurity.bib
```

---

### 📑 Contenido de la Ficha Bibliográfica

#### 1. Resumen Ejecutivo
Esta revisión sistemática de la literatura (SLR), desarrollada conforme a las directrices PRISMA 2020 y Kitchenham & Charters, analiza 54 estudios científicos publicados entre 2015 y 2023 sobre las amenazas de seguridad y estrategias de mitigación en la comunicación inter-servicios (*inter-service security*) de arquitecturas de microservicios (MSA). El estudio clasifica las amenazas en áreas críticas como el perímetro de seguridad difuso, expansión de superficie de ataque, confianza ciega entre servicios (*Confused Deputy Problem*), y vulnerabilidades en contenedores y herramientas de orquestación (Docker, Kubernetes). Asimismo, sintetiza las estrategias de mitigación líderes: DevSecOps, mTLS, Service Mesh (Istio, Linkerd), API Gateway, y principios Zero Trust.

#### 2. Palabras Clave
- *Microservices Architecture* (Arquitectura de Microservicios)
- *Inter-Service Security* (Seguridad entre Servicios)
- *Security Threats* (Amenazas de Seguridad)
- *Mitigation Strategies* (Estrategias de Mitigación)
- *Service Mesh & Sidecar* (Malla de Servicios y Patrón Sidecar)
- *Zero-Trust Model* (Modelo de Cero Confianza)

#### 3. Amenazas Clave en la Comunicación Inter-Servicios
1. **Expansión de la Superficie de Ataque:** La descentralización de servicios conectados a través de la red amplía exponencialmente los puertos y APIs expuestas.
2. **Confianza Implícita en la Red (*Pivoting*):** Asumir que el tráfico interno de la red es seguro permite que la vulneración de un solo microservicio otorgue al atacante acceso y control lateral sobre todo el ecosistema.
3. **Vulnerabilidades en Contenedores e Imágenes Base:** Uso de imágenes con configuraciones por defecto o bibliotecas desactualizadas compartidas en entornos homogéneos.
4. **Falta de Trazabilidad y Detección de Intrusos:** Dificultad para rastrear peticiones distribuidas a través de múltiples saltos de red.

#### 4. Estrategias de Mitigación y Patrones Arquitectónicos
- **Mutual TLS (mTLS):** Encriptación bidireccional y autenticación criptográfica obligatoria entre microservicios.
- **Service Mesh & Patrón Sidecar:** Delegación de la seguridad de red, balanceo y observabilidad a proxies ligeros sin tocar el código de negocio de cada servicio.
- **API Gateway:** Centralización de autenticación perimetral, limitación de tasa (*rate limiting*) y terminación SSL.
- **Principio de Mínimo Privilegio y Cero Confianza (Zero Trust):** Verificación continua de identidad y permisos para cada transacción, independientemente de su origen.

#### 5. Relevancia para los Fundamentos de Sistemas Distribuidos
El estudio fundamenta que la seguridad en sistemas distribuidos no puede tratarse con los enfoques perimetrales de los sistemas monolíticos tradicionales. En arquitecturas distribuidas, cada nodo debe asumir que la red subyacente es hostil y aplicar autenticación y autorización granular a nivel de servicio.

#### 6. Conclusión y Valoración Crítica
La investigación de Haindl et al. resalta una necesidad imperiosa: la estandarización de una taxonomía de seguridad y la adopción de arquitecturas Zero Trust en los sistemas distribuidos modernos. Para ingenieros de software, el artículo es una guía indispensable para seleccionar patrones y herramientas (como Istio o Envoy) que mitiguen de forma práctica las vulnerabilidades inherentes a la comunicación distribuida.
