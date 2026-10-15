# AMLR Art. 80 — Límite €10.000 en pagos en efectivo (España: €1.000, Ley 7/2012)

## Resumen

El AMLR establece un **límite máximo de €10.000 en pagos en efectivo** en toda la UE para quien comercia con bienes o presta servicios. Pero **los límites nacionales más bajos siguen aplicándose** (art. 80.3). En España el límite vigente es más estricto: **no se puede pagar en efectivo €1.000 o más** cuando una de las partes actúa como empresario o profesional (art. 7 de la Ley 7/2012); el límite sube a €10.000 solo si paga un particular sin domicilio fiscal en España que no actúa como empresario o profesional. Los pagos fraccionados de una misma operación se suman.

## Texto del artículo

[EUR-Lex — AMLR Art. 80](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624). Ley 7/2012, art. 7: [BOE-A-2012-13416](https://www.boe.es/buscar/act.php?id=BOE-A-2012-13416). El AMLR no sustituye el límite español de €1.000: lo mantiene, porque es más bajo que el de la UE.

## Cómo evidenciarlo

1. **Bloqueo en formularios** — cuando el operador intenta registrar una operación con `payment_method = "efectivo"` y `amount >= 1000` (límite español), el sistema debe alertar (alerta destructiva) o bloquear según política interna.
2. **Política documentada** — el manual PBC/FT del sujeto obligado debe explicitar cómo se gestionan operaciones cerca del umbral (ej. fragmentación = motivo automático para examen especial Art. 17).
3. **Detección de fragmentación** — si un cliente realiza varias operaciones en efectivo bajo el umbral en una ventana corta, el motor de monitorización debe agregar y disparar alerta.
4. **Comunicación al SEPBLAC** — el rechazo de la operación en efectivo no exime de comunicar por indicio (Art. 18 Ley 10/2010) si hay sospecha.

## Antipatrones comunes

- **"El cliente quería pagar €15.000 en efectivo, le dije que no y se fue"** — sin más documentación, esa interacción no queda registrada. Si después aparece otra operación del mismo cliente, no podrás vincular. Registra siempre el intento + decisión.
- **Permitir el pago "porque el cliente es de confianza"** — ni la Ley 7/2012 ni el AMLR admiten excepciones por relación.
- **Aplicar el límite de €10.000 del AMLR en España** — el límite español de €1.000 es más estricto y sigue vigente (art. 80.3 AMLR).
- **Calcular el umbral por operación, no por relación** — fragmentar deliberadamente es delito (smurfing). El motor de monitorización debe agregar.

## A quién aplica

Profesionales: comerciantes de bienes y servicios, agencias inmobiliarias, joyerías, marchantes de arte, comerciantes de vehículos de lujo, anticuarios, etc. **NO aplica entre particulares** que actúan en operación privada (compraventa entre vecinos, regalo familiar, etc.) — para esos casos hay un régimen distinto.

## Tools que automatizan esto

Alerta destructiva en el formulario + agregación temporal por persona + flag automático si se rechaza el pago: [VeriSafe AML](https://www.verisafeaml.com) (alerta de efectivo desde €1.000 integrada en el formulario de operación + reglas de monitorización pre-instaladas para detectar fragmentación).

## Ver también

- [Ley 10/2010 Art. 17 — Examen especial](../ley-10-2010/art-17-examen-especial.md)
- [F19-1 ROS](../sepblac-formularios/f19-1-ros.md)
