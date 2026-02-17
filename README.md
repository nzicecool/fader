# 🎚️ The Fader Specification (V1.0)

**Fader** (`.fdr`) is a high-level, constraint-based prompting language designed for **Vibecoding**. 

It allows non-coders to describe software not by writing syntax, but by defining the *feeling* (UI) and the *behavior* (Data) of an application. The Fader Engine (an LLM equipped with the Fader System Prompt) translates these percentage-based constraints into production-ready full-stack code.

---

## 📂 File Structure

A `.fdr` file consists of 5 core blocks:

1.  **METADATA**: Basic project info.
2.  **PROMPT**: The natural language goal (What does the app do?).
3.  **UI_MIX**: Percentage sliders (0-100%) defining visual aesthetics.
4.  **DATA_MIX**: Percentage sliders (0-100%) defining backend architecture.
5.  **TECH**: (Optional) Specific technical constraints (e.g., React, Supabase).

---

## 🎨 UI_MIX (The Visual Library)

These faders control the DOM, CSS, and animations.

| Slider | 0% Meaning (Low) | 100% Meaning (High) |
| :--- | :--- | :--- |
| **Density** | **Airy.** Massive padding (`p-12`), huge typography, single focal point. | **Dense.** Dashboard style, tight padding (`p-1`), small text, max data on screen. |
| **Pop** | **Muted.** Monochrome, flat design, matte finishes, no shadows. | **Loud.** High saturation, neon accents, thick borders, heavy drop shadows. |
| **Warmth** | **Cold.** Industrial, metallic, stark white/black, monospace fonts, sharp corners. | **Cozy.** Earth tones, serif fonts, fully rounded corners (`rounded-2xl`), soft shadows. |
| **Strictness** | **Loose.** Broken grids, overlapping elements, organic/asymmetrical layouts. | **Rigid.** Perfect 12-column grid, standard cards, symmetrical corporate structure. |
| **Motion** | **Static.** Instant state changes. No animations. | **Fluid.** Spring physics, page transitions, parallax, smooth layout shifts. |

---

## 💾 DATA_MIX (The Backend Library)

These faders control the database architecture, authentication, and state management.

| Slider | 0% Meaning (Low) | 100% Meaning (High) |
| :--- | :--- | :--- |
| **Persistence** | **Local.** Browser `localStorage` only. Data is lost if cache is cleared. | **Cloud.** Permanent database (Supabase/Firebase). |
| **Reactivity** | **Static.** Fetch on load. Requires page refresh to see updates. | **Live Sync.** WebSockets / Real-time subscriptions. Updates instantly across clients. |
| **Privacy** | **Public.** No auth required. Anyone can read/write data. | **Private.** Enforced Auth (OAuth/Email). Row Level Security (RLS) restricts access. |
| **Complexity** | **Flat.** Single NoSQL document or flat list. | **Relational.** Normalized SQL schema with foreign keys and join tables. |