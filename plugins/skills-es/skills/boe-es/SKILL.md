---
name: boe-es
description: Busca en el Boletín Oficial del Estado (BOE) con su API oficial de datos abiertos, tanto el sumario de un día como el texto consolidado y vigente de una ley, y cita el artículo exacto con enlace. Úsala cuando pregunten qué dice una ley o un artículo, qué se publicó en el BOE o cuándo entra en vigor una norma.
---

# Buscador del BOE

Responde siempre con el texto oficial, nunca de memoria: las leyes cambian. Cita el artículo y enlaza la fuente.

## API oficial (gratuita, sin clave)
| Para | Petición |
|---|---|
| Sumario de un día | `GET https://www.boe.es/datosabiertos/api/boe/sumario/AAAAMMDD` con cabecera `Accept: application/json` |
| Documento publicado | `GET https://www.boe.es/diario_boe/xml.php?id=BOE-A-AAAA-NNNNN` (XML) |
| Texto consolidado de una norma | `GET https://www.boe.es/datosabiertos/api/legislacion-consolidada/id/BOE-A-AAAA-NNNNN/texto` con `Accept: application/xml` |
| Metadatos de una norma | `GET https://www.boe.es/datosabiertos/api/legislacion-consolidada/id/BOE-A-AAAA-NNNNN/metadatos` |
| Página para el usuario | `https://www.boe.es/buscar/act.php?id=BOE-A-AAAA-NNNNN` (añade `#aNN` para ir al artículo NN) |

Usa la herramienta de lectura web disponible, o `curl`/Python en Claude Code.

## Identificadores de normas frecuentes
| Norma | Identificador |
|---|---|
| Constitución Española | BOE-A-1978-31229 |
| Ley 39/2015, Procedimiento Administrativo Común | BOE-A-2015-10565 |
| Ley 40/2015, Régimen Jurídico del Sector Público | BOE-A-2015-10566 |
| Estatuto de los Trabajadores (RDL 2/2015) | BOE-A-2015-11430 |
| Ley 37/1992 del IVA | BOE-A-1992-28740 |
| Ley 35/2006 del IRPF | BOE-A-2006-20764 |
| Ley 29/1994 de Arrendamientos Urbanos | BOE-A-1994-26003 |
| Ley 49/1960 de Propiedad Horizontal | BOE-A-1960-10906 |
| Ley 9/2017 de Contratos del Sector Público | BOE-A-2017-12902 |
| LO 3/2018 de Protección de Datos | BOE-A-2018-16673 |
| RDL 1/2007, Defensa de Consumidores | BOE-A-2007-20555 |
| Ley 7/1985, Bases de Régimen Local | BOE-A-1985-5392 |

Si la norma no está en la tabla, busca su identificador en `https://www.boe.es/buscar/` o en la web, y confírmalo con la API de metadatos.

## Cómo leer el texto consolidado
- El XML trae bloques `<bloque tipo="precepto" titulo="Artículo N">` con una o varias `<version>`.
- **La última `<version>` es la redacción vigente.** Las anteriores son históricas.
- Fíjate en la `fecha_vigencia` de la versión si el usuario pregunta por una fecha pasada.

## Respuesta
1. Respuesta directa en 1–3 frases.
2. Cita literal breve del artículo, entre comillas, con `Artículo N de <norma>` y enlace a `act.php?id=…#aN`.
3. Si hay reformas recientes o desarrollo reglamentario relevante, menciónalo.
4. No des asesoramiento jurídico personalizado: si el caso es complejo, recomienda un profesional.

Para el sumario de un día: agrupa por sección (I Disposiciones generales, II.B Oposiciones, III Otras disposiciones…) y resume lo que interese al usuario, con enlace a cada documento.
