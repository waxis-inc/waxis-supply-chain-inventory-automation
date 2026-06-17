# PRD: Waxis Supply Chain & Inventory Automation

Document status: Draft v1.0  
Owner: Waxis Inc  
Research snapshot: 2026-06-16 EDT  
Repository: `waxis-supply-chain-inventory-automation`

## 1. Problem Statement

Manufacturers, distributors, retailers, and trading companies often manage inventory, supplier lead times, purchase orders, demand signals, warehouse tasks, and exceptions across disconnected ERP, WMS, TMS, spreadsheets, emails, and supplier portals. Teams react late to stockouts, overstocks, delayed purchase orders, SKU exceptions, and demand shifts.

The core issue is not a lack of data. It is that operational data is fragmented, planning workflows are manual, and exceptions are not converted into structured, reviewable actions.

Common pain points:

- Inventory visibility is delayed or inconsistent across locations.
- Replenishment decisions depend on spreadsheet logic and planner memory.
- Supplier risk is discovered after delays already affect orders.
- Forecasting lacks near-term demand signals and exception explanations.
- Warehouse and purchase-order work is not tied to a unified exception queue.
- Leaders cannot see service-level, working-capital, and risk tradeoffs in one view.

## 2. Solution Summary

Waxis Supply Chain & Inventory Automation is an AI-assisted operations platform for inventory-heavy teams. It connects ERP, WMS, order, supplier, and external demand data into a governed operating layer that detects risks, recommends replenishment actions, explains exceptions, and coordinates human approvals.

The solution combines:

- Inventory health dashboard
- Demand sensing and forecast assist
- Replenishment queue
- Supplier lead-time and risk monitoring
- SKU exception management
- Warehouse task and order-flow visibility
- Scenario simulation and what-if analysis
- AI planner assistant with citations and approval workflows

## 3. Research-Backed Product Principles

1. Supply chain AI should combine visibility, prediction, optimization, and workflow execution.
2. AI should not replace planners blindly; it should highlight exceptions, explain drivers, and prepare actions for review.
3. Demand sensing should incorporate current signals, not only historical sales.
4. Replenishment must be grounded in service level, lead time, forecast error, inventory position, and business constraints.
5. Autonomous workflows require clear approval gates because inventory and purchasing actions affect cash, customer promises, and supplier relationships.
6. AI recommendations must show source data, confidence, assumptions, and impact.
7. Data quality issues should be surfaced as planning risks, not hidden under model output.

## 4. Market And Technology Signals

- SAP Integrated Business Planning highlights AI-powered forecasting, demand sensing, supply planning, what-if simulations, alerts, and inventory optimization.
- Oracle Fusion Cloud SCM 26B emphasizes built-in AI and agentic applications that help supply chains respond faster, automate manual work, and improve decisions across planning, manufacturing, logistics, and order management.
- Oracle's 2026 AI agents for SCM include planning cycle coordination and component replacement analysis embedded in supply chain processes.
- AWS supply chain guidance emphasizes AI-powered demand sensing that uses near-real-time data and external factors to detect demand shifts.
- Blue Yonder's 2026 Supply Chain Compass describes a shift from fragmented processes and point solutions toward integrated, data-driven, AI-shaped supply chain strategies.

## 5. Target Customers

### Primary

- Manufacturers, distributors, retailers, wholesalers, e-commerce operators, and trading companies.
- Companies with 1,000-100,000 SKUs, multiple warehouses, or recurring stockout/overstock problems.
- Teams using ERP/WMS systems but still relying on spreadsheets for daily planning.

### Secondary

- B2B companies with supplier lead-time volatility.
- Companies launching AI control-tower or planner-assist initiatives.
- Operations teams that need inventory, order, and supplier intelligence without replacing their ERP.

## 6. Personas

### Supply Chain Director

Needs visibility into risk, service level, inventory value, supplier performance, and operating bottlenecks.

### Inventory Planner

Needs replenishment recommendations, exception explanations, demand-shift alerts, and scenario comparisons.

