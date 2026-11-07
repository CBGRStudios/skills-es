---
name: alquiler-vivienda-es
description: Redacta, revisa o explica contratos de alquiler de vivienda habitual en España según la Ley de Arrendamientos Urbanos (LAU) vigente, con duración, prórrogas, fianza, actualización de la renta con el IRAV, gastos, reparaciones, desistimiento y zonas tensionadas. Úsala cuando un propietario o un inquilino pregunte por su contrato de alquiler, quiera hacer uno, revisar sus cláusulas, subir la renta, recuperar la fianza o dejar el piso.
---

# Contrato de alquiler de vivienda (LAU)

No eres abogado: das orientación general y recomiendas a un profesional cuando hay conflicto o mucho dinero en juego. Aplica a **vivienda habitual** (Título II LAU). Los alquileres de temporada y de local se rigen por otras reglas: avisa si es el caso.

## 0. Antes de dar un plazo: la LAU está cambiando
Verificado a **08/11/2026** en el texto consolidado del BOE (BOE-A-1994-26003, actualizado el 07/10/2026):
- En otoño de 2026 se aprobaron varios **reales decretos-ley** que modifican la LAU. El Congreso **derogó** el 26/2026 y el 27/2026 en octubre. El **28/2026** cambia la prórroga tácita (art. 10) **con efectos desde el 15/11/2026**, y el **29/2026** toca otros artículos.
- Un decreto-ley que el Congreso no convalida deja de aplicarse. Por eso, **si tienes acceso web, consulta el art. 10 en el BOE antes de responder** y di qué redacción aplicas y por qué. Si no puedes consultarlo, da las dos redacciones y dilo claramente.

## 1. Datos que necesitas
Pregunta solo lo que falte:
- ¿Eres propietario o inquilino? ¿Fecha de firma del contrato?
- Propietario persona física o persona jurídica (empresa).
- ¿Gran tenedor? ¿Está la vivienda en una zona de mercado residencial tensionado?
- Renta, fianza, garantías adicionales y quién paga cada gasto.

## 2. Reglas clave (texto literal del BOE a 07/10/2026)
| Tema | Regla | Artículo |
|---|---|---|
| Duración mínima | Libre, pero si es menor se prorroga por años hasta **5 años** (**7** si el propietario es persona jurídica). El inquilino puede no renovar avisando **30 días** antes | 9.1 |
| Prórroga tácita (redacción vigente hasta el 14/11/2026) | Cumplido el mínimo, si nadie avisa (propietario **4 meses** antes, inquilino **2 meses**), se prorroga por años hasta **3 años más** | 10.1 |
| Prórroga tácita (RDL 28/2026, desde el 15/11/2026, **si sigue en vigor**) | Preaviso del propietario **6 meses** e inquilino **2 meses**; prórrogas sucesivas de **5 años** (7 si es persona jurídica); si el propietario no prorroga, indemniza con el mayor de **12 mensualidades** o **una por año** de residencia | 10.1 |
| Desistimiento del inquilino | Tras **6 meses**, avisando con **30 días**. **No** genera indemnización para el propietario | 11.1 y 11.3 |
| Actualización de la renta | Solo en cada aniversario y **solo si se pactó**. Sin pacto, no se actualiza. Nunca por encima de la variación del **IRAV**. Se cobra desde el mes siguiente a notificarla | 18.1 y 18.2 |
| Zona tensionada | La renta del nuevo contrato no puede superar la del contrato anterior (últimos 5 años) actualizada, salvo excepciones de hasta un 10 %. Con gran tenedor, tope del índice de precios de referencia | 17.6 y 17.7 |
| Gestión y formalización | Los gastos de **inmobiliaria y de formalización** no se pueden repercutir al inquilino de ninguna forma | 20.2 |
| Reparaciones | Las necesarias para la habitabilidad, el propietario. Las **pequeñas por desgaste del uso ordinario**, el inquilino | 21.1 y 21.4 |
| Fianza | **Una mensualidad** en metálico. No se actualiza los primeros 5 años (7 si es persona jurídica) | 36.1 y 36.2 |
| Garantías adicionales | Como máximo **dos mensualidades** de renta | 36.5 |
| Por escrito | Cualquiera de las partes puede exigir formalizarlo por escrito | 37 |
| Cláusulas nulas | Las que empeoran lo que la ley garantiza al inquilino se tienen por no puestas | 6 |

La fianza se deposita en el organismo de la comunidad autónoma: indica que lo compruebe en la web de su comunidad.

## 3. Tareas
- **Revisar un contrato:** lista cada cláusula contraria a la tabla, con el artículo, y propón la redacción correcta.
- **Redactar un contrato:** partes, vivienda (dirección, referencia catastral, cédula de habitabilidad si aplica), duración, renta y forma de pago, actualización (IRAV o ninguna), fianza y garantías, gastos, reparaciones, inventario, cláusulas de desistimiento y notificaciones. Marca con `[COMPLETAR]` lo que falte.
- **Una duda concreta** (¿me pueden subir la renta?, ¿me devuelven la fianza?, ¿puedo irme antes?): responde en tres líneas con el artículo y lo siguiente que debe hacer.
- **Comunicación al otro:** redacta el escrito (preaviso, notificación de actualización, petición de fianza), recomendando burofax o un medio con acuse.

## 4. Entrega
- En Claude Code, si pide un documento: escribe en Markdown y conviértelo con `scripts/a_docx.py` de esta skill (`python scripts/a_docx.py contrato.md contrato.docx`, requiere `pip install python-docx`).
- Termina siempre con la fecha de verificación de la norma (08/11/2026) y una línea con lo que conviene confirmar con un profesional.
