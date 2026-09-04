# Administración de Propiedad Horizontal (PH) y Rentas Cortas: Análisis de Datos y Cumplimiento Normativo

## 1. Definición del Problema (Árbol de Problemas)
**Problema Central:** Incremento de la exposición fiduciaria y legal en la administración de propiedades horizontales con destinación turística mixta, derivado del incumplimiento normativo, brechas de privacidad y fallas en el debido proceso.

**Causas Directas:**
* **Causa 1:** Informalidad operativa por omisión del Registro Nacional de Turismo (RNT) y del Reglamento de Propiedad Horizontal (RPH).
* **Causa 2:** Brecha de privacidad en portería por recopilación de datos sensibles (biometría) sin autorización expresa de Habeas Data y ausencia de avisos de videovigilancia.
* **Causa 3:** Alta litigiosidad por imposición de sanciones de convivencia sin soporte técnico (sonómetros) o cumplimiento de etapas de debido proceso.

---

## 2. Hipótesis y Preguntas Analíticas

### Hipótesis 1: Control de Rentas Cortas (RNT)
* **Supuesto:** Si los administradores de PH implementan un módulo de validación automática integrado a la portería que verifique la vigencia del RNT y el estado de paz y salvo antes del pre-registro, se reducirá la informalidad de rentas cortas y se blindará la responsabilidad civil.
* **Pregunta Analítica:** ¿Cómo impacta la validación automatizada previa del RNT en la tasa de ingresos de turistas no autorizados por mes?
* **Métrica:** `Tasa_Ingreso_No_Autorizado = (huespedes_sin_preregistro / total_huespedes_mes) * 100`

**Clasificación de Variables:**
| Variable (Estandarizada) | Tipo de Variable |
| :--- | :--- |
| `tasa_ingreso_no_autorizado` | Outcome |
| `integracion_sap_refx` | Explicativa |
| `estado_rnt` | Control |
| `paz_salvo_propietario` | Control |
| `unidad_privada` | Segmento |
| `id_anfitrion` | Segmento |

### Hipótesis 2: Habeas Data y Privacidad
* **Supuesto:** Si la administración sustituye la biometría dactilar obligatoria por un pre-registro digital con aceptación previa de Habeas Data (código QR), se mitigará el riesgo de multas de la SIC y mejorará la trazabilidad.
* **Pregunta Analítica:** ¿Cómo influye el uso del pre-registro con aceptación previa de Habeas Data por QR en el índice de cumplimiento legal en portería?
* **Métrica:** `Indice_Cumplimiento_Privacidad = (ingresos_habeas_data_firmado / total_ingresos_mes) * 100`

**Clasificación de Variables:**
| Variable (Estandarizada) | Tipo de Variable |
| :--- | :--- |
| `indice_cumplimiento_habeas_data` | Outcome |
| `flujo_consentimiento_digital` | Explicativa |
| `tipo_mecanismo_autenticacion` | Control |
| `tipo_visitante` | Segmento |

### Hipótesis 3: Litigiosidad y Convivencia
* **Supuesto:** Si la administración apoya sus procesos sancionatorios en mediciones técnicas (sonómetros certificados) y agota el debido proceso, se reducirá la impugnación de sanciones.
* **Pregunta Analítica:** ¿Cómo influye el uso de sonómetros certificados en la tasa de multas revocadas judicialmente?
* **Métrica:** `Indice_Resolutividad = (multas_ratificadas_debido_proceso / total_sanciones_impuestas) * 100`

**Clasificación de Variables:**
| Variable (Estandarizada) | Tipo de Variable |
| :--- | :--- |
| `tasa_impugnacion_sanciones` | Outcome |
| `registro_sonometro_db` | Explicativa |
| `cumplimiento_debido_proceso` | Control |
| `unidad_infractora` | Segmento |

---

## 3. Estructura de la Base de Datos (Modelo Semántico)

Para la correcta visualización e ingesta en Power BI, la base de datos cruda de las encuestas está estructurada como una Tabla de Hechos (Fact Table) plana, garantizando una columna de marca temporal (`zona_extraccion_id`) para modelado de inteligencia de tiempo y estandarizando las respuestas nulas como `N/A`.

**Muestra Estructural de la Base de Datos (Primeros Registros):**

| zona_extraccion_id | id_encuestado | tipo_actor | p01_rnt_activo | p04_biometria_obligatoria | p05_firma_habeas_data | p09_percepcion_sanciones |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 2026-09-01 08:15:22 | E001 | Residente | N/A | Sí, es obligatorio | No, nunca ha firmado | Sí, percepción subjetiva |
| 2026-09-01 09:30:10 | E002 | Anfitrión | Sí, activo y visible | No, hay alternativa | Sí, ha firmado | N/A |
| 2026-09-01 10:45:00 | E003 | Administrador | N/A | Sí, es obligatorio | No, nunca ha firmado | No, usa pruebas técnicas |
