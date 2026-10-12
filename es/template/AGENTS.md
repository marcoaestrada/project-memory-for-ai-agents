# AGENTS.md — {{NOMBRE_DEL_PROYECTO}}

Instrucciones permanentes para cualquier agente (y cualquier persona) que trabaje en esta carpeta. Es breve a propósito: lo que no está aquí se encuentra en los documentos enlazados, y solo hay que leer los que tocan a la tarea. Una orden directa de {{RESPONSABLE}} en la conversación manda sobre este archivo; si cambia una regla, se anota en `docs/DECISIONES.md`.

## 1. Qué es este espacio

{{UN_PÁRRAFO: qué es el proyecto, a quién sirve y qué queda fuera}}

Estado en una línea: {{LÍNEA_DE_ESTADO}}. El estado vivo está en `docs/ESTADO_ACTUAL.md`.

## 2. Qué leer y cuándo

Al empezar, siempre: este archivo y `docs/ESTADO_ACTUAL.md`. Después, solo lo que corresponda:

| Si la tarea es… | Lee |
|---|---|
| {{TIPO_DE_TAREA_1}} | {{ARCHIVOS_1}} |
| {{TIPO_DE_TAREA_2}} | {{ARCHIVOS_2}} |
| Por qué algo es como es | `docs/DECISIONES.md` |
| Qué sigue abierto | `docs/TAREAS_ABIERTAS.md` |
| Nombres y términos | `docs/GLOSARIO.md` |
| De dónde sale un dato | `docs/FUENTES.md` |

## 3. Quién decide

{{RESPONSABLE}} decide sobre {{ÁREAS_DE_DECISIÓN}}. Los agentes investigan, organizan, redactan, construyen y verifican; separan **hechos** de **propuestas** y dicen dónde no están seguros.

## 4. Reglas permanentes

Cada regla viene de una corrección real. Pon entre paréntesis la fecha en que se dio. Borra los ejemplos que no necesites.

1. **Discrepar con claridad.** Si una idea no es viable o descansa en algo sin comprobar, dilo *antes* de construirla: la objeción, la razón y la alternativa, en pocas líneas. Si es buena idea, dilo también.
2. **Un entregable, parar.** Completa el entregable pedido hasta dejarlo utilizable, enséñalo y espera el OK antes de empezar el siguiente. Los pasos mecánicos dentro de una tarea acordada no piden parada.
3. **No se toca lo terminado.** Carpetas congeladas: {{CARPETAS_CONGELADAS}}. El trabajo nuevo va a carpetas nuevas. Antes de sobrescribir un archivo de trabajo propio, guarda la versión anterior en `versiones_anteriores/`.
4. **Idioma de la persona.** Todo lo que lee la persona va en {{IDIOMA}}. Si debe pulsar algo en una interfaz en otro idioma, da el nombre exacto del botón entre comillas y qué significa, un paso por acción.
5. **Los nombres se escriben de una sola forma.** {{REGLA_DE_NOMBRES}}
6. **{{AÑADE_LAS_TUYAS}}**

## 5. Qué se puede hacer solo y qué pide permiso

| Categoría | Acciones |
|---|---|
| **Libre** | Leer, investigar, analizar, redactar borradores, editar archivos de trabajo locales, hacer comprobaciones de solo lectura |
| **OK expreso de {{RESPONSABLE}}, cada vez** | Enviar correos o mensajes · publicar o subir algo · comprar o pagar · registrar cuentas o servicios · cambiar configuración en producción · borrar o mover en masa · compartir información con terceros · hacer algo irreversible |
| **Nunca** | Guardar contraseñas, claves de API, tokens o datos bancarios en archivos, ni pedir que se peguen en el chat. Los secretos los pega la persona en su propia terminal o gestor |

Estas reglas fijan roles y límites, pero **no amplían los permisos técnicos** del entorno: si una herramienta bloquea algo, este archivo no lo desbloquea.

## 6. Cómo se trabaja

- **Leer antes de escribir.** Revisa el contexto relevante y no rehagas decisiones ya tomadas (están en `docs/DECISIONES.md`). Si crees que una debe cambiar, dilo y propón el cambio; no lo apliques en silencio.
- **Fuentes.** Toda cifra, cita legal o afirmación sobre registros lleva fuente y fecha de consulta (`docs/FUENTES.md`). Un «cero resultados» solo vale con un control positivo que demuestre que la búsqueda puede encontrar algo.
- **Verificar.** Tras un cambio, comprueba el resultado (regenerar, abrir, comparar) y di qué verificaste y qué no.
- **Explicar al terminar:** qué cambió, dónde y qué queda pendiente, en lenguaje llano.
- **Rutas relativas** en los documentos, para que sobrevivan a renombrar carpetas.
- **Nombres:** carpetas numeradas por orden de uso, sin espacios. Fechas ISO en nombres de archivo (`cierre_de_sesion_2026-10-02.md`). Los documentos vivos van en MAYÚSCULAS y se sobrescriben (`ESTADO_ACTUAL.md`); los registros con fecha no se reescriben, se añaden.

## 7. Varios agentes a la vez

- Antes de editar un archivo, mira su fecha de modificación. Si cambió hoy y no fuiste tú, léelo entero y no lo reescribas desde cero.
- **Solo el agente principal de la sesión actualiza** `docs/ESTADO_ACTUAL.md`, `docs/DECISIONES.md` y `docs/TAREAS_ABIERTAS.md`. Los subagentes devuelven su resultado en el mensaje final. Cada actualización lleva fecha y agente (`03.10.2026 · Nombre del agente`).
- A un subagente se le da un encargo autocontenido: objetivo, archivos que leer, qué no tocar y formato de la respuesta.
- La memoria privada de un agente no la ven los demás. Lo que deba compartirse va a estos documentos.

## 8. Cierre de sesión

Cuando la persona diga «guarda todo» o «mañana seguimos»:

1. Crea `docs/cierre_de_sesion_AAAA-MM-DD.md`: resultado, decisiones, dónde está cada cosa, qué se verificó, borradores a la espera de OK y agenda de la próxima sesión.
2. Sobrescribe `docs/ESTADO_ACTUAL.md`, añade lo aprobado a `docs/DECISIONES.md` y pon al día `docs/TAREAS_ABIERTAS.md`.
3. Repite las comprobaciones baratas que caducan (enlaces, dominios, plazos) y anota el resultado.

## 9. Mapa

{{MAPA_DE_CARPETAS: una línea por carpeta de primer nivel}}
