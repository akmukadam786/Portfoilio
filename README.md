# Abdul Kadir Mukadam — Personal Portfolio
> Frontend Developer based in Pretoria, South Africa

🔗 **Live Site:** [akmukadam786.github.io/portfolio](https://akmukadam786.github.io/portfolio)

---

## What This Project Is

My personal portfolio website — built from scratch with pure HTML, CSS, and JavaScript. No frameworks, no templates, no page builders. Every animation, layout, and interaction was hand-coded.

---

## Animations & Interactions

### Custom Cursor
A two-part cursor replaces the default browser cursor — a sharp dot that follows the mouse exactly, and a larger ring that lags slightly behind using lerp (linear interpolation) inside a `requestAnimationFrame` loop.

### Hero Text Reveal
The name "ABDUL KADIR MUKADAM" is split into three lines, each hidden with `overflow: hidden`. On load, each word slides up into view with a staggered delay using CSS `@keyframes`.

### Typing Effect
A JavaScript function cycles through job titles — "Frontend Developer", "Web Developer", "UI Enthusiast", "Problem Solver" — typing and deleting each one character at a time using `setTimeout`. A blinking cursor is simulated with a CSS animation.

### Scroll Reveal
Every section uses the browser's `IntersectionObserver` API to detect when elements enter the viewport. When they do, a CSS class is added that transitions opacity from 0 to 1 and translates the element upward into its final position.

### 3D Card Tilt
Project cards track the mouse position on `mousemove` using `getBoundingClientRect()`. The offset from the card's center is converted into `rotateX` and `rotateY` values applied via CSS `perspective` transform. A radial gradient glow follows the cursor inside each card using CSS custom properties (`--mx`, `--my`).

### Scrolling Marquee
A skills ticker strip uses CSS `@keyframes` to continuously translate a doubled list of items from right to left, creating a seamless infinite loop without JavaScript.

### Frosted Glass Nav
The navigation starts transparent and switches to a backdrop-blurred, semi-opaque state when `window.scrollY` exceeds 50px — handled with a single scroll event listener toggling a CSS class.

---

## Sections

- **Hero** — Name reveal, typing effect, CTA buttons, grid background, floating glow blob
- **About** — Bio, background, fact cards with hover slide animation
- **Skills** — 16 skill tags with staggered scroll-reveal and hover lift
- **Projects** — 3 featured projects with 3D tilt, glow effect, live demo and source code links
- **Contact** — Email and GitHub links
- **Footer** — Minimal branding

---

## Tech Stack
| Technology | What it's used for |
|---|---|
| HTML5 | Semantic structure |
| CSS3 | All styling, animations, custom properties, grid/flexbox |
| Vanilla JavaScript | Cursor, typing effect, scroll reveal, 3D tilt, marquee |
| IntersectionObserver API | Scroll-triggered animations |
| requestAnimationFrame | Smooth cursor lag animation |
| Google Fonts (Barlow Condensed + DM Sans) | Typography |

---

## What I Learned / Would Add Next

**Learned:** Advanced CSS animations, the IntersectionObserver API, linear interpolation for smooth motion, CSS custom properties for dynamic theming, and how to build polished UI interactions without any libraries.

**Would add next:**
- Dark/light mode toggle
- Blog or writing section
- Contact form with EmailJS
- Page transitions between sections
- More projects as I build them

---

## Interview Talking Points

**Q: How does the cursor lag effect work?**
> I use a technique called lerp — linear interpolation. The ring's position moves 12% of the remaining distance to the mouse on every frame. This means it never quite catches up instantly, creating a smooth trailing effect. It runs inside `requestAnimationFrame` so it syncs with the browser's rendering cycle.

**Q: How does the IntersectionObserver work?**
> Instead of listening to the scroll event constantly (which fires hundreds of times per second and is bad for performance), IntersectionObserver watches specific elements and fires a callback only when they enter or leave the viewport. I add a `visible` class when they appear, which triggers a CSS transition.

**Q: Why no frameworks like React?**
> For a portfolio site this size, vanilla JavaScript is cleaner, faster, and loads instantly with no build step. It also demonstrates that I understand the fundamentals — frameworks are abstractions on top of these same concepts.

**Q: How did you do the 3D card tilt?**
> On `mousemove`, I calculate how far the cursor is from the card's center using `getBoundingClientRect()`. That offset is converted into rotation angles and applied using `CSS perspective` and `rotateX`/`rotateY` transforms. The glow follows the cursor by updating CSS custom properties `--mx` and `--my` which feed into a `radial-gradient`.

---

*Built by Abdul Kadir Mukadam · [github.com/akmukadam786](https://github.com/akmukadam786)*
