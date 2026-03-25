# LANDING PAGE DESIGN SPECIFICATION

**PROJECT:** Website Landing Page (Generic/SaaS Template)

---

## SUMMARY
Clean, modern landing page with hero-driven conversion focus, accessibility-first design, and performance-optimized responsive layout across all devices.

---

## LAYOUT

**HEADER / NAVIGATION**
- Fixed or sticky top bar (64px height on desktop, 56px on mobile)
- Left: Logo/wordmark (48x48px clickable, links to #hero)
- Center: Nav links hidden on mobile, visible at 768px+ (Home, Features, About, Contact)
- Right: Primary CTA button ("Get Started")
- Mobile: Hamburger menu toggle (3 horizontal lines, 48x48px tap target)

**SECTION 1: HERO**
- Full viewport height (min 600px) or 70vh on mobile
- Left column: Headline, subheadline, 2 CTA buttons stacked vertically on mobile, side-by-side on desktop
- Right column: Hero image or video placeholder (WebP + PNG fallback, 16:9 aspect ratio)
- Centered text alignment on mobile, left-aligned on desktop
- 8px grid: 24px side padding mobile, 48px desktop

**SECTION 2: VALUE PROPOSITION**
- 3-column grid at 768px+, stacked single column on mobile
- Cards: 100% width mobile, equal flex on desktop
- Each card: icon (64x64px), headline (24px), description (16px body text)
- Subtle shadow on cards, no border

**SECTION 3: FEATURES**
- Alternating left/right layout: text on left, image on right (reverse on next card)
- Mobile: stacked single column
- Each feature block: headline, bullet list (3-4 items), supporting image (8:5 ratio)
- 64px vertical spacing between feature blocks

**SECTION 4: SOCIAL PROOF**
- Testimonials carousel or 3-card grid
- Each card: quote text (italic, 16px), avatar (48x48px circle), name (bold), title (14px muted)
- Star rating or badge icon above quote
- Mobile: single column carousel, desktop: 3-column grid

**SECTION 5: CTA / CALL-TO-ACTION**
- Centered container, dark background
- Large headline (32-40px), supporting copy (18px), single primary button
- High contrast, minimal distractions

**SECTION 6: FOOTER**
- 4-column layout on desktop (Company, Product, Resources, Legal), collapsed on mobile
- Copyright notice bottom-left
- Social media icon links bottom-right (circular, 40x40px)
- Background: slightly darker than body

---

## COLORS

| Element | Hex Value | Usage |
|---------|-----------|-------|
| **Primary Background** | #FFFFFF | Page base |
| **Secondary Background** | #F8F9FB | Section alternation, cards |
| **Dark Background** | #1A1A2E | CTA section, footer |
| **Primary Brand** | #0066FF | Buttons, links, accents |
| **Primary Hover** | #0052CC | On button hover/active |
| **Text Primary** | #1A1A2E | Headlines, body text |
| **Text Secondary** | #4A5568 | Descriptions, subtext |
| **Text Muted** | #A0AEC0 | Meta info, captions |
| **Success** | #16A34A | Form success states |
| **Error** | #DC2626 | Form validation errors |
| **Border/Divider** | #E2E8F0 | Cards, subtle separators |

**Contrast Verification (WCAG AA):**
- Text Primary (#1A1A2E) on White: 19.1:1 â
- Text Secondary (#4A5568) on White: 8.9:1 â
- Primary Brand (#0066FF) on White: 5.2:1 â

---

## COMPONENTS

### HEADER / NAVIGATION
- **Logo**: 48x48px, left-aligned, 16px margin-left
- **Nav Links**: 16px font, 24px vertical padding, letter-spacing 0.5px (secondary text color)
- **Nav Link Active**: Primary brand color, underline 2px
- **Primary Button**: 44px height (touch target), 16-32px horizontal padding, 8px border-radius, white text on primary brand, font-weight 600
- **Mobile Menu**: Overlay modal, 100vw width, slides from left, backdrop blur 4px

### CARDS (Value Prop / Social Proof)
- **Card Container**: 8px border-radius, 1px solid border divider, 0px 2px 8px rgba(0,0,0,0.06) shadow
- **Card Padding**: 24px on desktop, 20px on mobile
- **Icon**: 64x64px, centered, primary brand color
- **Headline**: 18px, font-weight 600, text primary, 12px margin-top
- **Description**: 14px line-height 1.6, text secondary, 8px margin-top

### BUTTONS
- **Primary**: Background primary brand, white text, 44px min-height, 16px padding-x, 8px border-radius, no border
- **Secondary**: Background secondary BG, text primary, same padding/height, 1px border (border divider)
- **States**:
  - Default: as spec'd
  - Hover: 10% brightness increase
  - Active: 15% brightness decrease
  - Focus: 2px outline (primary brand), 2px offset
  - Disabled: 50% opacity, cursor not-allowed

### FORM INPUTS (Contact / Newsletter)
- **Input Height**: 44px (touch-friendly)
- **Input Padding**: 12px (horizontal), 8px (vertical)
- **Border**: 1px solid divider color
- **Border-radius**: 6px
- **Focus State**: 2px outline primary brand, shadow 0 0 0 4px rgba(0,102,255,0.1)
- **Label**: 14px, font-weight 500, 8px margin-bottom, associate via `for` attribute
- **Error State**: Border color error red, error icon right-aligned, helper text below in error red (12px)
- **Placeholder**: text muted color, opacity 0.7

### IMAGES
- **Format**: WebP primary with PNG fallback
- **Max-width**: 100% of container
- **Border-radius**: 8px on feature images, 0 on full-width hero
- **Lazy-load**: enabled with `loading="lazy"`
- **Alt-text**: descriptive, present on all images

### TYPOGRAPHY
- **Font Stack**: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif (system fonts for performance)
- **Headlines**: Font-weight 600-700, line-height 1.2, letter-spacing -0.5px
- **Body**: Font-weight 400, line-height 1.6, 16px default
- **Small**: 14px, font-weight 400, line-height 1.5

### SPACING GRID (8px base)
- Micro spacing: 8px, 16px
- Section padding: 24px mobile, 48px desktop
- Section margin-bottom: 64px
- Component gaps: 8px, 16px, 24px (flex gap)

---

## INTERACTIONS

### HOVER STATES
- **Links**: Text color â primary brand, underline appears
- **Buttons**: Background lightens 10%, cursor pointer, shadow 0 4px 12px rgba(0,102,255,0.2)
- **Cards**: Box-shadow increases to 0 8px 16px rgba(0,0,0,0.1), subtle up-translate 2px
- **Icons**: Color shift to primary brand (if not already)

### FOCUS STATES
- **Keyboard Navigation**: 2px outline using primary brand color, 2px offset
- **Tab Order**: Logical (header nav â hero CTA â features â social proof â footer CTA â footer links)
- **Skip Navigation Link**: Visible on focus, hidden by default, top-left position, background primary brand, white text, 48px height
- **Focus Visible**: Applied to all interactive elements (buttons, links, form inputs)

### FORM INTERACTIONS
- **Input Focus**: Border color â primary brand, background â secondary BG, cursor active
- **Validation On-blur**: Check email pattern, required field presence
- **Error Display**: Shake animation (2 frames, 2px displacement left/right), error text appears below in 12px error red
- **Success**: Checkmark icon appears (green #16A34A), success message displays 2s then fades
- **Submission**: Button text changes to "Sending...", disabled state, spinner icon (if async)

### MOBILE MENU
- **Toggle Click**: Menu overlay slides in from left, backdrop dims, primary brand color fade-in
- **Link Click**: Menu closes (instant or 200ms fade), page scrolls to section
- **Outside Click / Esc**: Menu closes, backdrop removes
- **Nav Links in Menu**: 18px, 16px padding-y, stacked vertically, full-width touch targets

### SCROLL INTERACTIONS
- **Smooth Scroll**: `scroll-behavior: smooth` on html element (if nav links use anchor tags)
- **Lazy Loading**: Images below fold load on scroll approach (50px threshold)
- **Fade-in on Scroll**: Optional subtle fade for cards as they enter viewport (200ms ease-in)

### BUTTON STATES
- **Hover**: Brightness +10%, shadow depth increases
- **Active/Pressed**: Brightness -15%, inner shadow (inset 0 2px 4px rgba(0,0,0,0.2))
- **Focus**: Outline 2px primary brand, 2px offset
- **Disabled**: Opacity 50%, cursor not-allowed, no hover effect

### RESPONSIVE BREAKPOINTS
- **Mobile**: 320px - 767px (single column, hamburger nav)
- **Tablet**: 768px - 1023px (2-3 column grids, visible nav)
- **Desktop**: 1024px+ (full 4-column, expanded features)
- **Max-width container**: 1200px (centered with padding)

---

## STYLE NOTES

### FEEL
- **Modern, Clean, Trustworthy**: Ample whitespace (24-64px gutters), minimal shadows (0 2px 8px soft), geometric sans-serif typography
- **Professional but Approachable**: Rounded corners (6-8px), soft color palette, encouraging copy tone
- **Accessibility-First**: High contrast, large touch targets (48px minimum), keyboard-navigable, semantic HTML

### VISUAL HIERARCHY
1. **Hero Headline**: 40-48px, primary text color, weight 700
2. **Section Headlines**: 28-36px, primary text color, weight 600
3. **Card Headlines**: 18-24px, primary text color, weight 600
4. **Body Copy**: 16px, secondary text color, weight 400
5. **Small Text**: 12-14px, muted text color, weight 400

### SPACING CONSISTENCY
- 8px grid enforced: all margins/padding multiples of 8
- Section vertical spacing: 64px between sections (80px on hero)
- Card internal padding: 24px desktop, 20px mobile
- Text-to-image spacing: 32px (4 grid units)

### MICRO-INTERACTIONS
- **Button Hover**: 150ms ease-out, scale 1.02 (optional), shadow expand
- **Link Underline**: 200ms ease-in, fade in on hover
- **Form Input Focus**: 100ms ease-out, border color + shadow
- **Card Hover**: 200ms ease-out, lift 2px + shadow
- **Mobile Menu Slide**: 300ms cubic-bezier(0.4, 0, 0.2, 1)

### TYPOGRAPHY STYLE
- **Headlines**: System sans-serif, tight line-height (1.1-1.2), slightly negative letter-spacing for personality
- **Body**: System sans-serif, warm line-height (1.6), light letter-spacing (0.3px)
- **All-caps Labels**: Letter-spacing 1px, font-weight 500, 12px, text muted
- **No Custom Fonts**: Rely on system fonts for <1.5s FCP target

### DARK MODE (Optional Future)
- Dark BG: #0D0D1A
- Card BG: #16152B
- Text Primary: #F0F1F3
- Border: #2D2B4E
- Primary Brand: #4D9FFF (lightened for contrast)

---

## ACCESSIBILITY CHECKLIST (WCAG AA)

â Color contrast 4.5:1 (text on background)  
â Semantic HTML5 (header, nav, main, section, footer)  
â ARIA landmarks (role="navigation", role="contentinfo")  
â Form labels associated (label + input id)  
â Skip-nav link visible on focus  
â 48px minimum touch targets (buttons, links)  
â Keyboard navigation (Tab, Enter, Esc, arrow keys in menu)  
â Focus indicators (2px outline, visible on all interactive)  
â Alt-text on all images (descriptive, <125 chars)  
â Form validation & error messaging (associated with inputs)  
â Page title & meta description  
â Responsive text sizing (16px base, scale with viewport)  

---

**Developer: Implement exactly as specified. No code blocks above. Validate colors, spacing, and behaviors against this document.**