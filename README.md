# Lynxaris — Trade Risk Intelligence

### Trade Compliance & Geopolitical Risk Intelligence Platform — Showcase

**Lynxaris.com** *(sitio en preparación)* · *Sanctions, goods and routes — with the evidence behind every call.*

**Engineered by [Kamil Slodki](https://www.linkedin.com/in/kamilslodki/)** · Valencia, España · Remote-first

**Plataforma SaaS multi-tenant de compliance para comercio internacional con 3 niveles de control integrados (sanctions screening contra listas oficiales públicas OFAC SDN · UN Consolidated · EU CFSP · UK OFSI · HMT · BIS vía ingest delta-tracking diario con upsert atómico; dual-use export controls contra EU Annex I del Reglamento 2021/821 + ECCN codes US BIS + HS/TARIC tariff codes con mapping textual fuzzy descripción técnica → código regulatorio + rule engine de destination controls por país; routes & geopolitical risk intelligence sobre corredores marítimos y aéreos principales globales con NLP keyword-based + negation detection + source credibility weighting sobre noticias en tiempo real + integración a fuentes OSINT públicas ACLED / GDELT / IMB piracy reports / USGS earthquakes / national travel advisories + cálculo de impacto geográfico vía Haversine distance + buffer expansion dinámico + intersección con geometría de rutas + scoring dinámico de eventos por tipo y severidad) con punto central de orquestación (Integrated Risk Decision Engine) que agrega los 3 niveles vía risk aggregator multi-señal y emite decisión auditable (AUTO-CLEAR · REVIEW · FLAG · BLOCK) con reason codes explicables, aplicación cross-cutting de marine cargo insurance con premium calculator multi-factor (valor carga · tipo cargo · risk score ruta · war risk premium · múltiples perfiles de carga con risk multipliers diferenciados), aplicaciones horizontales en desarrollo (case management workflow · OSINT enrichment · PEP / UBO monitoring · adverse media), motor de matching fuzzy ensemble propio con 3 algoritmos combinados (RapidFuzz token_set_ratio + Soundex + Metaphone para nombres no latinos transliterados) y oracle scoring multi-feature (similitud nombre · alias strength · multi-list bonus · program risk · entity type · pattern recognition) con reason codes auditables enumerables, motor de optimización de rutas multi-criteria con Pareto frontier analysis sobre múltiples dimensiones (cost · time · safety/geopolitical risk · carbon footprint · ESG · balanced) y constraints duros (sanciones bloquean automáticamente · bloqueos legales por jurisdicción · max_transit_days · max_cost · max_risk_score · max_carbon_kg · avoid_countries), audit log append-only inmutable a nivel de servicio con integrity validation, invariantes core declaradas y testeadas (matching determinista auditado · oracle scoring con reason codes · ingest con delta tracking y upsert atómico · audit log append-only · tenant_id derivado de API key con isolation estricta), multi-tenancy estricto con tenant_id FK en todas las tablas core + API key hash argon2 + rotación API keys + 2FA TOTP, ADRs versionadas con plantilla fija, documentación arc42 completa + auditorías internas previas con doctrina verify-findings, compliance posture documentada con DORA inventory + SOC2 / ISO27001 roadmap + Incident Response Plan + Single Source of Truth canónico, RBAC granular (Admin · Compliance Officer · Analyst · Viewer · Auditor) con matrix de permisos, integraciones outbound (webhooks via adapter pattern · APIs externas opcionales · email service · webhook signing), observabilidad con OpenTelemetry + Sentry, daily ingest scheduler con cron + Celery + Redis queue + healthchecks, frontend i18n multi-locale, deployment dual cloud con docker-compose para local dev. Stack Python + FastAPI + SQLAlchemy 2 + Alembic + PostgreSQL + Redis + Celery + RapidFuzz + Next.js + React + Radix UI + Tailwind + NextAuth + OpenTelemetry + Sentry. Diseñado como producto propio del autor — actualmente en estado de proyecto técnico (no en producción comercial activa).**

[![Type](https://img.shields.io/badge/type-showcase%20%C2%B7%20producto%20propio-blue.svg)](#sobre-este-showcase)
[![Track](https://img.shields.io/badge/track-dual%20%C2%B7%20A%20%2B%20B-blue.svg)](#tracks-target)
[![Status](https://img.shields.io/badge/status-proyecto%20t%C3%A9cnico%20avanzado-success.svg)](#estado-y-madurez-técnica)
[![Role](https://img.shields.io/badge/role-AI%20Systems%20Engineer%20%E2%80%A2%20B2B%20Delivery%20Engineer-blueviolet.svg)](#contacto)
[![Engineering Doctrine](https://img.shields.io/badge/engineering%20doctrine-5%20protocols-9cf.svg)](#sistema-operativo-de-ingeniería-del-autor)
[![Domain](https://img.shields.io/badge/domain-international%20trade%20compliance%20%C2%B7%20geopolitical%20risk-9cf.svg)](#funcionalidad-3-niveles--cross-cutting)
[![Stack](https://img.shields.io/badge/stack-FastAPI%20%7C%20Postgres%20%7C%20Redis%20%7C%20Celery%20%7C%20Next.js%20%7C%20OpenTelemetry-informational.svg)](#stack-técnico)

<sub>Última actualización: 2026-11-18</sub>

> **Nota sobre alcance del showcase (disciplina de OPSEC explícita)**: este repositorio NO menciona corredores marítimos específicos, NO publica parámetros operativos del matching engine, NO expone nombres de archivos del proyecto privado, NO revela región de deploy, NO publica versiones exactas del stack y NO incluye samples ECCN concretos. La sanitización es **prueba positiva de disciplina de compliance**, no limitación. Datos de listas de sanciones reales, identificadores de entidades, samples dual-use con clasificación específica, endpoints exactos, secretos de integración, identificadores de modelos ML por corredor concreto, configuración de infraestructura y artefactos comerciales **NO se publican** por consideraciones regulatorias (GDPR · LOPDGDD · MAR EU · export control US/EU) y prudencia operativa.

---

## Sobre este showcase

Plataforma técnicamente compleja de **compliance para comercio internacional** que integra en una sola arquitectura coherente tres dominios regulatorios habitualmente fragmentados (sanctions screening · dual-use export controls · routes & geopolitical risk) más una capa cross-cutting de marine cargo insurance que materializa el valor económico del scoring agregado.

**Es proyecto propio del autor en estado de producto técnico avanzado** — actualmente no en producción comercial activa. Lo que muestra el showcase no es marketing, son **patrones de ingeniería verificables** sobre uno de los dominios más regulados del software empresarial: trade compliance.

El interés del showcase es **técnico-arquitectónico**: la disciplina aplicada a un dominio con cero margen de error regulatorio (multas directas · bloqueo de comercio legítimo si falso positivo · permitir transacción sancionada si falso negativo).

---

## Tracks target

| Track A — AI Systems · Production LLM/ML | Track B — B2B Delivery Engineering |
|---|---|
| Matching fuzzy ensemble multi-algoritmo con oracle scoring multi-feature + reason codes auditables · NLP rule-based + negation + source credibility · optimización multi-criteria Pareto · sin LLM como decisor final (explicabilidad como invariante regulatoria) | Multi-tenant SaaS con tenant isolation estricta · audit log append-only inmutable · RBAC granular · ADRs versionadas · DORA inventory + SOC2/ISO27001 roadmap · documentación arc42 completa · auditorías internas con doctrina verify-findings · integraciones via adapter pattern · daily ingest scheduler con delta-tracking · compliance posture con Incident Response Plan |

Track dual: el proyecto cumple ambos. AI sin LLM como decisor (decisión determinista trazable) + delivery institucional con compliance verificable.

---

## El problema

El compliance del comercio internacional vive fragmentado en silos:

- **Sanctions screening** se hace contra listas oficiales públicas (OFAC · UN · EU · UK) con motores de fuzzy matching que producen miles de falsos positivos.
- **Export controls de dual-use** se gestionan manualmente con tablas de ECCN + Annex I del Reglamento EU 2021/821 + HS/TARIC, con clasificación textual propensa a error humano.
- **Geopolitical risk de rutas** se monitoriza con dashboards desconectados (cierres de corredores marítimos principales · piratería en estrechos críticos · sanciones que bloquean tránsito · conflictos que cambian el risk premium · catástrofes naturales que afectan corredores).
- **Marine cargo insurance** se cotiza con war risk premiums basados en heurísticas opacas.

Cada silo decide por su cuenta. **Cuando los 4 dominios convergen en una sola transacción** (¿este buyer está sancionado? ¿este producto es dual-use? ¿esta ruta atraviesa una zona con sanciones secundarias? ¿qué premium de seguro aplica?), la fragmentación dispara errores caros: bloqueo de comercio legítimo o autorización accidental de transacción sancionada (multa regulatoria directa).

Antipatrones sistémicos al construir una plataforma que unifique los 4 dominios:

| Antipatrón sistémico de la industria | Patrón aplicado en este sistema |
|---|---|
| Matching fuzzy con un solo algoritmo (típicamente Levenshtein) → no funciona con nombres no latinos transliterados | **Ensemble matcher de 3 algoritmos** (RapidFuzz token_set_ratio + Soundex + Metaphone) con oracle scoring multi-feature explícito y reason codes auditables enumerables |
| LLM como decisor final de compliance → alucinaciones · zero explicabilidad · regulator no acepta "el modelo dijo que sí" como respuesta | **NO LLM como decisor**. Toda decisión de matching / dual-use / route risk es determinista con reason codes auditables. LLM (cuando se usa) es solo enrichment / categorización de noticias OSINT, nunca decisor de compliance |
| Listas de sanciones cargadas full-snapshot diario → ingest pesada · sin trazabilidad de cambios · imposible auditar por qué una entidad apareció/desapareció | **Delta-tracking + upsert atómico** en ingest. Cada cambio (added · modified · removed) trazado con timestamp + source |
| Audit log mutable o ausente → regulator rechaza · imposible reconstruir decisión histórica | **Audit log append-only** con servicio dedicado que garantiza NO UPDATE NI DELETE como invariante validada. Audit trail por screening |
| Multi-tenancy soft (tenant_id en body de la request) → trivial bypass · primera vulnerabilidad explotada en pentest | **Tenant_id derivado de API key hashed (argon2)**, nunca del body. Invariante de tenant isolation testeada |
| Optimización de rutas con un único criterio (cost) → solución "óptima" inviable por riesgo · sin trazabilidad de por qué se eligió esa ruta | **Pareto frontier multi-criteria** sobre múltiples dimensiones (cost · time · safety · carbon · ESG · balanced) con constraints duros (sanciones bloquean · bloqueos legales · avoid_countries) y reasoning por ruta explícito |
| NLP de noticias con LLM puro → coste alto + alucinación geográfica + sin negation handling | **NLP keyword-based con negation detection + source credibility weighting + sentiment**. Tiers de keywords (critical · high · medium) · negation reduce severidad · pesos por credibilidad de fuente configurables · sin dependencia de modelos transformers caros |
| Tracking de catástrofes/conflictos con coordenadas exactas mapeadas a "afecta o no" → falso negativo si evento está cerca pero fuera del polígono | **Haversine distance + buffer expansion dinámico según severidad + intersección con geometría de rutas** (LineString GeoJSON). Permite eventos cercanos a corredor sin estar encima |
| Time-series forecasting sin uncertainty bands → predicción puntual sin contexto de confianza · usuario interpreta como certeza | **Sin cifra inventada**: mientras no haya un modelo entrenado y validado, la previsión responde `available: false` en lugar de un número. Cuando exista, saldrá siempre con banda de confianza, nunca como punto único |
| Forecasts ML como decisores de bloqueo → riesgo legal MAR (Market Abuse Regulation EU) si el output influye precios commodity/seguros | **Forecasts ML como input al risk aggregator, nunca decisor final**. El humano (compliance officer) aprueba/rechaza con audit trail completo |
| Documentación dispersa en wikis / Slack → drift entre código y doc · regulator pide arc42 / runbooks formales y no existen | **arc42 completa + ADRs versionadas + auditorías internas + DORA inventory + SOC2/ISO27001 roadmap + Incident Response Plan + Single Source of Truth canónico**. Documentación es activo de primera clase |
| Una clase / servicio mezcla policy + scoring + side effects → imposible testear · imposible auditar | **Service layer con responsabilidad única por servicio** y separación estricta entre matching · screening · audit · auth · tenant management · classification |

---

## Funcionalidad — 3 niveles + cross-cutting

### Nivel 1 — Sanctions Screening

Screening de entidades (personas físicas + jurídicas) contra **listas oficiales públicas** de sanciones internacionales.

- **Fuentes integradas**: OFAC SDN · UN Consolidated · EU CFSP · UK HMT/OFSI · BIS (más fuentes en pipeline).
- **Ingest diario**: scheduler cron + Celery + Redis queue + healthchecks · delta-tracking · upsert atómico.
- **Volumen**: decenas de miles de entidades canónicas consolidadas multi-fuente con miles de aliases y direcciones.
- **Matching engine**: ensemble multi-algoritmo (ver [stack IA](#stack-ia-detallado)).
- **Decisiones canónicas**: `AUTO-CLEAR` · `REVIEW` · `FLAG` · `BLOCK` — deterministas, auditadas, con reason codes.
- **API**: endpoints de screening individual + batch + integrated (orquestado con N2 y N3).

### Nivel 2 — Commodities / Dual-Use Export Controls

Clasificación y control de productos contra normativa de export control.

- **EU Annex I del Reglamento 2021/821** + **ECCN codes (BIS US)** + **HS/TARIC tariff codes**.
- **Catálogo amplio** de items dual-use indexados con descripción técnica.
- **Matching textual fuzzy** descripción → código regulatorio (descripción natural del producto → ECCN/HS code).
- **Rule engine de destination controls**: matriz país × código regulatorio.
- **Cross-check con N1**: ¿end-user del producto controlado está sancionado?

### Nivel 3 — Routes & Geopolitical Risk Intelligence

Análisis de riesgo geopolítico de **corredores marítimos y aéreos principales globales**.

- **Cobertura**: set de corredores principales globales (no enumerados por prudencia regulatoria — riesgo MAR EU si predicciones por corredor nombrado se interpretan como market-moving).
- **Previsión de conflictos por corredor**: en desarrollo. Hasta tener un modelo entrenado y validado, la API responde `available: false` (política sin mocks, noviembre de 2026).
- **NLP sobre noticias en tiempo real** (keyword-based, no LLM): múltiples categorías de evento clasificadas (conflict · sanctions · infrastructure · regulatory · port operations · maritime threats · …).
- **Fuentes OSINT públicas integradas** como categorías (ACLED conflict data · GDELT event database con Cameo codes · IMB piracy reports · USGS earthquakes · national travel advisories · feeds RSS oficiales).
- **Cálculo de impacto geográfico**: Haversine distance + buffer expansion dinámico según severidad + intersección con geometría de rutas (LineString GeoJSON) almacenada en BD.
- **Risk scoring dinámico**: base risk del corredor + escalation factor por eventos activos + temporal decay + amplificadores semánticos elevan severidad.
- **Outputs canónicos**: risk_level del corredor (LOW · MEDIUM · HIGH · CRITICAL) + alternative routes con tradeoff (cost / days / risk) + timeline histórico de eventos.

### Cross-cutting — Marine Cargo Insurance

Aplicación cross-cutting que materializa el risk score agregado en valor económico verificable.

- **Premium calculator multi-factor**: valor carga × tipo de cargo × risk score de ruta × war risk premium.
- **Perfiles de carga** con risk multipliers diferenciados (categorías industriales, productos perecederos, materiales raw, sectores especializados).
- **ROI analysis**: cambiar ruta = ahorrar $X premium con +Y días tránsito.
- **Cross-integración**: el premium incorpora score de N1 (sanciones en países tránsito) + N2 (¿commodity dual-use en tránsito?) + N3 (risk score corredor).

### Horizontales (en desarrollo)

Capa horizontal de funcionalidades complementarias: case management workflow con FSM explícita · OSINT enrichment sobre entidades flagged · PEP / UBO monitoring · adverse media continuo.

---

## Punto central — Integrated Risk Decision Engine

Los 3 niveles + insurance NO son monolíticos. Son **motores independientes que convergen en un orquestador**:

```
┌─────────────────────────────────────────────────────────┐
│  API client / Frontend                                   │
│  (transaction context: buyer · seller · product ·       │
│   origin · destination · route · value · cargo type)    │
└───────────────────────┬─────────────────────────────────┘
                        │
              ┌─────────▼─────────┐
              │  Integrated Check  │
              │  (orchestrator)    │
              └─────────┬─────────┘
                        │
       ┌────────────────┼────────────────┐
       │                │                │
       ▼                ▼                ▼
┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│  N1         │  │  N2         │  │  N3         │
│  Sanctions  │  │  Dual-Use   │  │  Routes &   │
│  Screening  │  │  Controls   │  │  Geopolitical│
│             │  │             │  │  Risk        │
└──────┬──────┘  └──────┬──────┘  └──────┬──────┘
       │                │                │
       │      ┌─────────┴─────────┐      │
       │      │ Cargo Insurance   │      │
       │      │ (cross-cutting)   │      │
       │      └─────────┬─────────┘      │
       │                │                │
       └────────────────┼────────────────┘
                        │
              ┌─────────▼─────────┐
              │  Risk Aggregator  │
              │  (multi-signal)   │
              └─────────┬─────────┘
                        │
              ┌─────────▼─────────────────────┐
              │  Decision + reason codes      │
              │  AUTO-CLEAR · REVIEW · FLAG · │
              │  BLOCK with explainability    │
              │  + audit log entry            │
              └───────────────────────────────┘
```

**Cada nivel funciona standalone** (un cliente puede llamar solo N1 sin pasar por N2/N3). **Cada nivel alimenta al siguiente** en cascada cuando hay orquestación. **Cada decisión final es auditada** con timestamp + tenant_id + reason codes + nivel que disparó.

---

## Cómo fluyen los datos del screening

Dos vistas complementarias del flujo: una de **flujo de datos end-to-end** (qué pasa con los datos desde que entran hasta que se renderizan en UI) y una de **componentes internos del orquestador** (cómo el Integrated Risk Decision Engine compone la decisión final).

### Vista 1 · Flujo de datos end-to-end

Muestra cómo los payloads de entrada (entity · product · geo · cargo · auth) viajan a través de los 3 niveles + insurance + risk aggregator hasta llegar al audit log y a los consumidores de UI (dashboard, Centro de Comando, mapa interactivo, case detail, regulatory intelligence). Incluye específicamente **cómo los mapas consumen los datos**: el `Route geometry store` aporta los GeoJSON `LineString` de cada corredor, el `Events store` aporta los markers georreferenciados, el `Geo impact engine` aporta los polígonos de buffer dinámico calculados por severidad, y el `vessel position lookup` opcional aporta la posición AIS en tiempo real.

[`assets/diagrams/data-flow.mmd`](assets/diagrams/data-flow.mmd) — render Mermaid en GitHub.

```mermaid
flowchart LR
    IN["Transaction context<br/>entity · product · geo ·<br/>cargo · API key"] --> N1["N1<br/>Sanctions<br/>Screening"]
    IN --> N2["N2<br/>Dual-Use<br/>Controls"]
    IN --> N3["N3<br/>Routes &<br/>Geopolitical"]
    N3 -.->|GeoJSON LineString<br/>events markers<br/>buffer polygons<br/>AIS position| MAPS["Map<br/>rendering"]
    N1 --> AGG["Risk<br/>Aggregator"]
    N2 --> AGG
    N3 --> AGG
    N1 --> INS["Cargo<br/>Insurance"]
    N2 --> INS
    N3 --> INS
    INS --> AGG
    AGG --> DEC["Decision<br/>AUTO-CLEAR / REVIEW /<br/>FLAG / BLOCK<br/>+ reason codes"]
    DEC --> AUDIT["Audit log<br/>append-only"]
    DEC --> UI["UI consumers<br/>dashboard · Centro de Comando ·<br/>case detail · regulatory intel"]
    MAPS --> UI

    classDef in fill:#FF6D00,stroke:#FF9100,color:white
    classDef n1 fill:#C62828,stroke:#B71C1C,color:white
    classDef n2 fill:#7C4DFF,stroke:#651FFF,color:white
    classDef n3 fill:#00897B,stroke:#00695C,color:white
    classDef agg fill:#AD1457,stroke:#880E4F,color:white
    classDef audit fill:#388E3C,stroke:#1B5E20,color:white
    classDef ui fill:#FBC02D,stroke:#F57F17,color:black
    classDef ins fill:#5C6BC0,stroke:#3949AB,color:white
    classDef map fill:#1976D2,stroke:#0D47A1,color:white

    class IN in
    class N1 n1
    class N2 n2
    class N3 n3
    class AGG,DEC agg
    class AUDIT audit
    class UI ui
    class INS ins
    class MAPS map
```

> Diagrama resumen embebido. El [`data-flow.mmd`](assets/diagrams/data-flow.mmd) completo expone componentes internos por nivel: normalizer · fuzzy matcher · phonetic matcher · ensemble combiner · oracle scoring (N1) · textual fuzzy · catalog lookup · destination rule engine (N2) · route geometry store · events store · NLP event classifier · OSINT ingest · geo impact engine · corridor baseline (N3) · cargo profile selector · premium calculator · ROI analysis (Insurance).

### Vista 2 · C4 Component del orquestador (Integrated Risk Decision Engine)

Vista de los **componentes internos del orquestador**: cómo el container central resuelve el tenant, valida schema, despacha en paralelo a los 3 niveles + insurance con timeout handling y partial degradation, agrega las señales con pesos por tenant, genera explicabilidad, emite decisión, escribe al audit log y dispara webhooks/email cuando hay FLAG/BLOCK.

[`assets/diagrams/c4-component-orchestrator.mmd`](assets/diagrams/c4-component-orchestrator.mmd) — render Mermaid en GitHub.

Esta vista complementa el flujo de datos: mientras el data-flow muestra **dónde van los datos**, el component diagram muestra **cómo el orquestador compone la decisión** internamente con sus 12 componentes (auth resolver · schema validator · tenant config loader · level dispatcher · 3 client adapters con caches · insurance client · signal collector · aggregator · explainability generator · decision emitter · audit writer · response serializer).

---

## Capturas de la plataforma

> Capturas tomadas en entorno técnico con datos de demostración. No representan producción comercial activa.

### Landing y propuesta de valor

| Hero | Módulos | Industrias | Demo |
|---|---|---|---|
| ![Landing hero](assets/screenshots/01-landing-hero.png) | ![Módulos](assets/screenshots/02-landing-modules.png) | ![Industrias](assets/screenshots/03-landing-industries.png) | ![Demo](assets/screenshots/04-landing-demo.png) |

### Centro de Comando — verificación unificada multi-nivel

Orquestación L1 (Sanciones) + L2 (Control de exportaciones) + L3 (Riesgo de ruta) + L5 (Medidas comerciales) en una sola operación, con resultado consolidado por nivel.

| Formulario de operación | Resultado consolidado |
|---|---|
| ![Centro de comando — input](assets/screenshots/25-command-center-form.png) | ![Centro de comando — output](assets/screenshots/26-command-center-results.png) |

### Panel principal — Unified Check

Dashboard operativo con 4 tools rápidas (Sanctions Check · Classify Product · Route Intelligence · Trade Monitor), Case Queue, calidad y rendimiento de verificación, fuentes activas, cobertura de datos.

![Unified Check dashboard](assets/screenshots/05-unified-check-dashboard.png)

### Verificación de sanciones (N1)

Screening individual con ensemble matcher multi-algoritmo, multi-list bonus, reason codes auditables y escalación recomendada por confianza.

| Formulario + resultado | Explicabilidad de coincidencias |
|---|---|
| ![Sanctions verification](assets/screenshots/08-sanctions-verification.png) | ![Match explanation](assets/screenshots/09-match-explanation.png) |

### Clasificación de productos / dual-use (N2)

Clasificación contra ECCN + HS/TARIC + EU Annex I con plantillas pre-definidas por categoría industrial, búsqueda rápida y subida de documentos.

| Formulario de clasificación | Evaluación de riesgo + decisión |
|---|---|
| ![Product classification form](assets/screenshots/06-product-classification-form.png) | ![Product classification result](assets/screenshots/07-product-classification-result.png) |

### Inteligencia de rutas (N3)

Mapa interactivo de corredores principales globales, estado en tiempo real, inteligencia en vivo, alertas por evento, alternativas con tradeoff cost/days/risk, vessel position lookup AIS, pre-execution gate con verdict + drivers + ETA confidence.

| Mapa mundial | Vista regional | Panel de detalle |
|---|---|---|
| ![Routes world](assets/screenshots/10-route-intelligence-world.png) | ![Routes Europe](assets/screenshots/11-route-intelligence-europe.png) | ![Routes detail](assets/screenshots/12-route-intelligence-detail.png) |

| Factores de riesgo + evento de impacto | Análisis de costos |
|---|---|
| ![Risk factors](assets/screenshots/13-route-risk-factors.png) | ![Cost analysis](assets/screenshots/14-route-cost-analysis.png) |

| Safe path + AIS lookup | Pre-execution verdict + drivers + alternatives |
|---|---|
| ![Safe path](assets/screenshots/23-route-intelligence-safe-path.png) | ![Pre-execution verdict](assets/screenshots/24-route-pre-execution-verdict.png) |

### Operaciones — hub multi-acción

Hub centralizado: evaluar operación · optimizador de rutas · análisis por lote · rutas guardadas · dossiers de compliance.

![Operations hub](assets/screenshots/15-operations-hub.png)

### Trade Monitor — impacto comercial y señales

Monitorización continua de señales políticas / sanciones / medidas con severidad clasificada, agrupación por tema y trazabilidad por fuente.

| Impacto comercial | Señales agrupadas |
|---|---|
| ![Trade monitor impact](assets/screenshots/16-trade-monitor-impact.png) | ![Trade monitor signals](assets/screenshots/19-trade-monitor-signals.png) |

### Aranceles y medidas

Registro de medidas comerciales (anti-dumping, restricciones de importación, controles de exportación) con detalle por medida, jurisdicción, base legal, vigencia y fuente oficial.

| Registro de medidas | Detalle de medida |
|---|---|
| ![Tariffs measures registry](assets/screenshots/17-tariffs-measures-registry.png) | ![Tariffs measures detail](assets/screenshots/18-tariffs-measures-detail.png) |

### Inteligencia regulatoria — narrative bundles

Agregación de señales y rumores en narrative bundles con confidence × impact matrix. Cada bundle escala por **maturity timeline** de 6 estados (latent → discussed → proposed → debated → measure announced → measure adopted), con confidence breakdown por fuente, event timeline y narrative coherence score.

| Vista de bundles | Detalle de señal regulatoria |
|---|---|
| ![Regulatory intelligence bundles](assets/screenshots/20-regulatory-intelligence-bundles.png) | ![Regulatory signal detail](assets/screenshots/21-regulatory-signal-detail.png) |

### Funciones de IA — 5 capacidades activas

Vista consolidada de las capacidades de IA del sistema:

- **AI Alert Prioritization** — scoring + ranking de alertas
- **Match Explanations** — explicaciones generadas por IA con contexto regulatorio
- **Predictive Route Risk** — previsión de riesgo geopolítico *(en desarrollo; hoy se declara no disponible)*
- **Compliance Q&A (RAG)** — preguntas sobre regulación con respuestas IA
- **Automated Models monitoring** — modelos monitorizados continuamente con detección de drift

![AI features overview](assets/screenshots/22-ai-features-overview.png)

---

## Stack IA detallado

Toda la inteligencia del sistema es **determinista y trazable**. NO hay LLM como decisor final (decisión consciente: regulator no acepta black-box).

### 1. Motor de matching — ensemble fuzzy

| Componente | Algoritmo | Propósito |
|---|---|---|
| **Fuzzy** | RapidFuzz `token_set_ratio` | Variaciones ortográficas, transposiciones, orden de tokens |
| **Phonetic** | Soundex + Metaphone + Double Metaphone | Nombres no latinos transliterados |
| **Ensemble** | Ponderación multi-algoritmo configurable | Combina los 3 con pesos calibrados (no publicados por prudencia operativa) |
| **Oracle** | Scoring multi-feature | similitud nombre · alias strength · multi-list bonus · program risk · entity type · pattern recognition |

**Reason codes auditables enumerables**. Cada decisión carga su reason code en audit log para reconstrucción regulatoria.

**Normalización**: lowercase + strip whitespace + diacríticos eliminados + transliteración multi-script.

**Deduplicación multi-source**: si entidad aparece en múltiples listas oficiales, bonus de confidence configurable.

### 2. NLP de eventos geopolíticos — keyword-based con detección de negación

Servicio de clasificación de noticias en múltiples categorías de evento:

- **3 tiers de keywords**: CRITICAL · HIGH · MEDIUM.
- **Negation detection**: palabras como `unlikely`, `denied`, `speculation`, `rumor` reducen severidad calculada.
- **Source credibility weighting**: pesos configurables por tipo de fuente (oficial vs. news vs. social).
- **Severity score**: rango normalizado 0.0–1.0 + confidence 0.0–1.0.
- **Sin transformers / BERT / GPT** — keyword + heurística + scoring lógico.

### 3. Impacto geográfico — Haversine + buffer dinámico

- **Haversine distance** entre evento georreferenciado y geometría de la ruta.
- **Buffer dinámico según severidad del evento**.
- **Intersección** con `LineString` GeoJSON almacenada en BD (geometry library estándar).
- **Temporal decay**: eventos antiguos pesan menos exponencialmente.
- **Sin clustering ML** — agregación por zona con servicio dedicado.

### 4. Previsión de series temporales (en desarrollo)

- **Estado**: retirada en noviembre de 2026. El modelo anterior era un relleno que devolvía riesgos aleatorios; ahora la API responde `available: false`.
- **Diseño previsto**: un modelo por corredor con regresores externos e intervalos de incertidumbre, siempre como entrada al agregador de riesgo y nunca como decisor final.
- **Condición para volver**: modelo entrenado, validado fuera de muestra y con la evaluación publicada en el repositorio privado.

### 5. Optimización de rutas — Pareto multi-criteria

- **Algoritmo**: generación de candidatos + scoring multi-factor + Pareto frontier filtering.
- **Múltiples criterios**: cost · time · safety/geopolitical risk · carbon footprint · ESG · balanced.
- **Constraints duros**: sanciones bloquean automáticamente · bloqueos legales por jurisdicción · `max_transit_days` · `max_cost_usd` · `max_risk_score` · `max_carbon_kg` · `avoid_countries` list.
- **Carbon intensity por modo**: sea · rail · air · road (valores públicos estándar kg CO2 / TEU-km).
- **EU ETS carbon pricing** integrado (configurable).
- **Reasoning per route**: cada ruta candidata explica por qué está bloqueada, recomendada o descartada.

### 6. Scoring agregado — explicabilidad del riesgo

Servicio de agregación multi-nivel con weighting configurable por tenant:

- **Desglose de factores** que contribuyeron al score final.
- **Compliance score** consolidado para shipment assessment + trade finance scoring.

---

## Arquitectura técnica

### Capas

```
┌──────────────────────────────────────────────────────────┐
│  Frontend                                                 │
│  Next.js + React + Radix UI + Tailwind + Mapbox          │
│  (dashboard · sanctions module · commodities module ·    │
│   routes interactive map · cases workflow · admin)       │
└──────────────────────────────────────────────────────────┘
                            │
                            │ NextAuth JWT + API key
                            ▼
┌──────────────────────────────────────────────────────────┐
│  API Layer                                                │
│  FastAPI (routers organizados por dominio)               │
│  - check / commodity_check / routes / insurance /         │
│    integrated_check / cases / admin / webhooks            │
└──────────────────────────────────────────────────────────┘
                            │
                            ▼
┌──────────────────────────────────────────────────────────┐
│  Service Layer                                            │
│  Servicios separados por responsabilidad única:           │
│  matching engine · ensemble matcher · fuzzy · phonetic ·  │
│  screening · audit + integrity · auth · jwt · API key     │
│  rotation · 2FA · event classifier · geopolitical OSINT · │
│  route closure prediction · route optimizer · insurance · │
│  premium calculator · PEP screening · policy versioning · │
│  tenant risk weights                                      │
└──────────────────────────────────────────────────────────┘
                            │
                            ▼
┌──────────────────────────────────────────────────────────┐
│  Ingest Layer (cron + Celery + Redis)                    │
│  Connectors por fuente oficial pública (OFAC · UN · EU ·  │
│  UK · BIS · …) con delta-tracking + upsert atómico +      │
│  healthchecks                                             │
└──────────────────────────────────────────────────────────┘
                            │
                            ▼
┌──────────────────────────────────────────────────────────┐
│  Data Layer                                               │
│  PostgreSQL (prod) + SQLite (dev) + Alembic migrations   │
│  Tablas multi-tenant FK · indexes en campos críticos     │
│  Audit log append-only inmutable                          │
└──────────────────────────────────────────────────────────┘
```

### Multi-tenancy estricto

- `tenant_id` FK en **todas** las tablas core.
- API key hash con **argon2** (no SHA-256 plain).
- **API key rotation** dedicada con servicio propio.
- **2FA TOTP** integrado.
- **Invariante**: tenant_id derivado de API key, nunca del body de la request. Testeada en suite dedicada de tenant isolation.

### Audit log append-only

- Modelo de historial de screening en BD.
- Servicio core con `log_screening` inmutable.
- Servicio de integridad que valida NO UPDATE NI DELETE.
- Endpoint dedicado para consulta auditada.

### Invariantes core declaradas

| Garantía |
|---|
| **Matching determinista auditado** (AUTO-CLEAR / REVIEW / FLAG / BLOCK) con tests |
| **Oracle scoring multi-feature** con reason codes |
| **Ingest con delta tracking** + upsert atómico |
| **Audit log append-only** (no UPDATE ni DELETE) |
| **Tenant isolation estricta**: tenant_id derivado de API key |

---

## Stack técnico

| Capa | Tecnología | Rol |
|---|---|---|
| **Backend** | Python + FastAPI + Pydantic 2 | API + validación de inputs/outputs |
| **ORM + migrations** | SQLAlchemy 2 + Alembic | Tablas multi-tenant · migraciones versionadas |
| **Database** | PostgreSQL (prod) + SQLite (dev) | Multi-tenant FK · audit log · GeoJSON |
| **Cache + queue** | Redis + Celery | Daily ingest scheduler · async jobs |
| **Fuzzy matching** | RapidFuzz + unidecode | Ensemble matcher |
| **Phonetic** | Custom Soundex + Metaphone + Double Metaphone | Nombres no latinos |
| **Geospatial** | shapely + GeoJSON | Geometría de rutas · Haversine · buffer expansion |
| **Frontend** | Next.js + React + Radix UI + Tailwind | UI |
| **i18n** | next-intl | Multi-locale (idiomas europeos principales) |
| **Auth** | NextAuth + JWT dual + 2FA TOTP | App + programmatic API |
| **Observability** | OpenTelemetry + Sentry | Traces · errors · custom metrics |
| **Deploy** | Dual cloud (PaaS) + docker-compose dev | Multi-environment · CI/CD |
| **Tests** | pytest + integration + E2E | Suite backend + frontend con cobertura de paths críticos |

---

## Engineering patterns visibles

- **ADRs versionadas** con plantilla fija (contexto · decisión · alternativas · consecuencias · plan rollout · plan rollback). Cubren multi-tenancy · audit log · matching governance · ML governance · route blocking rules · pricing model · tenant onboarding.
- **arc42 completa** con las 12 secciones canónicas (objetivos · restricciones · contexto · estrategia · bloques · runtime · despliegue · cross-cutting · decisiones · calidad · riesgos · glosario).
- **Auditorías internas previas** con doctrina **verify-findings**: ratio de ruido < 15% objetivo, 5 campos por hallazgo (cita · ubicación · severidad · fix · pasada adversarial).
- **CI/CD gates**: ruff (lint+format) · bandit (security) · detect-secrets con baseline · gitleaks · pytest · build.
- **RBAC granular**: Admin · Compliance Officer · Analyst · Viewer · Auditor con matrix de permisos.
- **Integrations via adapter pattern**: webhooks Slack / Teams / JIRA / SAP · APIs externas opcionales · webhook signing.
- **Daily ingest scheduler**: cron + Celery + Redis queue + healthchecks · delta-tracking · upsert atómico.
- **Policy versioning**: multi-versión de rules con rollback.
- **Data quality validators** integrados en ingest.

---

## Compliance posture

Documentación regulatoria publicada en el proyecto privado:

- **DORA inventory** (Digital Operational Resilience Act — aplicable a financial services / RegTech europeo).
- **SOC 2 / ISO 27001 roadmap** con compromisos de controles.
- **Incident Response Plan** formal.
- **Single Source of Truth** canónico (métricas e invariantes consolidadas, validables vía grep).
- **Pentest scope** documentado con metodología OWASP y SLAs.

Regulaciones a las que el sistema responde:

- **OFAC SDN** (US Treasury · Office of Foreign Assets Control).
- **UN Consolidated List** (UN Security Council).
- **EU CFSP** (Common Foreign and Security Policy) + **EU Annex I del Reglamento 2021/821** (dual-use).
- **UK HMT Sanctions** + **OFSI**.
- **BIS** (US Bureau of Industry and Security).
- **TARIC** (EU tariff).
- **MAR EU** (Market Abuse Regulation) — informa la decisión de NO publicar outputs de forecasts ML por corredor concreto.
- **GDPR + LOPDGDD** — informa multi-tenancy estricta y audit log inmutable.

---

## Novedades (octubre-noviembre 2026)

Trabajo de las últimas semanas, con su evidencia en el repositorio privado:

- **Solo lo legal bloquea** (ADR-0077). Una banda de riesgo CRITICAL sin motivo legal da REVIEW, no BLOCK; cada decisión declara sus dos ejes, legal y seguridad.
- **Calibración del screening**: las entidades sancionadas de Corea del Norte, Irán y Siria pasan de escalar el 34,3 % de las veces al 99,9 %, sin falsos positivos nuevos.
- **Una sola regla evento → corredor**: geometría, después zona y después país, con la base declarada. Los eventos enlazados pasan de 59 a 202 sin que cambie ninguno de los 26 scores. El modo de transporte entra en el enlace: un aviso marítimo deja de tocar 230 corredores aéreos, 150 de carretera y 118 de ferrocarril.
- **Política sin mocks**: la previsión de conflictos devolvía riesgos aleatorios desde un modelo de relleno. Se retiró: hoy responde `available: false` hasta que haya un modelo entrenado y validado.
- **Seguridad por clase, no por punto**: los tooltips de los mapas pintaban sin escapar lo que declara cualquier buque por AIS (su alfabeto incluye `<`, `>` y `=`); se cerró por construcción, con un guard sobre todo sumidero de HTML. Las rutas de lectura sin autenticación quedaron cerradas con un invariante medido por efecto, visto fallar antes del arreglo.
- **Contratos de API**: las rutas consumidas sin esquema bajan de 159 a 93, con snapshot de OpenAPI y un trinquete que impide volver atrás.
- **Fuentes honestas**: puerta de licencia antes de cada colector, detector de frescura por lista (deja de dar verde si una lista oficial se para) y token de la lista UE redactado en base de datos, logs y excepciones.
- **Reglas para afirmaciones de inteligencia** (en propuesta, ADR-0078): linaje, autoridad y ámbito de cada cifra antes de publicarla.
- **Ops Grid**: paleta única, mapa base propio sobre Natural Earth y un indicador LIVE que solo se enciende con dato vivo.
- **Verificación**: barrido completo del backend el 09/11 (368 ficheros: 354 en verde, 14 sin tests, 0 fallos) y los tres gates de CI en verde.

---

## Estado y madurez técnica

- **Proyecto técnico avanzado** del autor. **No en producción comercial activa**: la web pública lynxaris.com está en producción desde el 27/08/2026; la aplicación aún no está desplegada.
- **arc42 + ADRs versionadas + auditorías internas** documentadas.
- **Multi-tenant** estricto con tenant isolation testeada.
- **Audit log append-only** inmutable con servicio dedicado de integridad.
- **Invariantes core** declaradas y testeadas vía suite (backend + frontend tests cubriendo paths críticos).
- **Ingest delta-tracking** automatizado contra fuentes oficiales públicas.
- **Compliance posture** documentada (DORA · SOC2 · ISO27001 roadmap · IR plan · pentest scope).
- **CI/CD con security gates** (ruff · bandit · detect-secrets · gitleaks).
- **Internacionalización** multi-locale.

---

## Donde se aplica este patrón

El patrón "**plataforma multi-tenant de compliance con motor de matching ensemble + scoring agregado multi-dominio + audit log append-only + risk aggregator con explicabilidad + integraciones outbound vía adapter pattern**" es **horizontal a cualquier dominio RegTech** donde decisiones automatizadas requieren trazabilidad regulatoria:

- **KYC/AML** (Know Your Customer / Anti-Money Laundering).
- **Sanctions screening** corporativo (cross-border transactions, vendor onboarding).
- **Export controls** (dual-use, defense, technology transfer).
- **Trade-based money laundering detection**.
- **Geopolitical risk monitoring** para fondos, aseguradoras, supply chain.
- **DORA-compliant ICT third-party risk management**.
- **Fraud detection** con explicabilidad regulatoria.
- **PEP / UBO monitoring continuo**.
- **Healthcare compliance** con multi-tenant y audit trail (HIPAA · facturación regulada).
- **Insurance underwriting** con scoring multi-factor explicable.

Los patterns técnicos resueltos (ensemble fuzzy matching · delta-tracking ingest · multi-tenancy estricta con tenant derivado de API key · audit log append-only validado · NLP keyword-based con negation y source credibility · Pareto multi-criteria con constraints duros · NO LLM como decisor · invariantes validables · doctrina verify-findings) son **horizontales a cualquier sistema regulado donde un error puede disparar consecuencias administrativas o legales directas**.

---

## Sistema operativo de ingeniería del autor

Este proyecto se desarrolló bajo el sistema operativo de ingeniería propio del autor, replicado cross-proyecto en múltiples proyectos del ecosistema:

- **Automation Engineering Protocol** — stage-gate horizontal de cambio: change-spec → guard layer → release train → rollback playbook.
- **Prompt Engineering Protocol** — diseño modular con catálogo cerrado de patrones (aplicable a OSINT enrichment con LLM cuando se usa — nunca como decisor de compliance).
- **Post-Development Verification Protocol** — 4 niveles (estática · integración · canarios E2E con datos sintéticos · observabilidad).
- **Post-Development Gates** — gates pre-merge / pre-deploy / post-deploy con checklist bloqueante.
- **Frozen Zones & Regression Prevention** — CONFIG vs HEALTH, auditoría holística periódica.

Cada decisión estructural se documenta como ADR versionada. Cada cambio significativo pasa por `verify-findings` adversarial. Engineering-playbook propio con disciplina doctrinal cross-proyecto. La documentación es activo de primera clase.

Protocolo de documentación detallado (arc42 + C4 + ADR + runbooks + postmortems) en [`docs/documentation-protocol.md`](docs/documentation-protocol.md).

*Detalles operativos del proyecto privado (código fuente · endpoints exactos · samples de datos · secretos de integración · identificadores de corredores ML · dashboards en vivo · configuración de infraestructura) NO se publican por consideraciones regulatorias y de prudencia operativa.*

---

## Contacto

**Kamil Slodki** — Valencia, España

- Email: `solutions.satdata@gmail.com`
- LinkedIn: [Kamil Slodki](https://www.linkedin.com/in/kamilslodki/)
- Portfolio: [satdata-portfolio](https://github.com/KamilSlodki/satdata-portfolio)

Disponible para **founding / staff AI roles** (remote · full-time + equity) y **B2B consulting / fractional CTO engagements** (retainer · day-rate · proyectos cerrados). Para consultas técnicas concretas, briefings de proyecto o detalles de compensación, escribir directamente al email comercial.
