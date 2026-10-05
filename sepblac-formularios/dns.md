# DNS — Declaración Negativa Semestral

## Resumen

Comunicación al SEPBLAC, **semestral**, de que el sujeto obligado **no ha tenido operaciones declarables** en el período. Es la contraparte de la DMO: si DMO=0, DNS=1.

## Cuándo presentarlo

- **Periodicidad**: semestral, dentro de los 15 primeros días del mes siguiente al fin de cada semestre natural (julio para H1, enero para H2).
- **Sólo si efectivamente no has tenido operaciones declarables** — si has presentado DMO en algún mes del semestre, no hace falta DNS.

## Por qué es importante

- El SEPBLAC interpreta el silencio mal: si no presentas DMO ni DNS, asume que olvidaste presentar DMO. La DNS es la prueba activa de que el silencio es deliberado.
- Demuestra que el OCI está activo y revisa periódicamente.
- Protege contra apercibimientos por "no comunicación" en inspecciones.

## Cómo presentarlo

- Vía **CTL** del SEPBLAC.
- Formato simple — generalmente XML estándar muy ligero o formulario web.
- Sin operaciones — sólo metadatos del sujeto + período + declaración expresa.

## Cómo evidenciarlo

1. **Acuse del CTL** — recibo de presentación.
2. **Verificación interna** — lista de operaciones del semestre + razón por la que ninguna es declarable. Esta lista NO se envía al SEPBLAC pero se conserva durante el plazo legal.
3. **Decisión del OCI** — acta o registro de que el OCI ha revisado y confirmado la inexistencia de operaciones declarables.

## Antipatrones comunes

- **Olvidar la DNS porque "no había nada que declarar"** — error común. La DNS ES la declaración.
- **Presentar DNS sin verificar primero** — el SEPBLAC en inspección puede pedir la lista interna que justifica la "no declarabilidad". Si encuentras operaciones declarables, presentas una DMO retroactiva con justificación.

## Tools que automatizan esto

Generación automática de DNS cuando el motor detecta cero operaciones DMO en el semestre: [VeriSafe AML](https://www.verisafeaml.com) (cron semestral que pre-genera DNS y notifica al OCI para revisar+presentar).

## Ver también

- [DMO](./dmo.md) — declaración mensual cuando hay operaciones.
