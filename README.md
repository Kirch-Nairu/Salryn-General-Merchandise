# SALRYN
### General Merchandise Edition

**Point of sale. Inventory. Procurement. Business operations.**

Salryn is a Windows-based, offline-ready retail management system by **Kirjane Labs**, developed for general merchandise stores and small to medium-sized retail businesses. It connects the sales counter, stockroom, purchasing desk and management office in one application.

[**Windows downloads**](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases) · [Installation guide](INSTALLATION.md) · [Support & FAQ](SUPPORT.md)

> **Availability:** The Beta RC1 installer has completed internal build and installed-runtime acceptance. Public download has not yet been published. This repository will host authorized installers under Releases; it does not host application source code.

## Who Salryn is built for

- School and office supply stores, hardware and general merchandise shops.
- Neighborhood retailers, specialty stores and small businesses moving away from manual ledgers.
- Owners who need visibility into sales, operating cash, stock levels, supplier obligations and customer orders.
- Stores that need to keep selling even when internet connectivity is unreliable.

## Feature directory

| Workspace | What it handles |
| --- | --- |
| POS Checkout | Scan items, build carts, record sales and payments, manage cashier shifts |
| Price Canvass / Quote | Prepare itemized customer quotations |
| Sales & Receipts | Find transactions, review and reprint saved receipts, authorized voids |
| Customer Orders | Create and track advance orders through fulfillment |
| Product Catalog | Maintain item identities, barcodes, prices, units and classifications |
| Stock Movements | Stock-in, adjustments, inventory history and availability |
| Purchase Requests | Request goods and route them for purchasing decisions |
| Procurement & Logistics | Suppliers, quotations, purchase orders, deliveries and returns |
| Accounts Payable | Supplier invoices, matching, obligations and actual payment confirmation |
| Accounts Receivable | Customer credit and collections (optional licensed module) |
| Dashboard & Reports | Sales and inventory visibility, business summaries and financial analytics |
| Users & Audit | Role-based operator access and traceable activity |
| Store Settings | Business identity and receipt/print configuration |
| License | Manage the installation's authorized product entitlement |
| Backup & Restore | Protect and recover local business records |

## Features in depth

### 01 · POS Checkout

- Build a transaction using barcode scanning or product search; review quantities, unit prices and totals before completing payment.
- Recognize available, low-stock, out-of-stock, inactive and untracked items; enforce stock limits for tracked items.
- Fast Add: create a missing barcode item and its initial inventory from checkout when the operator has the required permission.
- Record supported cash and noncash payment methods; retain the transaction and payment history.
- Complete sales with corresponding tracked-inventory deductions; receipt printing follows persistence of the sale.
- Open and close cashier shifts; capture the physical cash count separately from expected cash. Submitted counts are preserved for reconciliation rather than silently overwritten.

**Business value:** Less repeated encoding, better counter visibility and a traceable link between completed sales and stock.

### 02 · Price Canvass / Customer Quotations

- Search the product catalog and assemble an itemized quotation with quantities and quoted prices.
- Record customer information, validity period and terms.
- Save quotations independently of completed sales; retrieve and prepare customer-facing PDF documents.
- Prepare offers without deducting stock or treating an estimate as a completed counter transaction.

**Business value:** Produce consistent price proposals for bulk buyers, schools, offices and walk-in customers.

### 03 · Sales & Receipts

- Search completed and voided transaction history and inspect saved line items, payment details and receipts.
- Reprint the original persisted receipt instead of creating another sale or stock movement.
- Authorized void operations retain the original transaction history and record a controlled reversal of applicable stock and receivables.
- Historical-shift and uncollected-credit-sale void scenarios have specific financial integrity controls. A void is not a general-purpose refund or cash payout.

**Business value:** Reliable transaction lookup and accountability when a sale needs correction.

### 04 · Customer Orders

- Create orders for walk-in guests or customer accounts and attach multiple product lines.
- Track the order lifecycle: Confirmed, Preparing, Ready, Fulfilled or Cancelled.
- Filter orders by lifecycle status; manage preparation and fulfillment through authorized screens.
- Prepare printable customer order documents and preserve the relationship between the order and its fulfillment.

**Business value:** Manage advance orders and items prepared for collection without relying on handwritten reminders.

### 05 · Product Catalog

- Create and edit item identities, SKU/barcode information, selling prices, units of measure, categories and brands.
- Organize items through search and category, brand and active-status filters.
- Configure stock tracking and reorder thresholds where applicable.
- Deactivate items without removing historical transactions; manage balance changes separately through stock movements.
- Product import/export capabilities are subject to available permissions and supported formats.

**Business value:** One organized product record for checkout, inventory, quotations and purchasing.

### 06 · Stock Movements & Inventory

- Record stock-in and controlled quantity adjustments with separate movement history.
- Review available inventory and product stock conditions; distinguish tracked from untracked items.
- Monitor reorder thresholds, low stock and out-of-stock items.
- Use procurement stock cards, stock valuation where cost coverage permits, physical inventory count adjustments and supplier return workflows.
- Maintain traceability of quantity changes instead of overwriting stock history without a movement record.

**Business value:** Understand where merchandise came from, what was sold and why inventory changed.

