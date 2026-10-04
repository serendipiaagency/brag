# brag

Skills [`/brag`](https://latent-spaces.github.io/brag/) y `/brag-slim` instaladas a nivel de proyecto.
Convierten el proyecto en un vídeo de lanzamiento de ~20 segundos con música, movimiento y copy para compartir.

## Qué hay en este repo

- `.agents/skills/brag/` — la skill completa (`/brag`), con referencias, scripts y música + SFX.
- `.agents/skills/brag-slim/` — la versión ligera (`/brag-slim`), un solo archivo y sin assets.
- `.claude/skills/` — enlaces simbólicos a las carpetas anteriores para que Claude Code las detecte.
- `skills-lock.json` — origen y hash de cada skill, para actualizarlas con `npx skills update`.

## Uso

Dentro de este proyecto, pídele al agente:

```text
let's /brag
```

Opciones útiles:

```text
/brag --tone "lanzamiento de Series A en 2016"
/brag --voice        # narración (Kokoro vía Hyperframes)
/brag --full         # fuerza el flujo clásico con Hyperframes
```

En Opus 5.5, `/brag` salta automáticamente a `/brag-slim`. El resultado queda en `brag-output/`.

## Requisitos

- Node.js 22+
- FFmpeg en el `PATH`
- Hyperframes CLI: `npx hyperframes` (comprueba con `npx hyperframes doctor`)

## Instalación en otros sitios

```bash
# Plugin de Claude Code (ámbito de usuario)
/plugin marketplace add latent-spaces/brag
/plugin install brag@brag

# Cualquier otro agente
npx skills add https://github.com/latent-spaces/brag --skill brag
```

Fuente: https://github.com/latent-spaces/brag
