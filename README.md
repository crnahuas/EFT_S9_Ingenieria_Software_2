# Nuevos Horizontes

Entrega de la EFT de Semana 9 de Ingeniería de Software II. El proyecto propone un sistema para gestionar residentes, cuotas de gastos comunes, pagos, morosidad, comprobantes, informes, personal e instalaciones del edificio Nuevos Horizontes.

## Integrantes

- Cristian Nahuas
- Johan Romanque
- Grupo 7

## Artefactos de la entrega

| Artefacto | Archivo | Contenido |
|---|---|---|
| Informe grupal DAS | [`docs/das/GRY2203_EFT_S9_Grupo7_DAS.docx`](docs/das/GRY2203_EFT_S9_Grupo7_DAS.docx) | Versión final del informe con requisitos, casos de uso, arquitectura 4+1, decisiones de diseño y trazabilidad del proyecto. |
| Diagramas editables | [`docs/arquitectura/EXP2_S9_Grupo7_Diagramas.drawio`](docs/arquitectura/EXP2_S9_Grupo7_Diagramas.drawio) | Archivo final con las vistas de escenarios, lógica, proceso, desarrollo y física, además de las especificaciones de casos de uso. |
| Prototipo de baja fidelidad | [`prototipos/baja-fidelidad/GRY2203_EFT_S9_Grupo7_Prototipo_Baja_Fidelidad.html`](prototipos/baja-fidelidad/GRY2203_EFT_S9_Grupo7_Prototipo_Baja_Fidelidad.html) | Wireframe navegable que documenta la estructura inicial, los perfiles y los flujos priorizados. |
| Prototipo de alta fidelidad | [`prototipos/alta-fidelidad/GRY2203_EFT_S9_Grupo7_Prototipo.html`](prototipos/alta-fidelidad/GRY2203_EFT_S9_Grupo7_Prototipo.html) | Mockup final navegable con acceso y opciones diferenciadas para Administración y Residente. |
| Matriz de trazabilidad | [`docs/MATRIZ_TRAZABILIDAD.md`](docs/MATRIZ_TRAZABILIDAD.md) | Relación entre casos de uso, requisitos funcionales y no funcionales, arquitectura y evidencia del prototipo. |

## Preparación de la entrega final

- Se consolidó el informe en `GRY2203_EFT_S9_Grupo7_DAS.docx`.
- Se normalizó el nombre del archivo editable a `EXP2_S9_Grupo7_Diagramas.drawio`.
- Se incorporó el wireframe navegable como `GRY2203_EFT_S9_Grupo7_Prototipo_Baja_Fidelidad.html`.
- Se identificó el prototipo final navegable como `GRY2203_EFT_S9_Grupo7_Prototipo.html`.
- Se actualizaron los enlaces y la estructura del repositorio para utilizar únicamente los nombres finales.

## Cobertura

- RF-01 a RF-19.
- RNF-01 a RNF-10.
- CU-01 a CU-09.
- Vistas de escenarios, lógica, proceso, desarrollo y física.
- Evolución demostrable desde el wireframe de baja fidelidad hasta el prototipo final con navegación por roles.

## Revisión de los prototipos

Abra cada archivo HTML directamente en un navegador. El prototipo de baja fidelidad es autocontenido; el de alta fidelidad necesita conexión a Internet para cargar Bootstrap y Bootstrap Icons desde CDN.

El prototipo de baja fidelidad permite recorrer las pantallas iniciales de administración y residente para observar la estructura y los flujos definidos antes del refinamiento visual.

En el prototipo de alta fidelidad:

- seleccione `Administración` o `Residente`;
- ingrese un correo con formato válido;
- ingrese una contraseña de al menos seis caracteres.

Después del ingreso, el menú muestra únicamente las funciones autorizadas para el perfil seleccionado. Ambos perfiles disponen de `Cerrar sesión`, y los intentos de abrir una pantalla ajena al rol son redirigidos a una vista permitida.

El prototipo es una simulación académica. No contiene backend, persistencia, autenticación ni integraciones reales.

## Estructura

```text
.
├── README.md
├── .gitignore
├── docs
│   ├── MATRIZ_TRAZABILIDAD.md
│   ├── arquitectura
│   │   └── EXP2_S9_Grupo7_Diagramas.drawio
│   └── das
│       └── GRY2203_EFT_S9_Grupo7_DAS.docx
└── prototipos
    ├── baja-fidelidad
    │   └── GRY2203_EFT_S9_Grupo7_Prototipo_Baja_Fidelidad.html
    └── alta-fidelidad
        └── GRY2203_EFT_S9_Grupo7_Prototipo.html
```

## Alcance técnico

Las tecnologías descritas en el DAS corresponden a una propuesta arquitectónica. Este repositorio contiene documentación, diagramas y un prototipo de interfaz; no incluye una implementación productiva del sistema.

Los criterios de accesibilidad toman como referencia WCAG 2.1 nivel AA. Esta referencia orienta el diseño del prototipo, pero no constituye una declaración de conformidad completa sin una auditoría formal.
