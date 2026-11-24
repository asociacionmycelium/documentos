# CLAUDE.md — documentos institucionales de la Asociación Mycelium

Repositorio **público** con el manifiesto y los estatutos (CC BY-SA 4.0). La plataforma de transparencia vive en el repositorio `transparencia`.

## Reglas
- Solo texto. Nunca PDF firmados, el acta fundacional ni certificados de firma (contienen nombres, DNI y domicilios).
- Hasta la inscripción en el Registro Nacional de Asociaciones no se publican datos de socios.
- El domicilio social solo aparece en el art. 7 de `estatutos.md`.
- Cada cambio de los Estatutos va en un commit propio con el motivo y el acuerdo de la Asamblea (art. 47).
- `manifiesto.md`: tono cercano, nada comercial, sin justificarse.

## Antes de cada push (obligatorio)
1. Invoca el subagente `revisor-publicacion` con el rango que se va a subir (`git log origin/main..HEAD`; en el primer push, todo el árbol). Si devuelve BLOQUEAR, corrige antes de seguir.
2. El hook `pre-push` (`scripts/guardia.sh`) se ejecuta solo. No lo saltes con `--no-verify`.
