# Guía de estructura y versionado

## Objetivo

Esta guía establece cómo mantener el repositorio de Nuevos Horizontes como evidencia de evolución, trazabilidad y control de versiones. La carpeta raíz contiene la presentación general y el historial; los documentos técnicos, diagramas y prototipos se separan por propósito.

## Criterio de organización

- `docs/das`: versiones de entrega del Documento de Arquitectura de Software.
- `docs/arquitectura`: fuentes editables de diagrams.net.
- `docs/MATRIZ_TRAZABILIDAD.md`: trazabilidad legible y revisable mediante Git.
- `prototipos/baja-fidelidad`: prototipos tempranos o wireframes.
- `prototipos/alta-fidelidad`: prototipos interactivos finales.
- `evidencias`: capturas seleccionadas para revisión rápida.

No se deben agregar copias con nombres como `FINAL_FINAL`, `CORREGIDO2` o `NUEVO`. Git conserva el historial; el nombre estable identifica el artefacto y el commit explica el cambio.

## Ramas

Para esta entrega académica basta con una estrategia simple:

- `main`: contenido revisado y listo para entregar.
- `docs/<tema>`: cambios temporales en DAS, trazabilidad o guías.
- `prototype/<tema>`: cambios temporales en los prototipos.
- `fix/<tema>`: correcciones acotadas.

Las ramas se integran en `main` solo después de revisar que los enlaces funcionen, el Draw.io abra y los prototipos conserven la navegación esperada.

## Convención de commits

Formato recomendado:

```text
tipo: descripción breve en presente
```

Tipos sugeridos:

- `docs`: documentación, DAS, diagramas o trazabilidad.
- `feat`: nueva función o pantalla del prototipo.
- `fix`: corrección de comportamiento o coherencia.
- `style`: cambios visuales que no alteran el flujo.
- `test`: evidencias o comprobaciones.
- `chore`: organización, configuración o mantenimiento.

Ejemplos:

```text
docs: incorpora requisitos funcionales y no funcionales
docs: agrega casos de uso nivel 2
docs: completa vistas de proceso desarrollo y física
feat: agrega prototipo de baja fidelidad
feat: incorpora prototipo de alta fidelidad por roles
fix: establece login como pantalla inicial
fix: restringe navegación según rol
fix: agrega cierre de sesión
docs: agrega matriz de trazabilidad global
docs: consolida DAS para EFT semana 9
```

Cada commit debe representar un cambio entendible y comprobable. Evite mezclar en un mismo commit una corrección del prototipo, un reemplazo completo del DAS y una reorganización de carpetas.

## Etiquetas

Etiquetas sugeridas para hitos que cuenten con sus artefactos reales:

```text
v0.1-semana3
v0.2-semana4
v0.3-das
v0.4-prototipo-baja
v0.5-prototipo-alta
v0.9-semana8
v1.0.0
v1.1.0
```

No reconstruya etiquetas históricas sobre archivos que no correspondan a esos hitos. Si el repositorio nace desde esta carpeta corregida, publique primero `v1.1.0` y agregue versiones anteriores solo si se recuperan sus artefactos originales.

## Secuencia recomendada para la primera publicación

1. Crear un repositorio vacío sin README automático.
2. Copiar el contenido de esta carpeta en la raíz del repositorio local.
3. Revisar nombres, enlaces relativos y datos de integrantes.
4. Confirmar que el DAS abre en Word.
5. Confirmar que el archivo Draw.io muestra 28 páginas en diagrams.net.
6. Probar ambos HTML en escritorio y móvil.
7. Crear commits separados por grupos de artefactos, si se desea un historial inicial más legible.
8. Etiquetar la revisión aceptada como `v1.1.0`.
9. Publicar el repositorio únicamente después de revisar que no existan credenciales ni datos sensibles.

Ejemplo de agrupación para los primeros commits:

```text
docs: crea estructura y documentación del repositorio
docs: incorpora DAS y arquitectura final
feat: agrega prototipos de baja y alta fidelidad
docs: registra trazabilidad y versión EFT semana 9
```

## Archivos binarios

El DAS `.docx` y el Draw.io se conservan como fuentes de entrega, pero Git no muestra diferencias detalladas del Word. Los cambios importantes también deben registrarse en `CHANGELOG.md` y en la matriz Markdown para que el historial sea legible.

No se requiere Git LFS para el tamaño actual de los archivos. Si en el futuro se agregan videos MP4 o muchas imágenes de alta resolución, conviene mantenerlos fuera del repositorio o utilizar Git LFS.

## Criterios antes de etiquetar una versión

- El DAS y el Draw.io usan la misma numeración de RF, RNF y CU.
- El prototipo conserva una pantalla o flujo demostrativo para CU-01 a CU-09 y la matriz identifica la evidencia correspondiente.
- El prototipo inicia en login y separa las opciones por rol.
- La matriz enlaza todos los CU con requisitos y componentes.
- Los enlaces del README funcionan desde GitHub.
- No existen archivos temporales, contraseñas, tokens o información personal innecesaria.
- `CHANGELOG.md` describe las correcciones incluidas.
