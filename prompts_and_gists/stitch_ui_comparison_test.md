# Stitch — Zero-UI Routing Engine (UI Comparison Test)

React/Tailwind generation prompt for Stitch.

---

```
Generate a React + Tailwind component for a Zero-UI Routing Engine interface.

AESTHETIC:
Strict B2B enterprise. The palette is slate, white, and subtle shadows only. No color accents. No gradients. No rounded corners beyond 4px. No drop shadows heavier than shadow-sm. This is a tool used by operations leads, not consumers.

LAYOUT:

1. HERO INPUT SECTION:
   Massive. Full-width. This is the primary interaction surface and it must feel like the most important element on the page. Use a large textarea or contenteditable div — minimum 180px height — with a placeholder that reads exactly: "Describe the trigger. The engine will route it."

   Font: monospace. Size: text-lg or larger. No label above the input. The input IS the UI.

2. LOGIC OUTPUT CARD:
   Appears below the hero input after submission. Card uses a clean white background with a 1px slate-200 border and shadow-sm.

   Inside the card, use a strict grid layout with three columns:

   | TRIGGERS | CONDITIONS | ACTIONS |

   Each column header in all-caps, text-xs, tracking-widest, text-slate-400.
   Each column contains a vertical list of plain text items — no badges, no pills, no icons.

   Below the grid: a single "Confidence" line in text-sm text-slate-500 with a percentage value.

3. PAGE CHROME:
   Minimal. A single top bar with the product name "Zero-UI Routing Engine" in text-sm font-medium text-slate-700, left-aligned. No navigation. No sidebar. No footer.

BEHAVIOR:
Wire the submit action to a mock function. The output card should render with hardcoded example data on first load so the layout is visible without interaction.

DO NOT:
- Use any color outside of the slate/white palette
- Add tooltips, modals, or onboarding flows
- Import any component library (shadcn, MUI, Radix, etc.)
- Add animations beyond a simple opacity transition on card appear
```
