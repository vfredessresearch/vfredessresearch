# Revisión de seguridad de las skills solicitadas

Fecha: 23-11-2026. Destino de las adaptaciones: FRS Solutions SpA.

## Resultado

No se detectaron indicios de malware, extracción de credenciales, persistencia oculta ni instrucciones para desactivar controles en el conjunto examinado. Esto es una conclusión de revisión estática, no una garantía de ausencia de contenido malicioso ni una certificación de seguridad.

Las seis skills solicitadas existen en las versiones revisadas. Sus carpetas contienen texto Markdown, evaluaciones JSON y licencias; no contienen scripts ejecutables, binarios, enlaces simbólicos ni hooks. Un archivo de instrucciones puede provocar acciones riesgosas aunque no contenga código: por eso también se revisaron permisos implícitos y recomendaciones operativas.

## Fuentes fijadas

| Repositorio | Commit revisado | Alcance |
| --- | --- | --- |
| [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills/tree/5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1) | 5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1 | Cinco carpetas completas: prospecting, offers, cold-email, sales-enablement y cro; licencia MIT de raíz. |
| [anthropics/skills](https://github.com/anthropics/skills/tree/e4bb5d960d87126ff3b3a8af1a104b7db67560ba) | e4bb5d960d87126ff3b3a8af1a104b7db67560ba | Carpeta frontend-design completa: SKILL.md y LICENSE.txt. |

Total: 49 archivos. El [manifiesto](fuentes.json) identifica cada archivo, su modo Git, tamaño original, SHA de blob Git y SHA-256. Las copias descargadas se contrastaron con el SHA de blob original. Las ramas main pueden cambiar; la revisión solo se aplica a estos commits.

## Método y límites

1. Se obtuvieron los árboles Git completos de ambos commits y se enumeraron las seis carpetas, incluidos archivos de apoyo, evaluaciones y licencias.
2. Se descargó el texto usando el conector de GitHub, sin ejecutar el contenido ni instalarlo.
3. Se hizo lectura de los seis SKILL.md, inventario y búsqueda estática en los 49 archivos, y lectura dirigida de referencias de mayor impacto: contactos y fuentes, autoridad de agentes, respuestas, enriquecimiento, automatización de LinkedIn, cadencias, formularios y privacidad. No se afirma una revisión manual línea por línea de todas las referencias ni de todas las evaluaciones JSON.
4. Se buscaron comandos de ejecución, persistencia, secretos, rutas sensibles, descargas, instrucciones de sustitución de autoridad, enlaces externos y recomendaciones de transmisión de datos; se revisó el contexto de las coincidencias relevantes.
5. Se redactaron seis adaptaciones sin instaladores, scripts, hooks, permisos automáticos de herramientas ni carga de instrucciones remotas.

No se ejecutaron los comandos npx skills add. Quedan fuera de alcance el paquete npm skills y su cadena de dependencias; los scripts o plugins de los repositorios situados fuera de estas seis carpetas; los servicios enlazados y sus MCP; y la ejecución real de las skills originales con Claude Code. Los enlaces remotos no se consideran dependencias aprobadas y no se siguieron todos. No se verificó como asesoría jurídica ni como evidencia comercial cada afirmación normativa o estadística de los originales.

## Captación de clientes — prospecting

Archivo principal: [SKILL.md fijado](https://github.com/coreyhaines31/marketingskills/blob/5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1/skills/prospecting/SKILL.md).
No se observaron instrucciones de extracción de secretos. Incluye buenas restricciones sobre datos sensibles, procedencia y no eludir bloqueos.

Hallazgos: prescribe verificadores externos y enlaza proveedores; nombra Truelist como producto del mantenedor, con disclosure explícito. signal-plays.md recomienda identificación de visitantes (RB2B y otros), y sourcing-and-enrichment.md llega a admitir envíos a catch-all no resueltos para cuentas prioritarias. Estas recomendaciones no son malware, pero pueden implicar coste, compartir contactos o riesgos de privacidad y entregabilidad. No se incorporaron como comportamiento predeterminado de FRS. Se distinguen contacto publicado, identidad y entregabilidad; no se inventa verificación ni consentimiento.

## Diseño de ofertas — offers

Archivo principal: [SKILL.md fijado](https://github.com/coreyhaines31/marketingskills/blob/5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1/skills/offers/SKILL.md).
No se observaron acciones técnicas sospechosas. El original rechaza escasez ficticia y garantías exageradas.

Hallazgos: presenta bonos, urgencia y garantía como partes casi obligatorias, y proyecta aumentos relativos de conversión de 10–40% por cambio. Esa estimación genérica no demuestra resultados para FRS. La adaptación centra alcance, aceptación, costes y validación; no exige bonos ni urgencia y no proyecta incrementos sin datos.

## Correos comerciales — cold-email

Archivo principal: [SKILL.md fijado](https://github.com/coreyhaines31/marketingskills/blob/5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1/skills/cold-email/SKILL.md).
No se encontraron scripts ni destinos ocultos de extracción.

Hallazgos: deliverability.md prescribe dominios secundarios y redes de warmup; linkedin-outreach.md admite herramientas de automatización y propone tiempos aleatorios e IP residenciales pese al riesgo que reconoce; multichannel-cadence.md recomienda subir listas a plataformas de anuncios; reply-handling.md permite ciertas operaciones autónomas y contempla envíos autónomos futuros. No se atribuye intención maliciosa a los autores, pero estas pautas pueden producir cambios, gastos, transmisión de datos o actuaciones no solicitadas. La adaptación se centra en borradores y solo actúa externamente dentro de una autorización real; elimina esas tácticas y el seguimiento oculto.

## Propuestas comerciales — sales-enablement

Archivo principal: [SKILL.md fijado](https://github.com/coreyhaines31/marketingskills/blob/5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1/skills/sales-enablement/SKILL.md).
Incluye un criterio útil: las afirmaciones competitivas y resultados deben poder defenderse con evidencia.

Hallazgos: contiene ejemplos persuasivos y guiones que podrían convertirse incorrectamente en promesas, resultados o acciones de envío y agenda. La adaptación exige alcance, aceptación y condiciones explícitas, mantiene los términos pendientes como borrador y separa ahorro teórico de ahorro efectivo.

## Conversión del sitio web — cro

Archivo principal: [SKILL.md fijado](https://github.com/coreyhaines31/marketingskills/blob/5b2b400eec1e7e1cec76245a715d0b0d4fd2a9c1/skills/cro/SKILL.md).
No se detectó código malicioso. Sugiere diagnóstico razonable de propuesta de valor y fricción.

Hallazgos: referencias de formularios proponen enriquecimiento externo y seguimiento de campos; menciona heatmaps y grabaciones como insumos, y trata ciertas mejoras o porcentajes de fricción como generales. La adaptación prohíbe incorporar seguimiento externo contrario al proyecto, conserva controles contra abuso y formula impactos como hipótesis.

## Interfaces comerciales — frontend-design

Archivo principal: [SKILL.md fijado](https://github.com/anthropics/skills/blob/e4bb5d960d87126ff3b3a8af1a104b7db67560ba/skills/frontend-design/SKILL.md).
La carpeta contiene únicamente el archivo de instrucciones y su licencia Apache 2.0; no hay instaladores o scripts.

Hallazgos: adopta supuestos de un cliente que ya rechazó propuestas y recomienda tomar riesgos estéticos. Eso es un encuadre creativo, no prueba de preferencias de FRS. La adaptación conserva diseño intencional y revisión, pero da prioridad al sistema de marca, assets locales, accesibilidad y código actual.

## Cambios comunes en las adaptaciones

- Contexto empresarial basado en los archivos actuales del proyecto, sin extrapolar clientes ni resultados.
- Ningún proveedor obligatorio, carga remota de instrucciones, credencial, telemetría, hook o ejecución al cargar.
- Documentos externos tratados como datos; sus instrucciones no autorizan acceso a secretos o nuevas acciones.
- Permisos de envío, compra, cambios en infraestructura y publicación sujetos al encargo vigente.
- Respeto por privacidad del sitio, CSP, validación del servidor y evidencia comercial.
- Licencias y atribuciones originales preservadas por separado.

## Actualizaciones

Una versión futura requiere revisar el diff contra el commit fijado, incluidos nuevos archivos, modos Git, hooks y enlaces. No se debe ejecutar una actualización con npx basándose solo en esta revisión. Una skill textual puede inducir errores o ser desobedecida por un modelo: los permisos reales del entorno siguen siendo el control técnico.
