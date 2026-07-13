---
name: Scholar Dialogue
colors:
  surface: '#fcf9f8'
  surface-dim: '#dcd9d9'
  surface-bright: '#fcf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f2'
  surface-container: '#f0eded'
  surface-container-high: '#eae7e7'
  surface-container-highest: '#e5e2e1'
  on-surface: '#1c1b1b'
  on-surface-variant: '#404750'
  inverse-surface: '#313030'
  inverse-on-surface: '#f3f0ef'
  outline: '#717881'
  outline-variant: '#c0c7d2'
  surface-tint: '#00629e'
  primary: '#00609b'
  on-primary: '#ffffff'
  primary-container: '#2079bc'
  on-primary-container: '#fdfcff'
  inverse-primary: '#9acbff'
  secondary: '#755b00'
  on-secondary: '#ffffff'
  secondary-container: '#fdcc3a'
  on-secondary-container: '#705600'
  tertiary: '#b51341'
  on-tertiary: '#ffffff'
  tertiary-container: '#d83358'
  on-tertiary-container: '#fffbff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#cfe4ff'
  primary-fixed-dim: '#9acbff'
  on-primary-fixed: '#001d34'
  on-primary-fixed-variant: '#004a79'
  secondary-fixed: '#ffdf91'
  secondary-fixed-dim: '#f0c02e'
  on-secondary-fixed: '#241a00'
  on-secondary-fixed-variant: '#594400'
  tertiary-fixed: '#ffd9dc'
  tertiary-fixed-dim: '#ffb2ba'
  on-tertiary-fixed: '#400010'
  on-tertiary-fixed-variant: '#910030'
  background: '#fcf9f8'
  on-background: '#1c1b1b'
  surface-variant: '#e5e2e1'
  surface-muted: '#F5F7F9'
  border-subtle: '#E2E8F0'
  academic-ink: '#2D3436'
typography:
  display-lg:
    fontFamily: Hanken Grotesk
    fontSize: 48px
    fontWeight: '800'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-sm:
    fontFamily: Source Serif 4
    fontSize: 24px
    fontWeight: '700'
    lineHeight: '1.3'
  title-md:
    fontFamily: Source Serif 4
    fontSize: 20px
    fontWeight: '600'
    lineHeight: '1.4'
  body-lg:
    fontFamily: Hanken Grotesk
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Hanken Grotesk
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  label-caps:
    fontFamily: Hanken Grotesk
    fontSize: 12px
    fontWeight: '700'
    lineHeight: '1'
    letterSpacing: 0.05em
  headline-lg-mobile:
    fontFamily: Hanken Grotesk
    fontSize: 32px
    fontWeight: '800'
    lineHeight: '1.2'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  container-max: 1280px
  gutter: 24px
  margin-mobile: 16px
  stack-sm: 8px
  stack-md: 16px
  stack-lg: 32px
---

## Brand & Style

This design system is tailored for large-scale academic environments, specifically the Social Sciences. It balances institutional authority with a vibrant, contemporary energy. The brand personality is intellectually rigorous yet accessible, designed to manage high information density without overwhelming the user.

The visual style is **Corporate / Modern** with a high-contrast editorial edge. It prioritizes clarity through a structured grid and a sophisticated interplay between bold sans-serif UI elements and elegant serif academic titles. The aesthetic reflects a prestigious conference that is forward-looking and inclusive, utilizing the primary palette to color-code disciplines and navigation paths.

## Colors

The palette is derived from the conference's visual identity, utilizing high-chroma primaries against a disciplined neutral base. 

- **Primary (Blue):** Used for primary actions, navigation headers, and institutional branding.
- **Secondary (Yellow):** Reserved for highlighting active states, symposium numbers, and search focus indicators.
- **Tertiary (Magenta):** Applied to key metadata, such as "Live Now" indicators or specific disciplinary tags.
- **Neutral (Black/Grey):** Foundations of the typography system. Pure black is avoided for long-form reading in favor of "Academic Ink" to reduce eye strain during schedule browsing.

Color is used functionally: it should differentiate types of sessions or specific days of the event, ensuring that even in dense tables, the user can visually anchor their location.

## Typography

The typography system employs a "Workhorse and Scholar" pairing. 

**Hanken Grotesk** handles the heavy lifting of the UI: navigation, labels, search inputs, and logistical metadata (time, location). Its modern, clean proportions ensure legibility at small sizes in dense tables.

**Source Serif 4** is used for academic content: symposium titles and research paper names. This serif face provides the necessary "literary" weight and authority required for social science discourse. 

For high-density schedule tables, use `body-md` for paper abstracts and `label-caps` for categorical markers like "Coordinación" or institutional acronyms (UNC, CONICET).

## Layout & Spacing

The system uses a **Fixed Grid** for desktop (12 columns) to maintain the structural integrity of complex data tables, and a **Fluid Grid** for mobile (4 columns).

The layout philosophy centers on "The Stack." In an academic context, content is nested. A symposium (Level 1) contains sessions (Level 2), which contain individual papers (Level 3). 
- Use 32px vertical rhythm to separate major symposia.
- Use 16px vertical rhythm for items within a session.
- Detailed session tables should utilize a "Sticky Column" for time slots on desktop, ensuring the temporal anchor remains visible while scrolling horizontally through concurrent rooms.

## Elevation & Depth

To maintain an institutional and professional feel, the system avoids heavy shadows. Instead, it utilizes **Tonal Layers** and **Low-contrast outlines**.

- **Level 0 (Background):** White or very light grey (#F5F7F9).
- **Level 1 (Cards/Containers):** Pure white background with a 1px border (#E2E8F0).
- **Level 2 (Active/Hover):** A subtle, tinted ambient shadow (Primary color at 5% opacity) to indicate interactivity without breaking the flat, academic aesthetic.

Depth is primarily communicated through color-blocking. For example, the search bar and filter headers use a slightly darker surface than the main results area to indicate they are "fixed" control surfaces.

## Shapes

The shape language is **Soft**. A 0.25rem (4px) base radius is applied to buttons, input fields, and cards. This provides a subtle modern touch that softens the density of the information without appearing too casual or "bubbly," which would detract from the academic seriousness. Tags and "Chips" for institutional affiliations use the `rounded-lg` (8px) setting to distinguish them from structural UI components.

## Components

### Search & Filters
The search bar is the primary entry point. It should be oversized, utilizing the `secondary_color` (Yellow) for the focus ring. Filter chips should toggle between a "border-only" state and a "filled" state using the `primary_color`.

### Symposium Cards
Cards act as the summary for major thematic blocks. They feature a vertical accent bar on the left using the Primary, Secondary, or Tertiary colors to categorize disciplines. The symposium number should be rendered in a bold, oversized `label-caps` format.

### Detailed Session Tables
For the full schedule, use a "Striped" table format. 
- **Header:** Background `neutral_color`, text white.
- **Rows:** Alternating white and `surface-muted`.
- **Time Cells:** Bold sans-serif, right-aligned to the divider.
- **Paper Titles:** Left-aligned, using `title-md` (Serif).

### Buttons & Inputs
Buttons are strictly rectangular with soft corners. Primary buttons use the `primary_color_hex` with white text. Secondary buttons use a transparent background with a 2px `primary_color` border. Input fields must include clear, persistent labels in `label-caps` above the field.