### Procurement Manager

Needs supplier risk, PO delay alerts, component replacement options, and approval workflows.

### Warehouse Manager

Needs inbound/outbound visibility, exception queues, task prioritization, and order impact.

### Finance Leader

Needs working-capital impact, inventory aging, overstock risk, and service-level tradeoffs.

### Customer Operations Leader

Needs early warning when inventory risk affects customer commitments.

## 7. Goals

1. Create unified inventory visibility across locations, SKUs, open orders, purchase orders, and supplier commitments.
2. Detect stockout, overstock, slow-moving, obsolete, and supplier-risk situations earlier.
3. Provide replenishment recommendations with explainable assumptions.
4. Use demand sensing and forecast assist to identify near-term demand changes.
5. Coordinate exceptions into a reviewable work queue.
6. Reduce manual spreadsheet planning and repeated data exports.
7. Improve service level, inventory turns, and planning cycle speed.

## 8. Non-Goals

- The product will not replace ERP, WMS, TMS, or APS systems in MVP.
- The product will not place purchase orders autonomously without configured approval.
- The product will not guarantee forecast accuracy where historical and current data quality is poor.
- The product will not optimize every supply chain constraint in MVP.
- The product will not support complex manufacturing finite-capacity scheduling in MVP.

## 9. Product Scope

### MVP

- ERP/WMS/order data connector framework.
- SKU-location inventory health dashboard.
- Open PO, sales order, and inbound/outbound visibility.
- Replenishment recommendation queue for selected SKU/location groups.
- Stockout, overstock, and slow-moving inventory alerts.
- Supplier lead-time tracking and late PO alerts.
- AI explanation for exceptions and recommended next action.
- Planner approval workflow and action log.
- Basic demand forecast assist using historical sales and configured business rules.

### V1

- Demand sensing with external or near-real-time signals where available.
- Scenario simulation for service level, lead time, forecast demand, and order changes.
- Supplier risk scoring and communication draft generation.
- Warehouse exception queue tied to SKU/customer impact.
- Inventory policy tuning: safety stock, reorder point, min/max, days of supply.
- Multi-echelon visibility across warehouse, store, and supplier nodes.
- AI planner chat over governed supply chain data.

### Future

- Automated purchase requisition creation with approval.
- Component substitution and BOM impact analysis.
- Transportation disruption and ETA prediction.
- Autonomous replenishment for low-risk SKUs.
- Integration with customer operations AI for inventory-aware customer promises.
- Digital twin and optimization solver integration.

## 10. Core User Stories

1. As an inventory planner, I want to see stockout risk by SKU and location, so that I can act before customer orders are missed.
2. As an inventory planner, I want replenishment recommendations with assumptions, so that I can approve or adjust them confidently.
3. As a supply chain director, I want inventory health by category, warehouse, supplier, and customer impact, so that I can prioritize resources.
4. As a procurement manager, I want late PO and supplier lead-time alerts, so that I can escalate early.
5. As a warehouse manager, I want exception tasks prioritized by customer and inventory impact, so that my team works on the right issues first.
6. As a finance leader, I want overstock and aging inventory visibility, so that working capital is managed.
7. As a planner, I want the AI assistant to explain why a SKU is at risk, so that I can trust or challenge the recommendation.
8. As a planner, I want to compare scenarios, so that I understand the service-level and inventory-cost tradeoff.
9. As a procurement manager, I want supplier communication drafts, so that I can quickly request updated ETAs or alternatives.
10. As an admin, I want approval rules for PO and replenishment actions, so that automation stays controlled.
11. As an operations leader, I want weekly planning-cycle reports, so that we can measure forecast error, stockout risk, and actions taken.
12. As a customer operations leader, I want alerts when inventory risk affects key accounts, so that we can communicate proactively.
13. As a data owner, I want data-quality flags, so that planning decisions do not depend on stale or invalid data.
14. As a planner, I want AI to identify repeated exception patterns, so that root causes can be fixed.
15. As a system admin, I want connector health monitoring, so that missing syncs do not silently corrupt planning output.

