# Nuevos Horizontes

Repositorio académico del Sistema de Gestión de Gastos Comunes del edificio Nuevos Horizontes, desarrollado para la EFT de Semana 9 de Ingeniería de Software II.

La entrega consolida requisitos, casos de uso, arquitectura 4+1, trazabilidad y prototipos navegables. El sistema propuesto centraliza la gestión de residentes, departamentos, conceptos de gasto, cuotas, pagos, morosidad, comprobantes, informes, personal e instalaciones.

Para delegar la actualización y publicación a una IA, consulte [la guía de publicación asistida](README_PUBLICACION_GITHUB.md) y las [instrucciones del agente](AGENTS.md).

## Integrantes

- Cristian Nahuas
- Johan Romanque
- Grupo 7

## Artefactos principales

| Artefacto | Ubicación | Descripción |
|---|---|---|
| DAS final | [`docs/das/GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx`](docs/das/GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx) | Documento de Arquitectura de Software consolidado, corregido según el formato institucional y revisado para Semana 9. |
| Diagramas | [`docs/arquitectura/EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio`](docs/arquitectura/EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio) | Archivo editable de 28 páginas con escenarios, especificaciones, vistas 4+1, trazabilidad, interfaces y despliegue referencial. |
| Baja fidelidad | [`prototipos/baja-fidelidad/prototipo_nuevos_horizontes_baja_fidelidad_autocontenido.html`](prototipos/baja-fidelidad/prototipo_nuevos_horizontes_baja_fidelidad_autocontenido.html) | Wireframe navegable autocontenido. |
| Alta fidelidad | [`prototipos/alta-fidelidad/prototipo_nuevos_horizontes_s9_corregido.html`](prototipos/alta-fidelidad/prototipo_nuevos_horizontes_s9_corregido.html) | Prototipo final con login, navegación por roles, cierre de sesión, cobertura CU-01 a CU-09 y diseño responsive. |
| Trazabilidad | [`docs/MATRIZ_TRAZABILIDAD.md`](docs/MATRIZ_TRAZABILIDAD.md) | Relación entre casos de uso, RF/RNF, arquitectura y pantallas. |
| Versionado | [`docs/GUIA_ESTRUCTURA_Y_VERSIONADO.md`](docs/GUIA_ESTRUCTURA_Y_VERSIONADO.md) | Convenciones para ramas, commits, etiquetas y publicación. |
| Verificación de pauta | [`docs/VERIFICACION_PAUTA.md`](docs/VERIFICACION_PAUTA.md) | Correspondencia final entre los criterios de evaluación y la evidencia disponible. |
| Presentación individual | [`docs/PRESENTACION_INDIVIDUAL_GUIA.md`](docs/PRESENTACION_INDIVIDUAL_GUIA.md) | Pauta de 3 a 5 minutos, reflexión personal y comprobaciones previas a la grabación. |
| Integridad | [`docs/MANIFIESTO_ARTEFACTOS.md`](docs/MANIFIESTO_ARTEFACTOS.md) | Tamaños y huellas SHA-256 de los archivos incluidos. |

## Evolución del prototipo

1. Prototipo de baja fidelidad para validar estructura, navegación y tareas principales.
2. Diseño de alta fidelidad en Adobe XD para definir el sistema visual, componentes y flujos.
3. Prototipo web interactivo en HTML, CSS, Bootstrap y JavaScript.
4. Corrección de Semana 9: inicio real en login, menús separados por rol, bloqueo de pantallas no autorizadas, cierre de sesión y mejoras responsive.
5. Cierre de cobertura: se incorporaron cálculo y emisión de cuotas, conceptos de gasto, informes y personal e instalaciones.

El diseño publicado en Adobe XD se encuentra en [Prototipo Nuevos Horizontes](https://xd.adobe.com/view/aba24512-c1cb-4a5e-8f3e-6a824c4666ce-fef1/).

## Cómo revisar los prototipos

### Baja fidelidad

Abra el archivo HTML de baja fidelidad directamente en un navegador. Es autocontenido y no requiere conexión a Internet.

### Alta fidelidad

Abra el archivo HTML de alta fidelidad directamente en un navegador. Requiere conexión a Internet para cargar Bootstrap y Bootstrap Icons desde CDN.

En la pantalla de inicio de sesión:

- seleccione `Administración` o `Residente`;
- ingrese un correo con formato válido;
- ingrese una contraseña de al menos seis caracteres.

El prototipo es una simulación académica: no contiene backend, persistencia ni autenticación real.

## Cobertura funcional

- RF-01 a RF-19.
- RNF-01 a RNF-10.
- CU-01 a CU-09 con especificaciones y trazabilidad.
- Vista de escenarios, lógica, procesos, desarrollo y física.
- Interfaces `IPasarelaPago` e `INotificador`.
- Tecnologías y nodos propuestos como configuración referencial sujeta a validación.

El prototipo de alta fidelidad dispone de una pantalla o flujo demostrativo para CU-01 a CU-09. Sigue siendo un mockup académico: las reglas, integraciones y persistencia se simulan en el navegador y deberán implementarse en una solución productiva.

## Estructura

```text
.
├── README.md
├── AGENTS.md
├── README_PUBLICACION_GITHUB.md
├── CHANGELOG.md
├── .gitignore
├── docs
│   ├── GUIA_ESTRUCTURA_Y_VERSIONADO.md
│   ├── MANIFIESTO_ARTEFACTOS.md
│   ├── MATRIZ_TRAZABILIDAD.md
│   ├── PLAN_COMMITS.md
│   ├── PRESENTACION_INDIVIDUAL_GUIA.md
│   ├── VERIFICACION_PAUTA.md
│   ├── arquitectura
│   │   └── EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio
│   └── das
│       └── GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx
├── evidencias
│   └── README.md
└── prototipos
    ├── alta-fidelidad
    │   └── prototipo_nuevos_horizontes_s9_corregido.html
    └── baja-fidelidad
        └── prototipo_nuevos_horizontes_baja_fidelidad_autocontenido.html
```

## Versiones sugeridas

| Versión | Hito | Contenido principal |
|---|---|---|
| `v0.1-semana3` | Análisis | Requisitos, contexto y escenarios iniciales. |
| `v0.2-semana4` | Arquitectura | Vistas de proceso, desarrollo y física. |
| `v0.3-das` | Consolidación | DAS y especificaciones de casos de uso. |
| `v0.4-prototipo-baja` | Validación temprana | Prototipo de baja fidelidad. |
| `v0.5-prototipo-alta` | Diseño e interacción | Adobe XD y prototipo web. |
| `v0.9-semana8` | Integración | DAS y artefactos integrados de Semana 8. |
| `v1.0.0` | Entrega inicial EFT | DAS, Draw.io, prototipos y trazabilidad integrados. |
| `v1.1.0` | Revisión final de pauta | Formato institucional, trazabilidad RNF y cobertura demostrativa CU-01 a CU-09. |

Los tags históricos deben crearse únicamente si se publican los artefactos reales de cada hito. Para una publicación que comienza con esta carpeta corregida, use `v1.1.0` como primera etiqueta.

## Alcance técnico

Las tecnologías descritas en el DAS —Java 17, Spring Boot 3.x, PostgreSQL 16, Nginx, Docker y Ubuntu Server 24.04 LTS— corresponden a una propuesta referencial. El repositorio contiene documentación y prototipos; no incluye una implementación productiva del backend.

## Estado de publicación

La rama `main` contiene la entrega preparada. La publicación se considera confirmada únicamente después de comprobar que `origin/main` coincide con el último commit local y que los artefactos se visualizan correctamente en GitHub.
