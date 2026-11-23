# Skills de FRS Solutions SpA

Seis skills propias para Claude Code, adaptadas a la empresa a partir de una revisión de las fuentes indicadas por Vicente Fredes. Versión inicial: 1.0.0, 23 de noviembre de 2026.

| Comando en Claude Code | Uso |
| --- | --- |
| /frs-prospeccion | Investigar y priorizar potenciales clientes con evidencia pública. |
| /frs-ofertas | Diseñar entregables, alcance y condiciones comercialmente viables. |
| /frs-correos-comerciales | Preparar primeros contactos, respuestas y seguimientos. |
| /frs-propuestas | Elaborar propuestas y fichas para oportunidades concretas. |
| /frs-conversion-web | Diagnosticar fricción y proponer o implementar mejoras de conversión. |
| /frs-interfaces | Construir interfaces coherentes con marca, privacidad y código existente. |

## Uso en Claude Code

El paquete usa carpetas con SKILL.md dentro de .claude/skills/, de acuerdo con la [documentación oficial de Claude Code](https://code.claude.com/docs/en/skills). No requiere npx, dependencias, hooks, comandos al cargar ni servidores MCP adicionales.

Para trabajar en el proyecto Empresa, copia las seis carpetas de este paquete desde .claude/skills/ a la carpeta .claude/skills/ de ese proyecto. Si ya hay una carpeta con el mismo nombre, compara antes de reemplazarla. Para disponibilidad personal en varios proyectos, la ubicación es ~/.claude/skills/. Conserva cada subcarpeta references/ junto a su SKILL.md.

Este paquete está guardado en la subcarpeta frs-skills de un repositorio: clonar el repositorio completo no instala por sí solo sus skills en todos tus proyectos. Abre frs-skills como proyecto o copia sus carpetas al proyecto donde trabajarás.

Ejemplos:
- “/frs-prospeccion Encuentra diez empresas de Santiago con una señal pública de necesidad de automatización. Entrega fuentes y no envíes mensajes.”
- “/frs-ofertas Diseña un piloto con estos costes y requisitos; deja precio e impuestos pendientes donde falten datos.”
- “/frs-correos-comerciales Redacta un correo a esta empresa usando únicamente los hechos de estas fuentes.”
- “/frs-propuestas Prepara una propuesta con este alcance confirmado, plazo y precio.”
- “/frs-conversion-web Audita el formulario de contacto y distingue hallazgos de hipótesis.”
- “/frs-interfaces Implementa esta mejora en la vista previa del sitio y verifica móvil y teclado.”

## Contexto y mantenimiento

Cada skill incluye una copia del contexto mínimo de FRS para funcionar de forma independiente. Está basado en CLAUDE.md y README.md del proyecto Empresa consultados el 23-11-2026. No incluye credenciales, datos de clientes ni información privada de prospectos. La copia no reemplaza las instrucciones y fuentes actuales del proyecto. Si cambia un dato transversal, actualiza las seis copias de references/frs-contexto.md.

Las skills pueden seleccionarse automáticamente por su descripción. Solo contienen instrucciones: no conceden permisos de envío, publicación, compra o cambios de infraestructura. Las acciones externas se rigen por el encargo y permisos reales de cada sesión.

## Revisión y atribuciones

- [Informe de seguridad](auditoria/INFORME.md): alcance, hallazgos y límites.
- [Inventario de fuentes](auditoria/fuentes.json): commits, rutas, hashes de Git y SHA-256 de los 49 archivos examinados.
- [Validación del paquete](auditoria/VALIDACION.md): comprobaciones estructurales y casos de revisión.
- [Atribuciones](THIRD_PARTY_NOTICES.md) y textos de licencia en licenses/.

Los originales se conservaron fuera del paquete activo para su revisión y no se instalaron. No se revisó ni ejecutó el instalador npm skills. Ninguna conclusión cubre futuras versiones o servicios externos enlazados.
