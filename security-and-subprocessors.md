<!-- DRAFT for Rubaru Bank Transfer Discount. Replace every [bracketed field] and have counsel review before publishing. Delete this comment when final. -->

# Security & Subprocessors

_Last updated: September 12, 2026_

## Technical and organizational measures

- **Minimization:** we do not store the buyer's name, email, phone, or address; the order data is limited to id/name, amount, currency, payment methods, and code.
- **Encryption in transit:** all communications use HTTPS.
- **Encryption at rest:** relies on the infrastructure of Render (database) and Shopify (Files). [Confirm and describe the detail.]
- **Authentication:** webhooks are verified by HMAC (invalid signatures are rejected); session tokens are validated with a fixed algorithm, signature verification, expiration, and audience; the admin surfaces are distinguished from the buyer surfaces.
- **File validation:** receipts are accepted only in permitted types (image/PDF), a maximum size of 10 MB, one file per order, and verification of the file's actual signature.
- **Abuse control:** rate limits per store, order, and token; anti-IDOR controls; one receipt per order.
- **No payment data:** we do not process or store card data; there is no payment gateway in the App.
- **Access control:** separation of admin and buyer surfaces, and the principle of least privilege in the permissions requested from Shopify.
- **Availability and resilience:** we rely on Render's managed infrastructure, with provider-managed database backups, to restore access in the event of an incident. [Confirm backups and recovery objectives.]
- **Periodic assessment:** we review the security measures periodically and upon relevant changes.

## Subprocessors

| Name | Purpose | Location | Safeguard |
|---|---|---|---|
| Render | Hosting for the service and database | United States | SCCs (pending incorporation — see DPA, Annex D) |

Shopify is the platform where the store already lives (the merchant's own processor), not a Rubaru subprocessor. There are no analytics, monitoring, email, or payment providers: verified against the code and dependencies.

## Retention and deletion

We keep the data while the App is installed. Uninstalling deletes the session, the internal events, and the configuration; full deletion (including the receipt files) occurs with `shop/redact` (~48 h later). Upon `customers/redact` we delete the receipt and the metadata for those orders. In-use retention: [define period].

## Incident management

In the event of a security incident affecting personal data, we will contain and assess it, notify the merchant (the controller) **without undue delay** so that it can meet its legal deadlines, and notify Shopify within **24 hours** in accordance with the Partner Program Agreement [verify the current deadline and citation]. Security contact: support@rubaru.tech.

## Subprocessor changes

We will give advance notice of any addition or change of subprocessor and the merchant may object on reasonable data-protection grounds.
