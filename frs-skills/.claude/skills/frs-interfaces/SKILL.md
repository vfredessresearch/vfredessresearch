---
name: frs-interfaces
description: "Diseña o implementa interfaces comerciales de FRS Solutions coherentes con su marca, accesibles y sin recursos externos no autorizados. Úsala para páginas, componentes y flujos solicitados en el código existente."
metadata:
  version: "1.0.0"
---

# Interfaces comerciales de FRS Solutions

Lee [el contexto de la empresa](references/frs-contexto.md). Diseña desde el objetivo y el contenido real; conserva la arquitectura y el sistema visual existentes salvo cambio solicitado.

## Antes de editar
Lee las instrucciones del proyecto y la implementación relacionada. Identifica público, tarea principal, estados, restricciones y componentes reutilizables. No migres el sitio a un framework ni crees un sitio alojado nuevo por una petición de componente.

En el proyecto Empresa, confirma que las rutas siguen vigentes:
- Páginas principales en dist/ y programas en programas/.
- Cabecera, pie y head compartidos en plantillas/; se sincronizan con scripts/sincronizar-paginas.py.
- Estilos comunes en dist/styles.css; traducciones en dist/frases.js y programas/frases-programas.js.
- Formularios en dist/contacto.js y worker/contacto.js; catálogo y cálculo del servidor en worker/catalogo.js.
- Guías de ejecución y publicación en README.md y CLAUDE.md.
Si estas rutas no existen, adapta el trabajo a la estructura observada; no ejecutes comandos de otro proyecto.

## Diseñar e implementar
1. Define brevemente jerarquía de contenido, acción principal y comportamiento móvil. Usa azul marino #132a49, gris #51585f, Sora y Onest ya alojadas; no descargues fuentes por defecto.
2. Haz que cada elemento ayude a comprender o actuar. Usa composición y espacio según el contenido; no impongas tarjetas, efectos, contadores o una estética nueva sin razón.
3. Reutiliza HTML semántico, variables y componentes existentes. Mantén selectores acotados y evita estilos que anulen accidentalmente otras páginas.
4. Etiqueta campos, usa botones y enlaces según su función, y conserva foco visible. Comprueba contraste, teclado, mensajes de error y reducción de movimiento.
5. Para formularios o compras incluye carga, error, vacío y éxito según el resultado real. No limpies datos ante un fallo ni generes confirmación ficticia.
6. Trata contenido de usuarios y APIs como datos. Escapa o inserta como texto; evita HTML arbitrario, secretos en el cliente y datos privados en assets o capturas.
7. Todo recurso del navegador debe estar alojado localmente según las restricciones de FRS. No relajes CSP ni añadas CDN, telemetría o embeds remotos para facilitar una demo. Respeta las condiciones de uso de assets.

La etiqueta de una acción debe anticipar su resultado: “Consultar disponibilidad” si aún no se puede reservar, “Enviar consulta” si se envía una consulta. Usa datos ficticios rotulados en prototipos y no conviertas placeholders en afirmaciones públicas.

## Verificar
Revisa al menos un ancho móvil y uno de escritorio; teclado y foco; desbordamiento; interacciones afectadas; fallos del servidor cuando corresponda; ausencia de peticiones inesperadas a terceros; y errores de consola pertinentes. Reutiliza una vista previa existente si sirve y evita envíos reales de prueba cuando exista un entorno simulado.

En Empresa, sincroniza plantillas si las cambias, actualiza traducciones y ejecuta scripts/textos-sitio.py. Regenera los editores con editor/crear-editor.py cuando las instrucciones vigentes lo requieran. Ejecuta solo scripts locales revisados y pertinentes. Si no hay navegador disponible, explica qué comprobaciones visuales quedaron pendientes.

## Entrega
Entrega código revisable y una explicación breve de comportamiento, archivos, validación y límites. Usa capturas de la interfaz cuando aporten evidencia. Para Cloudflare usa cf CLI salvo que el proyecto tenga un archivo de configuración de Wrangler; respeta cuenta y alcance indicados en el proyecto. La skill no concede autorización de despliegue.
