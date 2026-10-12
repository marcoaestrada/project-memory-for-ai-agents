# Memoria compartida de proyecto para agentes de IA (versión en español)

Una plantilla pequeña, en Markdown plano, que da a un proyecto una **memoria compartida** para personas y agentes de IA (Claude Code, Codex, Cursor o cualquier agente que lea archivos). Responde cuatro preguntas cada vez que empieza el trabajo:

1. **¿Cuáles son las reglas?** → `AGENTS.md`
2. **¿Dónde estamos ahora?** → `docs/ESTADO_ACTUAL.md`
3. **¿Qué se decidió ya, y por qué?** → `docs/DECISIONES.md`
4. **¿Qué sigue abierto y de quién es?** → `docs/TAREAS_ABIERTAS.md`

Sin herramientas ni dependencias. Copia los archivos, rellena los huecos y haz commit.

> Salió de un flujo de trabajo real con varios agentes y una persona sobre la misma carpeta durante semanas. Cada regla de la plantilla existe porque, sin ella, algo salió mal.

## Por qué existe

Un agente de IA empieza cada sesión sin memoria, y una persona que vuelve tras una semana tiene el mismo problema. Sin un registro compartido:

- un agente rehace una decisión ya tomada, o la revierte sin avisar;
- dos agentes editan el mismo archivo y uno pisa al otro;
- un dato verificado una vez se «recuerda» mal más tarde;
- nadie sabe qué se aprobó y qué solo se propuso.

La plantilla lo resuelve con unos pocos hábitos, no con software.

## Contenido

```
template/
  AGENTS.md              reglas para cualquier agente: qué leer, quién decide, qué pide permiso
  CLAUDE.md              una línea que importa AGENTS.md
  docs/
    ESTADO_ACTUAL.md     instantánea viva: se sobrescribe al abrir y cerrar cada sesión
    DECISIONES.md        registro solo de adición: qué se decidió, quién y por qué
    TAREAS_ABIERTAS.md   una fila por tarea, con siguiente paso concreto y responsable
    GLOSARIO.md          nombres y términos, para que los agentes no inventen sinónimos
    FUENTES.md           de dónde sale cada dato, con la fecha de comprobación
```

El ejemplo relleno (en inglés) está en `../examples/bakery/` y el razonamiento de cada regla, en `../docs/PRINCIPLES.md`.

## Cómo usarla

1. Copia `es/template/` en la raíz de tu proyecto.
2. Abre `AGENTS.md` y sustituye cada `{{MARCADOR}}`. Borra las secciones que no necesites: **cuanto más corto, mejor**.
3. Dile a tu herramienta que lea `AGENTS.md` primero (Claude Code lee `CLAUDE.md`, que lo importa).
4. Al final de cada sesión, pide al agente que ejecute la rutina de *cierre de sesión* de `AGENTS.md`.

## Los cinco hábitos que más importan

1. **Una sola fuente de reglas.** `AGENTS.md` es el único sitio donde viven; los demás archivos apuntan a él.
2. **Los documentos vivos se sobrescriben; los registros se añaden.** El estado es una instantánea. Las decisiones y los registros con fecha no se reescriben.
3. **Solo un agente actualiza los archivos compartidos.** Los demás informan en su mensaje final. Así no se pisan.
4. **Propuesto no es decidido.** Una decisión se anota solo si la persona la aprobó. Lo que sugiere un agente va a la lista de tareas.
5. **Cada dato lleva fuente y fecha.** Un «cero resultados» solo vale con un control positivo que demuestre que la búsqueda puede encontrar algo.

## Qué no es

- No es un marco ni una herramienta: es una convención escrita en Markdown.
- No es una barrera de seguridad. Los documentos describen funciones y límites, pero **no amplían ni restringen** lo que un agente puede hacer técnicamente. Para eso usa permisos reales.
- No es asesoramiento jurídico, fiscal ni de cumplimiento.

## Soporte

Se comparte tal cual. **No hay soporte garantizado**; las incidencias y las propuestas pueden tardar mucho en contestarse o no contestarse.

## Licencia

MIT. Véase [LICENSE](../LICENSE).
