# RESPUESTAS — Reflexión y Resumen (Plantilla genérica)

> **Actividad / ID:** 2.a.e
> **Unidad / Tema:** UD 2: Análisis de incidentes de ciberseguridad
> **Alumno/a:** Carlos Alcina Romero
> **Fecha:** 2026-02-23

---

## 1) Reflexión crítica (preguntas)
Responde con **lenguaje técnico** y **argumentos** (no solo opiniones). Si procede, usa ejemplos, riesgos y decisiones justificadas.

### 1.1) ¿Qué te han parecido los temas tratados en la unidad?
- Me han parecido temas bastante bien conectados entre sí: empiezas aprendiendo a **nombrar y clasificar** incidentes (taxonomía) y acabas viéndolos en un flujo real de trabajo: **logs/SIEM → alertas → investigación (OSINT) → respuesta**.
- Me quedo con que no basta con “detectar”: en un entorno tipo SOC importa el **proceso completo** (contención, erradicación, recuperación) y que la **documentación** es lo que da trazabilidad y permite mejorar en las lecciones aprendidas.

### 1.2) ¿Qué ha sido más útil para tu futuro puesto de trabajo? ¿Por qué?
- **Casos de uso + SIEM**: porque en un SOC al final trabajas por alertas, correlación y procedimientos de respuesta; tener casos de uso claros reduce improvisación.
- **Documentación de incidentes**: porque aporta trazabilidad, mejora la respuesta y permite aprender (y defender decisiones técnicas ante responsables o auditorías).

### 1.3) ¿Qué partes ya conocías y cuáles han sido nuevas para ti?
- Conocía: la idea de **CIA (confidencialidad, integridad, disponibilidad)** y el concepto general de “incidente”.
- Nuevo/afianzado: **diferencias SOC vs CERT/CIRT/CSIRT**, cómo un **SIEM** recoge logs (agentes, syslog, agentless), el enfoque de **casos de uso** (IOC, fuentes, reglas, validación) y la importancia de **retención** y **fatiga de alertas**.
- Nuevo: ver **OSINT** como apoyo rápido para dar contexto (sin técnicas invasivas) y cómo encaja en investigación.

### 1.4) ¿Qué concepto/idea te ha llamado más la atención y por qué?
- La **fatiga de alertas** y la idea de que “más herramientas” no significa “mejor seguridad”. Si no hay flujo de trabajo, priorización y contexto, el equipo se satura y el riesgo sube.

### 1.5) ¿Qué parte recortarías o simplificarías si hubiera menos tiempo? Justifica.
- Recortaría detalles muy de “panorama de mercado” (p. ej., listados de productos o referencias) y me quedaría con lo operativo: **qué objetivos tiene el SIEM**, **qué fuentes priorizar**, **cómo crear y validar casos de uso** y **cómo responder/documentar**.
- Justificación: con poco tiempo, lo que más impacta en un puesto junior es saber **triage + respuesta + documentación** con criterios claros.

### 1.6) ¿Qué tema has echado en falta o ampliarías? Justifica.
- Más parte práctica de **tuning** de reglas (reducir falsos positivos), y ejemplos completos de un caso de uso “de principio a fin” (logs → regla → alerta → investigación → cierre).
- Ampliaría ejercicios tipo simulacion, tomar decisiones de contención/erradicación con un “timeline” y evidencias.

### 1.7) ¿Qué aplicarías “mañana” en un entorno real con recursos limitados?
- Definir una **taxonomía mínima** de incidentes + severidades para hablar todos el mismo idioma.
- Centralizar logs básicos (autenticación, endpoints, firewall/proxy) con **syslog** o agentes y llevarlos a un SIEM.
- Crear 3–5 **casos de uso** de alto valor (cuentas comprometidas, movimiento lateral, exfiltración, phishing) con procedimientos de respuesta cortos.
- Montar una **plantilla de documentación**: qué pasó, cuándo, impacto, evidencias, acciones, y “lecciones aprendidas”.

### 1.8) ¿Qué duda, riesgo o punto crítico te queda abierto tras la unidad?
- Riesgo: montar un SIEM “por acumular logs” sin objetivos ni priorización de fuentes (ruido y coste).
- Duda práctica: cómo equilibrar **detección** vs **falsos positivos** para no caer en fatiga de alertas.
- Punto crítico: definir bien **retención** (qué guardar y cuánto) y asegurar trazabilidad/evidencias para investigación posterior.


## 2) Resumen esquematizado (obligatorio)
Incluye **todos los puntos** vistos en la unidad. Prioriza esquema/tabla/listas sobre párrafos largos.

### 2.1) Mapa/índice de la unidad (visión global)
- **2.1.1 Taxonomía de incidentes**: lenguaje común para clasificar y comunicar.
- **2.2.1 SOC**: objetivos (prevención/detección/respuesta/recuperación) + ecosistema de herramientas.
- **2.2.2 Casos de uso**: cómo pasar de logs/IOC/reglas a alertas y respuesta repetible.
- **2.2.2 SIEM**: qué es y cómo funciona (recolección, almacenamiento, correlación y alertas).
- **2.2.3 Implantación SIEM**: fases, objetivos, fuentes y retención.
- **2.2.4 Evolución SIEM + SOAR**: automatización/orquestación y gestión de fatiga de alertas.
- **2.3.1 OSINT**: fuentes abiertas para aportar contexto rápido en incidentes.
- **2.4.1 Documentación de incidentes**: qué documentar y por qué (seguimiento + mejora continua).
- **2.5 Informes técnicos**: estructura y estilo para comunicar hallazgos.

