# Nuevos Horizontes

Entrega grupal de la EFT de Semana 9 de Ingeniería de Software II. El proyecto propone un sistema para gestionar residentes, cuotas de gastos comunes, pagos, morosidad, comprobantes, informes, personal e instalaciones del edificio Nuevos Horizontes.

## Integrantes

- Cristian Nahuas
- Johan Romanque
- Grupo 7

## Artefactos de la entrega

| Artefacto | Archivo | Contenido |
|---|---|---|
| Informe grupal DAS | [`docs/das/GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx`](docs/das/GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx) | Requisitos, casos de uso, arquitectura 4+1, decisiones de diseño y trazabilidad del proyecto. |
| Diagramas editables | [`docs/arquitectura/EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio`](docs/arquitectura/EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio) | Vistas de escenarios, lógica, proceso, desarrollo y física, además de especificaciones de casos de uso. |
| Prototipo interactivo | [`prototipos/alta-fidelidad/prototipo_nuevos_horizontes_s9_corregido.html`](prototipos/alta-fidelidad/prototipo_nuevos_horizontes_s9_corregido.html) | Mockup navegable con acceso y opciones diferenciadas para Administración y Residente. |
| Matriz de trazabilidad | [`docs/MATRIZ_TRAZABILIDAD.md`](docs/MATRIZ_TRAZABILIDAD.md) | Relación entre casos de uso, requisitos funcionales y no funcionales, arquitectura y evidencia del prototipo. |

## Cobertura

- RF-01 a RF-19.
- RNF-01 a RNF-10.
- CU-01 a CU-09.
- Vistas de escenarios, lógica, proceso, desarrollo y física.
- Prototipo demostrativo con navegación por roles.

## Revisión del prototipo

Abra el archivo HTML directamente en un navegador. Se necesita conexión a Internet para cargar Bootstrap y Bootstrap Icons desde CDN.

En la pantalla de inicio:

- seleccione `Administración` o `Residente`;
- ingrese un correo con formato válido;
- ingrese una contraseña de al menos seis caracteres.

El prototipo es una simulación académica. No contiene backend, persistencia, autenticación ni integraciones reales.

## Estructura

```text
.
├── README.md
├── .gitignore
├── docs
│   ├── MATRIZ_TRAZABILIDAD.md
│   ├── arquitectura
│   │   └── EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio
│   └── das
│       └── GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx
└── prototipos
    └── alta-fidelidad
        └── prototipo_nuevos_horizontes_s9_corregido.html
```

## Presentación individual

La presentación y reflexión son individuales. Cada integrante debe entregar por separado su grabación MP4 de 3 a 5 minutos y el material visual de apoyo correspondiente.

## Alcance técnico

Las tecnologías descritas en el DAS corresponden a una propuesta arquitectónica. Este repositorio contiene documentación, diagramas y un prototipo de interfaz; no incluye una implementación productiva del sistema.