## 11. Functional Requirements

### 11.1 Data Integrations

- FR-001: Connect to ERP for SKUs, locations, inventory balances, purchase orders, sales orders, suppliers, customers, and item costs.
- FR-002: Connect to WMS for on-hand, allocated, inbound, outbound, pick/pack/ship status, and warehouse tasks.
- FR-003: Connect to demand sources such as sales orders, forecasts, e-commerce feeds, CRM opportunities, or uploaded files.
- FR-004: Support CSV/SFTP ingestion for clients without APIs.
- FR-005: Track source freshness, sync errors, schema changes, and data completeness.

### 11.2 Inventory Health

- FR-010: Calculate inventory position by SKU-location: on hand, allocated, available, inbound, outbound, backordered, and projected.
- FR-011: Calculate days of supply, reorder point, safety stock, stockout date, excess quantity, aging bucket, and inventory value.
- FR-012: Classify SKUs by velocity, margin, service-level target, supplier risk, and strategic importance.
- FR-013: Display risk by location, SKU, category, supplier, customer, and planner.
- FR-014: Provide drill-down from executive view to source transactions.

### 11.3 Forecast And Demand Sensing

- FR-020: Provide baseline demand forecast using historical demand and configured seasonality.
- FR-021: Support forecast override and annotation by planners.
- FR-022: Detect demand anomalies, trend changes, and order spikes.
- FR-023: In V1, incorporate near-real-time signals where available, such as order velocity, promotions, weather, market signals, customer commitments, or web demand.
- FR-024: Track forecast accuracy and bias by SKU, category, location, and planner.

### 11.4 Replenishment Recommendations

- FR-030: Generate replenishment recommendations using demand forecast, service-level target, lead time, inventory position, minimum order quantity, pack size, supplier constraints, and current open POs.
- FR-031: Provide recommendation reason, assumptions, confidence, and expected impact.
- FR-032: Support approve, edit, defer, reject, and comment actions.
- FR-033: Generate draft purchase requisitions or transfer recommendations after approval where integrated systems allow.
- FR-034: Record human decisions for learning and audit.

### 11.5 Supplier Risk

- FR-040: Track supplier lead time, fill rate, late PO rate, quality flags, and communication history.
- FR-041: Alert when supplier delays affect stockout risk or customer commitments.
- FR-042: Recommend escalation, expedite, split order, substitute supplier, or adjust demand promise where data supports it.
- FR-043: Generate supplier email drafts with PO context and requested action.

### 11.6 Exception Management

- FR-050: Maintain a unified exception queue across stockout, overstock, late PO, demand spike, inventory mismatch, blocked warehouse task, and data-quality issue.
- FR-051: Prioritize exceptions by impact, urgency, confidence, value, customer importance, and due date.
- FR-052: Assign exceptions to owners and teams.
- FR-053: Track status, decision, action taken, and resolution outcome.
- FR-054: Summarize exception trends and repeated root causes.

### 11.7 AI Planner Assistant

- FR-060: Answer natural-language questions over governed inventory, order, supplier, and forecast data.
- FR-061: Provide source-backed answers and calculations.
- FR-062: Explain recommendations in business language.
- FR-063: Draft communications and action summaries.
- FR-064: Refuse or escalate actions outside user permissions or approval policy.
- FR-065: Support saved prompts for weekly planning review, supplier review, and inventory-risk review.

### 11.8 Scenario Simulation

- FR-070: Allow planners to simulate demand increase/decrease, lead-time change, supplier delay, service-level target change, and inventory policy change.
- FR-071: Show impact on stockout risk, inventory value, days of supply, purchase quantity, and service level.
- FR-072: Compare current plan vs proposed plan.
- FR-073: Save scenarios with assumptions and owner.

### 11.9 Analytics

- FR-080: Provide dashboards for stockout risk, excess inventory, aging inventory, inventory turns, service level, forecast accuracy, supplier performance, and exception closure.
- FR-081: Provide planning-cycle summary with actions taken, recommendations accepted, and risk avoided.
- FR-082: Export reports to CSV/PDF and share scheduled summaries.

