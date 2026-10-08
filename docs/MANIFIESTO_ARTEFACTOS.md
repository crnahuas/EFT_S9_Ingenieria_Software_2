# Manifiesto de artefactos

Registro de integridad de la entrega corregida el 8 de octubre de 2026. Los valores SHA-256 permiten comprobar que los archivos no fueron modificados después de generar este paquete.

| Archivo | Tamaño (bytes) | SHA-256 |
|---|---:|---|
| `.gitignore` | 458 | `ac9972b82359d33e7b20fbbcd1541eaeea587f4646d2e68d154c231f2f3b8a56` |
| `AGENTS.md` | 3.630 | `95261d9b2a9cfb3ab36d1f8590af8d68940f16d8de31aace91f77b8b9412af34` |
| `CHANGELOG.md` | 3.111 | `28a89f2c29f2dbe421e6a24c3fce592adca2e62436c30d9f678530a3200de74a` |
| `README.md` | 6.959 | `99d2db83db3b8db15c2b5575eed0ab46a760fe0d898a7351a8fb5f8aa766f386` |
| `README_PUBLICACION_GITHUB.md` | 2.075 | `cc46adf4128c50e9421f4cbe1cefaa942759737e616a80a5f9f8d8af00567370` |
| `docs/GUIA_ESTRUCTURA_Y_VERSIONADO.md` | 4.881 | `848f78a18fbe0f46293c90497fa812caaecb9209ed6c383f82d5d53b6001f312` |
| `docs/MATRIZ_TRAZABILIDAD.md` | 6.095 | `cce1158703bb240f00e3a509e3276c2487e3b6a32c4789789cd057da2139f96b` |
| `docs/PLAN_COMMITS.md` | 5.597 | `ee41d3e5c0d4234f6556611acdd5a80f831f95ae704b332c7b2695f5e8cdebf3` |
| `docs/PRESENTACION_INDIVIDUAL_GUIA.md` | 2.450 | `09e9beb42c6df151720aabb31784d9928c7dcf94657cdd82f974f40090b07b27` |
| `docs/VERIFICACION_PAUTA.md` | 3.420 | `e6d41e5ae0957672cf597a6370f2252f5416caf82448d4e30c1263dfc6b00061` |
| `docs/arquitectura/EXP2_S9_Grupo7_Diagramas_CORREGIDO.drawio` | 221.834 | `414881cf371aecc3aedb300c05783d5c2968c4a0a523c8f90a4e8548cbb27430` |
| `docs/das/GRY2203_EFT_S9_Grupo7_DAS_ENTREGA_DEFINITIVA_V3.docx` | 3.311.815 | `0a2f6a5fe57764a4ba7a6751aff2993d431bb33f6f81df27ee76cd7f10b8301b` |
| `evidencias/README.md` | 836 | `72436ab094499186e0e83c8d38799494411b535bf8695f9a5872aea57f085051` |
| `prototipos/alta-fidelidad/prototipo_nuevos_horizontes_s9_corregido.html` | 63.396 | `b91e519b0b5df3415528368487f98ee08864258da9844a8a396562a6bae8bb05` |
| `prototipos/baja-fidelidad/prototipo_nuevos_horizontes_baja_fidelidad_autocontenido.html` | 337.651 | `38751d278628d2b1c6dbc114e355dbd497f156d88d761667a7318bd253390f17` |

## Verificación

En macOS o Linux, desde la raíz del repositorio:

```bash
shasum -a 256 RUTA_DEL_ARCHIVO
```

El resultado debe coincidir con el valor correspondiente de esta tabla. Este manifiesto no se incluye a sí mismo para evitar una referencia circular.
