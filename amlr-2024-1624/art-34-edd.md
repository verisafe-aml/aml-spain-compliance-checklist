# AMLR Art. 34 — Medidas de diligencia debida reforzada (EDD)

## Resumen

Cuando el riesgo es alto (PEP, jurisdicción de alto riesgo, operación inusual, sector de alto riesgo, etc.), el sujeto obligado debe aplicar **medidas reforzadas** además de la diligencia normal. El Art. 34 AMLR define **7 medidas predefinidas** que deben registrarse explícitamente.

## Texto del artículo

[EUR-Lex — AMLR Art. 34](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624). Las 7 medidas (resumen):

1. **Información adicional sobre el cliente** — actividad económica detallada, propósito específico de la operación, fuentes de riqueza más allá de las declaradas en CDD.
2. **Información adicional sobre el titular real** — verificación cruzada con registros oficiales, evidencia de la cadena societaria.
3. **Información adicional sobre el origen de los fondos y de la riqueza** — documentación bancaria, contratos, declaraciones fiscales, herencias, ventas de activos.
4. **Información adicional sobre el propósito y la naturaleza de la relación** — narrativa específica sobre la operativa esperada.
5. **Aprobación por la dirección** — la decisión de iniciar/continuar la relación EDD se eleva al órgano directivo (compliance officer + miembro del consejo según Art. 11 AMLR).
6. **Monitorización reforzada** — frecuencia de revisión más alta, umbrales de alerta más estrictos.
7. **Limitación de productos / canales** — restringir el acceso del cliente a productos de bajo riesgo o canales con mayor trazabilidad.

## Cuándo aplicar EDD

- Cliente o titular real es PEP (incluyendo cooling-off de 12 meses tras el cese — Art. 45(2)).
- Operación con persona o jurisdicción de alto riesgo (FATF lista negra/gris, paraíso fiscal).
- Cliente con perfil de riesgo "alto" o "muy alto" según tu calculadora.
- Operación compleja o inusual sin propósito económico aparente.
- Servicios de banca privada / wealth management con clientes high-net-worth.
- Sector con riesgo intrínseco elevado (juego, crypto, arte, joyería, inmobiliaria de lujo).

## Cómo evidenciarlo

1. **Disparador documentado** — qué activó la EDD (PEP detectado en screening, cliente declarado VIP, alerta de monitorización con score X).
2. **Las 7 medidas aplicadas** — registro explícito de cuáles aplicaste y cuáles descartaste (con motivo).
3. **Aprobación de la dirección** — firma electrónica o registro nominal del oficial de cumplimiento + miembro del consejo si aplica.
4. **Monitorización reforzada activa** — confirmación de que las reglas de monitorización con umbrales más estrictos están activas para ese cliente.
5. **Revisión periódica acelerada** — nuevo `next_review_date` calculado con la frecuencia EDD.

## Antipatrones comunes

- **Marcar "EDD" sin documentar las 7 medidas** — el SEPBLAC quiere ver qué hiciste concretamente, no un checkbox genérico.
- **EDD se aplica al alta y nunca más** — la EDD es un estado del cliente, no un evento puntual. La monitorización continua sigue siendo reforzada.
- **Aprobación informal por email** — el AMLR exige aprobación documentada de la dirección. Email no firmado no cumple.

## Tools que automatizan esto

Las 7 medidas EDD predefinidas registrables en cada revisión KYC + monitorización reforzada con umbrales por persona: [VeriSafe AML](https://www.verisafeaml.com) (campo `edd_measures_applied TEXT[]` en `kyc_reviews`).

## Ver también

- [Ley 10/2010 Art. 7 CDD](../ley-10-2010/art-7-cdd.md)
- [AMLR Art. 45(2) PEP cooling-off](./art-45-2-pep-cooling-off.md)
- [AMLR Art. 11 Compliance Officer](./art-11-compliance-officer.md) (pendiente)
