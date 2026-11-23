---
name: frs-conversion-web
description: "Audita y mejora la conversión de páginas, formularios y flujos comerciales de FRS Solutions con evidencia y respeto a su privacidad. Úsala para diagnosticar fricción y priorizar cambios; para diseño de interfaces usa frs-interfaces."
metadata:
  version: "1.0.0"
---

# Conversión web de FRS Solutions

Lee [el contexto de la empresa](references/frs-contexto.md). Optimiza que una persona adecuada entienda la oferta y complete la acción correcta.

## Establecer la base
Identifica página y versión, público, origen del tráfico si se conoce y acción principal: consultar, solicitar presupuesto, reservar o usar un programa. Lee el flujo completo y el código pertinente si están disponibles. Si solo hay una captura o HTML parcial, limita el diagnóstico a lo observado.

Registra problemas observados separados de hipótesis. Sin datos no afirmes que una página “pierde el 30%” ni estimes aumentos de conversión como hechos.

## Auditar
1. Claridad de la oferta: qué hace FRS, para quién, alcance y siguiente paso.
2. Coherencia entre promesa, CTA y resultado del flujo. Una reserva pendiente de pago no se debe mostrar como pagada; un formulario fallido no se debe confirmar como enviado.
3. Jerarquía, legibilidad, navegación y uso móvil. En el inicio con varias áreas, facilitar elegir la adecuada puede ser la acción principal.
4. Confianza: identidad y contacto reales, proceso claro, condiciones y evidencia disponible. No inventes reseñas, logotipos ni sellos.
5. Fricción del formulario: propósito de cada campo, etiquetas visibles, datos mínimos necesarios, errores específicos, preservación de datos al fallar y estados de carga.
6. Accesibilidad: teclado, foco, contraste, nombres accesibles y movimiento reducido.
7. Requisitos de privacidad, validación y protección contra abuso. No elimines controles del servidor, límites, campos trampa o comprobaciones de origen para reducir fricción.

## Proponer o implementar
Si se solicita auditoría, entrega recomendaciones; si se solicita implementación, modifica el alcance autorizado y verifica las interacciones afectadas. Coordina cambios de campo entre navegador y servidor. Conserva la fuente de precios y los cálculos del servidor; nunca confíes en el total del navegador.

No agregues píxeles, identificación de visitantes, grabaciones de sesión, fuentes externas, chat o calendarios incrustados que contacten a terceros en www. No subas consultas del formulario a un enriquecedor ni las descartes por una calificación comercial inferida.

Para medir, define numerador, denominador, periodo y exclusiones, usando datos existentes legítimamente disponibles. Una respuesta HTTP exitosa no demuestra recepción del correo ni una venta. Propón métricas mínimas propias solo si hacen falta y están autorizadas; no registres texto libre o datos personales en eventos. Con poco tráfico, prioriza pruebas de comprensión y tareas de uso; no prometas significación estadística con muestras insuficientes.

## Entrega
Presenta hallazgo, evidencia/ruta o captura, efecto probable como hipótesis, cambio, prioridad, esfuerzo y comprobación. Incluye alternativas de texto solo para elementos relevantes.

Para un experimento, define hipótesis, variante, métrica principal, resguardos, criterio de decisión y condiciones mínimas para interpretar el resultado. No confundas comparación antes/después con causalidad demostrada.

Si editas, comunica archivos cambiados y pruebas realizadas. Mantén borrador o vista previa antes de la publicación cuando así lo exijan las instrucciones vigentes del proyecto.
