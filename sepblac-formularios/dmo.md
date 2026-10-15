# DMO — Declaración Mensual de Operaciones

## Resumen

Comunicación al SEPBLAC de las operaciones realizadas por el sujeto obligado durante el mes que cumplan determinados criterios objetivos (sin necesidad de sospecha): los supuestos del art. 27.1 del RD 304/2014. **Mensual**.

## Cuándo presentarlo

- **Periodicidad**: mensual, entre los días 1 y 15 (naturales) del mes siguiente al de las operaciones (Instrucción 1/2006 del SEPBLAC).
- **Fuera de plazo**: hay que remitir al SEPBLAC un escrito justificativo firmado electrónicamente por el representante o su autorizado, por el Registro electrónico de la Oficina Virtual del Banco de España.
- **Si no hay operaciones declarables**: presenta una **DNS** (Declaración Negativa Semestral) en su lugar.

## Qué se declara

Los supuestos del art. 27.1 del RD 304/2014 (solo para los sujetos de las letras a) a j) y z) del art. 2.1 de la Ley 10/2010, salvo corredores de seguros y EAF):

- **a)** movimiento físico de efectivo de más de 30.000 € sin reflejo en cuenta;
- **b)** envíos de dinero con movimiento físico de efectivo de más de 1.500 €;
- **c)** operaciones de más de 30.000 € con residentes en territorios o países designados, o transferencias a o desde ellos. Mientras no haya Orden de designación, la lista es la de la Orden HFP/115/2023 (con la Orden HAC/649/2026) más los ocho países de la Orden ECO/2652/2002 (disposición transitoria segunda del RD 304/2014). La lista de la UE de jurisdicciones no cooperativas no cuenta.

Cada operación lleva un **tipo de operación** (1 a 22, descrito desde el punto de vista del cliente: por ejemplo, 1 emisión de transferencia u orden de pago, 12 compra de billetes extranjeros) y **al menos una característica** (efectivo sin reflejo en cuenta; transferencia a o desde territorios designados; operación con residentes en ellos; operación no ejecutada por documentación insuficiente), con las combinaciones que admite el cuadro de la Instrucción 1/2006 del SEPBLAC.

## Cómo presentarlo

- Vía **CTL** del SEPBLAC.
- En formato **XML conforme al XSD 3.0** (la versión vigente desde 2024).
- El XSD se actualiza periódicamente — el sujeto debe seguir las publicaciones del SEPBLAC y aplicar la versión vigente en el momento de la presentación.

## Cómo evidenciarlo

1. **Acuses del CTL** — guarda los recibos de presentación de cada DMO mensual.
2. **Lista de operaciones incluidas** — qué operaciones se declararon ese mes con su código asignado.
3. **Lista de operaciones excluidas con justificación** — si una operación cae en el umbral pero se decide no declarar (caso raro, suele requerir justificación del OCI), documenta el motivo.
4. **DMO mensual generada en el momento, no retroactiva** — el SEPBLAC valora la oportunidad (puntualidad).

## Antipatrones comunes

- **Generar DMO desde cero cada mes en Excel** — propenso a errores. Las herramientas serias generan el XML automáticamente desde las operaciones del mes que cumplen criterios.
- **Aplicar el XSD anterior cuando ya hay uno nuevo** — el SEPBLAC rechaza el XML por validación de esquema. Mantén tu plataforma actualizada.
- **No presentar DNS los meses sin operaciones declarables** — algunos sectores pueden estar exentos (verifica), pero en general: si no hay DMO, hay DNS. Quedarse callado es lo que el SEPBLAC interpreta mal.

## Tools que automatizan esto

Generación nativa DMO XSD 3.0 con asignación automática de tipo de operación desde el rule engine: [VeriSafe AML](https://www.verisafeaml.com) (motor de monitorización con `include_in_dmo` + `dmo_type_code` + arbitraje cuando varias reglas firman). Para sujetos sin herramienta: plantilla XSD + validador antes del envío.

## Ver también

- [DNS](./dns.md) — declaración negativa semestral.
- [Cuentas Mula](./cuentas-mula.md) — XSD 2.4 distinto del DMO.
