# Design System Strategy: The Editorial Pantry

## 1. Overview & Creative North Star
This design system is built on the Creative North Star of **"The Digital Ephemera."** It rejects the sterile, high-gloss "SaaS" aesthetic in favor of the warmth found in a cherished, hand-annotated cookbook. We are building a high-end editorial experience that feels human, intentional, and tactile.

To break the "template" look, we utilize **Intentional Asymmetry**. Layouts should not always be perfectly centered; allow for generous, "unbalanced" white space and overlapping elements—such as a product image breaking the container of a card—to simulate the organic feel of items placed on a kitchen counter. This system is a conversation, not a transaction.

---

## 2. Colors & Tonal Architecture
Our palette transitions away from digital coldness into organic warmth. We use deep forest greens and sun-bleached corals to evoke a sense of harvest and home.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections or containers. Structure must be achieved through **Background Color Shifts** or **Tonal Transitions**. For example, a `surface-container-low` list item should sit on a `surface` background to define its shape. We define boundaries through mass and tone, not outlines.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—stacked sheets of fine, heavy-stock paper.
- **Base:** `background` (#fef9ee)
- **Sections:** `surface-container-low` (#f9f3e9)
- **Interactive Cards:** `surface-container-lowest` (#ffffff)
- **Elevated Modals:** `surface-bright` (#fef9ee)

### The "Glass & Gradient" Rule
To add "soul" to the interface, use subtle, organic gradients. Main CTAs should not be flat; apply a soft linear gradient from `primary` (#0f5238) to `primary-container` (#2d6a4f) at a 145-degree angle. For floating navigation or headers, use **Glassmorphism**: apply a semi-transparent `surface` color with a `20px` backdrop-blur to allow the "ingredients" of the list to peek through.

---

## 3. Typography: Editorial Authority
The interplay between the sophisticated **Playfair Display** (Serif) and the pragmatic **DM Sans** (Sans-serif) creates an "Editorial-meets-Utility" vibe.

*   **Display & Headlines (Playfair Display):** Used for "The Narrative." This includes page titles, category headers (e.g., "The Produce Aisle"), and empty state messaging. Use `headline-lg` (2rem) for a bold, confident start.
*   **Body & UI (DM Sans):** Used for "The Task." List items, quantities, and descriptions. `body-md` (0.875rem) is our workhorse for legibility.
*   **Labels:** To add a touch of "Archival" feel, use `label-sm` (0.6875rem), strictly uppercase, with `0.12em` tracking. This creates a functional, stamped-ink appearance for metadata like "EXPIRES SOON" or "SHARED BY."

---

## 4. Elevation & Depth: Tonal Layering
Traditional shadows are too "tech." We use light and layering to create presence.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a "soft lift" that feels architectural rather than digital.
*   **Ambient Shadows:** If a floating action button (FAB) or modal requires a shadow, use a `12%` opacity version of `on-surface` (#1d1c16) with a `32px` blur and `8px` Y-offset. It should feel like a soft shadow cast on a linen tablecloth.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke (e.g., in a high-glare environment), use the `outline-variant` token at **15% opacity**. Never use a 100% opaque border.

---

## 5. Signature Components

### Primary Buttons (The Pill)
*   **Shape:** `xl` radius (3rem / 9999px).
*   **Style:** Gradient fill (`primary` to `primary-container`).
*   **Typography:** `title-sm` (DM Sans, Bold).
*   **Interaction:** On hover, a subtle `surface-tint` overlay at 8% opacity.

### The Grocery Card
*   **Mandate:** **No Divider Lines.**
*   **Structure:** Use `1.5rem` (md) vertical padding to separate items.
*   **Visuals:** Use an asymmetric layout where the item quantity is tucked into the top-right corner in a `tertiary-container` chip, breaking the top edge of the card.

### Round Checkboxes
*   **Unchecked:** A soft `surface-container-highest` circle.
*   **Checked:** `primary` fill with a white checkmark.
*   **Animation:** A slight "bounce" (scale 1.1) when toggled to reinforce the playful tone.

### The "Aisle" List
*   **Separation:** Instead of lines, use a `surface-variant` background for every second item (zebra striping) at a very low 4% opacity, or simply rely on the `3` (1rem) spacing scale.

---

## 6. Do’s and Don’ts

### Do
*   **Do** use the `2.25rem` (display-sm) Playfair Display for empty states to make the app feel like a lifestyle magazine.
*   **Do** use `tertiary` (#7c2e19) sparingly as an "accent of urgency" (e.g., "Out of stock").
*   **Do** lean into the `3.5rem` (10) to `5.5rem` (16) spacing tokens for page margins to create a high-end gallery feel.

### Don’t
*   **Don’t** use pure black (#000000). Always use `on-surface` (#1d1c16) to maintain the "Ink on Paper" warmth.
*   **Don’t** use "Default" shadows. If the shadow looks like it came from a standard UI kit, it’s too heavy.
*   **Don’t** crowd the interface. If you feel the need to add a line to separate content, you likely need more white space instead. Use the `6` (2rem) spacing token first.