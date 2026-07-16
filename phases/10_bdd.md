# Behavior-Driven Development

## Template

Read [Templates/10.01_bdd_scenarios.md](Templates/10.01_bdd_scenarios.md) before generating [10.01_bdd_scenarios.md](10.01_bdd_scenarios.md).

## Required topics

Cover `bdd.happy_path`, `bdd.exception_handling`, `bdd.concurrency`, and `bdd.abuse_cases`. Build each scenario iteratively in Given/When/Then form.

> **Validation Note:** If [02.01_5w1h_discovery.md](02.01_5w1h_discovery.md) exists in the current interview directory (`destination_path`), actively cross-reference its answers. The *Who* (Actors), *How* (Happy Path), and *Why* of the 5W1H are the exact anatomy of a BDD user story. Proactively suggest the `Feature` and `Scenario` elements based almost entirely on the Phase 02 answers. Additionally, if [06.02_cqrs_specs.md](06.02_cqrs_specs.md) exists, ensure that BDD Scenarios directly materialize the Specific Business Rules and validate the input limits/expected errors (e.g. validation errors, business rule conflicts) from the CQRS Specifications. If [05.02_ddd_strategic_design.md](05.02_ddd_strategic_design.md) exists, prioritize and expand the scenarios for Bounded Contexts classified as Core Domains, as they contain the heart of the business logic.


