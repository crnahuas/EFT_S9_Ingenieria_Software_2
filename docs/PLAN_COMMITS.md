# Plan de commits para la IA

Destino: `https://github.com/crnahuas/EFT_S9_Ingenieria_Software_2.git`.

Esta secuencia organiza la primera publicación de la carpeta preparada. Son grupos de incorporación actuales, no una reconstrucción del desarrollo de semanas anteriores. Ejecutar dentro de una copia local del repositorio y únicamente cuando el usuario solicite publicar. Leer primero `AGENTS.md`.

## Primera publicación

| Orden | Mensaje exacto del commit | Archivos que debe incluir |
|---:|---|---|
| 1 | `chore: configura exclusiones del repositorio` | `.gitignore` |
| 2 | `docs: incorpora arquitectura editable y casos de uso` | `docs/arquitectura/EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio` |
| 3 | `docs: incorpora DAS final revisado de semana 9` | `docs/das/GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx` |
| 4 | `feat: incorpora prototipo de baja fidelidad` | `prototipos/baja-fidelidad/prototipo_nuevos_horizontes_baja_fidelidad_autocontenido.html` |
| 5 | `feat: incorpora prototipo de alta fidelidad por roles` | `prototipos/alta-fidelidad/prototipo_nuevos_horizontes_s9_corregido.html` |
| 6 | `docs: incorpora trazabilidad y verificacion de pauta` | `docs/MATRIZ_TRAZABILIDAD.md`, `docs/VERIFICACION_PAUTA.md` |
| 7 | `docs: agrega guias de versionado presentacion y evidencias` | `docs/GUIA_ESTRUCTURA_Y_VERSIONADO.md`, `docs/PRESENTACION_INDIVIDUAL_GUIA.md`, `evidencias/README.md` |
| 8 | `docs: define publicacion asistida por IA y plan de commits` | `AGENTS.md`, `README_PUBLICACION_GITHUB.md`, `docs/PLAN_COMMITS.md` |
| 9 | `docs: publica portada e historial de la entrega` | `README.md`, `CHANGELOG.md` |
| 10 | `docs: registra integridad del paquete final` | `docs/MANIFIESTO_ARTEFACTOS.md`, regenerado después de completar los demás archivos |

## Ramas y merges de la primera publicación

Para conservar la evolución visible en el grafo de Git, los grupos se preparan en ramas temáticas y se integran en `main` mediante merges `--no-ff`:

- `docs/arquitectura-das`: grupos 2 y 3; merge `merge: integra arquitectura y DAS de semana 9`.
- `prototype/baja-fidelidad`: grupo 4; merge `merge: integra prototipo de baja fidelidad`.
- `prototype/alta-fidelidad`: grupo 5; merge `merge: integra prototipo de alta fidelidad por roles`.
- `docs/trazabilidad-cierre`: grupos 6 a 10; merge `merge: integra trazabilidad y documentacion final`.

Cada rama debe nacer desde el estado actualizado de `main`. Los merges conservan la agrupación del trabajo sin inventar fechas ni autores de etapas anteriores.

## Cómo ejecutar la secuencia

1. Consultar el estado local, el historial y las referencias remotas. Confirmar el destino y la rama de publicación.
2. Comparar el contenido existente con la entrega. Si un grupo ya está incorporado sin diferencias, omitir su commit. Si contiene una versión más nueva, conservarla y resolver la discrepancia antes de continuar.
3. Para cada fila, seleccionar explícitamente sus archivos, revisar el contenido preparado y crear el commit con el mensaje indicado. No usar un agregado global que incluya modificaciones ajenas al encargo.
4. No crear commits vacíos ni duplicar archivos solo para cumplir diez pasos. Si el repositorio ya tiene contenido, adaptar la secuencia a las diferencias reales y usar mensajes que describan la actualización.
5. Regenerar el manifiesto al final, incluyendo todos los archivos de entrega excepto el propio manifiesto. Excluir `.git/`, temporales y respaldos.
6. Verificar la entrega completa y consultar nuevamente el remoto. Publicar los commits juntos mediante un push cuando la solicitud vigente autorice publicar y las comprobaciones hayan terminado.
7. Confirmar que el extremo remoto coincide con el último commit local. Entregar enlace y hash del último commit, además de la lista de commits creados y los grupos omitidos por estar actualizados.

El primer push puede contener toda esta secuencia: no hace falta que el usuario publique cada commit por separado. Los enlaces de la portada se comprueban sobre el estado final de la entrega.

## Actualizaciones posteriores

Después de la primera publicación, no repetir la secuencia completa. Elegir el grupo que corresponda al trabajo realizado y mantener los artefactos relacionados dentro del mismo commit cuando sea necesario para su coherencia.

| Cambio real | Mensaje sugerido | Archivos relacionados |
|---|---|---|
| Requisitos o casos de uso | `docs: actualiza requisitos y trazabilidad` | DAS, Draw.io, matriz y CHANGELOG según el cambio |
| Arquitectura | `docs: actualiza vistas arquitectonicas` | Draw.io, DAS, matriz y CHANGELOG según el cambio |
| Nueva pantalla o flujo | `feat: agrega flujo de [nombre]` | HTML y recursos, matriz, evidencia, DAS y CHANGELOG cuando corresponda |
| Corrección de comportamiento | `fix: corrige [problema concreto]` | HTML y documentación afectada |
| Nuevas capturas verificadas | `docs: incorpora evidencias del prototipo` | Capturas actuales y su documentación |
| Cambios en instrucciones de IA | `docs: actualiza flujo de publicacion asistida` | AGENTS.md, guía y plan según corresponda |
| Cierre de un paquete | `docs: actualiza manifiesto de entrega` | Manifiesto regenerado, si no se incluyó en el commit de la actualización |

Reemplazar los textos entre corchetes por el cambio concreto. En actualizaciones pequeñas, incluir CHANGELOG y manifiesto en el mismo commit del cambio para mantenerlos sincronizados. Una etiqueta o release es un hito adicional, no un commit; crearla solo cuando el usuario lo solicite y sin reemplazar etiquetas existentes.
