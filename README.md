# Proyecto de Investigación: Gobernanza Turística, Control Fiduciario y Seguridad de Datos en la PH Colombiana (2026)

## 1. Generalidades del Proyecto

- **Título del Proyecto:** Gobernanza turística, control fiduciario y seguridad de datos en la PH colombiana (Vigencia 2026)
- **Entidad de Estudio:** Copropiedades Residenciales y Mixtas en Colombia
- **Muestra Estadística:** $N = 149$ encuestados reales (80 Residentes, 45 Anfitriones, 24 Administradores)
- **Nivel de Confianza:** 95% (Margen de error: 8.03%)

---

## 2. Tablero de Prioridades de Hipótesis (Metodología Design Thinking)

| Atributo / Fila | Hipótesis 1: Validación SAP/RNT | Hipótesis 2: Habeas Data QR | Hipótesis 3: Sonometría y Mediación |
| :--- | :--- | :--- | :--- |
| **Fila A: Causas** | Informalidad operativa por propietarios que ofrecen vivienda turística evadiendo el RNT y silenciando el Reglamento de Propiedad Horizontal. | Brecha de privacidad en portería por recopilación ilegal de datos sensibles (biometría dactilar obligatoria) e inexistencia de avisos visibles de videovigilancia. | Alta litigiosidad por sanciones y manuales de convivencia arbitrarios debido al vacío de idoneidad formativa en turismo del administrador tradicional. |
| **Fila B: Fase DT Origen** | Empatizar & Definir: Se consolidó el perfil fiduciario del administrador y del turista en el lienzo de Dave Gray. | Ideación & Prototipado: Se codificaron alternativas de acceso QR compatibles con las directrices SIC. | Definir & Evaluar: Se identificaron vacíos de competencia técnica en el consejo de administración. |
| **Fila C: Insight de Empatía** | El 79% de los administradores descubre el alquiler ilegal solo cuando ve turistas con maletas en la portería física sin RNT. | El 85% de los residentes se siente incómodo entregando su huella dactilar obligatoria a empresas de seguridad privada. | El 73% de las multas se caen legalmente porque se imponen por chismes y apreciaciones subjetivas sin sonómetros. |
| **Fila D: Supuesto Central** | Si implementamos la API en SAP RE-FX para validar RNT y Paz y Salvo, reduciremos las rentas cortas clandestinas. | Si sustituimos la huella por pre-registro digital QR de Habeas Data, mitigaremos el riesgo de multas de la SIC de 2000 SMMLV. | Si medimos el ruido objetivamente en decibeles y entrenamos al administrador en RUAPH, reduciremos la revocabilidad de multas. |
| **Fila E: Pregunta Analítica** | ¿Cómo varía la tasa de reserva clandestina al automatizar la verificación del RNT en el software de administración? | ¿Cuál es el efecto de suprimir la biometría obligatoria en el nivel de cumplimiento normativo ante la Superintendencia? | ¿Qué correlación existe entre el uso de sonómetros y la tasa de multas que se sostienen en los descargos fiduciarios? |
| **Fila F: Variables exactas** | 1. `tasa_ingreso_huespedes_no_autorizados`<br>2. `nivel_automatizacion_validacion_rnt`<br>3. `propietario_paz_y_salvo_financiero`<br>4. `rnt_estado_registro`<br>5. `unidad_privada_id`<br>6. `coeficiente_copropiedad` | 1. `tasa_investigaciones_quejas_sic`<br>2. `flujo_consentimiento_digital_previo`<br>3. `tiempo_registro_porteria_segundos`<br>4. `tipo_mecanismo_autenticacion_ingreso`<br>5. `copropiedad_id`<br>6. `fecha_registro_acceso` | 1. `tasa_impugnacion_sanciones_pecuniarias`<br>2. `idoneidad_acreditacion_administrador_ruaph`<br>3. `registro_ruido_objetivo_decibeles`<br>4. `cumplimiento_debido_proceso_descargos`<br>5. `unidad_infractora_id`<br>6. `reincidencia_unidad_habitacional` |
| **Fila G: Tipo de Variable** | 1. Outcome<br>2. Explicativa<br>3. Control<br>4. Control<br>5. Segmento<br>6. Control | 1. Outcome<br>2. Explicativa<br>3. Outcome Secundario<br>4. Control<br>5. Segmento<br>6. Control | 1. Outcome<br>2. Explicativa<br>3. Explicativa<br>4. Control<br>5. Segmento<br>6. Control |
| **Fila H: Cálculo / Transformación** | `COUNTIFS` en microdatos filtrando por Rol = 'Anfitrión' y Reglamento = 'No'. | `COUNTIF` en microdatos contando respuestas de 'No' en Habeas Data Firmado. | `COUNTIFS` en microdatos filtrando por impugnaciones ganadas por anfitriones frente a sanciones subjetivas. |
| **Fila I: Métrica Principal** | **Tasa de Validación Previa (TVP-VT):**<br>$\frac{\text{Reservas RNT y Paz y Salvo Validados}}{\text{Total Reservas Solicitadas}} \times 100$ | **Índice de Cumplimiento de Privacidad (ICRP):**<br>$\frac{\text{Turistas con Habeas Data Firmado}}{\text{Total Turistas Registrados}} \times 100$ | **Índice de Resolutividad de Conflictos (IRCC):**<br>$\frac{\text{Sanciones Firmes (Sostienen Descargos)}}{\text{Total Sanciones Impuestas}} \times 100$ |
| **Fila J: Horizonte SIII** | Semanas 1 a 4: Periodo de implementación de la API en el ERP SAP RE-FX. | Semanas 1 a 3: Retiro de lectores dactilares y despliegue del pre-registro QR. | Semanas 1 a 6: Habilitación de sonómetros y auditoría de debidos procesos. |
| **Fila K: Patrón Esperado** | La TVP-VT aumenta a > 95% de forma inmediata y se reduce a cero la morosidad de cartera. | Las quejas ante la SIC disminuyen a cero y el tiempo de portería baja de 180s a 30s. | La tasa de multas revocadas disminuye a < 15%, logrando un 85% de sanciones sólidas. |
| **Fila L: Condición Refutación** | TVP-VT $\le$ 60% | ICRP $\le$ 80% | IRCC $\le$ 40% |
| **Fila M: Valor Esperado Usuario** | Mayor seguridad comunitaria, control de sobrecupo (límite: 16 personas) e identificación para prevención de ESCNA. | Protección total del derecho constitucional a la intimidad y Habeas Data. | Tranquilidad acústica nocturna verificable e insonorización de fachadas (Decreto 768 de 2025). |
| **Fila N: Riesgo si Falsa** | Evasión tributaria y de seguros, sobreexplotación de zonas comunes y multas de hasta 3 SMMLV del MinCIT. | Multas millonarias de la SIC de hasta 2.000 SMLMV e inoperancia probatoria de CCTV. | Invasión de tutelas por violación al libre desarrollo de la personalidad y mascotas (Sentencia T-199 de 2026). |
| **Fila O: Acción si Confirma** | Protocolizar reforma del reglamento en asamblea calificada (70% coeficientes) y bloquear API a morosos. | Adquirir terminales QR y registrar bases de datos ante el RNBD de la SIC. | Implementar el RUAPH permanente y exigir póliza de responsabilidad civil extracontractual. |
| **Fila P: Acción si Refuta** | Modificar reglamento interno para restringir visitas no registradas con 2 días de antelación. | Habilitar citofonía virtual y firmas con clave OTP temporal en la aplicación. | Vincular un conciliador externo o mediador especializado del Centro de Conciliación de la Alcaldía. |
| **Fila Q: Experimento Analítico** | `SELECT COUNT(reserva_id) FROM reservas WHERE rnt_validado = TRUE;` | `SELECT AVG(tiempo_porteria_seg) FROM accesos GROUP BY tipo_mecanismo;` | `SELECT COUNT(sancion_id) FROM sanciones WHERE debido_proceso_ok = TRUE;` |
| **Fila R: Estado** | **Validado** | **Activo** | **Validado** |

