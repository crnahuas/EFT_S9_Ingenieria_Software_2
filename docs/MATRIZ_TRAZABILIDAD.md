# Matriz de trazabilidad

## Propósito

Esta matriz relaciona los casos de uso con los requisitos, las decisiones arquitectónicas y la evidencia disponible en los prototipos. Su objetivo es facilitar la revisión de coherencia entre análisis, diseño y validación.

## Casos de uso y artefactos

| Caso de uso | Requisitos funcionales | Requisitos no funcionales directos | Arquitectura y componentes | Evidencia en prototipo | Estado |
|---|---|---|---|---|---|
| CU-01 Autenticar usuario | RF-01, RF-02, RF-18 | RNF-01, RNF-02 | Autenticación y roles; API REST; Auditoría | Inicio de sesión; selección de rol; cierre de sesión | Cubierto |
| CU-02 Gestionar residentes, departamentos y ocupaciones | RF-03, RF-04, RF-18 | RNF-02, RNF-03 | Residentes y unidades; Persistencia; Auditoría | Gestión de residentes | Cubierto por mockup interactivo |
| CU-03 Calcular y emitir cuotas | RF-05, RF-06, RF-07, RF-18 | RNF-04, RNF-10 | Cobranza; Cuotas; Gastos y distribución; Auditoría | Cálculo y emisión de cuotas | Cubierto por mockup interactivo |
| CU-04 Registrar pago | RF-08, RF-09, RF-10, RF-11, RF-12, RF-18 | RNF-04, RNF-07, RNF-10 | Cobranza; `IPasarelaPago`; Comprobantes; Auditoría | Cuotas y pagos; Mis cuotas y pagos | Cubierto |
| CU-05 Consultar estado de cuenta | RF-02, RF-15, RF-18 | RNF-03, RNF-04, RNF-06 | Consultas; Autorización; Persistencia; Auditoría | Mis cuotas y pagos | Cubierto |
| CU-06 Gestionar morosidad | RF-13, RF-14, RF-18 | RNF-04, RNF-10 | Cobranza; `INotificador`; Auditoría | Alertas de morosidad y recordatorio | Cubierto |
| CU-07 Generar informes | RF-16, RF-17, RF-18 | RNF-03, RNF-04, RNF-10 | Consultas e informes; Auditoría | Informes con filtros, vista previa y exportación simulada | Cubierto por mockup interactivo |
| CU-08 Gestionar conceptos de gasto | RF-05, RF-18 | RNF-02, RNF-10 | Gastos y distribución; Cobranza; Auditoría | Conceptos de gasto por período | Cubierto por mockup interactivo |
| CU-09 Mantener personal e instalaciones | RF-17, RF-18, RF-19 | RNF-02, RNF-10 | Personal e instalaciones; Consultas; Auditoría | Personal e instalaciones con estados vigentes | Cubierto por mockup interactivo |

El prototipo es una representación de interacción y no una implementación productiva. Las pantallas demuestran los flujos principales y sus estados de retroalimentación, pero no ejecutan reglas de negocio en un servidor ni mantienen persistencia real.

## Cobertura de requisitos funcionales

| Requisito | Descripción resumida | Casos de uso relacionados | Evidencia o decisión principal |
|---|---|---|---|
| RF-01 | Autenticar usuarios | CU-01 | Login y componente de autenticación. |
| RF-02 | Autorizar por rol | CU-01, CU-05 | Menús separados; validación de pantalla autorizada. |
| RF-03 | Gestionar residentes | CU-02 | Pantalla de residentes y módulo de residentes. |
| RF-04 | Gestionar departamentos y ocupaciones | CU-02 | Modelo de unidades y reglas de vigencia. |
| RF-05 | Gestionar conceptos de gasto | CU-03, CU-08 | Módulo de gastos y pantalla Conceptos de gasto. |
| RF-06 | Calcular cuotas | CU-03 | Servicio de cobranza, reglas de distribución y simulación del cálculo. |
| RF-07 | Emitir cuotas | CU-03 | Pantalla Cálculo y emisión de cuotas y publicación para residentes. |
| RF-08 | Registrar pagos administrativos | CU-04 | Flujo de pago administrativo. |
| RF-09 | Procesar pagos electrónicos | CU-04 | `IPasarelaPago` y adaptador externo. |
| RF-10 | Validar pagos | CU-04 | Validación de cuota, monto, saldo y referencia. |
| RF-11 | Emitir comprobantes | CU-04 | Componente de comprobantes. |
| RF-12 | Actualizar saldo | CU-04 | Operación transaccional de pago. |
| RF-13 | Identificar morosidad | CU-06 | Lista de alertas de morosidad. |
| RF-14 | Enviar recordatorios | CU-06 | `INotificador` e interacción de envío. |
| RF-15 | Consultar estado de cuenta | CU-05 | Pantalla Mis cuotas y pagos. |
| RF-16 | Generar informes financieros | CU-07 | Pantalla Informes con filtros y vista previa. |
| RF-17 | Generar informes operacionales | CU-07, CU-09 | Pantallas Informes y Personal e instalaciones. |
| RF-18 | Registrar auditoría | CU-01 a CU-09 | Auditoría transversal. |
| RF-19 | Mantener personal e instalaciones | CU-09 | Pantalla Personal e instalaciones y módulo operacional. |

## Cobertura de requisitos no funcionales

| Requisito | Decisión o mecanismo asociado | Verificación prevista |
|---|---|---|
| RNF-01 Seguridad de acceso | TLS 1.2+; hash adaptativo; autenticación centralizada. | Revisión de configuración y almacenamiento de credenciales. |
| RNF-02 Control de autorización | Autorización en servidor; mínimo privilegio; roles Administrador y Residente. | Pruebas negativas de acceso. |
| RNF-03 Privacidad | Filtrado por rol y departamento asociado. | Pruebas con usuarios de distintos departamentos. |
| RNF-04 Rendimiento | API separada, consultas por módulo y dimensionamiento referencial. | Prueba de carga para 160 departamentos. |
| RNF-05 Disponibilidad | Nodos separados, monitoreo y tratamiento de fallas externas. | Medición mensual de disponibilidad. |
| RNF-06 Usabilidad | Navegación clara, feedback visual y tareas prioritarias accesibles. | Prueba de tareas con usuarios representativos. |
| RNF-07 Integridad transaccional | Pago, saldo y comprobante en una operación consistente. | Prueba de falla inducida y rollback. |
| RNF-08 Respaldo y recuperación | PostgreSQL con respaldo diario; RPO 24 h; RTO 4 h. | Restauración trimestral documentada. |
| RNF-09 Compatibilidad | Diseño responsive desde 360 px y navegadores modernos. | Matriz de Chrome, Edge y Safari. |
| RNF-10 Auditabilidad | Auditoría transversal e inmutable para usuarios comunes, retención de 24 meses. | Consulta histórica por usuario, fecha, acción y entidad. |

## Pendientes de implementación

- Construir el backend y la persistencia real.
- Integrar proveedores reales para pagos y notificaciones mediante los contratos definidos.
- Ejecutar pruebas de carga, seguridad, recuperación, compatibilidad y usabilidad.
