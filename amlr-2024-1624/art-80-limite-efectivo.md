# AMLR Art. 80 — Límite €10.000 en pagos en efectivo

## Resumen

El AMLR establece un **límite máximo de €10.000 en pagos en efectivo** para personas que actúen profesionalmente en una operación. Por debajo, se permiten pagos en efectivo sin obligación específica; igual o por encima, hay que rechazar el pago en efectivo o aplicar tratamiento PBC/FT reforzado.

## Texto del artículo

[EUR-Lex — AMLR Art. 80](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624). Refuerza el régimen español pre-existente (Ley 7/2012 y posteriores establecían €1.000 para profesionales en algunos contextos; el AMLR uniforma a €10.000 en toda la UE para profesionales).

## Cómo evidenciarlo

1. **Bloqueo en formularios** — cuando el operador intenta registrar una operación con `payment_method = "efectivo"` y `amount >= 10000`, el sistema debe alertar (alerta destructiva) o bloquear según política interna.
2. **Política documentada** — el manual PBC/FT del sujeto obligado debe explicitar cómo se gestionan operaciones cerca del umbral (ej. fragmentación = motivo automático para examen especial Art. 17).
3. **Detección de fragmentación** — si un cliente realiza varias operaciones en efectivo bajo el umbral en una ventana corta, el motor de monitorización debe agregar y disparar alerta.
4. **Comunicación al SEPBLAC** — el rechazo de la operación en efectivo no exime de comunicar por indicio (Art. 18 Ley 10/2010) si hay sospecha.

## Antipatrones comunes

- **"El cliente quería pagar €15.000 en efectivo, le dije que no y se fue"** — sin más documentación, esa interacción no queda registrada. Si después aparece otra operación del mismo cliente, no podrás vincular. Registra siempre el intento + decisión.
- **Permitir el pago "porque el cliente es de confianza"** — el AMLR no admite excepciones por relación. Aplica a todos los profesionales por igual.
- **Calcular el umbral por operación, no por relación** — fragmentar deliberadamente es delito (smurfing). El motor de monitorización debe agregar.

## A quién aplica

Profesionales: comerciantes de bienes y servicios, agencias inmobiliarias, joyerías, marchantes de arte, comerciantes de vehículos de lujo, anticuarios, etc. **NO aplica entre particulares** que actúan en operación privada (compraventa entre vecinos, regalo familiar, etc.) — para esos casos hay un régimen distinto.

## Tools que automatizan esto

Alerta destructiva en el formulario + agregación temporal por persona + flag automático si se rechaza el pago: [VeriSafe AML](https://www.verisafeaml.com) (alerta de €10k integrada en el formulario de operación + reglas de monitorización pre-instaladas para detectar fragmentación).

## Ver también

- [Ley 10/2010 Art. 17 — Examen especial](../ley-10-2010/art-17-examen-especial.md)
- [F19-1 ROS](../sepblac-formularios/f19-1-ros.md)
