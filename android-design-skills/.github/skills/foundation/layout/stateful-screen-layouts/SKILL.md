---
name: stateful-screen-layouts
description: Use this skill to design consistent loading, empty, error, success, and offline layouts in Android apps. It helps each screen state feel intentional rather than like an afterthought.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - loading state
  - empty state
  - error state
  - offline
  - ui states
---

## Objective

Design each major screen state as part of the product experience so users always
understand what is happening and what they can do next.

## Core workflow

1. Enumerate the screen's major states: loading, content, empty, error, offline, success, or blocked.
2. Decide whether each state should replace content, overlay content, or coexist with content.
3. Give every non-happy state a clear explanation and next action when possible.
4. Maintain structural continuity so transitions between states feel related.
5. Review the states for emotional tone, clarity, and actionability.

## State rules

- Loading **SHOULD** preserve the expected content shape when possible.
- Empty states **MUST** explain why the space is empty and what the user can do next.
- Error states **MUST** offer recovery when recovery is possible.
- Offline states **SHOULD** preserve cached content instead of replacing it unnecessarily.
- Success states **MUST NOT** interrupt the user if lightweight confirmation is enough.

## Layout guidance

- Reuse the same top-level scaffold or structure across states when possible.
- Place the main message and primary action near the visual center for full-screen states.
- Use illustrations sparingly and only when they support comprehension or tone.
- Keep destructive or irreversible actions visually distinct from retry and continue actions.

## Validation checklist

- Every screen state answers: what happened, what now, and what action is available.
- Transitions do not cause jarring layout jumps without reason.
- Non-content states remain accessible and readable on small devices.
- Cached or partial data is retained when it improves usability.
