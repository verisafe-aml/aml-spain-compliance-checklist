# Art. 25 Ley 10/2010 — Conservación de documentación

## Resumen

Conservas la documentación de diligencia debida + las operaciones realizadas + las comunicaciones al SEPBLAC durante **el plazo legal** (Art. 25; el Art. 77 AMLR lo revisará), en formato accesible y trazable. La integridad debe ser demostrable ante una inspección.

## Texto del artículo

[BOE — Ley 10/2010, Art. 25](https://www.boe.es/buscar/act.php?id=BOE-A-2010-6737#a25). El AMLR refuerza este punto en sus Art. 56-58.

## Cómo evidenciarlo

1. **Soporte duradero** — papel, electrónico u otro soporte que garantice integridad y legibilidad durante todo el plazo legal. Email o WhatsApp NO califican.
2. **Acceso rápido** — el SEPBLAC puede pedir documentación retrospectiva con plazo corto (típicamente 10 días). Tu sistema debe poder recuperar cualquier expediente sin trabajo arqueológico.
3. **Integridad** — el SEPBLAC tiene que poder comprobar que la documentación no ha sido modificada después de su creación. Hashing + firma + (idealmente) anclaje en blockchain o sistema externo de notarización.
4. **Eliminación al vencimiento** — vencido el plazo legal, debes eliminar la documentación salvo que haya base legal específica para conservarla (caso abierto, requerimiento judicial, etc.).

## Antipatrones comunes

- **"La conservo en Dropbox personal"** → no es soporte duradero corporativo. Necesitas backups, control de acceso y trazabilidad.
- **"La integridad la garantizo con la firma del director"** → la firma humana es revocable. Mejor: hash criptográfico + log de auditoría inmutable.
- **"Conservo todo indefinidamente para estar seguro"** → infringe el RGPD principio de limitación del plazo (Art. 5(1)(e)). Vencido el plazo legal, eliminar es la opción correcta salvo excepciones documentadas.
- **"Los certificados antiguos los regenero cuando los necesito"** → si el sistema regenera el PDF, el hash original no se puede verificar. Conserva el binario original (write-once, content-addressable).

## Tools que automatizan esto

Conservación durante el plazo legal, mientras la cuenta esté activa, con anclaje blockchain de cada certificado para integridad demostrable independientemente del proveedor: [VeriSafe AML](https://www.verisafeaml.com) (anclaje en Polygon + OpenTimestamps + auditoría diaria con árbol de Merkle, backup en R2). Para entidades que prefieren on-premise, soluciones tipo [DocuShare](https://www.xerox.com/digital-services/insights/docushare-flex.html) o gestores documentales tradicionales con e-signature notarizada.

## Ver también

- [AMLR Art. 56-58 — Conservación de información](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32024R1624)
- [F19-1 ROS](../sepblac-formularios/f19-1-ros.md)
