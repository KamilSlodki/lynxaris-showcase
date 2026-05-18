# Protocolo de documentación

Este proyecto se desarrolló bajo el protocolo de documentación propio del autor, replicado cross-proyecto en múltiples proyectos del ecosistema. **La documentación es activo de primera clase, no afterthought.**

> Este showcase aplica **sanitización agresiva por sensibilidad regulatoria del dominio**. Datos de listas de sanciones concretas, identificadores de entidades reales, samples ECCN dual-use, outputs de modelos ML por corredor específico, endpoints exactos, secretos de integración, configuración de infraestructura, dashboards en vivo, datos de clientes pilotos y artefactos comerciales NO se publican. El subset técnico mostrado es la arquitectura y los patterns que demuestran disciplina de ingeniería sin comprometer compliance regulatorio (GDPR · LOPDGDD · MAR EU · export control US/EU).

---

## 5 capas documentales

### 1. arc42 — Marco de arquitectura del software

Marco estandarizado de 12 secciones. El proyecto privado tiene arc42 completo cubriendo objetivos · restricciones · contexto · estrategia de solución · vista de bloques · vista de runtime · vista de despliegue · conceptos cross-cutting · decisiones · requisitos de calidad · riesgos · glosario. En el showcase público se proyectan las secciones genéricas (estrategia · vista de bloques · cross-cutting · calidad técnica). Secciones con datos sensibles (despliegue específico · riesgos detallados · glosario regulatorio interno) quedan fuera.

### 2. C4 — Modelo visual de arquitectura

Notación Simon Brown: Context · Container · Component · Code. En este showcase se publican los niveles **Context** y **Container** vía Mermaid (render nativo en GitHub) con identificadores abstractos. Niveles Component y Code quedan fuera del scope público — y los nombres de archivos / endpoints / esquemas internos NO se publican en ningún nivel.

### 3. ADR — Architecture Decision Records

ADRs versionadas con plantilla fija:

```
contexto: <problema o trade-off>
decisión: <qué se elige y por qué>
alternativas: <evaluadas y descartadas>
consecuencias: <impacto positivo + negativo + nuevas dependencias>
plan_rollout: <pasos para aplicar>
plan_rollback: <pasos para revertir>
```

ADRs concretas con detalles internos quedan en el proyecto privado. El showcase referencia el patrón y la disciplina, no el contenido específico.

### 4. Runbooks operativos

Procedimientos de daily ingest · matching engine deployment · audit log integrity check · tenant onboarding · API key rotation · incident response. NO se publican por contener credenciales, paths y referencias a infraestructura concreta.

### 5. Postmortems formales

Cada incidente cierra con postmortem: cronología · causa raíz (5 whys) · acción correctiva → ADR · métrica de prevención. Los aprendizajes transferibles alimentan el engineering-playbook cross-proyecto. Los postmortems concretos quedan en privado.

---

## Auditorías internas (verify-findings)

El proyecto privado tiene auditorías internas previas bajo doctrina verify-findings cubriendo arquitectura · integración · semántica de modelos · módulos · validación enterprise · niveles de producto + AI · UX · diagnóstico · cross-references. Cada una con:

- 5 campos obligatorios por hallazgo (cita textual · ubicación archivo:línea · severidad · fix concreto · pasada adversarial).
- Ratio de ruido objetivo < 15%.
- Pasada adversarial con segundo agente independiente.

---

## Compliance documental

Documentos regulatorios formales mantenidos en privado:

- **DORA inventory** (Digital Operational Resilience Act).
- **SOC 2 / ISO 27001 roadmap** con compromisos de controles.
- **Incident Response Plan** formal.
- **Single Source of Truth** canónico (métricas e invariantes validables vía grep).
- **Pentest scope** documentado con metodología OWASP y SLAs.

---

## Disciplina cross-proyecto

- **Engineering-playbook propio** con disciplina doctrinal cross-proyecto.
- **`verify-findings` adversarial**: auditoría con segundo agente independiente. Ratio de ruido objetivo < 15 %.
- **Convenciones**: español · sin emojis decorativos · tono operativo y directo.
- **Invariantes core** declaradas (matching determinista · oracle scoring · ingest delta + upsert · audit log append-only · tenant isolation) testeadas vía suite.
- **NO LLM como decisor** de compliance (explicabilidad como invariante regulatoria).
- **OPSEC explícita**: el showcase NO menciona corredores específicos, NO publica parámetros operativos, NO expone nombres de archivos del proyecto privado, NO revela región de deploy, NO publica versiones exactas del stack y NO incluye samples ECCN concretos.

---

*Detalles operativos completos del playbook y del proyecto privado bajo consideraciones de compliance y prudencia operativa.*
