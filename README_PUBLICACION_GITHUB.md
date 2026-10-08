# Publicación asistida por IA

Repositorio de destino: [EFT_S9_Ingenieria_Software_2](https://github.com/crnahuas/EFT_S9_Ingenieria_Software_2).

Las instrucciones que debe seguir la IA están en [AGENTS.md](AGENTS.md). Ese archivo explica qué subir, cómo mantener trazabilidad, qué comprobar y cómo agrupar y publicar los commits.

El [plan de commits](docs/PLAN_COMMITS.md) detalla los diez grupos de la primera publicación, sus mensajes exactos y los archivos de cada uno. La IA debe omitir los grupos ya publicados sin cambios y gestionar el push de la secuencia completa.

## Qué se necesita una sola vez

- Una herramienta de IA con acceso a los archivos locales y a Git.
- Una copia local del repositorio y los artefactos finales disponibles.
- Inicio de sesión en GitHub con permiso de escritura, mediante la herramienta o el gestor de credenciales del equipo. No enviar contraseñas ni tokens por el chat.

## Encargo listo para copiar

> Lee AGENTS.md y actualiza https://github.com/crnahuas/EFT_S9_Ingenieria_Software_2.git con los artefactos finales de Nuevos Horizontes. Conserva el trabajo existente, sincroniza documentación y trazabilidad, actualiza el manifiesto, verifica los cambios y crea y publica los commits necesarios. Gestiona los mensajes y la agrupación de commits sin pedirme que prepare cada uno. Entrega el enlace al commit publicado y los pendientes reales.

La IA gestiona los commits por tarea terminada. Se publican los archivos descomprimidos, incluyendo DAS, Draw.io, HTML, matriz y documentación. El ZIP sirve para transportar la entrega.

## Ejecución sin enviar un mensaje

Para sincronizar periódicamente se necesita además una tarea programada con una frecuencia o disparador definido. AGENTS.md no ejecuta procesos por sí solo. GitHub Actions puede validar lo que llega al repositorio, pero no recoger archivos que siguen en este computador.

La frecuencia de una tarea recurrente todavía no está definida. Esta carpeta prepara las instrucciones; no configura una ejecución periódica ni confirma una publicación.