### 07 · Purchase Requests (PR)

- Prepare itemized purchase requisitions for needed or replenishment goods.
- Allow authorized cashier request preparation without granting full purchasing or payable authority.
- Review requisitions and route approval or rejection through the applicable management permissions.
- Use approved purchasing requests as input to supplier purchase orders when appropriate.

**Business value:** Separate what staff request from what management authorizes the business to buy.

### 08 · Procurement & Logistics

- Maintain a supplier directory and review procurement activity.
- Record supplier quotations and compare offers.
- Create purchase orders through an approved requisition workflow or permitted direct purchasing; generate orders for selected suppliers.
- Record deliveries against purchase orders using receiving reports, inspection lines and authorized exception handling for overdelivery.
- Manage stock cards, physical count variance adjustments, supplier returns and associated debit-memo records.
- Preserve distinct receiving-line identities and validate cumulative quantities to prevent duplicate-line overbilling or over-return.
- Generate applicable purchase requisition, purchase order and receiving-report business documents.

**Business value:** Trace goods and purchasing decisions from request through delivery and return.

### 09 · Accounts Payable (AP)

- Intake supplier invoices and reconcile them against purchase orders and goods receipts through three-way matching.
- Keep unmatched documents pending verification rather than automatically treating them as approved liabilities.
- Route invoice variances through authorized review.
- Inspect the supplier payable subledger, outstanding obligations and aging categories.
- Prepare supplier disbursements, retain payment method/reference information and confirm actual payment before settlement.
- Produce payment voucher documents; retain preparation, approval and actual disbursement information.

**Business value:** Improve visibility into supplier obligations and distinguish preparing a payment from money actually leaving the business.

### 10 · Accounts Receivable / Utang (optional)

- Record eligible customer credit transactions within the licensed receivables workflow.
- Review customer balances, collections and historical ledger entries.
- Record supported collection methods and applicable references.
- Authorized collection reversals restore the relevant ledger balance while preserving original history.

**Availability:** Receivables / Utang requires the applicable paid Host entitlement. It is an operational credit ledger, not a replacement for a full accounting system.

### 11 · Dashboard & Business Reports

- Review completed daily sales, transaction counts, low-stock indicators and void activity.
- Use date-based sales reporting and product/category performance summaries.
- Inspect available gross-margin, stock, receivables and payables analytics; missing cost or entitlement data can limit certain reports.
- Review AP aging and authorized financial summaries.
- Use cashier shift count and reconciliation records to investigate operating-cash discrepancies.

**Business value:** Move from disconnected records to actionable store-level information.

### 12 · Users, Permissions & Audit

- Individual user sign-in with Admin, Manager and Cashier role-based access.
- Restrict sensitive actions such as stock changes, voids, supplier approvals and financial settlement to authorized operators.
- Manage staff accounts and review recorded activity through permitted administrative tools.
- Keep historical audit records for relevant operational changes.

**Business value:** Distinguish daily counter work from managerial and administrative responsibilities.

### 13 · Store Settings & Business Documents

- Configure store identity, receipt presentation and Windows print queue settings.
- Test the configured receipt printer from the application; existing saved receipts retain their original record.
- Use native PDF business documents where provided, including quotations, customer orders, purchasing and payment documents.
- Use keyboard-wedge barcode scanners and compatible Windows receipt printers; verify actual hardware compatibility during onboarding.

**Business value:** Present business documents consistently and tailor the application to the store's operating setup.

### 14 · Licensing & Data Protection

- License the Windows Host through the applicable Kirjane agreement.
- Store transactions and operational data locally; routine Host operation does not depend on a continuous internet connection.
- Create, download, import, verify and restore local backups using authorized controls.
- Preserve the application-data directory during supported upgrades and uninstallation. Always maintain a separate verified backup before an update.
- Installation does not require a developer toolchain or a separately launched web server.

## Edition boundaries

| Capability | Availability |
| --- | --- |
| Windows Host retail operations | Included in the documented candidate |
| Accounts Receivable / Utang | Optional licensed entitlement |
| LAN terminals / multi-workstation rollout | Future feature; not supplied for production use in this candidate |
| Cloud sync, hosted multi-branch management | Not advertised as included |
| Tax authority approval / official compliance | No certification or BIR approval claimed |

Operational reports, receipts and PDFs are business-management tools. Confirm applicable government registration and invoicing requirements separately with your business adviser and the publisher.

## Download & installation

Go to [GitHub Releases](https://github.com/Kirch-Nairu/Salryn-General-Merchandise/releases). When an authorized version is published, download its Windows setup executable from **Assets**, not GitHub's automatically generated source-code archives.

The planned Beta RC1 setup filename is `Salryn-POS-BetaRC1-Setup.exe`. Installation and upgrade guidance is available in [INSTALLATION.md](INSTALLATION.md).

## About & support

**Salryn General Merchandise** · A Kirjane Labs product  
Installer publisher display name: Kirjane Information Technology Services  
Product assistance: [salryn.info@gmail.com](mailto:salryn.info@gmail.com)

Salryn is proprietary software. Public access to this download repository does not grant rights to the application source code or an unrestricted software license. Installation, activation and use are subject to the applicable customer agreement.
