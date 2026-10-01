# Cómo contribuir

Convenciones comunes a los repositorios de Distribuidora Excel. Cada repositorio puede tener su
propio `CONTRIBUTING.md` con lo específico —cómo compilar, cómo correr las pruebas—; lo de aquí es
lo que no cambia de uno a otro.

## Flujo

1. Rama desde `main`, con nombre `tipo/descripción` (el tipo es el del commit): `fix/cfdi-pendientes`, `ci/release-msix`.
   **Nunca se empuja directo a `main`.**
2. Un commit por idea.
3. Pruebas que acompañen al cambio. Si arreglas un error, primero la prueba que falla.
4. Pull request con la plantilla: qué cambia, por qué, cómo se comprobó.
5. Se fusiona con la integración continua en verde, con *merge commit* (las reglas de la organización no admiten
   *squash* ni *rebase*: cada commit queda en el historial), y la rama se borra.

## Mensajes de commit

[Conventional Commits](https://www.conventionalcommits.org/es/), con el resumen en español:

```
tipo(ámbito): resumen en imperativo, minúscula, sin punto final

Cuerpo opcional a 72 columnas: por qué se hace, no qué se hizo —el diff ya
dice qué—. Si arregla algo, qué se rompía y cómo se comprobó que ya no.
```

| Tipo | Cuándo |
|---|---|
| `feat` | funcionalidad nueva para quien usa el sistema |
| `fix` | corrige un comportamiento equivocado |
| `perf` | mismo comportamiento, menos tiempo o menos recursos |
| `refactor` | reorganiza sin cambiar el comportamiento |
| `test` | añade o corrige pruebas |
| `docs` | documentación, comentarios, README |
| `style` | formato y orden; nada de lógica |
| `build` | compilación, paquetes, versiones, empaquetado |
| `ci` | integración continua, releases y automatización |
| `chore` | mantenimiento sin efecto en el producto |

Los ámbitos válidos los define cada repositorio.

## Código

- El dominio se nombra en español; lo que viene del marco se deja como está.
- Los comentarios explican *por qué*, no *qué*.
- Los nombres de las pruebas son frases que se leen como afirmaciones.
- Ningún secreto, cuenta, servidor ni ruta de un equipo entra al repositorio.
- Los commits van firmados.
