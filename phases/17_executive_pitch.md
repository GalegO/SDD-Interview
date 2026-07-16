# Executive Summary & Pitch

**Methodology:** Executive Summary & Pitch
**Topics:** 5
**Outputs:** [98.01_executive_summary_business_view.md](98.01_executive_summary_business_view.md); [98.02_marketing_pitch_deck.md](98.02_marketing_pitch_deck.md); [98.03_seo_metadata_plan.md](98.03_seo_metadata_plan.md) (optional)
**Dependencies:** Should be executed after all other methodologies are complete.

## Goal

To provide a business-focused summary of the entire project architecture and key decisions, and translate these technical decisions into a compelling commercial narrative (elevator pitch, target audience, key selling points).

## Topics

### `exec_summary.generate`

Do not ask any questions in this phase. The Executive Summary is an autonomous synthesis phase.
Read the contents of all completed business, scope, and technical phases in the destination path (including [00.01_initial_discovery_project_briefing.md](00.01_initial_discovery_project_briefing.md), [01.01_bmc_business_canvas.md](01.01_bmc_business_canvas.md), [02.01_5w1h_discovery.md](02.01_5w1h_discovery.md), [03.01_moscow_prioritization.md](03.01_moscow_prioritization.md), [04.01_user_request_epic_breakdown.md](04.01_user_request_epic_breakdown.md), and all DDD (`05.xx`), CQRS (`06.xx`), SDD (`07.01`), and EDD (`08.01`) files if they exist). Cross-reference the collected data to automatically draft a comprehensive Executive Summary. Present this complete draft directly to the user for validation and final approval.

### `pitch.target_audience`

Ask the user to define or refine the primary non-technical audience (e.g., investors, end-users, C-level executives) and their main pain points that this project solves.

### `pitch.value_proposition`

Based on the previous answer and the overall project, ask the user to craft a high-impact "Elevator Pitch" (a 30-second summary) that highlights the unique value proposition and the "wow" factor of the product.

### `pitch.key_selling_points`

Ask the user to list 3 to 5 key selling points or marketing hooks that translate the complex architectural features (e.g., speed, security, scalability) into tangible business benefits (e.g., "Zero downtime for customers", "Bank-grade protection").

### `pitch.seo_metadata`

Ask the user if the target platform is geared towards the public web and if they want an optional SEO & Metadata Plan artifact generated to map indexability strategy.

## Completion

When the `exec_summary.generate` topic draft is approved by the user, read [Templates/98.01_executive_summary_business_view.md](Templates/98.01_executive_summary_business_view.md) and generate [98.01_executive_summary_business_view.md](98.01_executive_summary_business_view.md).
When all topics are covered and the final commercial pitch is approved, read [Templates/98.02_marketing_pitch_deck.md](Templates/98.02_marketing_pitch_deck.md) and generate [98.02_marketing_pitch_deck.md](98.02_marketing_pitch_deck.md).
If the user approved the generation of the SEO plan, read [Templates/98.03_seo_metadata_plan.md](Templates/98.03_seo_metadata_plan.md) and generate [98.03_seo_metadata_plan.md](98.03_seo_metadata_plan.md).
