# Rodrigo André Torres Pastor

Consultor en IA aplicada y desarrollador fullstack. Fundador de Árkos, software
a medida para PYMEs en Perú y clientes en Latinoamérica, EE. UU. y Europa.

Integro modelos de lenguaje, agentes y automatización dentro de sistemas de
negocio que ya están en producción. Mi diferencial es una combinación poco
común: IA aplicada más integración fiscal peruana de punta a punta (SUNAT,
SIRE, PLE, libros contables electrónicos, Culqi, Izipay, Yape, Plin).

Lima, Perú · Remoto a tiempo completo · rodrigoan.torresp@gmail.com ·
linkedin.com/in/rodrigo-torres-arkos

---

## Trabajo público

Estos dos se pueden abrir, correr y verificar.

**[Precio Vivo](https://github.com/RodrigoFK06/PrecioVivo)** — Inteligencia de
precios mayoristas del Gran Mercado Mayorista de Lima. Ingesta diaria
desatendida en AWS con Step Functions y 6 Lambdas, desplegada como
infraestructura como código con CDK e IAM de permisos mínimos, sin un solo
recurso creado desde la consola. Encima corre un RAG híbrido de 9.281 chunks
que fusiona BM25 y búsqueda vectorial con RRF, un agente LangGraph con
StateGraph explícito y presupuesto de pasos, y un servidor MCP propio escrito
desde cero. 435 pruebas.

Cada decisión de arquitectura tiene una medición detrás: cargar el snapshot
fuera del handler porque el init son 707 ms contra 1,78 ms de p50; repartir el
forecast en un Map porque en serie tarda 52 minutos contra un tope de 15;
concurrencia 8 porque la cuota de la cuenta es 10 y no es ajustable. Y el
kill-gate reporta que mi propio modelo GBM pierde contra AR(1) en ambos
horizontes. Un sistema que publica que su modelo no es el mejor es lo que hace
creíble el resto de sus números.

**[FacturArkos](https://github.com/RodrigoFK06/FacturArkos)** — Extracción y
clasificación de comprobantes con LLM para emisión ante SUNAT. La salida se
valida contra esquema antes de enviar y lo de baja confianza pasa a una cola de
revisión humana en vez de emitirse. El tiempo de emisión bajó 60 %.

---

## Trabajo de cliente

Bajo acuerdo de confidencialidad, por eso no está en repos públicos.

**RestHUB** (cofundador) — ERP y POS para restaurantes: sala, cocina, caja y
administración. 49 módulos de backend, 130 pantallas, 2.371 tests automatizados.
Arquitectura offline-first con cola de eventos ordenada e IDs idempotentes,
porque la caja tiene que seguir cobrando cuando se cae internet. Facturación
SUNAT más Culqi, Izipay, Yape y Plin. Superó el primer filtro de COFIDE
Launchpad 2026. TypeScript, NestJS, Next.js, PostgreSQL.

**Solutec** — ERP de gestión de servicios técnicos, en producción hace más de
dos años: órdenes de servicio, técnicos, inventario, cuentas, pagos y módulo
SUNAT. Procesa unas 650 órdenes al mes y redujo el tiempo de cierre 45 %.
TypeORM, PostgreSQL, SQL Server.

**OrquestadorADM** — Revenue management y facturación electrónica para
hotelería. Ocupación, ADR y RevPAR desde una fuente única de cálculo, forecast
de demanda con contraste de predicciones contra lo ocurrido, y emisión SUNAT
con correlativos atómicos verificados bajo 20 emisiones simultáneas. La
aritmética fiscal se deriva hacia atrás desde el total cobrado para que base
más IGV sea exactamente lo que entró a caja. 543 tests más 53 E2E. Next.js,
Prisma, PostgreSQL.

**All White Vacations** — Gestión de overbooking y revenue para operación
turística internacional. Next.js, Supabase.

**LearnLux** (cofundador) — SaaS EdTech de lectura rápida por RSVP, con ingesta
de PDF y suscripciones internacionales vía Paddle. Next.js, Firebase, MongoDB.

Clientes adicionales bajo NDA en logística y transporte, consultoría, comercio
y sector naval.

¿Necesitas ver código de cliente? Escríbeme y coordinamos un walkthrough en vivo
de la arquitectura, o te comparto un extracto sanitizado.

---

## Stack

**IA y automatización** — Orquestación de agentes · LLM en producción (OpenAI,
Anthropic Claude, Google Gemini) · RAG híbrido y búsqueda vectorial · Servidores
MCP · Evaluación de LLM en CI · Desarrollo asistido por agentes (Claude Code,
Codex) · Forecasting con scikit-learn y statsmodels · Extracción de datos no
estructurados

**Desarrollo** — TypeScript · React · Next.js · NestJS · Node.js · Python ·
FastAPI · PostgreSQL con pgvector · SQL Server · MongoDB · Prisma · TypeORM ·
Supabase · Firebase · AWS (Lambda, S3, DynamoDB, Step Functions, CDK) · Docker ·
Vercel · pytest, Jest, Vitest, Playwright

**Fiscal y pagos (Perú)** — SUNAT · SIRE · PLE · Libros contables electrónicos ·
Facturación electrónica · Culqi · Izipay · Yape · Plin

---

## Formación

Ingeniería de Sistemas Computacionales, Universidad Privada del Norte
(2021-2026). Último ciclo, 195 de 200 créditos. Bachiller 2026, título previsto
2027.

Certificaciones — Scrum Master · EF SET (inglés) · AI Capabilities and
Limitations y AI Fluency for Small Businesses (Anthropic, 2026).

Idiomas — Español nativo · Inglés: lectura y comprensión avanzadas, conversación
intermedia.
