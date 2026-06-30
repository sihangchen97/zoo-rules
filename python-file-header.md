# python-file-header — Strict File Header Rule

## Rule

**All non-trivial Python files must complete their overview within the first 15 lines.**

AI tools read the first 15 lines for overview, then dive deeper only when needed. If a file can't be described in 15 lines, consider splitting it.

## Skip Trivial Files

Files that are a single function, thin wrapper, or obvious utility don't need this header. The header must earn its place — only add it when the file has enough content to justify an overview.

## Mandatory Structure

Every header must answer three questions:

1. **What does this file contain?** — Core classes/functions only. Omit helpers and constants.
2. **What can it do?** — Key capabilities, configurable behaviors, important parameters.
3. **How do you use it?** — Registry name, usage pattern, input/output contract.

Use a module-level docstring. Keep it within 15 lines including blank lines.

## Example

```python
"""
DINOv2 ViT backbone for feature extraction.

Contains:
- DINOv2Backbone: Backbone with optional multi-layer feature concatenation

Capabilities: feature_layers param controls which layers output; supports
              intermediate feature extraction for dense prediction tasks.

Usage: Register as "backbone/dinov2", model=dinov2_vits14
Input/Output: [B, 3, H, W] -> [B, C, H//14, W//14]
"""
```

## Violations

- **Too brief** — `"""Backbone."""` says nothing useful.
- **Too long** — Past 15 lines, the header loses its purpose. Ask user and suggest split the file.
- **Lists helpers** — Don't enumerate constants, utility variables, or internal helpers.

## Checklist

- [ ] Does the first 15 lines answer "what does this file contain?" (core items only)
- [ ] Does the first 15 lines answer "what can it do?" (key capabilities)
- [ ] Does the first 15 lines answer "how do you use it?"
- [ ] Is the file complex enough to warrant a header?
- [ ] Total line count within 15 (including blank lines)?

## Exceptions

- `__init__.py`: Listing exports is sufficient
- Pure test files: One-line purpose is enough
- Single-function files: Skip the header
- Third-party code (`third_party/`): Not enforced
