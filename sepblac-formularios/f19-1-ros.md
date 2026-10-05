# F19-1 — Reporte de Operación Sospechosa (ROS)

## Resumen

Comunicación al SEPBLAC cuando, tras el examen especial del Art. 17 Ley 10/2010, persiste la sospecha de blanqueo de capitales o financiación del terrorismo. Es la herramienta principal del régimen español de comunicación por indicio (Art. 18).

## Cuándo presentarlo

- Cuando una operación, hechos u operaciones presentan indicios de estar relacionados con blanqueo de capitales o financiación del terrorismo (Art. 18 Ley 10/2010).
- **Sin demora**: el SEPBLAC espera presentación en plazo razonable tras la decisión interna de comunicar (típicamente 7-10 días desde la decisión del OCI).
- **Antes** de ejecutar la operación si es posible (la Ley 10/2010 contempla retención cautelar en algunos supuestos).

## Estructura del formulario

El F19-1 incluye:

1. **Datos del sujeto obligado comunicante** (auto-cumplimentados desde tu registro SEPBLAC).
2. **Operación(es) comunicada(s)** — fecha, importe, divisa, medio de pago, contrapartes (intervinientes).
3. **Personas intervinientes** — datos completos de identificación (incluyendo titulares reales si aplica).
4. **Narrativa** — el campo libre donde se explica:
   - Hechos detectados.
   - Por qué se sospecha.
   - Qué información adicional se ha recabado (Art. 17).
   - Decisión del OCI.
5. **Documentación adjunta** — evidencia electrónica (transcripciones, capturas, correos, contratos).

## Cómo presentarlo

- Vía **CTL** (Centro de Trámites en Línea) del SEPBLAC, en formato XML conforme al esquema oficial.
- Hasta que SEPBLAC publique un XSD, el F19-1 se presenta como **PDF certificado**. La plataforma operativa genera el PDF + lo certifica + lo entrega al CTL.

## Cómo evidenciarlo

1. **Comunicación enviada** — guarda recibo de presentación + número de comunicación SEPBLAC.
2. **Decisión del OCI** — acta o registro interno con la decisión (comunicar / no comunicar) + fecha + miembros del OCI.
3. **Evidencia narrativa** — todo lo recabado durante el examen especial (Art. 17).
4. **Conservación durante el plazo legal** (Art. 25).

## Antipatrones comunes

- **Narrativa genérica copy-paste** — "el cliente realizó una operación inusual" sin detalles. El SEPBLAC pide detalles concretos.
- **Comunicar tarde** — la presentación a meses vista perjudica la utilidad del SEPBLAC y revela problemas internos del sujeto.
- **Tipping-off** — alertar al cliente de que se ha presentado el ROS es ilegal (Art. 24 Ley 10/2010 + Art. 54 6AMLD).
- **No comunicar por miedo** — el sujeto obligado tiene **inmunidad civil** (Art. 24). Comunicar es lo seguro.

## Tools que automatizan esto

Generación nativa F19-1 con narrativa AI-asistida pre-rellenada desde el caso AML + certificación con anclaje blockchain: [VeriSafe AML](https://www.verisafeaml.com) (workflow ROS desde un caso → generación PDF → certificación → entrega al CTL). Para sujetos sin herramienta, plantillas Word + presentación manual al CTL son válidas pero más lentas.

## Ver también

- [Ley 10/2010 Art. 17 — Examen especial](../ley-10-2010/art-17-examen-especial.md)
- [Ley 10/2010 Art. 18 — Comunicación por indicio](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a18)
- [Ley 10/2010 Art. 25 — Conservación](../ley-10-2010/art-25-conservacion.md)
