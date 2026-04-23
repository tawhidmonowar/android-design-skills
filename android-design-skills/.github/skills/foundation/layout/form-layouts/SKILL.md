---
name: form-layouts
description: Use this skill to create clear, accessible Android forms in Jetpack Compose. It covers field grouping, labels, helper text, validation placement, keyboard behavior, and submit action layout.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - forms
  - text fields
  - validation
  - ime
  - accessibility
---

## Objective

Design forms that feel easy to complete, minimize user error, and remain usable
with the keyboard open.

## Core workflow

1. Group inputs by task and completion order.
2. Reduce the form to only necessary fields and decisions.
3. Place labels, helper text, and validation messaging close to the relevant field.
4. Keep the submit action visible and understandable throughout the flow.
5. Verify focus order, keyboard actions, error states, and small-screen behavior.

## Form rules

- Forms **SHOULD** follow a single clear completion path from top to bottom.
- Related fields **MUST** be grouped into sections with meaningful spacing and headings where needed.
- Required and optional status **MUST** be communicated consistently.
- Error text **MUST** appear near the field it describes.
- Primary submit actions **SHOULD** remain available without requiring users to dismiss the keyboard unnecessarily.

## Layout guidance

- Prefer one-column forms for phones.
- Multi-column forms **SHOULD** be reserved for wide layouts and only when the field relationships are obvious.
- Inline helper text is better than distant explanatory paragraphs.
- Use progressive disclosure for advanced settings instead of exposing everything at once.

## Validation checklist

- The tab and focus order matches the visual order.
- The keyboard does not obscure the current field or CTA.
- Error, loading, and disabled states remain legible.
- The form remains understandable with accessibility font scaling.
