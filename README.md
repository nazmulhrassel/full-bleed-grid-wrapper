# full-bleed-grid-wrapper

This code defines a responsive grid layout using CSS Grid and custom CSS variables (--space-lr, --space-gap, --col-count). It adapts to different screen widths through media queries, ensuring the layout remains functional and visually appealing across devices. Here's a brief breakdown:

Key Features:

1. CSS Variables:
   --space-lr: Controls left-right spacing of the grid.
   --space-gap: Defines the gap between grid items.
   --col-count: Specifies the number of columns in the grid.
   The values for these variables change dynamically at specific breakpoints (e.g., 43.75em, 62.5em, 90em) to ensure responsiveness.
2. .grid-wrapper (Grid Container):
   Uses display: grid to define a grid layout.
   Grid Columns (grid-template-columns):
   Includes outer margins (1fr on both sides) and a dynamic number of columns (var(--col-count)).
   Columns' widths are calculated based on the available space, subtracting gaps between them.
   Gaps (gap): Controlled by --space-gap, adjusted at breakpoints.
3. Responsive Layout Adjustments:
   Media queries define changes for larger screen sizes:
   @media (width >= 43.75em): Increases column count and spacing.
   Further increases are made at 62.5em and 90em breakpoints.
4. Child Elements:
   .hero-content:
   Centers itself within specific grid columns (grid-column).
   Adjusts its placement across different breakpoints for optimal display.
   .hero-image:
   Positioned behind other elements (z-index: -1) and spans multiple grid columns.
   Its grid placement adjusts at each breakpoint for responsive image positioning.

Explanation of Layout Behavior:

The grid layout ensures the design is flexible, with dynamic column counts and spacing for various screen widths.
grid-column allows child elements like .hero-content and .hero-image to span specific ranges of columns, creating a structured yet adaptable layout.
The use of CSS variables makes it easier to manage spacing and column configurations across the breakpoints.
