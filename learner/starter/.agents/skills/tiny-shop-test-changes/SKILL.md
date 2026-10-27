---
name: tiny-shop-test-changes
description: Use when changing or extending Tiny Shop Checkout functionality. Add or update focused tests and run the complete project test suite after the change.
---

# Tiny Shop Checkout Functional Changes

When implementing a requested change to checkout behavior or another user-visible function in this project:

1. Read the relevant implementation and tests before editing. Keep the change within the requested scope and preserve existing behavior unless the request changes it.
2. Add or update focused tests in `tests/test_checkout.py` for the new behavior and relevant edge or boundary cases. Use the standard-library `unittest` framework and the existing `test_*` naming style.
3. After implementation and test updates, run the entire defined suite from the project root:

   ```sh
   python3 -m unittest discover -s tests -v
   ```

4. Review the result. If any test fails, diagnose and fix failures caused by the change, then rerun the full suite. Do not report success unless the command exits successfully. If the runtime is unavailable or tests cannot run, report that clearly and include the reason.
5. In the completion report, summarize the behavior change, list changed files, and give the test command and its result. Mention any unverified behavior or remaining issue.

Do not add third-party dependencies or broaden the change beyond the request. This project intentionally uses floats for its teaching contract; retain that contract unless the task explicitly asks to change it.
