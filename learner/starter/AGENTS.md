# Project Instructions

## Project

This is a small teaching project for a shop checkout. Its public calculation API is `src/checkout.py:calculate_total(items)`, which sums each item's `price * quantity` and returns a `float`. Items use the existing `name`, `price`, and `quantity` fields. An empty cart returns `0.0`. `sample_orders.json` is example data; the checkout function does not read it. See `README.md`, `task_card.md`, and `Agent.md` for the lab setup, tasks, and current behavior.

## Technology and architecture

- Use Python and the standard library; the project has no third-party dependencies or build system.
- Keep the implementation small and organized around the existing `src/` module and `tests/` suite.
- Keep calculation logic in `src/checkout.py`. Put presentation or formatting helpers in a separate function when a task asks for them.
- Preserve the established float-based contract unless a task explicitly changes it. Do not silently migrate money handling to another representation.

## Conventions

- Follow the surrounding Python style: four-space indentation, descriptive `snake_case` names, and focused functions.
- Preserve the current item schema and existing calls when extending the API, unless the requested task explicitly changes them.
- Keep sample data synthetic and in its existing JSON format. Avoid unrelated cleanup or scope expansion.
- Add focused `unittest` cases alongside related tests in `tests/test_checkout.py`; name test methods `test_*`.

## Testing

Run checks from the `starter/` directory:

```sh
python3 -m unittest discover -s tests -v
```

For behavior changes, add or update focused tests for the requested behavior and relevant boundary cases, then run the full command above. If the command cannot run in the available environment, report that and the reason; do not claim the checks passed.

## Avoid

- Do not add dependencies, frameworks, databases, servers, or a build system for this small project.
- Do not change the item schema, remove or rename the public `calculate_total` function, or break existing calls without an explicit requirement.
- Do not add validation, discounts, rounding, formatting, or other behavior unless the task asks for it.
- Do not edit lab comparison materials or sample data unless the task requires it.
- Do not commit credentials, real customer data, generated artifacts, or environment-specific files.

## Completion report

After completing a task, report:

- A concise summary of the behavior changed.
- The files changed and the reason for each.
- The test command run and its result, or why it could not be run.
- Any relevant assumptions, limitations, or follow-up needed.
