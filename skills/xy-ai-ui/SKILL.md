---
name: xy-ai-ui
description: Generic desktop UI/UX and task-flow standards for Electron-style apps. Use when refining visual consistency, alignment, modal flows, cancellation behavior, and long-running task interactions.
metadata:
  short-description: Desktop UI/UX and task-flow standards for Electron apps
license: Complete terms in LICENSE.txt
---

# xy-ai-ui

Lightweight standards skill for desktop app UI and interaction quality.

## Use This Skill When
- Unifying layout, spacing, and component consistency
- Fixing left/right asymmetry, scrollbar gaps, and alignment drift
- Adding confirmation modals, progress modals, and cancellation UX
- Refactoring long-running operation flows (confirm -> run -> cancel -> result)
- Defining reusable UI/interaction standards for teams

## Scope
- Primary: Electron desktop apps
- Also applicable to other desktop webview containers

## Windows 11 UI Style Prompt
When the user requests modern Windows desktop aesthetics, apply the following prompt constraints:
- Main window uses Mica-like translucent material.
- Cards and floating panels use Acrylic-like frosted surfaces.
- Use large rounded corners (12px) and soft layered shadows.
- Support global window dragging on blank background regions.
- Controls should lift on hover with deeper shadows.
- Remove default focus rings/highlight outlines unless accessibility requires visible focus.
- Typography uses Segoe UI sans-serif.
- Color system: brand blue primary + neutral-dominant palette + high contrast.
- Match Windows 11 visual language: clean, lightweight, system-native feel.
- Keep seamless integrated layout: no heavy borders, use depth and hierarchy to separate content.
- Motion should be smooth and natural, with restrained but clear transitions.

## Core Rules
1. Architecture boundaries:
- Main: system operations + orchestration
- Bridge: safe API exposure
- Renderer: UI state + interaction only

2. UI consistency:
- Single-surface visual shell
- Shared horizontal alignment token (example: --edge-align)
- Shared component states (hover/active/focus/disabled)

3. Symmetry and scrolling:
- Keep major sections on one horizontal baseline
- Handle scrollbar reservation to avoid false right whitespace
- Ensure rows fill available width where needed

4. Interaction safety:
- Background drag region; interactive elements are no-drag
- Destructive actions require custom confirm modal
- Long tasks must support cancel (including top-right X)

5. Task semantics:
- Use explicit states: idle/running/waiting/completed/warning/failed/canceled
- Cancel must short-circuit downstream steps
- Prefer automatic completion detection over manual confirmation

## Implementation Checklist
- [ ] Shared alignment token applied across topbar/filters/table/modals
- [ ] No visual frame/radius mismatch
- [ ] Confirm modal before destructive actions
- [ ] Progress modal supports cancel + close semantics
- [ ] Canceled task does not continue follow-up flow
- [ ] Auto-detection gates next-step actions
- [ ] IPC responses normalized and predictable
