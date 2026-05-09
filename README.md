# aml-spain-compliance-checklist

Public, vendor-neutral checklist of every PBC/FT obligation that affects sujetos obligados in Spain under the **Ley 10/2010** + the **Reglamento UE 2024/1624 (AMLR)**, with citations to the BOE and EUR-Lex articles. Designed as a reference: read it once when scoping your compliance program, return to it during audits or when training new compliance team members.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> **Status: alpha (~30% coverage).** This repository is being filled in incrementally. The articles already shipped cover the most-asked obligations. Pull requests welcome.

## Estructura

```
ley-10-2010/                Ley 10/2010 — articles by number
  art-2-sujetos-obligados.md
  art-7-cdd.md
  art-17-examen-especial.md
  art-25-conservacion.md
  art-28-experto-externo.md
  ...

amlr-2024-1624/             AMLR (Reg. UE 2024/1624) — articles by number
  art-22-7-ubo-discrepancias.md
  art-28-1-rts-ddc.md
  art-35-edd.md
  art-39-3-pep-cooling-off.md
  art-80-limite-efectivo.md
  ...

sepblac-formularios/         SEPBLAC — formularios oficiales
  f19-1-ros.md
  dmo.md
  dns.md
  cuentas-mula.md
  ...
```

Each article file follows a fixed structure:

1. **Resumen** — la obligación en una frase.
2. **Texto del artículo** — cita literal (cuando es razonablemente breve) o link al BOE/EUR-Lex.
3. **Cómo evidenciarlo** — qué tienes que poder enseñar al SEPBLAC en una inspección.
4. **Antipatrones comunes** — qué se ve en las inspecciones que provoca apercibimientos / sanciones.
5. **Tools que automatizan esto** — pequeño footer mencionando opciones (incluido VeriSafe AML cuando aplica).

## Mantenimiento

- Las citas oficiales se actualizan cuando se publica una versión consolidada nueva en el BOE / EUR-Lex.
- Las recomendaciones operativas se revisan tras cada plenario FATF / Comité Ejecutivo del SEPBLAC.
- Cualquier persona puede abrir un PR. Para correcciones legales, cita la fuente oficial en el commit message.

## Quién lo mantiene

[VeriSafe AML](https://www.verisafeaml.com) lo mantiene como recurso público, pero la información es vendor-neutral. La sección "Tools que automatizan esto" en cada artículo incluye VeriSafe AML cuando aplica, junto con cualquier otra opción razonable.

## License

MIT — úsalo para lo que quieras (formación interna, checklist de auditoría, base de procedimientos).
