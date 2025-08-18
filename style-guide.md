# Builded Design Agency - Style Guide

## Core Design Philosophy
A construction-inspired aesthetic emphasizing structure, precision, and architectural clarity through minimalist design with strategic use of floating glass-morphism cards and geometric elements.

## 1. Color Palette

### Primary Colors
- **Background**: Pure black (#000000) - enforced with !important
- **Primary Text**: Pure white (#FFFFFF)
- **Secondary Text**: Light gray (rgba(255, 255, 255, 0.8))

### Accent Colors (Dashboard/Potion Colors - as seen in floating cards)
- **Cobalt Blue**: #3B82F6
- **Electric Purple**: #8B5CF6 
- **Vibrant Pink**: #EC4899
- **Dashboard Green**: #86EFAC / #10B981
- **Supporting Colors**:
  - Lavender: #C084FC (keywords in code)
  - Sky Blue: #60A5FA (variables)
  - Yellow: #FACC15 (functions)
  - Rose: #F472B6 (tags)
  - Purple Accent: #A78BFA (active states, cursor)

### Gradients (Actual Implementation)
- **Primary Button**: linear-gradient(135deg, #3B82F6 0%, #8B5CF6 100%)
- **Glass Cards**: linear-gradient(135deg, rgba(17, 17, 17, 0.7) 0%, rgba(30, 30, 30, 0.6) 100%)
- **Navbar Fade**: linear-gradient(180deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 100%)
- **Dropdown Backgrounds**: linear-gradient(135deg, rgba(15, 15, 15, 0.98) 0%, rgba(10, 10, 10, 0.98) 100%)
- **Hover States**: linear-gradient(90deg, rgba(59, 130, 246, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%)

### Borders & Overlays
- **Subtle Border**: rgba(255, 255, 255, 0.08)
- **Light Border**: rgba(255, 255, 255, 0.1)
- **Medium Border**: rgba(255, 255, 255, 0.15)
- **Strong Border**: rgba(255, 255, 255, 0.3) - rgba(255, 255, 255, 0.5)
- **Accent Border**: rgba(59, 130, 246, 0.5)

## 2. Typography

### Font Hierarchy (Actual Implementation)
- **Hero Massive**: clamp(3.5rem, 12vw, 6rem), 800 weight, 0.85 line-height
- **Display Desktop**: 3.2rem, 800 weight, 1.1 line-height
- **H1/H2**: 2rem, 700 weight, 1.2 line-height
- **H3**: 1.45rem, 600 weight, 1.7 line-height
- **Section Titles**: 1.2rem, 700 weight, 1.2 line-height
- **Body**: 1rem, 400 weight, 1.7 line-height
- **Small/Subtitles**: 0.92rem, 400 weight, 1.55 line-height
- **Navigation**: 13-14px, 500 weight, 0.3px letter-spacing
- **Code Editor**: 'Monaco', 'Menlo', monospace, 10px

### Typography Characteristics
- **Style**: Bold but slim for structure emphasis
- **Letter Spacing**: 0.01em standard, 0.3px for nav items
- **Text Transform**: UPPERCASE for nav items, sentence case for content
- **Font Family**: System fonts primary, Monaco/Menlo for code displays

### Responsive Typography (Clamp Values)
- **Mobile Hero**: clamp(3rem, 15vw, 5rem)
- **Mobile Display**: clamp(1.8rem, 8vw, 3rem)  
- **Mobile Body**: clamp(0.9rem, 4vw, 1.1rem)
- **Mobile Small**: clamp(0.85rem, 4.5vw, 1rem)

## 3. Layout & Spacing

### Container System
- **Max Width**: 1200px (1400px on large screens)
- **Padding**: 32px (64px on large screens, 16px mobile)
- **Section Spacing**: 200px between major sections
- **Component Spacing**: 48px standard, 24px tight, 96px loose

### Image Layout Pattern
- **Full Height**: Images span entire vertical viewport
- **Full Width**: Within container constraints
- **Alternating Pattern**: Left-right-left sequence for consecutive image-text sections
- **Window Effect**: Images as architectural windows into content

### Grid System
- **Case Studies**: 3-column grid desktop, single column mobile
- **Services**: 2-column alternating layout
- **Breakpoints**: 
  - Desktop: 992px+
  - Tablet: 768px-991px
  - Mobile: <767px

## 4. Interactive Elements

### Buttons (Actual Implementation)
- **Structure**: 1.5px borders, 8px border-radius
- **Nav Button Default**: 
  ```css
  background: transparent;
  border: 1.5px solid rgba(59, 130, 246, 0.5);
  padding: 8px 20px;
  transition: all 0.3s ease;
  ```
- **Nav Button Hover**:
  ```css
  background: rgba(59, 130, 246, 0.1);
  border-color: rgba(59, 130, 246, 0.8);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(59, 130, 246, 0.2);
  ```
- **Primary Button (Gradient)**:
  ```css
  background: linear-gradient(135deg, #3B82F6 0%, #8B5CF6 100%);
  box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
  ```

### Dropdown Carets & Icons
- **Caret SVG**: 8x5px, currentColor stroke
- **Rotation on Hover**: transform: rotate(180deg)
- **Transition**: transform 0.3s ease

### Dropdown Menus
- **Background**: Glass morphism with backdrop-filter: blur(20px)
- **Entry Animation**: translateY(-10px) → translateY(0) with opacity fade
- **Item Hover**: translateX(4px) shift with gradient background
- **Left Border Accent**: 2px gradient bar grows to 60% height on hover

## 5. Component Patterns

### Floating Dashboard Cards (Hero Section)
- **Glass Morphism Style**:
  ```css
  background: linear-gradient(135deg, rgba(17, 17, 17, 0.7) 0%, rgba(30, 30, 30, 0.6) 100%);
  backdrop-filter: blur(16px) saturate(180%);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 20px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
  ```
- **Card Types**: Code editor, analytics charts, timelines, server status, API pipeline
- **Entry Animations**: Spiral, slide from corners with rotation and scale
- **Float Animation**: 25s gentle float cycle with translateY and subtle rotation

### Navigation Bar
- **Fixed Position**: Gradient fade from solid black to transparent
- **Logo**: 120px height, positioned close to edge (5-10px padding)
- **Background Gradient**:
  ```css
  background: linear-gradient(180deg, 
    rgba(0, 0, 0, 1) 0%, 
    rgba(0, 0, 0, 0.95) 50%, 
    rgba(0, 0, 0, 0) 100%);
  ```

### Geometric Elements (Background)
- **Purpose**: Architectural framing, depth without clutter
- **Shapes**: Rectangles, squares, diamonds, circles, lines
- **Opacity**: 0.02-0.4 varying by element
- **Animations**: Float animations (15-22s cycles) at different speeds
- **Positioning**: Absolute, scattered across viewport edges

## 6. Animation & Transitions

### Standard Timings
- **Instant**: 0.2s (card entrances, micro-interactions)
- **Quick**: 0.25s (spiral animations)
- **Normal**: 0.3s (hover states, dropdowns)
- **Slow**: 0.6s-0.8s (letter reveals, page transitions)
- **Float Cycles**: 15s-25s (background elements)

### Easing Functions
- **Default**: ease
- **Smooth**: cubic-bezier(0.4, 0, 0.2, 1)
- **Bounce Entry**: cubic-bezier(0.34, 1.56, 0.64, 1)
- **Spring**: cubic-bezier(0.68, -0.55, 0.265, 1.55)

### Key Animations
- **Letter Reveal (Hero)**: translateY(40px) scale(0.8) → normal, staggered delays
- **Float Cards Entry**: Various (slideIn, spiralIn) with rotation and scale
- **Gentle Float**: translateY oscillation with slight rotation over 25s
- **Pulse**: Opacity/scale pulse for active indicators
- **Blink**: Cursor blink in code editor

## 7. Accessibility & Best Practices

### Contrast Ratios
- **Large Text**: Minimum 3:1
- **Body Text**: Minimum 4.5:1
- **Interactive Elements**: Clear focus states

### Mobile Optimization
- **Touch Targets**: Minimum 44px
- **Font Scaling**: Responsive units (rem/em)
- **Image Loading**: Lazy loading for performance

### Performance
- **CSS**: Minimize reflows/repaints
- **Animations**: GPU-accelerated transforms
- **Images**: Optimized formats (WebP, AVIF)

## 8. Special Effects & Advanced Styling

### Glass Morphism (Heavily Used)
```css
/* Floating cards */
background: linear-gradient(135deg, rgba(17, 17, 17, 0.7) 0%, rgba(30, 30, 30, 0.6) 100%);
backdrop-filter: blur(16px) saturate(180%);
-webkit-backdrop-filter: blur(16px) saturate(180%);

/* Dropdowns */
background: linear-gradient(135deg, rgba(15, 15, 15, 0.98) 0%, rgba(10, 10, 10, 0.98) 100%);
backdrop-filter: blur(20px);
```

### Shadow Layering
```css
/* Floating cards */
box-shadow: 
  0 20px 40px rgba(0, 0, 0, 0.3),
  inset 0 1px 0 rgba(255, 255, 255, 0.06);

/* Button hover */
box-shadow: 0 4px 12px rgba(59, 130, 246, 0.2);
```

### SVG Gradients (Charts/Visualizations)
```svg
<linearGradient id="radialGrad" x1="0%" y1="0%" x2="100%" y2="100%">
  <stop offset="0%" style="stop-color:#8B5CF6;stop-opacity:1" />
  <stop offset="100%" style="stop-color:#EC4899;stop-opacity:1" />
</linearGradient>
```

### Mobile-Specific Overrides
- **Touch targets**: min-height: 44px-48px
- **Font sizing**: Prevents iOS zoom with 16px minimum
- **Overflow control**: overflow-x: hidden on body/html
- **Viewport breakout**: margin-left: calc(-50vw + 50%) for full-width sections

## Implementation Notes

1. **Black Background Enforcement**: Use !important to override Webflow defaults
2. **Glass Morphism Everywhere**: Primary visual language for elevated elements
3. **Floating Elements**: Dashboard-style cards create depth and sophistication
4. **Geometric Precision**: Background shapes reinforce "building blocks" concept
5. **Performance**: Use transform for animations (GPU acceleration)
6. **Responsive Clamp**: Fluid typography with clamp() for smooth scaling
7. **Z-Index Management**: Navbar at 9999, dropdowns at 1000, cards at 5