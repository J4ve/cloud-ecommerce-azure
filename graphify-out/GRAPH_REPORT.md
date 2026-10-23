# Graph Report - cloud-ecommerce-azure  (2026-10-23)

## Corpus Check
- Large corpus: 500 files · ~680,437 words. Semantic extraction will be expensive (many Claude tokens). Consider running on a subfolder.

## Summary
- 126 nodes · 266 edges · 13 communities
- Extraction: 86% EXTRACTED · 12% INFERRED · 2% AMBIGUOUS · INFERRED: 32 edges (avg confidence: 0.92)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- catalog.html (Catalog page)
- server.js
- catalog.js
- GenericMart Cloud README
- Azure Portal Screenshot Index
- setupSearch()
- GitHub Actions CI/CD (Optimization
- Deployment Guide - GenericMart
- a11y.js
- product.js
- validation.js

## God Nodes (most connected - your core abstractions)
1. `Deployment Guide - GenericMart Cloud (Scenario B)` - 12 edges
2. `Azure Portal Screenshot Index` - 12 edges
3. `GenericMart Cloud README` - 11 edges
4. `GenericMart Cloud - Architecture & Design Report` - 11 edges
5. `Azure App Service Plan + Web App (Standard S1, Linux, Node 22, 2 instances)` - 11 edges
6. `CHANGELOG.md (GenericMart Cloud)` - 10 edges
7. `catalog.html (Catalog page)` - 10 edges
8. `index.html (GenericMart homepage)` - 10 edges
9. `Azure SQL Database (DTU S0)` - 10 edges
10. `deploy.azcli (Bash Azure CLI IaC script)` - 10 edges

## Surprising Connections (you probably didn't know these)
- `Azure SQL Database (DTU S0)` --shares_data_with--> `ensureSchema()`  [INFERRED]
  report/report.md → src/server.js
- `Azure login via OIDC federation (azure/login@v2)` --semantically_similar_to--> `System-assigned Managed Identity on Web App (security control)`  [INFERRED] [semantically similar]
  .github/workflows/azure-deploy.yml → report/report.md
- `renderSummary() inline checkout order summary` --semantically_similar_to--> `calcShipping()`  [INFERRED] [semantically similar]
  src/public/checkout.html → src/public/js/cart.js
- `Azure Portal Screenshot Index` --references--> `POST /api/checkout and GET /api/orders (SQL order persistence)`  [AMBIGUOUS]
  deployment/screenshots/README.md → CHANGELOG.md
- `Deploy app.zip to Azure Web App (azure/webapps-deploy@v3)` --semantically_similar_to--> `Manual zip deploy via az webapp deploy`  [INFERRED] [semantically similar]
  .github/workflows/azure-deploy.yml → deployment/README.md

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **GenericMart baseline Azure architecture (compute, data, storage, security control)** — cloud_ecommerce_azure_deployment_readme_resource_group, cloud_ecommerce_azure_report_report_azure_app_service, cloud_ecommerce_azure_report_report_azure_sql_database, cloud_ecommerce_azure_report_report_azure_blob_storage, cloud_ecommerce_azure_report_report_managed_identity [EXTRACTED 1.00]
- **GenericMart storefront customer flow (home, catalog, product, cart, checkout)** — cloud_ecommerce_azure_src_public_index, cloud_ecommerce_azure_src_public_catalog, cloud_ecommerce_azure_src_public_product, cloud_ecommerce_azure_src_public_cart, cloud_ecommerce_azure_src_public_checkout [EXTRACTED 1.00]

## Communities (13 total, 0 thin omitted)

### Community 0 - "catalog.html (Catalog page)"
Cohesion: 0.20
Nodes (16): TeknikkTorget UI port rebranded as GenericMart, cart.html (Cart page), Cart rows and order summary containers (#tt-cart-rows, #tt-cart-summary), catalog.html (Catalog page), checkout.html (Checkout page), renderSummary() inline checkout order summary, index.html (GenericMart homepage), Featured products grid with pill filters (#tt-featured) (+8 more)

### Community 1 - "server.js"
Cohesion: 0.15
Nodes (19): POST /api/checkout and GET /api/orders (SQL order persistence), Commit src/package-lock.json to unblock CI npm cache, server.js rewrite: client-side localStorage cart + SQL order API, Post-deploy verification (/health sql:true, /cart, /orders), build-and-deploy job (push to main on src/**), Smoke test /health endpoint (curl after 30s, fail build on error), Setup Node.js 20.x with npm cache (src/package-lock.json), CARL GERALD J. PARRO (application code / UI port / architecture diagram) (+11 more)

### Community 2 - "catalog.js"
Cohesion: 0.27
Nodes (11): Catalog filter rail (category, brand, price, motor, battery) and sort, Responsive filter-rail relocation into offcanvas (max-width 991.98px), bind(), emptyState(), filtered(), renderChips(), renderResults(), setupBrandList() (+3 more)

### Community 3 - "GenericMart Cloud README"
Cohesion: 0.23
Nodes (13): CHANGELOG.md (GenericMart Cloud), azure-deploy.yml (Deploy GenericMart to Azure App Service), INSTRUCTIONS.md (CSEC 3 Final Project Brief), Deliverable 1: Architecture Diagram (20 pts), Deliverable 3: Cost Estimate Report (15 pts), Deliverable 4: Live Demo & Video Presentation (35 pts), Keep a Changelog format (Section 7 CHANGELOG requirements), Scenario B: E-Commerce Storefront (App Service 2+ instances, Azure SQL, optional Redis) (+5 more)

### Community 4 - "Azure Portal Screenshot Index"
Cohesion: 0.67
Nodes (9): Azure Portal Screenshot Index, GenericMart Cloud (Node.js Express storefront on Azure), Itemized monthly cost: $99.54/mo, $1,194.43/yr (Japan East), GenericMart Cloud - Architecture & Design Report, Application Insights telemetry (Optimization #1, Monitoring & Operations), Azure App Service Plan + Web App (Standard S1, Linux, Node 22, 2 instances), Azure Storage Account + Blob container 'products' (Standard_LRS), Azure SQL Database (DTU S0) (+1 more)

### Community 5 - "setupSearch()"
Cohesion: 0.28
Nodes (8): Header search combobox with autocomplete (#tt-search-input), Welcome guide overlay (#tt-welcome), setupSearch(), highlight(), render(), runQuery(), setupWelcome(), render()

### Community 6 - "GitHub Actions CI/CD (Optimization"
Cohesion: 0.25
Nodes (8): Manual zip deploy via az webapp deploy, Azure login via OIDC federation (azure/login@v2), Deploy app.zip to Azure Web App (azure/webapps-deploy@v3), Section 6 Cloud Optimization Requirements (at least two), JAVE A. BACSAIN (infrastructure / IaC / OIDC CI/CD), Intentional trade-offs: no Redis, no Front Door/CDN, single region, no WAF, GitHub Actions CI/CD (Optimization #2, Security & DevOps), Security boundary (public HTTPS app + blobs, SQL limited to Azure-internal via AllowAzureServices)

### Community 7 - "Deployment Guide - GenericMart"
Cohesion: 0.57
Nodes (7): Deployment Guide - GenericMart Cloud (Scenario B), deploy.azcli (Bash Azure CLI IaC script), deploy.ps1 (PowerShell mirror of deploy.azcli), Resource Group rg-genericmart-cloud (Japan East), SQL_ADMIN_PASSWORD environment variable (no hardcoded secrets), Deliverable 2: Deployment Documentation (30 pts), Method A (Code): Azure CLI or Bicep deployment

### Community 8 - "a11y.js"
Cohesion: 0.48
Nodes (5): apply(), bind(), chime(), load(), save()

### Community 9 - "product.js"
Cohesion: 0.52
Nodes (6): gallery(), readId(), recommend(), render(), specsTable(), Product detail root #tt-pd-root (reads ?id=)

### Community 10 - "validation.js"
Cohesion: 0.60
Nodes (5): Checkout form #tt-checkout-form (data-rule inline validation), clearError(), setupForm(), showError(), validateField()

## Ambiguous Edges - Review These
- `server.js` → `Documented routes (/cart, /cart/add, /cart/remove, POST /checkout, /orders)`  [AMBIGUOUS]
  src/README.md · relation: references
- `Azure Portal Screenshot Index` → `POST /api/checkout and GET /api/orders (SQL order persistence)`  [AMBIGUOUS]
  deployment/screenshots/README.md · relation: references
- `POST /api/checkout and GET /api/orders (SQL order persistence)` → `Post-deploy verification (/health sql:true, /cart, /orders)`  [AMBIGUOUS]
  deployment/README.md · relation: references
- `POST /api/checkout and GET /api/orders (SQL order persistence)` → `Checkout form #tt-checkout-form (data-rule inline validation)`  [AMBIGUOUS]
  src/public/checkout.html · relation: references
- `Azure SQL Database (DTU S0)` → `System-assigned Managed Identity on Web App (security control)`  [AMBIGUOUS]
  report/report.md · relation: references
- `Azure Storage Account + Blob container 'products' (Standard_LRS)` → `Product detail root #tt-pd-root (reads ?id=)`  [AMBIGUOUS]
  report/report.md · relation: shares_data_with

## Knowledge Gaps
- **2 isolated node(s):** `__dirname`, `app`
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 11 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **What is the exact relationship between `server.js` and `Documented routes (/cart, /cart/add, /cart/remove, POST /checkout, /orders)`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._
- **What is the exact relationship between `Azure Portal Screenshot Index` and `POST /api/checkout and GET /api/orders (SQL order persistence)`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._
- **What is the exact relationship between `POST /api/checkout and GET /api/orders (SQL order persistence)` and `Post-deploy verification (/health sql:true, /cart, /orders)`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._
- **What is the exact relationship between `POST /api/checkout and GET /api/orders (SQL order persistence)` and `Checkout form #tt-checkout-form (data-rule inline validation)`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._
- **What is the exact relationship between `Azure SQL Database (DTU S0)` and `System-assigned Managed Identity on Web App (security control)`?**
  _Edge tagged AMBIGUOUS (relation: references) - confidence is low._
- **What is the exact relationship between `Azure Storage Account + Blob container 'products' (Standard_LRS)` and `Product detail root #tt-pd-root (reads ?id=)`?**
  _Edge tagged AMBIGUOUS (relation: shares_data_with) - confidence is low._
- **Why does `TeknikkTorget UI port rebranded as GenericMart` connect `catalog.html (Catalog page)` to `server.js`, `GenericMart Cloud README`?**
  _High betweenness centrality (0.312) - this node is a cross-community bridge._