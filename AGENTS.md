# Instrucciones para la IA: publicación y trazabilidad

Destino: `https://github.com/crnahuas/EFT_S9_Ingenieria_Software_2.git`.

Para la primera incorporación, seguir la secuencia de archivos y mensajes de `docs/PLAN_COMMITS.md`. Omitir grupos sin diferencias; para actualizaciones posteriores, aplicar solo los commits pertinentes.

## Encargo

Cuando el usuario solicite actualizar y publicar la entrega, gestionar revisión, sincronización, validación, commits y push sin pedirle que prepare cada commit. Una solicitud de revisión o preparación local no autoriza por sí sola publicar. Estas instrucciones no instalan un monitor ni programan ejecuciones.

## Archivos

Versionar README, AGENTS.md, CHANGELOG, .gitignore, documentación de docs/, DAS vigente, Draw.io corregido, prototipos y sus recursos, y evidencias verificadas. Excluir ZIP, temporales, respaldos, dependencias, credenciales y datos reales de residentes. No agregar automáticamente los MP4 individuales.

## Procedimiento

1. Revisar el estado local, remoto e historial. Verificar que origin apunta al destino indicado y consultar la rama predeterminada real.
2. Si falta una copia local, clonar el repositorio a una carpeta nueva. Preservar cambios existentes y comparar contenidos antes de reemplazar artefactos; no sobrescribir una versión remota más nueva con una copia antigua.
3. Incorporar los artefactos finales disponibles conservando sus rutas. Mantener coherentes DAS, Draw.io y matriz para RF-01 a RF-19, RNF-01 a RNF-10 y CU-01 a CU-09. Documentar cambios autorizados de identificadores.
4. Actualizar README y CHANGELOG con cambios reales. No inventar hitos, fechas, pruebas ni aportes personales.
5. Regenerar tamaños y SHA-256 del manifiesto para todos los archivos de entrega, excluyendo el propio manifiesto, .git/ y temporales.
6. Verificar enlaces Markdown. Si cambian prototipos, comprobar scripts, navegación, login y roles. Si cambia Draw.io, validar XML y sus 28 páginas actuales. Si cambia Word, renderizar y revisar formato, índice, tablas y trazabilidad. Distinguir pruebas ejecutadas de comprobaciones pendientes.
7. Revisar el diff y seleccionar explícitamente archivos de la tarea. Agrupar cambios relacionados en uno o pocos commits por tarea, no uno por archivo o edición. Ejemplos: `docs: actualiza DAS y trazabilidad`, `fix: corrige navegación por rol`.
8. Si no hay diferencias, no crear commits vacíos. Antes del push consultar cambios remotos, conservar trabajo de ambas partes y resolver conflictos dentro del alcance autorizado. No usar force push ni reescribir historial compartido.
9. Publicar cuando el encargo actual lo autorice. Respetar protecciones de rama; usar rama y PR si el encargo incluye ese flujo. Crear tags/releases solo si se solicita una versión; comprobar etiquetas existentes. La entrega preparada corresponde a v1.1.0.
10. Confirmar el resultado remoto e informar enlace y hash del commit. Si falta autenticación, conservar el trabajo y explicar cómo iniciar sesión mediante la herramienta. Nunca pedir tokens o contraseñas en el chat. Distinguir commit local de publicación confirmada.

## Límites de la entrega

Los HTML son prototipos académicos; no declarar backend, persistencia ni integraciones reales. La presentación MP4 y reflexión son individuales y solo pueden declararse completas si están disponibles.

Una automatización recurrente requiere frecuencia o disparador solicitado por el usuario, acceso a los archivos y autenticación. GitHub Actions puede comprobar archivos tras un push, pero no recoge por sí solo documentos del computador del usuario.