**Flujo “de extremo a extremo” (idea central de la unidad):**
- Taxonomía → Logs (fuentes) → SIEM (correlación/alerta) → Triage/Investigación (incluye OSINT) → Respuesta (contener/erradicar/recuperar) → Documentación → Lecciones aprendidas.

### 2.2) Conceptos clave (lista breve)
- **Incidente de seguridad**: afecta a CIA (confidencialidad, integridad, disponibilidad).
- **Incidencia**: problema de servicio, no necesariamente de seguridad.
- **Ciclo de vida**: preparación → identificación → contención → erradicación → recuperación → lecciones aprendidas.
- **Taxonomía**: clasificación estándar para describir incidentes.
- **SOC**: monitoriza, detecta, responde y previene (operación continua).
- **CERT/CIRT/CSIRT**: equipos orientados a respuesta ante incidentes (más “reactivo/crítico”).
- **SIEM**: centraliza logs, normaliza, correlaciona y alerta; incluye paneles e informes; define **retención**.
- **Caso de uso**: escenario + fuentes + IOC + regla/alerta + procedimiento de respuesta + validación.
- **IOC**: indicador de compromiso (IP, hash, URL, patrón, etc.).
- **OSINT**: inteligencia con fuentes públicas/legítimas para contexto.
- **Fatiga de alertas**: demasiadas alertas sin priorización/flujo → saturación.
- **SOAR**: orquestación/automatización de respuesta (playbooks/runbooks).

### 2.3) Procesos / procedimientos (pasos o checklist)
- **A) Gestión de incidentes (SANS / 6 pasos)**
	- Preparación
	- Identificación
	- Contención
	- Erradicación
	- Recuperación
	- Lecciones aprendidas

- **B) Caso de uso en un SOC (checklist de creación)**
	- Amenaza relevante → escenario → fuentes de logs
	- Definir IOC → regla/correlación → alerta
	- Procedimiento de respuesta (quién hace qué)
	- Validación (pruebas/simulaciones) → ajuste (tuning) → documentación/capacitación
	- Revisión periódica (mejora continua)

- **C) Implantación de SIEM (checklist mínimo viable)**
	- Objetivos (detección/cumplimiento/visibilidad/métricas)
	- Inventario y priorización de fuentes
	- Método de recolección (agentes / syslog / agentless)
	- Normalización y almacenamiento
	- Retención (qué, cuánto, dónde) + acceso forense
	- Casos de uso iniciales + métricas + tuning

- **D) OSINT en investigación de incidentes**
	- Recopilar información pública → validar/contrastar → añadir contexto → registrar hallazgos (para trazabilidad)

- **E) Documentación del incidente (qué no puede faltar)**
	- Timeline + evidencias + impacto + decisiones/acciones + estado/seguimiento + cierre + lecciones aprendidas

### 2.4) Herramientas / técnicas (si aplica)
| Bloque | Qué aporta | Ejemplos/Notas |
|---|---|---|
| **SIEM** | Centraliza logs, correlaciona y genera alertas | Base de trabajo del analista SOC |
| **Recolección de logs** | Llevar eventos al SIEM | **Agentes**, **syslog**, **agentless** |
| **Agentes** | Parseo/buffer/integridad/cifrado (según agente) | Beats (Elastic), NXLog (open source populares) |
| **Controles/telemetría** | Señales para detección | IDS/IPS, firewalls, EDR, etc. |
| **SOAR** | Automatizar/orquestar respuestas | Playbooks/runbooks (con control y trazabilidad) |
| **UEBA / TIP** | Contexto y análisis más avanzado | Útil para reducir falsos positivos si se aplica bien |
| **OSINT** | Contexto verificable con fuentes públicas | Reputación de IP/dominio, relaciones, campañas |
| **Red/monitorización** | Evidencia técnica de tráfico | Wireshark (ejemplo citado) |

### 2.5) Buenas prácticas y errores típicos
| Buenas prácticas | Errores típicos |
|---|---|
| Objetivos claros del SIEM (qué quiero conseguir) | “Meter logs por meter” (ruido + coste) |
| Priorizar fuentes (las que dan señal de verdad) | No diferenciar señal vs ruido |
| Casos de uso con procedimiento y validación | Reglas sin tuning → falsos positivos |
| Medir y ajustar (mejora continua) | No revisar casos de uso con el tiempo |
| Retención y trazabilidad bien definidas | Sin evidencias/timeline → investigación débil |
| Documentar en todas las fases | Cerrar incidentes sin lecciones aprendidas |

### 2.6) Glosario mínimo (términos y definiciones cortas)
- **Taxonomía de incidentes:** clasificación estándar para describir incidentes.
- **SOC:** operación continua de seguridad (monitorización, detección, respuesta, prevención).
- **SIEM:** centraliza logs, correlaciona eventos y genera alertas/reporting.
- **Caso de uso:** detección + respuesta definida para un escenario repetible.
- **IOC:** indicador observable de compromiso (IP/hash/URL/patrón).
- **Syslog:** protocolo para enviar logs por red (UDP/TCP, opcional TLS).
- **Retención:** cuánto tiempo se guardan logs/evidencias y cómo se accede a histórico.
- **Triage:** priorización rápida de alertas (qué es crítico vs qué puede esperar).
- **OSINT:** inteligencia con fuentes abiertas/legítimas para dar contexto.
- **SOAR:** orquestación/automatización de respuestas (playbooks/runbooks).


## 3) Conclusión (cierre)
- La unidad me deja una idea clara: para analizar incidentes hace falta **método** (taxonomía + procesos), **visibilidad** (logs/SIEM) y **disciplina** (documentación y mejora continua).
- Si tuviera que resumirlo en una frase: “detectar rápido está bien, pero responder y dejarlo documentado es lo que hace que la organización aprenda y sea más fuerte”.
