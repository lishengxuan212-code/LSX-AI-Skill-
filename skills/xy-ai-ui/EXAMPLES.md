# xy-ai-ui Usage Examples

## Example 1: Visual Consistency Refactor
User asks:
- "Unify all panel spacing and make left/right alignment symmetric."

Expected skill behavior:
- Introduce a shared alignment token (e.g. `--edge-align`)
- Align titlebar, toolbar, table header, and rows to same horizontal baseline
- Correct scrollbar-related false whitespace

## Example 2: Safe Uninstall Flow
User asks:
- "Add second confirmation and allow cancel during uninstall."

Expected skill behavior:
- Add custom confirmation modal before destructive action
- Add progress modal with cancel (including top-right close affordance)
- Ensure cancel state short-circuits downstream residue/cleanup steps

## Example 3: Windows 11 Style Prompt
User asks:
- "Adopt Windows 11 style look and keep seamless integrated UI."

Expected skill behavior:
- Use Mica-like translucent shell
- Use Acrylic-like frosted cards and 12px corners
- Use Segoe UI typography and blue/neutral high-contrast palette
- Keep smooth, restrained motion and border-light hierarchy

