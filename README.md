# CargoWise (cargowise)

CargoWise is WiseTech Global's logistics execution platform - a single-database ERP for international freight forwarding, customs, warehousing, transport, and landside logistics. Its integration surface is real but **heavily gated**. Data moves in and out of a CargoWise (CW1) instance primarily through **eAdaptor**, which pairs a RESTful XML **inbound** service (push, query, add, and update records) with a SOAP-based **outbound** service (a webhook equivalent that emits messages when Workflow Template milestones fire). Payloads use CargoWise's **Universal XML** schemas - Universal Shipment (XUS), Universal Event (XUE), and Universal Transaction - or the legacy **Native XML** format, wrapped in a `UniversalInterchange` envelope. A newer REST path (**eAdaptor Next / xHub**) adds OAuth 2.0 authorization-code access and is positioned to replace SOAP.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cargowise/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cargowise/refs/heads/main/apis.yml)

## Access Model (read this first)

CargoWise's integration API is **not open or self-serve**:

- The **eAdaptor Developers Guide** and the actual per-tenant endpoints are released only **after a customer purchases the eAdaptor modules** for their instance.
- Integrator/partner access runs through **WiseTech accreditation and certification** (see the [Become a Partner](https://www.cargowise.com/partners/become-a-partner/) path).
- There is **no public API reference, sandbox, or price list**. Behavior can differ between instances based on each client's configuration.
- Pricing is **transaction-based** (Value Packs) with core API/EDI bundled into per-transaction fees; enterprise cost is **contact-sales**.

Because the authoritative specification is gated, the APIs documented here are **modeled from public developer references** (open-source eAdaptor clients, integrator docs, and product sheets) - not from a published CargoWise specification. Concrete, publicly attested facts include the SOAP operations `Ping` / `SendStream` / `ProcessStream` (deprecated) on an `eAdapterStreamedService.wsdl` endpoint, the `XUS`/`XUE` action codes, the `ORP` (Organization Proxy) recipient, and the Universal vs Native XML formats. Endpoints are marked `endpointsModeled` in `review.yml`.

## Tags

- Logistics
- Freight Forwarding
- Supply Chain
- Customs
- Shipping
- eAdaptor
- Universal XML
- EDI
- WiseTech Global

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### CargoWise eAdaptor Inbound API

The eAdaptor Inbound Service is a RESTful XML interface for pushing data into a CargoWise instance and querying records. A single inbound endpoint accepts a Universal XML or Native XML payload; the XML determines whether the request queries, adds, or updates records. Endpoints are per-tenant and gated behind the eAdaptor module purchase.

- **Human URL:** [https://wisetechacademy.com/explore/product-learning/](https://wisetechacademy.com/explore/product-learning/)

### CargoWise eAdaptor Outbound API

The eAdaptor Outbound Service is the webhook equivalent - CargoWise emits messages to a listening SOAP service when configured Workflow Template milestones or triggers fire. Actions are set to `XUS` (full Universal Shipment detail) or `XUE` (minimal Universal Event detail) with the recipient set to the Organization Proxy (`ORP`). The reference open-source client exposes the SOAP operations `Ping`, `SendStream`, and the deprecated `ProcessStream` against an `eAdapterStreamedService.wsdl` endpoint. Only one outbound SOAP URL can be configured per instance.

- **Human URL:** [https://wisetechacademy.com/explore/product-learning/](https://wisetechacademy.com/explore/product-learning/)

### CargoWise Universal Shipment API

The Universal Shipment (`XUS`) message is CargoWise's canonical XML model for a full logistics record - forwarding shipment, customs declaration, warehouse order, transport leg, and the associated organizations, packing lines, and charges. It is carried over eAdaptor inbound (to create or update) and outbound (to notify), wrapped in a `UniversalInterchange` envelope.

- **Human URL:** [https://www.scribd.com/document/725844283/Universal-XML-Universal-Activity-Module-Mapping-Guide](https://www.scribd.com/document/725844283/Universal-XML-Universal-Activity-Module-Mapping-Guide)

### CargoWise Universal Event API

The Universal Event (`XUE`) message carries a minimal record identifier plus the event or milestone responsible for a notification - the basis for tracking and status integrations. XUE messages are emitted by the eAdaptor Outbound Service when a Workflow Template milestone completes, and can also be posted inbound to raise events against a record.

- **Human URL:** [https://www.complect.io/docs/cargowise-integrations/cargowise-eadaptor/workflow-templates/](https://www.complect.io/docs/cargowise-integrations/cargowise-eadaptor/workflow-templates/)

### CargoWise REST Integration API

WiseTech's newer integration path (referred to as eAdaptor Next and xHub) adds REST access authenticated with OAuth 2.0 authorization-code flow, where a registered application receives a client ID and secret to mint access tokens. eAdaptor Next is positioned to fully replace SOAP for both inbound and outbound communication. Access is partner-gated through WiseTech accreditation; no public REST reference is published.

- **Human URL:** [https://www.cargowise.com/partners/become-a-partner/](https://www.cargowise.com/partners/become-a-partner/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/wisetech-global)
- [Website](https://www.cargowise.com/)
- [Documentation](https://wisetechacademy.com/explore/product-learning/)
- [Partners](https://www.cargowise.com/partners/become-a-partner/)
- [Pricing](https://www.cargowise.com/lp/cargowise-value-pack/)
- [Company](https://www.wisetechglobal.com/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
