<!-- DRAFT for Rubaru Bank Transfer Discount. Replace every [bracketed field] and have counsel review before publishing. Delete this comment when final. -->

# Protected Customer Data

_Rubaru Bank Transfer Discount · Level 1_

## Justification (Spanish)

La app solicita `read_orders` y `write_orders` y escucha `orders/create`, por lo que trata datos de orden, que Shopify clasifica como Datos Protegidos del Cliente de Nivel 1. Los usa exclusivamente para (1) atribuir las órdenes pagadas por transferencia y mostrar el ahorro en el panel del comercio, y (2) marcar como pagada una orden que el comercio aprobó. La app **no** solicita ni almacena nombre, dirección, teléfono ni email del comprador. El comprobante que el comprador sube es contenido provisto por el propio comprador; se guarda en Shopify Files (del comercio) y se elimina con `customers/redact` y `shop/redact`. No se envían datos del comprador a terceros; el único subprocesador es el hosting en Render (EE. UU.). Los datos se cifran en tránsito (HTTPS). El cifrado en reposo se apoya en la infraestructura de nuestro proveedor de hosting (Render) y de Shopify (Files); la aplicación no añade un cifrado adicional a nivel de app [confirmar y adjuntar la atestación de cifrado en reposo del proveedor antes de enviar el formulario]. Aplicamos además minimización, limitación de propósito y borrado por los webhooks de cumplimiento.

## Justification (English)

The app requests `read_orders`/`write_orders` and subscribes to `orders/create`, so it processes order data, which Shopify classifies as Protected Customer Data (Level 1). It uses this data only to (1) attribute bank-transfer orders and show the merchant's savings dashboard, and (2) mark an order the merchant approved as paid. The app does **not** request or store the buyer's name, address, phone or email. The transfer receipt the buyer uploads is buyer-provided content, stored via Shopify Files (merchant-owned) and deleted on `customers/redact` and `shop/redact`. No customer data is sent to any third party; the only subprocessor is hosting on Render (US). Data is encrypted in transit (HTTPS). Encryption at rest relies on our hosting provider's (Render) and Shopify's (Files) infrastructure; the application adds no at-rest encryption layer of its own [confirm and attach the provider's at-rest attestation before submitting]. We also apply data minimization, purpose limitation, and deletion via the compliance webhooks.

## Commitments by requirement (Level 1)

| Requirement | How it is met |
|---|---|
| Minimization | No buyer PII is stored; only order id/name, amount, currency, methods, and code. |
| Purpose limitation | Order access used only for attribution and to mark as paid. |
| Transparency | Declared in the Privacy Policy (document A). |
| Retention | Deletion on uninstall and `redact`; in-use period: [define]. |
| Encryption | In transit: HTTPS. At rest: Render/Shopify infrastructure [confirm]. |
| Consent / opt-out | No sale of data; the merchant manages the buyer's consent. |