---

## 3. Ficha Técnica de Indicadores (Metodología Marco Lógico)

| Metadato / Fila | Indicador 1: Tasa Validación (TVP-VT) | Indicador 2: Cumplimiento Privacidad (ICRP) | Indicador 3: Resolutividad Convivencia (IRCC) |
| :--- | :--- | :--- | :--- |
| **Fila A: Supuestos Centrales** | Asumimos que si los anfitriones deben validar automáticamente el RNT y la cartera en SAP RE-FX, se reducirá la clandestinidad. | Asumimos que si implementamos un registro QR digital de Habeas Data, se erradicará el uso dactilar obligatorio. | Asumimos que si el administrador se profesionaliza ante el RUAPH y se usan sonómetros homologados, las multas respetarán el debido proceso. |
| **Fila B: Acción (¿Qué hago?)** | Establecer la verificación automática de vigencia del RNT e integrar pasarelas de pago de expensas en el pre-registro. | Suprimir dispositivos de huella dactilar en portería y habilitar terminales móviles para lectura QR. | Capacitar al administrador en legislación turística colombiana y dotar con sonómetro calibrado ONAC. |
| **Fila C: Método (¿Cómo lo hago?)** | A través de una API que conecta el ERP de la PH (SAP/RE-FX) con Confecámaras en tiempo real. | Enviando un enlace cifrado al huésped por correo/WhatsApp para firmar el consentimiento antes de emitir QR. | Medición objetiva del ruido (en decibeles) en la puerta de la unidad y plazos escritos de descargos. |
| **Fila D: Propósito (¿Para qué?)** | Eximir al administrador de multas fiduciarias de hasta 3 SMMLV y preservar el estado financiero de bienes comunes. | Blindar a la copropiedad de investigaciones de la SIC y multas de hasta 2.000 SMLMV. | Reducir la litigiosidad por tutelas por debido proceso e inhabilitar prohibición arbitraria de mascotas. |
| **Fila E: Aspecto a Medir** | Proporción de unidades turísticas operando con reglamento de PH compatible y RNT vigente. | Proporción de usuarios que ingresan con registro digital auditable y consentimiento firmado. | Proporción de multas por perturbación acústica o convivencia que resisten impugnaciones. |
| **Fila F: Público Objetivo** | Anfitriones y propietarios de vivienda turística en copropiedades residenciales colombianas. | Turistas, huéspedes nacionales e internacionales, visitantes, residentes y personal de seguridad. | Residentes afectados por perturbación de tranquilidad y anfitriones sancionados. |
| **Fila G: Dimensión** | Eficacia Operativa y Control de Riesgo Fiduciario. | Eficacia Legal y Cumplimiento Normativo (Habeas Data). | Eficacia Convivencial y Debido Proceso (Rigor Constitucional). |
| **Fila H: Nombre Indicador** | Tasa de Validación Previa de Vivienda Turística (TVP-VT) | Índice de Cumplimiento de Registro de Privacidad (ICRP) | Índice de Resolutividad de Conflictos de Convivencia (IRCC) |
| **Fila I: Numerador (Variable Y)** | 16 (Anfitriones con reglamento en regla) | 9 (Respuestas cumplidoras en la base) | 12 (Sanciones objetivas validadas) |
| **Fila J: Denominador (Población)** | 45 (Total Anfitriones) | 149 (Total Encuestados) | 45 (Total Anfitriones Sancionables) |
| **Fila K: Fórmula Matemática** | `=(Numerador / Denominador) * 100` | `=(Numerador / Denominador) * 100` | `=(Numerador / Denominador) * 100` |
| **Fila L: Prueba de Estrés** | Fallo temporal del RNT de Confecámaras o corte de energía local que obligue al libro físico. | Huéspedes extranjeros sin datos móviles en portería o fallas en el envío de correos con QR. | Disputas sobre calibración del sonómetro u obstrucción del infractor a recibir notificaciones. |
| **Fila M: Tipo** | Tasa porcentual | Tasa porcentual | Tasa porcentual |
| **Fila N: Frecuencia** | Semanal (primer mes de implementación), mensual de ahí en adelante. | Quincenal (etapa de transición dactilar a QR), mensual en régimen ordinario. | Mensual: Coincidiendo con las sesiones ordinarias del Consejo de Administración. |
| **Fila O: Fuente de Datos** | Logs transaccionales de SAP RE-FX cruzados con registros de portería. | Servidor de base de datos cifrada de firmas de consentimiento digital auditable por la SIC. | Libro de actas de asamblea general, comités de convivencia y registro de sonómetros. |
| **Fila P: Línea Base Actual** | **35.56%** | **6.04%** | **26.67%** |
| **Fila Q: Patrón Esperado (Meta)** | **100% (1.0)** | **100% (1.0)** | **85% (0.85)** |
| **Fila R: Condición Refutación** | $\le$ 60% (0.6) | $\le$ 80% (0.8) | $\le$ 40% (0.4) |
