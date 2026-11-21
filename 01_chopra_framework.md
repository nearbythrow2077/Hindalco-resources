# Chopra framework applied to this research

**Framework source:** Sunil Chopra, _Supply Chain Management: Strategy, Planning and Operation_, seventh-edition publisher contents [S01]. Full-text page citations require the group's actual edition. Explanations and case applications here are original analytical notes.

## Central question and knowledge structure

The central question is: **How should the network, operating policies and relationships match customer requirements while maximising total supply-chain surplus?** High tonnage, low local cost or high plant utilisation alone cannot answer it.

1. Customer needs and competitive strategy determine required cost, delivery, quality, variety and innovation.
2. These requirements create **implied demand uncertainty**; uncertain inputs, yields and disruptions add **supply uncertainty**.
3. The chain needs a suitable position on the **efficiency–responsiveness spectrum**.
4. The six drivers implement that position: facilities, inventory, transportation, information, sourcing and pricing.
5. Decisions across stages must be coordinated because local objectives can undermine total performance.
6. Financial and operational measures test whether the chosen configuration actually creates value.

### Product configuration versus supply-chain configuration

Product configuration means material, alloy/grade, geometry, processing and customer-specific requirements. Supply-chain configuration means where and by whom the stages are performed, their capacities, transport links, ownership, sourcing and customer channels. A copper rod's diameter is product configuration; allocating its manufacture between Dahej and Asoj is a network decision. A battery enclosure's design may impose engineering coordination and qualification requirements beyond metal availability.

## Chapter crosswalk: seventh edition

| Chapters | Concept | Hindalco research use |
|---|---|---|
| 1–2 | Supply chain; surplus; strategic fit | Boundaries and product segmentation |
| 3 | Drivers and performance measures | Six-driver evidence and proposed KPIs |
| 4–6 | Distribution; network design; global networks | Refineries/smelters; warehouses; ports; global rolling; tariffs |
| 7–9 | Forecasting; aggregate planning; S&OP | Demand plans by product, energy/feedstock and bottleneck feasibility |
| 10 | Coordination | Shared plans, incentives, information and contracting |
| 11–13 | Cycle inventory; safety inventory; availability | Batch sizes; supply buffers; service-cost trade-offs |
| 14 | Transportation | Bulk rail/sea; dedicated conveyor; road; alternative gateways |
| 15 | Sourcing | Captive versus purchased inputs; supplier risk and contracts |
| 16 | Pricing and revenue management | Metal indexation, conversion value and spot tenders |
| 17 | Sustainability | Recycling, emissions, waste utilisation and responsible sourcing |

Publisher-listed online IT material also informs the information-driver vocabulary. Do not invent chapter/page numbers for another edition.

## Three decision horizons

| Horizon | Decision | Example/application |
|---|---|---|
| Strategy/design, usually years | Facility location, capacity, ownership, technology, supplier network | Smelter or recycling investment; new rolling mill; captive gateway |
| Planning, usually months | Allocation, aggregate output, supplier commitments, transport capacity, inventory targets | S&OP aligning product demand with feedstock and bottleneck capacity |
| Operations, days or weeks | Order promising, batch sequencing, dispatch, replenishment and exception handling | Assign an available qualified coil to an order; reschedule a delayed rail consignment |

“Usually” is a conceptual distinction, not a verified Hindalco meeting calendar. A strategic expansion should not be counted as available operational capacity.

## Process views

**Cycle view:** customer ordering; replenishment between distribution/conversion stages; manufacturing; procurement. Hindalco's B2B chains need not contain a retailer. Internal movements still have replenishment requirements even without external invoices.

**Push/pull view:** push processes anticipate demand; pull processes respond to a specific order. Proposed decoupling points appear in `14_products_and_strategic_fit.csv`. Continuous smelting plausibly needs forecast-based aggregate planning, while grade/size-specific finishing may respond to orders. These are hypotheses: an actual make-to-stock/make-to-order boundary requires order-release and inventory evidence.

**Macro-process view:** SRM connects procurement with suppliers; ISCM connects demand, production, inventory and fulfilment inside the firm; CRM connects the firm with customer requirements and orders. ERP is an information enabler across these processes, not a substitute for their ownership or incentives.

## Core analytical equations

These are analytical tools, **not calculated Hindalco operating policies**. Use consistent units, periods and perimeters.

- **Supply-chain surplus = customer value − total supply-chain cost.** Hindalco EBITDA is a firm-level measure; it is not total chain surplus.
- **Total landed cost** includes acquisition, conversion where relevant, transport, handling, duties, holding, quality losses and disruption exposure. Avoid counting the same cost twice when an invoice already includes freight or conversion.
- **Inventory turns = annual cost of goods sold / average inventory value.** Inventory days = 365 / turns. Do not substitute revenue for cost of goods sold without changing the interpretation.
- **Cash-to-cash days = inventory days + receivable days − payable days.** A supplier-finance arrangement can change different parties' cash timing differently; an improved buyer metric is not automatically a total-chain improvement.
- **Little's law: average inventory = throughput rate × average flow time**, for a stable system and consistent boundary. Suitable for testing process/WIP relationships; not enough to estimate safety stock.
- **EOQ = sqrt(2DS/H)**, where D is annual demand, S ordering/setup cost and H annual holding cost per unit. Its assumptions include stable demand and simplified replenishment. Furnace campaigns, quality, transport lots and joint products can make the simple EOQ model inadequate.
- **Reorder point = expected demand during replenishment lead time + safety stock.** Under constant lead time L, independent period demand with standard deviation σd and a normal approximation: SS = zσd√L. If independent lead time is also random: SS ≈ z√(E[L]σd² + μd²Var[L]). Correlated disruptions, seasonality and non-normal tails need other models. Cycle service level and fill rate are different measures; z does not directly specify fill rate.
- **Capacity utilisation = actual output / capacity on the same process, unit and time basis.** Shipments can include inventory release, outside purchases or other products, so shipments/nameplate is not necessarily utilisation.
- **Material balance:** output metal + metal in residues/losses + increase in metal inventory = input contained metal. Concentrate tonnes, alumina tonnes and copper/aluminium metal tonnes are not interchangeable.
- **Bullwhip indicator = variance of upstream orders / variance of downstream demand**, with matched periods and units. A high inventory figure or a shortage alone does not establish bullwhip.

For copper smelting, a useful economic decomposition is treatment/refining income plus eligible metal/by-product contributions, less processing, energy, logistics and financing costs. Payability, deductions, penalties, price-period rules and recovery terms require the actual contract. Do not present a generic formula as Hindalco's agreement.

## Strategic-fit hypotheses to test

| Segment | Likely emphasis | Evidence needed before making a firm conclusion |
|---|---|---|
| Primary aluminium and standard copper | Efficient, reliable bulk supply | Demand volatility; service promise; batch and transport economics |
| Specialty alumina; precision extrusions; copper tubes | Grade/quality matching and selected responsiveness | Qualification times; SKU mix; changeover cost; rejection and service data |
| EV battery enclosures and automotive sheet | Engineering integration and delivery reliability | Customer schedules; design changes; traceability; alternate-source approvals |
| Recycled metal loops | Cost-efficient recovery with quality-responsive sorting/blending | Return variability; alloy contamination; collection and recovery yield |

These are differentiated policy hypotheses, not a simplistic assertion that every commodity chain is predictable or every downstream product is highly uncertain.
