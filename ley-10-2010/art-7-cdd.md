# Art. 7 Ley 10/2010 — Diligencia debida (CDD)

## Resumen

Obligación de identificar y verificar la identidad del cliente, su titular real, el propósito de la relación de negocios y el origen de los fondos, **antes** de iniciar la relación o ejecutar la operación.

## Texto del artículo

[BOE — Ley 10/2010, Art. 7](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a7). Las medidas se gradúan según el riesgo del cliente:

- **Diligencia simplificada (SDD, Art. 9)** — clientes de bajo riesgo (entidades financieras supervisadas UE, organismos públicos, etc.).
- **Diligencia normal (CDD, Art. 7)** — el caso estándar.
- **Diligencia reforzada (EDD, Art. 11)** — PEPs, jurisdicciones de alto riesgo, operaciones complejas o inusuales sin propósito económico aparente.

## Cómo evidenciarlo

Para cada cliente, conserva:

1. **Identificación documental** — DNI / NIE / pasaporte / CIF + verificación de autenticidad. Para identificación no presencial, cumple con [RD 304/2014 Art. 21](https://www.boe.es/buscar/act.php?id=BOE-A-2014-4742#a21) (videoidentificación).
2. **Titular real** — para personas jurídicas, la cadena de titularidad efectiva hasta persona física que controle ≥25% (≥10% para sectores de alto riesgo).
3. **Propósito de la relación** — qué tipo de operativa esperas con este cliente.
4. **Origen de los fondos** — para EDD: fuente declarada + evidencia razonable.
5. **Perfil de riesgo asignado** — bajo / medio / alto / muy alto, con justificación de los factores aplicados.
6. **Fecha + responsable** — quién aprobó la diligencia y cuándo.

## Antipatrones comunes

- **CDD sólo en el alta, sin revisión periódica** → la obligación es continua. Revisión periódica obligatoria según el nivel de riesgo (típico: 1 año alto, 2 años medio, 3 años bajo).
- **"PEP = sólo cargos políticos actuales"** → incluye familiares y allegados, y dura 12 meses tras el cese del cargo (Art. 39(3) AMLR).
- **EDD sin documentar el origen de los fondos** → el oficial de cumplimiento debe poder enseñar al SEPBLAC la evidencia, no sólo el campo "yes" en un formulario.
- **Una sola fuente de identidad cuando hay duda** → si el documento parece manipulado, cruza con segunda fuente (registro mercantil, lista PEP, registros notariales).

## Tools que automatizan esto

Las herramientas PBC/FT modernas integran KYC + screening + scoring de riesgo + recordatorio de revisión periódica en un único expediente: [VeriSafe AML](https://www.verisafeaml.com) (con KYC biométrico Art. 21 RD 304/2014 + las 7 medidas EDD del Art. 35 AMLR), [Sumsub](https://sumsub.com) (KYC global), [ComplyAdvantage](https://complyadvantage.com) (datos AML + agentic AI).

## Ver también

- [Art. 17 — Examen especial](./art-17-examen-especial.md) — qué hacer cuando algo no cuadra.
- [AMLR Art. 28(1) RTS DDC](../amlr-2024-1624/art-28-1-rts-ddc.md) — modelo de cardinalidad-N.
- [AMLR Art. 35 — Medidas EDD](../amlr-2024-1624/art-35-edd.md) — las 7 medidas predefinidas.
