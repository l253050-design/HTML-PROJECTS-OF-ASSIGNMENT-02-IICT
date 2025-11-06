# Saffron Labs — AI-Powered Mental Wellness Companion  
**README.md** for the **CSS-Only Responsive Single-Page Site**

> **Live Demo** → [Open index.html in your browser](#)  
> **Tools used:** HTML5 + CSS3 (zero JavaScript, zero frameworks)  
> **Responsive:** Mobile (≤480 px) • Tablet (481–900 px) • Desktop (≥901 px)

---

## Project Overview

**Saffron Labs** is a fictional AI startup that offers a pocket-sized wellness companion.  
This single-page marketing site showcases the product, lets visitors **pre-order**, and collects **feedback** — **all with pure HTML + CSS**.

### Core Features Delivered

| Requirement | Implementation |
|-------------|----------------|
| **CSS Grid + Flexbox layout** | 12-column grid for global sections, Flexbox for cards & form rows |
| **3 CSS-only interactive components** | 1. Pure-CSS **hamburger menu** (mobile) <br>2. **Accordion FAQ** with `:checked` checkboxes <br>3. **Image lightbox** using `:target` |
| **Fully-styled HTML form** | Custom checkboxes, radios, select, range slider, and focus states |
| **Accessibility** | `<label for>`, `aria-labelledby`, visible focus rings, `tabindex`, logical tab order |
| **Responsive breakpoints** | Mobile-first, `@media` queries at 481 px and 901 px |

---

## File Structure

---

## How to Run

1. Clone or download the folder.  
2. Open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge).  
3. No build step needed!

---

## Layout Breakdown

### 1. Grid Areas (Desktop)

```css
grid-template-areas:
  "header header"
  "hero   hero"
  "features features"
  "faq    faq"
  "form   form"
  "footer footer";
<input type="checkbox" id="nav-toggle" class="nav-toggle">
<label for="nav-toggle" class="hamburger">☰</label>
#nav-toggle:checked ~ nav { transform: translateX(0); }
<input type="checkbox" id="q1">
<label for="q1">How does Saffron work?</label>
<div class="answer">…</div>
#q1:checked ~ .answer { max-height: 200px; }
<a href="#img1"><img src="thumb.jpg"></a>
<div id="img1" class="lightbox">…</div>
.lightbox:target { opacity: 1; visibility: visible; }
