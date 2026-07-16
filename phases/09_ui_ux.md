# UI/UX (Atomic Design)

## Template

Read [Templates/09.01_ui_ux_atomic_design.md](Templates/09.01_ui_ux_atomic_design.md) before generating [09.01_ui_ux_atomic_design.md](09.01_ui_ux_atomic_design.md).

## Required topics

Cover `uiux.responsive_approach`, `uiux.structure_grid`, `uiux.design_tokens`, `uiux.interface_states`, `uiux.accessibility`, `uiux.frontend_security`, and `uiux.references`.

### `uiux.a11y_opt_in` (Bonus)

If the project has a Frontend for the general public, present a grounded recommendation to map Automated Accessibility Tests and WCAG compliance. Explicitly ask the user for the final decision (Yes/No). If Yes, ask the necessary questions and generate `09.02_ui_ux_a11y_tests.md` based on [Templates/09.02_ui_ux_a11y_tests.md](Templates/09.02_ui_ux_a11y_tests.md).

> **Validation Note:** If [00.01_initial_discovery_project_briefing.md](00.01_initial_discovery_project_briefing.md) exists in the current interview directory (`destination_path`), cross-reference the defined Platform. IF the platform warrants UI/UX specific considerations (e.g., Mobile needs touch-targets, CLI needs terminal typography), use it to guide your Atomic Design suggestions. If the project is agnostic or doesn't need UI specifics, do not force these suggestions. Additionally, if [06.02_cqrs_specs.md](06.02_cqrs_specs.md) exists, ensure the Interface States (loading, success, error) and layout inputs map directly to the API Contracts and expected payload fields/error codes defined in the CQRS Specifications.


