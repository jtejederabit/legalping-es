# Legalize ES

### Legislación española consolidada en Markdown, versionada con Git.

Cada ley es un fichero. Cada reforma es un commit.

**12,235 normas** · **17 comunidades autónomas** · **Actualización diaria**

Parte del proyecto [Legalize](https://github.com/legalize-dev/legalize) · [legalize.dev](https://legalize.dev)

> **Early stage** — This repository is under active development. File structure, commit history, and content may undergo significant changes, including full regeneration.

## Inicio rápido

```bash
# Clonar la legislación española
git clone https://github.com/legalize-dev/legalize-es.git

# ¿Qué dice el artículo 14 de la Constitución?
grep -A 5 "Artículo 14" es/BOE-A-1978-31229.md

# ¿Cuántas veces se ha reformado el Código Penal?
git log --oneline -- es/BOE-A-1995-25444.md

# Ver el diff exacto de una reforma
git show <commit> -- es/BOE-A-1995-25444.md
```

## Estructura

```
es/                          ← legislación estatal (8,646 normas)
  BOE-A-1978-31229.md        — Constitución Española
  BOE-A-1995-25444.md        — Código Penal
  BOE-A-1889-4763.md         — Código Civil
  BOE-A-2015-11430.md        — Estatuto de los Trabajadores
  ...

es-an/                       ← Andalucía
es-ct/                       ← Cataluña
es-md/                       ← Madrid
es-pv/                       ← País Vasco
...                          ← 17 jurisdicciones autonómicas
```

El rango normativo (ley, real decreto, ley orgánica, etc.) va en el frontmatter YAML de cada fichero, no en la estructura de directorios.

## Formato

Cada fichero contiene:

- **Frontmatter YAML** — metadatos: título, identificador, rango, fecha de publicación, estado jurídico, departamento, número oficial, diario, identificador ELI
- **Cuerpo Markdown** — texto consolidado con estructura jerárquica (títulos, capítulos, artículos)

Los commits usan la fecha histórica de publicación oficial en el BOE. Cada commit incluye trailers con el identificador de la norma y de la reforma, lo que permite reconstruir el historial legislativo completo con `git log`.

## Fuente

Datos obtenidos de la API de datos abiertos del [BOE](https://www.boe.es/datosabiertos/) (Boletín Oficial del Estado), publicados por la [Agencia Estatal Boletín Oficial del Estado](https://www.boe.es/).

## Prensa

- [Xataka](https://www.xataka.com/aplicaciones/alguien-ha-cogido-12-000-leyes-espanolas-ha-pasado-a-codigo-fuente-autentica-joya-para-buscar-legislacion) — *"Este programador es un héroe sin capa: ha convertido 12.000 leyes del BOE a código fuente"*
- [Ecosistema Startup](https://ecosistemastartup.com/legalize-es-automatizacion-para-leyes-espanolas-en-github/) — *"Automatización para leyes españolas en GitHub"*

## Licencia

Los textos legislativos son de dominio público. La estructuración y el formato están bajo licencia [MIT](LICENSE).

---

Creado por [Enrique Lopez](https://enriquelopez.eu) · [legalize.dev](https://legalize.dev)
