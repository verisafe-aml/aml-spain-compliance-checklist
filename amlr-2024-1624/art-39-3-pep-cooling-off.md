# AMLR Art. 39(3) — Período de enfriamiento PEP (12 meses)

## Resumen

Cuando una **Persona Políticamente Expuesta (PEP) cesa en el cargo**, las medidas de diligencia reforzada (EDD) **siguen aplicando durante 12 meses**. El factor de riesgo se gradúa, no se elimina al instante.

## Texto del artículo

[EUR-Lex — AMLR Art. 39(3)](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624). Cambio respecto al régimen anterior, donde algunas interpretaciones permitían retirar la condición PEP el día siguiente al cese.

## Cómo evidenciarlo

1. **Campo `pep_ended_at`** en el expediente del cliente — fecha exacta de cese del cargo.
2. **Cálculo automático del cooling-off** — durante 12 meses tras `pep_ended_at`, aplicar 50% del factor de riesgo PEP (típicamente 50% de 40 puntos = 20 puntos).
3. **Re-evaluación automática a los 12 meses** — el sistema baja el factor a 0 sólo cuando han pasado 12 meses + el sujeto ha confirmado el cese (no se asume).
4. **Trazabilidad** — quién registró el cese, sobre qué evidencia (publicación oficial, BOE, fuente de prensa).

## Antipatrones comunes

- **Retirar PEP el día del cese** — incumple el AMLR. La inspección ve "cliente fue PEP el lunes, normal el martes" y eso es una falta.
- **Reactivar PEP automáticamente cuando vuelve a cargo** — bien, pero requiere monitorización proactiva del cliente (no esperar a que el cliente lo declare).
- **Cooling-off de menos de 12 meses** — algunos sistemas usan 6 meses por inercia del régimen pre-AMLR. 12 meses es lo correcto desde 2024.

## Tools que automatizan esto

Cooling-off automático con factor decremental: [VeriSafe AML](https://www.verisafeaml.com) (campo `pep_ended_at` + factor configurable `pep_cooling_off_points` por defecto 50% de los puntos PEP durante 12 meses; help article: [`/help/personas-kyc/personas-politicamente-expuestas`](https://www.verisafeaml.com/help/personas-kyc/personas-politicamente-expuestas)).

## Ver también

- [AMLR Art. 35 EDD](./art-35-edd.md) — qué medidas aplicar mientras dura el cooling-off.
- [Ley 10/2010 Art. 14 — PEPs](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a14)
