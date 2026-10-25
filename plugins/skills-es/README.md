# SkillsES

Skills en español para trabajar en España con Claude Code, Claude y Cowork. Cada skill aplica la normativa y las costumbres españolas y, cuando un dato es decisivo, consulta la fuente oficial (BOE, AEAT) en lugar de responder de memoria.

## Skills incluidas
- **Correos profesionales en español** (`correo-formal-es`): Redacta y revisa correos de trabajo con el tono y las fórmulas que se usan en España: peticiones, reclamaciones, seguimientos, disculpas y negativas.
- **Presupuestos para autónomos y pymes** (`presupuesto-es`): Genera presupuestos claros con IVA, retención de IRPF, condiciones de pago y validez, listos para enviar en Word o PDF.
- **Calendario fiscal del autónomo** (`calendario-fiscal-es`): Te dice qué modelos de Hacienda te tocan según tu actividad y cuándo vencen, con recordatorios en tu calendario.
- **Buscador del BOE** (`boe-es`): Consulta el sumario diario y la legislación consolidada del BOE con la API oficial y cita el artículo exacto.

## Instalación
En Claude Code:

```
/plugin install skills-es --marketplace CBGRStudios/skills-es
```

o en la terminal: `claude plugin marketplace add CBGRStudios/skills-es` y después `claude plugin install skills-es@skills-es`.

## Uso
Pide la tarea en lenguaje normal (por ejemplo: «Escribe un correo a un cliente que lleva 45 días sin pagar la factura 2026-031, firme pero cordial.») y Claude cargará la skill adecuada. También puedes invocarlas con `/skills-es:<skill>`.

Para generar documentos Word desde Claude Code, algunas skills usan `scripts/a_docx.py`, que necesita `pip install python-docx`.

Las skills ayudan a redactar y consultar; no sustituyen el asesoramiento profesional. Proyecto independiente, no afiliado a Anthropic. Más información: https://skillses.cbgrstudios.com
