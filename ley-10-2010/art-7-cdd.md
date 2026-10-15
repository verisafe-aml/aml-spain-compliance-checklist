# Art. 7 Ley 10/2010 — Diligencia debida (CDD)

## Resumen

Obligación de identificar y verificar la identidad del cliente, su titular real, el propósito de la relación de negocios y el origen de los fondos, **antes** de iniciar la relación o ejecutar la operación.

## Texto del artículo

[BOE — Ley 10/2010, Art. 7](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a7). Las medidas se gradúan según el riesgo del cliente:

- **Diligencia simplificada (SDD, Art. 9)** — clientes de bajo riesgo (entidades financieras supervisadas UE, organismos públicos, etc.).
- **Diligencia normal (CDD, Art. 7)** — el caso estándar.
- **Diligencia reforzada (EDD, Art. 11)** — PEPs, jurisdicciones de alto riesgo, operaciones complejas o inusuales sin propósito económico aparente.

## Cómo evidenciarlo

Para cada cliente, conserva:

1. **Identificación documental** — DNI / NIE / pasaporte / CIF + verificación de autenticidad. Si el cliente no está físicamente presente, la identidad debe quedar acreditada por una de las vías del [art. 21.1 RD 304/2014](https://www.boe.es/buscar/act.php?id=BOE-A-2014-4742#a21), y debe constar cuál se usó:
   - **a)** identificación electrónica conforme a la normativa de firma electrónica (por ejemplo, un certificado cualificado del cliente);
   - **b)** copia del documento de identidad expedida por un fedatario público;
   - **c)** primer ingreso desde una cuenta a nombre del mismo cliente en una entidad domiciliada en España, en la UE o en un país tercero equivalente;
   - **d)** otro procedimiento seguro de identificación no presencial que cumpla los requisitos de las autorizaciones generales del SEPBLAC (videoconferencia, 12/02/2016; vídeo-identificación, 11/05/2017; remisión a las autorizaciones generales en la redacción del RD 813/2026, en vigor desde el 28/10/2026).

   Una verificación remota automatizada (fotos del documento, prueba de vida y comparación facial) comprueba el documento y que la persona es su titular, pero **por sí sola no es un procedimiento de vídeo-identificación** conforme a la autorización de 2017: esta exige, entre otros requisitos, transmisión en directo de imagen y sonido, grabación continua de todo el proceso que permita reproducirlo en secuencia, exhibición del anverso y el reverso del documento en esa grabación, revisión individual por personal formado antes de operar, un análisis de riesgo específico previo y pruebas de eficacia del procedimiento. Si no se cumplen, completa la identificación por la vía a), b) o c) y no ejecutes operaciones hasta tenerla. Con la vía d), obtén además en el plazo de un mes copia de los documentos necesarios para la diligencia debida (art. 21.1.d RD 304/2014).
2. **Titular real** — para personas jurídicas, la cadena de titularidad efectiva hasta persona física que controle ≥25% (≥10% para sectores de alto riesgo).
3. **Propósito de la relación** — qué tipo de operativa esperas con este cliente.
4. **Origen de los fondos** — para EDD: fuente declarada + evidencia razonable.
5. **Perfil de riesgo asignado** — bajo / medio / alto / muy alto, con justificación de los factores aplicados.
6. **Fecha + responsable** — quién aprobó la diligencia y cuándo.

## Antipatrones comunes

- **CDD sólo en el alta, sin revisión periódica** → la obligación es continua. Revisión periódica obligatoria según el nivel de riesgo (típico: 1 año alto, 2 años medio, 3 años bajo).
- **"PEP = sólo cargos políticos actuales"** → incluye familiares y allegados, y las medidas siguen 2 años tras el cese del cargo (art. 14.9 Ley 10/2010; el Art. 45(2) AMLR exige al menos 12 meses).
- **EDD sin documentar el origen de los fondos** → el oficial de cumplimiento debe poder enseñar al SEPBLAC la evidencia, no sólo el campo "yes" en un formulario.
- **Tratar una verificación remota automatizada como vídeo-identificación** → selfie o vídeo corto + fotos del documento no equivalen al procedimiento de la autorización del SEPBLAC de 2017. Sin la vía a), b) o c) documentada, la identificación no presencial está incompleta.
- **CDD sin análisis de riesgo escrito detrás** → el art. 7.1 exige poder demostrar que el alcance de las medidas es adecuado «mediante un previo análisis de riesgo que en todo caso deberá constar por escrito». Ver [Art. 7.1 — Análisis de riesgo](./art-7-1-analisis-riesgo.md).
- **Una sola fuente de identidad cuando hay duda** → si el documento parece manipulado, cruza con segunda fuente (registro mercantil, lista PEP, registros notariales).

## Tools que automatizan esto

Las herramientas PBC/FT modernas integran KYC + screening + scoring de riesgo + recordatorio de revisión periódica en un único expediente: [VeriSafe AML](https://www.verisafeaml.com) (con KYC biométrico a distancia, evidencias con sello de tiempo cualificado y guía para completar la identificación no presencial por las vías del art. 21.1 RD 304/2014, + las 7 medidas EDD del Art. 34 AMLR).

## Ver también

- [Art. 7.1 — Análisis de riesgo](./art-7-1-analisis-riesgo.md) — el análisis escrito en el que se apoya la graduación de las medidas.
- [Art. 17 — Examen especial](./art-17-examen-especial.md) — qué hacer cuando algo no cuadra.
- [AMLR Art. 28(1) RTS DDC](../amlr-2024-1624/art-28-1-rts-ddc.md) — modelo de cardinalidad-N.
- [AMLR Art. 34 — Medidas EDD](../amlr-2024-1624/art-34-edd.md) — las 7 medidas predefinidas.
