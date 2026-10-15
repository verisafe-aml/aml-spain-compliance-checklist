# AMLR Art. 45(2) — Ex-PEP: medidas tras el cese (en España, 2 años)

## Resumen

Cuando una **Persona Políticamente Expuesta (PEP) cesa en el cargo**, las medidas de diligencia reforzada no se retiran el día del cese. El AMLR exige mantenerlas **al menos 12 meses y mientras persista el riesgo** (art. 45.2). En España, la **Ley 10/2010 (art. 14.9)** es hoy más estricta: obliga a **seguir aplicándolas durante 2 años**; transcurrido ese plazo, se aplican en función del riesgo.

## Texto del artículo

- [EUR-Lex — AMLR Art. 45(2)](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624).
- [Ley 10/2010 Art. 14.9](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a14): «continuarán aplicando las medidas previstas en este artículo por un periodo de dos años».

«Preparado para el AMLR» significa hacer además lo que añade el AMLR, nunca sustituir la regla española vigente más estricta por la futura más laxa.

## Cómo evidenciarlo

1. **Campo `pep_ended_at`** en el expediente del cliente — fecha exacta de cese del cargo.
2. **Mismas medidas durante 2 años** — puntos PEP completos, riesgo al menos alto y diligencia reforzada mientras no hayan pasado 2 años desde `pep_ended_at`.
3. **Revisión al final del periodo** — a los 2 años, valorar si el riesgo persiste (AMLR art. 45.2) antes de bajar el nivel; no bajarlo de forma automática.
4. **Trazabilidad** — quién registró el cese, sobre qué evidencia (publicación oficial, BOE, fuente de prensa).

## Antipatrones comunes

- **Retirar PEP el día del cese** — incumple la Ley 10/2010 y el AMLR.
- **Aplicar solo los 12 meses del AMLR en España** — el art. 14.9 de la Ley 10/2010 exige 2 años y sigue vigente.
- **Reducir los puntos de riesgo durante el periodo** — el art. 14.9 exige las mismas medidas, no unas atenuadas.

## Tools que automatizan esto

[VeriSafe AML](https://www.verisafeaml.com) (campo `pep_ended_at`; durante 2 años tras el cese mantiene los puntos PEP completos y la diligencia reforzada; help article: [`/help/personas-kyc/personas-politicamente-expuestas`](https://www.verisafeaml.com/help/personas-kyc/personas-politicamente-expuestas)).

## Ver también

- [AMLR Art. 34 EDD](./art-34-edd.md) — qué medidas aplicar mientras dura el periodo.
- [Ley 10/2010 Art. 14 — PEPs](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a14)
