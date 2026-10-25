---
name: calendario-fiscal-es
description: Indica qué modelos tributarios de la AEAT debe presentar un autónomo o una pyme en España según su actividad y en qué plazos, y crea recordatorios (.ics) para su calendario. Úsala cuando pregunten por obligaciones fiscales, trimestres, el 303, el 130, el 111, el 115, el 390, el 347 o fechas de Hacienda.
---

# Calendario fiscal del autónomo y la pyme (AEAT)

No eres asesor fiscal: das la orientación general y recomiendas confirmarla con la gestoría o en la sede de la AEAT. Los territorios forales (País Vasco y Navarra) tienen haciendas propias; avisa si el usuario es de allí.

## 1. Perfil
Pregunta solo lo que falte:
- Forma: autónomo persona física o sociedad.
- Régimen de IRPF: estimación directa (simplificada o normal) o módulos.
- IVA: régimen general, recargo de equivalencia (comercio minorista), exento.
- ¿Tiene trabajadores o paga a profesionales con retención?
- ¿Alquila un local u oficina a un particular o empresa con retención?
- ¿Opera con empresas de otros países de la UE?
- ¿Factura más del 70 % a empresas o profesionales que le retienen?

## 2. Modelos habituales
| Modelo | Quién | Periodicidad |
|---|---|---|
| 303 IVA | Casi todos los que facturan con IVA | Trimestral |
| 390 Resumen anual IVA | Quien presenta el 303 (salvo exoneraciones) | Anual |
| 130 Pago fraccionado IRPF | Autónomos en estimación directa. **No** si más del 70 % de los ingresos llevan retención | Trimestral |
| 131 Pago fraccionado IRPF | Autónomos en módulos | Trimestral |
| 111 Retenciones de trabajo y profesionales | Quien tiene nóminas o paga facturas con retención | Trimestral (mensual si es gran empresa) |
| 190 Resumen anual del 111 | Quien presenta el 111 | Anual |
| 115 Retenciones de alquileres | Quien paga un alquiler de local con retención | Trimestral |
| 180 Resumen anual del 115 | Quien presenta el 115 | Anual |
| 349 Operaciones intracomunitarias | Quien compra o vende a empresas de la UE | Trimestral (mensual según volumen) |
| 347 Operaciones con terceros | Quien tenga operaciones de más de 3.005,06 € con un mismo tercero no declaradas en otros modelos | Anual |
| 100 Renta | Persona física | Anual |
| 200 Impuesto sobre Sociedades / 202 pagos fraccionados | Sociedades | Anual / abril, octubre, diciembre |

## 3. Plazos generales
| Periodo | Plazo |
|---|---|
| 1T | del 1 al 20 de abril |
| 2T | del 1 al 20 de julio |
| 3T | del 1 al 20 de octubre |
| 4T | del 1 al 30 de enero del año siguiente |
| Resúmenes anuales 390, 190, 180 | hasta el 30–31 de enero |
| 347 | febrero |
| Renta | normalmente de principios de abril al 30 de junio |
| Impuesto sobre Sociedades | 25 días naturales tras los seis meses posteriores al cierre (julio, si el ejercicio coincide con el año natural) |

Reglas:
- Si el último día cae en sábado, domingo o festivo nacional, el plazo pasa al siguiente día hábil.
- Con domiciliación bancaria el plazo termina unos días antes (habitualmente 5).
- Comprueba siempre el calendario del año en curso en la sede electrónica de la AEAT (sede.agenciatributaria.gob.es → Calendario del contribuyente). Si tienes acceso web, consúltalo antes de dar fechas concretas.

## 4. Entrega
1. Lista personalizada: modelo → qué es en una frase → próximas fechas.
2. Si lo pide, un archivo `.ics` con un evento por vencimiento y aviso 5 días antes. Genéralo con código: un VEVENT por fecha, `DTSTART;VALUE=DATE`, `SUMMARY:Modelo 303 (3T)`, y `VALARM` con `TRIGGER:-P5D`.
3. Una línea final con lo que conviene confirmar con su gestoría.
