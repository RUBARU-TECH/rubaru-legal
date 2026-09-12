<!-- DRAFT for Rubaru Bank Transfer Discount. Replace every [bracketed field] and have counsel review before publishing. Delete this comment when final. -->

# Data Processing Agreement (DPA)

_Between [Legal entity name] ("Rubaru", processor) and the Merchant ("controller") · Annex to the Service Agreement_

1. **Roles.** The Merchant is the **controller** of its buyers' personal data. Rubaru is the **processor** and processes it solely on behalf of the Merchant. Shopify acts as the Merchant's own processor under its own agreement, and is **not** a Rubaru subprocessor. This DPA prevails over any conflicting terms regarding the processing of personal data.
2. **Subject matter and scope.** The subject matter, duration, nature, and purpose of the processing, the types of data, and the categories of data subjects are set out in **Annex A**. Rubaru will process the data only to provide the App.
3. **Documented instructions.** Rubaru processes personal data only according to the Merchant's documented instructions (including international transfers), unless legally required otherwise, in which case it will inform the Merchant unless legally prohibited. Rubaru will inform the Merchant, without delay, if it considers that an instruction infringes the GDPR or another applicable data-protection rule.
4. **Confidentiality.** Rubaru ensures that the persons authorized to process the data are bound by a duty of confidentiality.
5. **Security.** Rubaru implements the appropriate technical and organizational measures (Art. 32 GDPR), described in **Annex C** and in the Security document (G).
6. **Subprocessors.** The Merchant grants general authorization for the use of the subprocessors listed in **Annex B**. Rubaru will give advance notice of any change and the Merchant may object on reasonable data-protection grounds. Rubaru imposes on each subprocessor the same obligations as this DPA and is liable for its performance.
7. **Assistance with data subjects' rights.** Taking into account the nature of the processing, Rubaru assists the Merchant with appropriate technical and organizational measures to respond to requests for access, rectification, erasure, objection, restriction, and portability; and it integrates Shopify's compliance webhooks for that purpose.
8. **Assistance with security, breaches, and assessments.** Rubaru assists the Merchant with its obligations under Arts. 32-36 (security, breach notification, impact assessments, and prior consultation).
9. **Incident notification.** Rubaru will notify the Merchant **without undue delay** after becoming aware of a security breach affecting personal data, with the information reasonably available so that the Merchant can meet its legal deadlines [e.g. 72 h].
10. **Deletion or return.** At the end of the service, and in any case within **30 days** of uninstall or the request, Rubaru deletes or, if the Merchant so requests and it is technically feasible, returns (for example, via export from Shopify) all personal data, and deletes the copies, unless legally required to retain them. Deletion is carried out through the uninstall flows and `shop/redact`/`customers/redact`.
11. **Audit.** Rubaru makes available to the Merchant the information necessary to demonstrate compliance with this DPA and allows reasonable audits, which may be satisfied through third-party reports or certifications when available.
12. **Records.** Rubaru maintains the records of the processing activities carried out on behalf of the Merchant (Art. 30(2) GDPR).
13. **International transfers.** Where the processing involves transferring data subject to the GDPR to a country without an adequate level of protection, the Standard Contractual Clauses (Decision 2021/914) apply, in the corresponding module, incorporated by reference in **Annex D**, together with the UK addendum where applicable. [Diego: define the module and risk assessment for the leg to Render US.]
14. **"Service provider" terms (CCPA/CPRA).** With respect to the personal information of California residents, Rubaru: does not sell or share it; does not retain, use, or disclose it outside the service relationship or for any other purpose; does not combine it with data from other sources except as permitted; certifies that it understands and will comply with these restrictions; and cooperates with consumer rights requests.
15. **No AI training and no reselling.** Rubaru does not use the Merchant's personal data to train artificial intelligence models, nor does it resell it.
16. **Liability and term.** This DPA is in force while Rubaru processes data on behalf of the Merchant and forms part of the Service Agreement, whose liability clauses apply.

## Annex A — Processing details

**Subject matter:** provision of the App. **Duration:** while the App is installed. **Nature and purpose:** apply the bank-transfer discount, display the Merchant's bank details, receive and manage the receipt, attribute orders, and mark the approved order as paid. **Types of data:** order data (id/name, amount, currency, payment methods, code) and the receipt file (which may contain the buyer's personal/financial data). **Categories of data subjects:** the Merchant's buyers.

## Annex B — Subprocessors

| Subprocessor | Purpose | Location | Safeguard |
|---|---|---|---|
| Render | Hosting for the service and database | United States | SCCs (pending incorporation — see Annex D) |

Shopify is not listed as a Rubaru subprocessor: it is the Merchant's own processor under its agreement with Shopify.

## Annex C — Security measures

See document G (Security): encryption in transit, authentication of webhooks and tokens, minimization, file validation, rate limits, and separation of surfaces and least privilege.

## Annex D — Standard Contractual Clauses

[Attach the applicable module of Decision 2021/914 and, where relevant, the UK addendum.]
