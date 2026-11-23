# Decisiones SEO para el sitio de FRS

Contexto técnico local consultado el 23-11-2026. Comprueba los archivos y respuestas actuales antes de diagnosticar; esta referencia no es prueba del estado publicado ni de indexación.

## Dominios, rutas e indexación
www.frssolutions.cl usa páginas en dist/; programas.frssolutions.cl usa programas/ y tiene su propio robots.txt y sitemap. Comprueba cada host por separado. En la copia revisada, dist/_headers aplica X-Robots-Tag: noindex, nofollow únicamente a /admin/*; dist/robots.txt excluye /admin/ y /api/. No generalices esa regla a todo www ni retires las exclusiones administrativas. Noindex y robots.txt no reemplazan autenticación.

Las páginas tienen canonical en HTML; plantillas/ contiene head, cabecera y pie compartidos. Evita propagar accidentalmente el canonical de la portada a otras páginas. Consulta README.md y CLAUDE.md actuales antes de modificar plantillas; sincroniza con scripts/sincronizar-paginas.py cuando corresponda. Revisa dist/sitemap.xml y programas/sitemap.xml sin asumir que su existencia demuestra indexación. No actualices lastmod como si el contenido hubiera cambiado cuando no cambió.

Para excluir una URL con noindex, Google necesita acceder a su respuesta y leer la regla; un Disallow puede impedirlo. Si el objetivo es privacidad, conserva el control de acceso y explica la limitación de indexación. [Documentación de noindex](https://developers.google.com/search/docs/crawling-indexing/block-indexing).

## Idiomas de FRS
En la copia revisada, el HTML parte en español y idiomas.js sustituye texto y metadatos con frases.js; programas añade frases-programas.js. El selector usa localStorage y ?lang=. Esto permite elegir idioma al visitante, pero no demuestra que Google encuentre, renderice e indexe cuatro versiones distintas.

Inspecciona respuesta original y renderizado de cada URL antes de recomendar hreflang. Si se pide posicionamiento multilingüe, plantea URLs estables con contenido completo por idioma, enlaces accesibles y metadatos coherentes. La migración requiere alcance, mapeo de URLs y evaluación de mantenimiento: no la ejecutes solo por una auditoría.

Cuando existan variantes reales, hreflang debe apuntar a ellas con códigos válidos y relaciones recíprocas, incluida la propia página. x-default es opcional. No apuntes cuatro idiomas a una sola URL cuyo texto depende únicamente de una preferencia local. Para traducciones distintas evita consolidar todo al español; para duplicados regionales del mismo idioma evalúa un canonical preferido. No garantices que cada variante se indexará. Fuentes: [sitios multilingües](https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites), [versiones localizadas](https://developers.google.com/search/docs/specialty/international/localized-versions).

## Datos estructurados
Comprueba JSON-LD en HTML original y DOM cuando sea necesario. Una extracción de texto que elimina scripts no demuestra ausencia de schema; un HTML original sí puede mostrar JSON-LD estático. No confundas esos métodos.

Escoge el tipo adecuado según la página y hechos visibles: organización, servicio, producto o software cuando corresponda. No añadas precios, disponibilidad, ofertas, puntuaciones o capacidades clínicas no comprobadas. Un @context de schema.org en JSON-LD no exige descargar recursos ni autoriza añadir scripts externos; no añadas resoluciones remotas innecesarias. Conserva CSP.

La validez del marcado no garantiza que Google muestre un resultado enriquecido. Verifica los requisitos vigentes del tipo antes de prometer elegibilidad; una FAQ o un testimonio no produce estrellas o FAQ enriquecidas por defecto. Usa validadores públicos solo con URLs o contenido públicos autorizados. [Datos estructurados de Google](https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data).

## Presencia local y contenido
La dirección comercial de FRS no prueba una oficina que reciba público. Verifica la operación real y elegibilidad antes de recomendar Google Business Profile; una oficina virtual usada solo como dirección postal no la establece. Si la actividad elegible visita clientes, comprueba la base y área atendida reales, preservando direcciones privadas. No fabriques sucursales por comuna ni cobertura nacional. [Reglas de representación empresarial](https://support.google.com/business/answer/3038177).

Prioriza páginas útiles de las áreas que FRS realmente ofrece. No conviertas HistoPanorama en un servicio diagnóstico ni uses la formación del fundador para inventar acreditaciones de la empresa. Rechaza páginas puerta, contenido masivo sin utilidad, reseñas y enlaces comprados. [Políticas de spam](https://developers.google.com/search/docs/essentials/spam-policies).

Para títulos y descripciones usa claridad y fidelidad al contenido; los rangos de caracteres son orientativos. Google puede generarlos desde otras señales. Fuentes: [títulos](https://developers.google.com/search/docs/appearance/title-link), [descripciones y snippets](https://developers.google.com/search/docs/appearance/snippet).

## Herramientas y resultados
No hay proveedor obligatorio. Empieza con fuentes y herramientas disponibles y datos autorizados de Search Console si existen. Sin acceso declara límites en lugar de fingir métricas. Comprueba documentación oficial actual para requisitos cambiantes. No incrustes analítica, grabaciones ni recursos de terceros en www para medir SEO.

No confundas clic orgánico, consulta comercial y venta. Comunica incertidumbre y mide cambios en periodos comparables; preserva datos personales y excluye exportaciones privadas de GitHub público.
