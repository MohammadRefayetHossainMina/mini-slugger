# Bug Specification (BUG_SPEC.md)

**Issue Reference:** #12  
**Investigator:** Mohammad Refayet Hossain  
**Date:** 2026-11-03  

---

### 1. Current Behavior
Describe the exact failure mode observed in the system right now. Include error outputs, status codes, or stack trace snippets if applicable.
- **Observed Outcome:** Passing input strings containing trailing whitespace or punctuation (e.g., `"Hello, World!"` or `"Hello World! "`) leaves an unwanted trailing hyphen on the generated slug.
- **Failure Symptoms:** Malformed slug outputs containing dangling trailing hyphens.
- **Observed Logs / Output:**
  ```text
  AssertionError: 'hello-world-' != 'hello-world'
  - hello-world-
  + hello-world