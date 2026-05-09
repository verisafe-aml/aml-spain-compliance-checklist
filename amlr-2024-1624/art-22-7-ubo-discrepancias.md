# AMLR Art. 22(7) — Discrepancias en el registro UBO

## Resumen

Cuando los sujetos obligados detectan discrepancias entre la información de titularidad real (UBO) declarada por el cliente y la inscrita en el registro central de UBO (en España: Registro Mercantil + Registro de Titularidades Reales del Consejo General del Notariado), deben **comunicarlas a la autoridad responsable del registro**.

## Texto del artículo

[EUR-Lex — AMLR Art. 22(7)](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624). Directamente aplicable desde julio 2027.

## Cómo evidenciarlo

1. **Comprobación obligatoria** — al iniciar la relación, consulta el registro central UBO (oficial) y compara con la declaración del cliente.
2. **Documentar la consulta** — fecha, registro consultado, resultado obtenido, persona del equipo que la realizó.
3. **Si hay discrepancia** — registra la discrepancia + su naturaleza (porcentajes diferentes, persona declarada como UBO no figura en el registro, etc.).
4. **Comunicación a la autoridad** — al registro mercantil / al notariado / al SEPBLAC según el tipo de discrepancia.
5. **Continuar con la diligencia** — la discrepancia no impide la relación per se, pero refuerza el riesgo y suele justificar EDD.

## Antipatrones comunes

- **No consultar el registro porque "el cliente nos lo ha dicho"** → el AMLR exige la comprobación cruzada. La declaración del cliente NO es prueba suficiente.
- **Detectar y no comunicar** — la obligación es activa. La comunicación protege al sujeto obligado.
- **Asumir que el registro está actualizado** — los registros UBO son alimentados por las propias empresas; pueden tener años de retraso. La consulta + comparación es lo que importa.

## Tools que automatizan esto

Tracking de la comprobación + flag automático cuando la declaración del cliente no coincide con el registro: [VeriSafe AML](https://www.verisafeaml.com) (campos `registry_checked_at` + `registry_discrepancy_notes` en el registro UBO + workflow de comunicación). Para integraciones en tiempo real con eInforma / Axesor / proveedores de datos UBO, herramientas KYB especializadas.

## Ver también

- [Ley 10/2010 Art. 7 CDD](../ley-10-2010/art-7-cdd.md)
- [AMLR Art. 28(1) RTS DDC — modelo de cardinalidad-N](./art-28-1-rts-ddc.md)
