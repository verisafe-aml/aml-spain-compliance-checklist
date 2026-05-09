# Cuentas Mula — Reporting de cuentas mula al SEPBLAC

## Resumen

Comunicación específica al SEPBLAC sobre cuentas detectadas como **cuentas mula** (cuentas usadas por terceros para mover fondos de origen ilícito). Aplica principalmente a entidades financieras, EMIs, entidades de pago y proveedores de servicios crypto.

## Cuándo presentarlo

- Cuando el sujeto obligado detecta una cuenta con patrón mula tras los procedimientos de monitorización transaccional.
- **Sin demora** — la rapidez es crítica porque la mula puede vaciarse en horas.

## Qué es una cuenta mula (patrones)

- **Bajo saldo medio** + recibe transferencias inusuales por importe alto.
- **Re-emite los fondos** en cuestión de horas o pocos días.
- **Ratio entrada/salida ~1** — el saldo final es cercano a cero.
- **Cuenta nueva** — la antigüedad de la cuenta vs el primer movimiento alto suele ser baja.
- **Titular sin perfil económico** que justifique el movimiento — estudiantes, jubilados, personas con renta declarada baja.

## Estructura del XML

- **XSD 2.4** (la versión vigente del SEPBLAC para Cuentas Mula).
- Estructura: cuenta + titulares + movimientos sospechosos + narrativa breve.

## Cómo presentarlo

- Vía **CTL** del SEPBLAC.
- En formato XML conforme al **XSD 2.4**.

## Cómo evidenciarlo

1. **Detección** — qué regla del motor de monitorización disparó la sospecha + score asociado.
2. **Investigación** — análisis de los movimientos del período, perfil del titular, contraparte de los movimientos.
3. **Decisión del OCI** — confirmar la calificación como cuenta mula.
4. **Acción inmediata** — bloqueo precautorio de la cuenta + comunicación al SEPBLAC + (opcional) ROS si hay sospecha clara de blanqueo en el origen de los fondos.
5. **Comunicación al cliente** — el AMLR + Ley 10/2010 limitan qué puedes decir al titular (anti-tipping-off).

## Antipatrones comunes

- **Detectar y no actuar rápido** — las mulas se vacían en 24-48 horas. La detección sin acción inmediata es prácticamente inútil.
- **Notificar al titular antes de presentar** — tipping-off (Art. 24 Ley 10/2010 + Art. 54 6AMLD). Ilegal.
- **Confundir mula con cliente legítimo con operativa puntual rara** — el patrón mula es persistente (ratio + frecuencia), no puntual.

## Tools que automatizan esto

Detección automática del patrón + generación nativa Cuentas Mula XSD 2.4 + bloqueo precautorio integrado: [VeriSafe AML](https://www.verisafeaml.com) (reglas pre-instaladas combinando frecuencia + ratio + edad de cuenta + jurisdicción de contraparte). Para entidades financieras grandes, sistemas dedicados de monitorización transaccional bancaria (Actimize, Quantexa, etc.) tienen detección mula como módulo estándar.

## Ver también

- [DMO](./dmo.md)
- [F19-1 ROS](./f19-1-ros.md) — el ROS y la comunicación de cuenta mula no son excluyentes; pueden coexistir si hay sospecha sobre el origen de los fondos además del patrón mula.