## 12. Non-Functional Requirements

- NFR-001: Inventory health calculations should refresh within agreed sync windows and show data timestamp.
- NFR-002: Recommendation explanations must show key assumptions and source data.
- NFR-003: The system must support role-based permissions for cost, supplier, customer, and inventory data.
- NFR-004: Planning actions must be idempotent where integrated systems support writes.
- NFR-005: The exception queue must remain usable with at least 100,000 active SKU-location combinations.
- NFR-006: Every recommendation and approval must be auditable.
- NFR-007: If a connector fails, dashboards must visibly mark stale data.

## 13. Data Model Concepts

- SKU
- Location
- Inventory Balance
- Inventory Position
- Supplier
- Purchase Order
- Sales Order
- Transfer Order
- Warehouse Task
- Demand Signal
- Forecast
- Inventory Policy
- Replenishment Recommendation
- Supplier Risk Signal
- Exception
- Scenario
- Approval Event
- Audit Event

## 14. Key Workflows

### Daily Planning Review

1. Planner opens inventory health dashboard.
2. System highlights top stockout, overstock, supplier, and data-quality exceptions.
3. Planner reviews AI explanations and recommendations.
4. Planner approves, edits, defers, or rejects each action.
5. Approved actions create drafts or updates in connected systems.
6. Outcomes are logged for weekly review.

### Supplier Delay

1. PO ETA changes or delay is detected.
2. System identifies affected SKUs and customer orders.
3. AI recommends expedite, partial shipment, alternate supplier, transfer, or customer-risk alert.
4. Procurement approves communication or action.
5. Status and impact are tracked.

### Demand Spike

1. Demand anomaly is detected.
2. System compares forecast, sales orders, inventory position, and lead time.
3. AI proposes replenishment adjustment and explains assumptions.
4. Planner runs scenario and approves or rejects.

## 15. Analytics And KPIs

### Operational

- Stockout risk count
- Stockout incidents
- Excess inventory value
- Aging inventory value
- Inventory turns
- Days of supply
- Backorder count
- Exception closure time
- Planner action acceptance rate

### Forecast And Planning

- Forecast accuracy
- Forecast bias
- Demand anomaly precision
- Replenishment recommendation acceptance rate
- Planning cycle duration
- Scenario usage

### Supplier

- Supplier on-time delivery
- Lead-time variance
- Late PO risk
- Fill rate
- Expedite rate

### Financial

- Working capital tied in inventory
- Inventory carrying cost proxy
- Cost of stockout proxy
- Value of risk avoided

## 16. Security And Governance Requirements

- Enforce role-based access to supplier pricing, item cost, customer commitments, and financial impact.
- Require approval for purchase, transfer, supplier substitution, and customer promise actions.
- Log all recommendations, changes, approvals, and system writes.
- Support separation of duty between recommendation author, approver, and executor where required.
- Redact sensitive supplier/customer information in AI traces when configured.
- Flag low-confidence recommendations instead of presenting them as deterministic decisions.
- Use AI output as decision support unless autonomy is explicitly enabled for low-risk workflows.

## 17. UX Requirements

### Control Tower

- Executive inventory health score
- Stockout, overstock, supplier, and warehouse risk panels
- Top exceptions
- Trend charts
- Drill-down by SKU, supplier, location, category, and customer impact

### Planner Workbench

- Exception queue
- Recommendation card with impact, assumptions, confidence, and source data
- Approve/edit/defer/reject actions
- Scenario side panel
- AI explanation and chat

### Supplier View

- Supplier scorecard
- Late PO timeline
- Lead-time variance
- Affected SKUs and orders
- Draft communication

### Admin Console

- Data connector setup
- Inventory policy settings
- Forecast settings
- Approval rules
- Role mapping
- Data-quality thresholds

## 18. Implementation Decisions

