## $${\color{red}Email \ Development \ Cheat \ Sheet}$$

### 🧠 1. Fundamental Principles

**Email ≠ Web Development**

* Limited CSS & HTML support
* No modern layout systems (Flexbox, Grid mostly unsupported)
* Heavy reliance on legacy techniques

**Key Rules**

* Use **table-based layouts**
* Inline all CSS
* Keep structure simple and predictable
* Always design for worst-case client (e.g. Outlook)

---

### 🧱 2. HTML Structure (Best Practices)

**Do**

* Use nested `<table>` for layout
* Use `<tr>`, `<td>` for spacing and alignment
* Set widths explicitly (`width="600"`)
* Use `role="presentation"` for layout tables

**Avoid**

* `<div>`-based layouts (unreliable)
* Semantic HTML5 elements (`<section>`, `<article>`)
* External stylesheets

---

### 🎨 3. CSS Support & Limitations

**Supported (generally)**

* `color`, `font-family`, `font-size`
* `background-color`
* `padding`, `margin` (partial)
* `border`
* `text-align`

**Partially Supported**

* `line-height`
* `max-width`
* `display`

**Not Reliable**

* `float`
* `position`
* `flexbox`, `grid`
* `:hover` (limited to some clients)

**Golden Rule**
👉 Use **inline CSS**

```html
<td style="font-size:16px; color:#333333;">
```

---

### 📱 4. Responsive Design Techniques

**Approaches**

* Hybrid (fluid + fixed)
* Mobile-first (limited use)
* Desktop-first with media queries

**Media Queries Example**

```css
@media only screen and (max-width: 600px) {
  .container {
    width: 100% !important;
  }
}
```

**Fallback**

* Use fluid tables (`width="100%"`)
* Stack columns using block display

---

### 🧩 5. Outlook-Specific Handling

**Problem**

* Outlook uses **Microsoft Word rendering engine**

**Solution: Conditional Comments**

```html
<!--[if mso]>
  <table>
    <tr><td>Outlook-specific content</td></tr>
  </table>
<![endif]-->
```

**Common Fixes**

* VML for background images
* Fixed widths
* Avoid complex CSS

---

### 🖼️ 6. Images & Media

**Best Practices**

* Use absolute URLs
* Always include `alt` text
* Set width/height attributes
* Optimize file size

**Fallback**

```html
<img src="..." alt="Description" width="600" style="display:block;">
```

**Background Images**

* Not widely supported → use **VML fallback for Outlook**

---

### 🔤 7. Typography

**Safe Fonts**

* Arial
* Verdana
* Georgia
* Times New Roman

**Web Fonts**

* Limited support (Apple Mail, iOS Mail)
* Always define fallback stack

```css
font-family: 'Roboto', Arial, sans-serif;
```

---

### 🔗 8. Links & CTAs

**CTA Buttons**

* Use **bulletproof buttons (HTML + inline CSS)**

```html
<a href="#" style="background:#000; color:#fff; padding:12px 24px; text-decoration:none;">
  Click me
</a>
```

**Avoid**

* JS-based interactions
* Complex hover effects

---

### 📦 9. Deliverability Basics

**Key Factors**

* Clean HTML (no broken tags)
* Proper text-to-image ratio
* Avoid spam trigger words
* Use ALT text

**Authentication**

* SPF
* DKIM
* DMARC

---

### 🧪 10. Testing & Debugging

**Popular Tools**

* Litmus
* Email on Acid

**Test For**

* Client compatibility
* Dark mode
* Image blocking
* Responsiveness

---

### 🌙 11. Dark Mode Handling

**Issues**

* Colors inverted automatically
* Logos disappear

**Solutions**

* Transparent PNG logos
* Explicit background colors
* Use `prefers-color-scheme` (limited support)

---

## 📏 12. Layout Patterns

**Common Structures**

* Single column (safest)
* Two-column (stack on mobile)
* Hero image + CTA
* Grid-like (table-based)

---

## ⚠️ 13. Key Limitations

* No JavaScript ❌
* No external CSS ❌
* Limited forms ❌
* Inconsistent rendering across clients ❌
* Gmail strips `<style>` in some cases ❌

---

## 🧩 14. Important Concepts

**Bulletproof Email**

* Works across all major clients

**Progressive Enhancement**

* Basic experience everywhere, enhanced where supported

**Graceful Degradation**

* Advanced features degrade safely

**Fallback Content**

* Always provide backup (fonts, images, layouts)

---

## 🛠️ 15. Workflow & Tools

**Development**

* Hand-coded HTML
* MJML (email framework)
* Foundation for Emails

**Optimization**

* CSS inliner tools
* Minifiers

**Versioning**

* Component-based templates
* Modular partials

---

## 📚 16. Common Gotchas

* Gmail ignores `<head>` styles (sometimes)
* Outlook adds extra spacing
* iOS auto-links phone numbers
* Line-height inconsistencies
* Margin collapsing issues

---

## ⚡ TL;DR Rules

* 🧱 Tables over divs
* 🎨 Inline CSS only
* 📱 Design mobile-friendly
* 🧪 Test everywhere
* 📎 Always include fallbacks
* 💀 Expect things to break
