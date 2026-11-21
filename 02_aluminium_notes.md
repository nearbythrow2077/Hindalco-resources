# Indian aluminium: configuration and analysis notes

## Boundary and evidence map

Hindalco's Indian aluminium business spans mining, refining, primary metal and downstream conversion [E002–E004; S06]. Analyse it separately from Novelis before drawing group-level conclusions. The selected facilities and reported connections are in `12_facilities.csv` and `13_material_flows.csv`; those tables are the factual network record.

The main transformation is **bauxite → alumina → primary aluminium → cast feedstock → rolled/extruded/foil/fabricated products**. It branches: specialty alumina/hydrates can be sold without smelting; primary metal can be sold without Hindalco downstream conversion; rolling, extrusion and foil are not stages through which every tonne passes. This makes the chain a branching production network, not one universal linear route [E013–E017; S11; S22; S23; S37].

### Verified links and limits

Use E005–E010 for mine/refinery/smelter/downstream connections. Baphlimali–Utkal is the clearest dedicated inbound lane. Mahan and Hirakud have disclosed refinery sources. Historical BTAP evidence is preserved as historical rather than used to assert current modal allocation. Do not create a complete all-to-all plant network merely because common ownership makes it plausible.

Renukoot illustrates co-located processing; Mahan illustrates supporting carbon and power capacity [E011–E012; S12; S13; S50]. In SCM terms, effective capacity depends on the limiting stage and supporting inputs, not simply the largest furnace nameplate.

## Input and product configuration

| Input or stream | SCM role and evidence status | Required follow-up |
|---|---|---|
| Bauxite | Captive upstream material; disclosed links in E005–E006 | Grade variability, mine availability, allocation and stock cover |
| Caustic soda, steam, furnace oil | Refinery inputs identified in Renukoot technical source [E061; S50] | Supplier identity, consumption norms, contract and substitution options |
| Alumina | Intermediate input and external saleable product | Grade, moisture, internal allocations, merchant-sale commitments |
| Electricity and carbon systems | Smelting support; plant evidence in E012 and E062 | Energy reliability, carbon-material sourcing, maintenance constraints |
| Alloying additions and process consumables | General metallurgical input category, not a verified Hindalco supplier list | Exact BOM, criticality and supplier concentration |
| Red mud | Historical cement-use arrangement [E018; S28] | Current utilisation, transport economics and environmental specifications |
| Customer/process scrap | Relevant reverse-flow category; do not transfer Novelis loop evidence automatically to every India plant | Collection ownership, alloy segregation, recovery and remelting routes |

A process BOM should use material-specific conversion yields. Do not apply a memorised ore-to-metal ratio as a measured Hindalco yield. Refineries also differ in their product mix, so a tonne of hydrate capacity is not automatically comparable with a tonne of calcined alumina capacity.

## Efficiency–responsiveness trade-offs

**Upstream facilities:** analytical emphasis is reliable high-volume production, energy availability, maintenance and economical bulk transport. Integration can improve availability and reduce interface costs, but may also tie the business to fixed assets and common disruption points. Verify total costs before claiming that integration is always cheaper.

**Downstream facilities:** separate generic feedstock from alloy-, gauge-, surface- and customer-specific finishing. Holding common intermediate stock may offer pooling or postponement benefits if technical constraints permit. Finishing already fixes some attributes irreversibly; postponement is an option to evaluate, not an established company practice.

**Customer-engineered products:** the Mahindra enclosure relationship provides a concrete design-collaboration example [E015; S27]. Its SCM significance is that design changes, qualification and assembly schedules can dominate service requirements even when metal supply is secure. Product-level strategic-fit hypotheses are recorded in the product CSV.

**New capacity:** FRP and foil create coupled processing requirements [E016; S37]. For planning, separate mechanical commissioning, saleable yield, customer approval and sustainable operating rate. A downstream investment can shift the bottleneck into feedstock, finishing, testing or dispatch.

## Transportation and stock-location questions

Dedicated conveyors or rail can suit stable bulk flows; road can offer smaller lots and route flexibility. This is a general trade-off, not a verified cost ranking for every lane. Evaluate freight together with transit stock, frequency, handling losses and delivery reliability. The Aditya–Hirakud EV corridor is a specific reported interplant example [E038; S03], not evidence that the whole network uses electric trucks.

At each candidate stock point ask: what uncertainty does this buffer protect against, what downstream products can use it, and what conversion/transport time remains? Pooling at a refinery or casting stage reduces duplication only if grades are substitutable and replenishment is fast enough.

## Quantitative cautions

Use `15_metrics.csv` for dated numbers. The four selected smelter website capacities sum to a different figure from the FY26 group summary: do not silently force reconciliation. Refinery capacity, alumina production, metal production, shipments and downstream sales answer different questions. The conflict register records all material discrepancies.

For later analysis prioritise a mass-balance and capacity table by stage, energy-adjusted effective capacity, inbound lead-time variability, product-family demand, and customer OTIF. These data would permit a defensible strategic-fit assessment; the public figures alone cannot establish optimal inventory or service policy.
