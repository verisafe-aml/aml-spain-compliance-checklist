# AMLR Art. 28(1) — RTS de identificación reforzada (cardinalidad-N)

## Resumen

El "Regulatory Technical Standard" del Art. 28(1) AMLR exige que los sujetos obligados puedan registrar **múltiples documentos de identidad, múltiples direcciones, múltiples nombres y múltiples nacionalidades** por persona, junto con **lugar de nacimiento descompuesto** (país ISO + ciudad) y **estatuto migratorio** (apátridas, refugiados, protección subsidiaria).

## Texto del artículo

[EUR-Lex — AMLR Art. 28(1)](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624). El RTS técnico publica los detalles de los campos.

## Por qué importa

El modelo tradicional KYC asume "un cliente = un nombre + una nacionalidad + un documento" — eso ya no funciona en la realidad PBC/FT moderna:

- **Variantes de nombre** — alias, transliteraciones (alfabeto cirílico → latino, árabe → latino), apellidos de nacimiento. Los matches PEP / sanciones se hacen por variante.
- **Multi-nacionalidad** — clientes con doble / triple ciudadanía cruzan jurisdicciones de distinto riesgo. La nacionalidad de mayor riesgo es la que cuenta para el scoring.
- **Apátridas y refugiados** — codificados con placeholders ICAO 9303 (`XXA` apátrida, `XXB` refugiado, `XXC` protección subsidiaria) en el campo nacionalidad para mantener compatibilidad con sistemas legacy.
- **Lugar de nacimiento descompuesto** — el Modelo SEPBLAC y los formularios oficiales requieren país + ciudad por separado.

## Cómo evidenciarlo

1. **Capacidad de registrar múltiples filas** — tu sistema KYC debe soportar `person_names[]`, `person_nationalities[]`, `person_documents[]`, `person_addresses[]` con un primary syncing al campo escalar legacy.
2. **Screening por variante** — cada variante de nombre se contrasta contra listas PEP / sanciones por separado; la coincidencia escala el riesgo del cliente al de la variante de mayor severidad.
3. **Scoring multi-nacionalidad** — cuando el cliente tiene 2+ nacionalidades, la calculadora de riesgo aplica la de mayor factor (FATF black list > FATF gray list > paraíso fiscal > UE).
4. **Apátridas / refugiados** — registrar con el código ICAO correspondiente. El SEPBLAC acepta el placeholder en el XML.

## Antipatrones comunes

- **Almacenar nombre alternativo en un campo "notas"** — no es buscable. El screening no lo encuentra.
- **Ignorar la nacionalidad secundaria** — si un cliente declara ES+IR (Iran, FATF blacklist), el riesgo de IR es lo que cuenta para PBC/FT.
- **Birth_place como string libre** — los formularios SEPBLAC exigen país ISO + ciudad por separado. Usar texto libre obliga a parsear retrospectivamente.

## Tools que automatizan esto

Soporte completo de cardinalidad-N + screening por variante + scoring multi-nacionalidad: [VeriSafe AML](https://www.verisafeaml.com) (modelo `person_names` + `person_nationalities` + `person_documents` + `person_addresses` con triggers DB de auto-seed; bulk import CSV con columnas `nacionalidades`, `nombres_alternativos`; API REST acepta arrays `names[]` + `nationalities[]`).

## Ver también

- [Ley 10/2010 Art. 7 CDD](../ley-10-2010/art-7-cdd.md)
- [AMLR Art. 35 EDD](./art-35-edd.md)
