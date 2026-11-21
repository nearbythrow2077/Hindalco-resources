# Data dictionary and conventions

All tables are UTF-8 CSV with a header row and standard quoted fields where necessary. They are research datasets, not a validated operational database. Decimal values use a period; thousands separators are omitted from numeric cells. Empty cells mean unavailable, unverified or not applicable; qualifications distinguish these cases.

## Keys and relationships

| File | Row key | Field meanings |
|---|---|---|
| 10_sources.csv | source_id S## | title; author_publisher; publication_date as disclosed; url; locator; access_status; source_type; scope_and_limitations; access_date |
| 11_evidence.csv | evidence_id E### | business_scope; claim; evidence_class; period_or_asof; source_ids; locator; chopra_concept; qualification |
| 12_facilities.csv | facility_id F## | name; business; location; country; supply_chain_role; status_as_reported; capacity_value/unit/basis; source_ids; evidence_ids; caution |
| 13_material_flows.csv | flow_id L## | from_node; to_node; business; material; flow_type; transport_mode; edge_status; source_ids; evidence_ids; qualification |
| 14_products_and_strategic_fit.csv | product_id P## | business; product_family; customer_need; observed_configuration; recommended_scm_interpretation; candidate_push_pull_boundary; source_ids; evidence_ids; status |
| 15_metrics.csv | metric_id M## | business_scope; metric; value; unit; period; basis; source_ids; locator; caution |
| 16_recent_issues.csv | issue_id I## | business; issue; event_period; status_at_cutoff; observed_mechanism; reported_response; academic_implication; suggested_analysis_not_company_action; source_ids; evidence_ids; limitation |
| 17_swot.csv | swot_id SW## | quadrant; business; analytical_statement; supporting_evidence_ids; source_ids; scm_mechanism; qualification; possible_metric_or_test |
| 19_copper_sourcing.csv | record_id C## | country; relationship_type; period; company_country_red_flag; source_ids; evidence_ids; qualification |
| 20_research_coverage.csv | requirement | research_files; evidence_ids; coverage; remaining_work |

Multi-valued source/evidence fields use semicolons. Facility references F## refer to the facility table; a text endpoint denotes a broader external actor or process category, not an undisclosed named company. Evidence lists identify supporting records, not necessarily every detail in an analyst recommendation. Reference ranges such as E005–E010 in Markdown are inclusive.

## Evidence and status vocabulary

- `reported_fact` / `reported_process`: a source describes the fact/process; independent validation may be absent.
- `historical_fact`, `historical_case`, `historical_contract`, `historical_process_fact`: useful past evidence; do not assume current operation or identical terms.
- `announced_plan` / `announced_process_change`: announcement without verified completion.
- `policy`: expected behaviour, distinct from demonstrated compliance.
- `attributed_management_statement` / `attributed_third_party_statement`: preserve whose assessment it is.
- `certification_body_fact` / `certification_body_finding`: scoped external certification evidence.
- `analyst_inference`: original application of SCM concepts; not a company claim.
- `research_gap`: not found in this review, not proof of nonexistence.
- Mixed labels such as `reported_milestone_and_plan` mean the row explicitly separates an achieved milestone from a future target.

Access status `opened` means the relevant web page/PDF sections were read; it does not imply every page or linked document was audited. `search_excerpt` is weaker evidence. Blocked sources are retained for follow-up and cannot establish unreviewed claims.

## Units, dates and calculations

One kt = 1,000 metric tonnes; one Mt = 1,000,000 tonnes; one INR crore = 10,000,000 rupees. MW measures power capacity; MWh measures energy. Tonnes/year is capacity or an annualised rate, not automatically achieved production. Units/year of fabricated products cannot be summed with tonnes/year of metal.

FY26 ends 31 March 2026; FY27 ends 31 March 2027. Q2 FY27 is July–September 2026; Q1 FY28 is April–June 2027. `undated` is not the access date. Period labels and management targets are deliberately retained as text rather than converted to invented precise dates.

M46 = 100 × 373/487. M47 = 100 × (487/491 − 1). M48 = 100 × (69838/54703 − 1). M49 = 100 × (2809/3025 − 1). These rounded calculations use the same copper segment periods and source table. They are sales-mix and growth calculations, not estimates of process yield, capacity utilisation or causation.

Never sum capacities across successive processing stages, add CCR sales to copper total sales, mix planned and operating capacity, or infer mass shares from value shares. Monetary data remain in original currencies; no exchange-rate conversion has been performed.

## Updating

Keep stable IDs. Add the new dated source first, then update/add evidence and dependent metrics. Preserve superseded historical rows or state the change explicitly. Refresh the research cutoff and annotate any revised scope. Verify references and numeric calculations after every material update.