- Start as a decision-support and workflow layer on top of existing ERP/WMS systems.
- Use SKU-location as the primary operational grain for inventory health.
- Keep recommendation generation separate from action execution.
- Require explicit approval for any write-back in MVP.
- Store planner decisions as training and evaluation data.
- Show source timestamps on every planning view.
- Model data-quality issues as first-class exceptions.

## 19. Testing Decisions

- Validate calculations with fixed fixture datasets for inventory position, days of supply, reorder point, and stockout date.
- Test connector freshness and stale-data warnings.
- Test approval flows for purchase and transfer actions.
- Backtest forecast and replenishment recommendations against historical periods.
- Test scenario output with controlled assumptions.
- Test role permissions for cost, supplier, and customer data.
- Test AI explanations for source-grounding and refusal when data is insufficient.

## 20. Rollout Plan

### Phase 0: Data And Process Mapping

- Identify source systems and data owners.
- Select pilot SKU groups and locations.
- Define inventory policies and approval rules.
- Create baseline KPIs.

### Phase 1: Visibility And Exceptions

- Launch inventory health dashboard and exception queue.
- Enable late PO, stockout, overstock, and data-quality alerts.
- Keep recommendations advisory.

### Phase 2: Recommendation Workflow

- Add replenishment queue, AI explanations, and planner decisions.
- Add supplier communication drafts.
- Start weekly planning review.

### Phase 3: Scenario And Automation

- Add scenario simulation.
- Add approved write-back for selected low-risk actions.
- Expand to more SKU groups and locations.

## 21. Risks And Mitigations

| Risk | Mitigation |
| --- | --- |
| Bad data creates bad recommendations | Data-quality exceptions, source timestamps, confidence scoring, and human approval |
| Planners distrust AI | Explain assumptions, show sources, track accepted/rejected decisions, and start advisory-only |
| ERP integration is slow | Support read-only CSV/SFTP ingestion for MVP and prioritize high-value APIs |
| Recommendations increase working capital | Show service-level and inventory-value impact before approval |
| Supplier actions have commercial sensitivity | Require approval and restrict supplier/cost fields by role |
| Forecast model overfits historical data | Track forecast accuracy and bias, include planner overrides, and backtest |

## 22. Open Questions

1. Which ERP/WMS platforms should be first-class integrations?
2. What SKU/location volume should MVP support for pilot clients?
3. Which inventory policy formulas should be configurable vs fixed?
4. Should demand sensing include external data in MVP or V1?
5. What approval threshold should apply to purchase recommendations?
6. Should customer-impact alerts integrate directly with Sales & Customer Service AI?

## 23. Acceptance Criteria

- A planner can see inventory health by SKU-location with source timestamps.
- The system identifies stockout, overstock, slow-moving, late PO, and data-quality exceptions.
- The system generates replenishment recommendations with source-backed assumptions.
- A planner can approve, edit, defer, or reject recommendations and leave comments.
- Supplier delay alerts show affected SKUs and customer/order impact.
- Manager dashboards show risk trends, forecast accuracy, supplier performance, and actions taken.
- Write-back actions require configured approvals.

## 24. Research References

- SAP Integrated Business Planning: https://www.sap.com/products/scm/integrated-business-planning.html
- Oracle Supply Chain Management and 26B AI positioning: https://www.oracle.com/scm/
- Oracle AI Agents for SCM announcement, February 10, 2026: https://www.oracle.com/news/announcement/oracle-ai-agents-help-boost-supply-chain-efficiency-and-strengthen-resiliency-2026-02-10/
- AWS AI-powered demand sensing overview: https://aws.amazon.com/executive-insights/content/ai-powered-demand-sensing/
- Blue Yonder 2026 Supply Chain Compass: https://blueyonder.com/resources/supply-chain-compass-how-supply-chain-leaders-are-navigating-complexity
- NIST AI Risk Management Framework: https://www.nist.gov/itl/ai-risk-management-framework
- OWASP Top 10 for LLMs and Gen AI Apps 2025: https://genai.owasp.org/llm-top-10/

