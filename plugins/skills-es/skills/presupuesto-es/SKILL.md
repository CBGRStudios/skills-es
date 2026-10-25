---
name: presupuesto-es
description: Genera presupuestos profesionales en español para autónomos y pymes de España, con partidas, IVA, retención de IRPF, condiciones de pago y validez, en Word o PDF. Úsala cuando el usuario pida hacer, calcular o revisar un presupuesto u oferta económica.
---

# Presupuestos para autónomos y pymes (España)

Un presupuesto es una oferta, no una factura. No le pongas número de factura ni lo llames factura.

## Datos que necesitas
Pide solo lo que falte:
- **Emisor**: nombre o razón social, NIF, dirección, email y teléfono.
- **Cliente**: nombre, NIF (si es empresa) y dirección.
- **Partidas**: descripción, cantidad, unidad y precio unitario sin IVA.
- **Tipo de IVA**:
  - 21 % general.
  - 10 % reducido (p. ej., obras de renovación en vivienda particular con requisitos, hostelería).
  - 4 % superreducido.
  - Exento (art. 20 Ley 37/1992: p. ej., formación reglada, sanidad). Si dudas, pregunta y no inventes.
- **Retención de IRPF**: solo si el emisor es profesional (persona física) y el cliente es empresa o autónomo:
  - 15 % general.
  - 7 % en el año de inicio de actividad y los dos siguientes.
  - Nunca a particulares.
- **Validez**: por defecto 30 días.
- **Forma de pago**: por defecto transferencia, 50 % al aceptar y 50 % a la entrega.

## Cálculos
- Importe de cada partida = cantidad × precio unitario, redondeado a 2 decimales.
- Base imponible = suma de las partidas (si hay varios tipos de IVA, una base por tipo).
- Cuota de IVA = base × tipo.
- Retención = base × % de IRPF (se resta).
- **Total = base + IVA − retención.**

Haz las cuentas con código (Python) cuando haya más de tres partidas y comprueba que cuadran antes de entregar.

## Estructura del documento
1. Título "PRESUPUESTO", número (`P-2026-014`) y fecha.
2. Datos del emisor y del cliente.
3. Objeto del presupuesto en una frase.
4. Tabla: Concepto | Cantidad | Precio unit. | Importe.
5. Resumen: Base imponible, IVA (x %), Retención IRPF (x %) si aplica, **TOTAL**.
6. Condiciones:
   - validez;
   - plazo de ejecución o entrega;
   - forma y calendario de pago;
   - qué no incluye;
   - cómo se gestionan los cambios de alcance (presupuesto adicional).
7. Aceptación: "Conforme, el cliente", con fecha y firma.

Importes con formato español: `1.250,00 €`.

## Entrega
- Si hay una herramienta o skill de Word, crea el .docx con ella.
- Si no, escribe el presupuesto en Markdown y conviértelo con el script `scripts/a_docx.py` de esta skill (`python scripts/a_docx.py presupuesto.md presupuesto.docx`; requiere `pip install python-docx`).
- Ofrece también la versión en PDF si el usuario la necesita.

Termina con un resumen de una línea: total, IVA aplicado y si lleva retención.
