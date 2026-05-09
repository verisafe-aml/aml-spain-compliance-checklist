# DMO — Declaración Mensual de Operaciones

## Resumen

Comunicación al SEPBLAC de las operaciones realizadas por el sujeto obligado durante el mes que cumplan determinados criterios objetivos (sin necesidad de sospecha): movimientos en efectivo, operaciones con paraísos fiscales, operaciones de envío de dinero superiores a determinados importes, etc. **Mensual**.

## Cuándo presentarlo

- **Periodicidad**: mensual, dentro de los 15 primeros días del mes siguiente al de las operaciones.
- **Si no hay operaciones declarables**: presenta una **DNS** (Declaración Negativa Semestral) en su lugar.

## Qué se declara

Las categorías típicas (varían por sector):

- **`cash`** — operaciones en efectivo iguales o superiores a €30.000 mensuales por cliente.
- **`money_transfer`** — envíos de dinero internacional iguales o superiores a €1.500.
- **`tax_haven`** — operaciones con personas o jurisdicciones consideradas paraísos fiscales (umbrales según operación).
- **`occasional`** — operaciones ocasionales superiores a €1.000 cuando no hay relación de negocio establecida.

Cada operación lleva un **`<TipoOperacion>`** que mapea a un código SEPBLAC. La plataforma operativa debe asignar el código automáticamente según las reglas de monitorización + la naturaleza de la operación.

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

Generación nativa DMO XSD 3.0 con asignación automática de tipo de operación desde el rule engine: [VeriSafe AML](https://www.verisafeaml.com) (motor de monitorización con `include_in_dmo` + `dmo_type_code` + arbitraje cuando varias reglas firman). [ApreNet](https://www.aprenet.es) también tiene generación DMO nativa. Para sujetos sin herramienta: plantilla XSD + validador antes del envío.

## Ver también

- [DNS](./dns.md) — declaración negativa semestral.
- [Cuentas Mula](./cuentas-mula.md) — XSD 2.4 distinto del DMO.
