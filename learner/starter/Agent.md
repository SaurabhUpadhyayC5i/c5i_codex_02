# Project Overview

## Purpose

This is a small teaching example for a shop checkout. It calculates a cart total from a sequence of line items and is used in a lab about project-specific agent instructions.

## How it works

- `src/checkout.py` defines `calculate_total(items)`.
- Each item is expected to provide `name`, `price`, and `quantity` fields. The calculation uses `float(item["price"]) * int(item["quantity"])` for each item and returns the sum as a float.
- An empty sequence returns `0.0`.
- The implementation does not currently validate item fields or apply discounts.
- `sample_orders.json` contains example order lines; the checkout function itself accepts Python data and does not load this file.

## Tech stack

- Python; no third-party packages are required.
- Tests use the Python standard library `unittest` framework.
- There is no build system, web framework, database, or application server in this starter.

## Verification

Run from the `starter` directory:

```sh
python3 -m unittest discover -s tests -v
```

The tests cover a single line item, multiple items, an empty cart, and the float return type.

## Project files

- `src/checkout.py` — checkout calculation.
- `tests/test_checkout.py` — visible unit tests.
- `sample_orders.json` — synthetic sample order data.
- `task_card.md` — lab tasks for discount support and total formatting.
- `comparison_worksheet.md` — worksheet for comparing instruction-guided runs.
- `README.md` — lab setup, workflow, and submission instructions.
