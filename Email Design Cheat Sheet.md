## $${\color{red}Email \ Design \ Cheat \ Sheet}$$

### 📧 4 Main Types of Marketing Emails — Cheat Sheet
---

#### 1. 🛍️ Promotional Emails

**Goal:** Drive immediate conversions (sales, clicks)

**Typical Content:**

* Discounts / offers / coupons
* Product launches
* Limited-time deals
* Seasonal campaigns (Black Friday, holidays)

**Key Elements:**

* Strong CTA (“Buy now”, “Get 20% off”)
* Urgency (countdown, limited stock)
* Eye-catching visuals

**Best Practices:**

* Keep it short and action-focused
* Highlight value above the fold
* Use urgency carefully (avoid spam feel)

**KPIs:**

* Conversion rate
* Click-through rate (CTR)
* Revenue per email

---

#### 2. 📰 Newsletter Emails

**Goal:** Build relationships & engagement

**Typical Content:**

* Articles / blog posts
* Company updates
* Tips / curated content
* Industry news

**Key Elements:**

* Multiple sections (modular layout)
* Soft CTAs (“Read more”)
* Consistent branding

**Best Practices:**

* Maintain regular schedule (weekly/monthly)
* Keep content scannable
* Balance value vs promotion (80/20 rule)

**KPIs:**

* Open rate
* CTR
* Engagement time

---

#### 3. 🤖 Transactional Emails

**Goal:** Deliver important user-triggered information

**Triggered By:**

* Purchases
* Account actions
* System events

**Typical Content:**

* Order confirmations
* Password resets
* Shipping updates
* Receipts

**Key Elements:**

* Clear information hierarchy
* Functional CTA (“Track order”)
* Minimal distractions

**Best Practices:**

* Prioritize clarity over design
* Ensure fast delivery & reliability
* Add subtle upsell/cross-sell (optional)

**KPIs:**

* Delivery rate
* Open rate (usually very high)
* CTR on functional links

---

#### 4. 🧠 Lifecycle (Automated) Emails

**Goal:** Guide users through the customer journey

**Common Flows:**

* Welcome series
* Onboarding
* Abandoned cart
* Re-engagement (win-back)

**Key Elements:**

* Personalization (name, behavior)
* Timing & sequencing
* Context-aware messaging

**Best Practices:**

* Map emails to user journey stages
* Use behavioral triggers
* A/B test timing & content

**KPIs:**

* Conversion rate per flow
* Retention rate
* Lifetime value (LTV)

---

### ⚡ Quick Comparison

| Type          | Trigger        | Goal        | Frequency  |
| ------------- | -------------- | ----------- | ---------- |
| Promotional   | Campaign-based | Sales       | Occasional |
| Newsletter    | Scheduled      | Engagement  | регулярna  |
| Transactional | User action    | Information | Instant    |
| Lifecycle     | Behavior/time  | Retention   | Automated  |


---

## 🎨 Advanced Email Design Tips

---

### 🧱 1. Email Layout Architecture

**Golden Rule:** Design for **inbox constraints**, not web freedom.

### Core Structure

```
[ Preheader ]
[ Header / Logo ]
[ Hero Section ]
[ Body (modular blocks) ]
[ CTA Section(s) ]
[ Footer (legal + unsubscribe) ]
```

#### Layout Systems

* **Single-column (600px max)** → safest standard
* **Hybrid / spongy layout** → better mobile control
* **Z-pattern / F-pattern scanning**

#### Spacing System

* Outer padding: `16–24px`
* Section spacing: `24–40px`
* Line height: `1.4–1.6`

---

### 📱 2. Responsive Design (Email Reality)

**Reality:** Not all clients support media queries (especially Outlook).

#### Mobile-First Priorities

* Font size: **≥14px body / 22px headline**
* CTA button: **≥44px height**
* Max width: **100% fluid on mobile**

#### Techniques

* **Fluid tables (percentage widths)**
* **Stack columns (display:block)**
* **Ghost tables for Outlook**

#### Avoid

* Complex grids (3–4 columns)
* Tiny text or tight spacing
* Side-by-side CTAs

---

### 🎯 3. Visual Hierarchy & Attention Design

#### Hierarchy Flow

1. **Hero (value proposition)**
2. Supporting content
3. CTA
4. Secondary info

#### Design Techniques

* Contrast (color, size, spacing)
* Directional cues (arrows, faces, lines)
* Whitespace = focus tool

#### CTA Rules

* One primary CTA per section
* Use **button, not text link**
* Action-oriented copy:

  * ❌ “Submit”
  * ✅ “Get My Discount”

---

### 🎨 4. Color, Typography & Branding

#### Colors

* 2–3 primary colors max
* CTA color = **highest contrast element**
* Follow **WCAG contrast (4.5:1)**

#### Typography (Email-Safe)

* Sans-serif: Arial, Helvetica, Verdana
* Serif: Georgia, Times New Roman
* Fallback stack required

```css
font-family: Arial, Helvetica, sans-serif;
```

#### Font System

* H1: 24–32px
* H2: 18–24px
* Body: 14–16px
* Small: 12–13px

---

### 🧩 5. Modular Design System

**Think in components, not full emails.**

#### Core Modules

* Hero block
* Text + image
* Product cards
* CTA banner
* Divider / spacer
* Footer

#### Benefits

* Faster production
* Easier A/B testing
* Consistency across campaigns

---

### 🖼️ 6. Images & Media Optimization

#### Rules

* Use **2x resolution (retina)**
* Optimize weight (<200KB per image ideally)
* Always include **ALT text**

#### Formats

* JPG → photos
* PNG → UI / transparency
* GIF → simple animation

#### Critical Principle

👉 Emails must work **without images**

---

### ♿ 7. Accessibility (Often Ignored, High Impact)


#### Essentials

* Semantic structure (headings hierarchy)
* ALT text for all images
* Sufficient contrast
* Bulletproof buttons (HTML, not image)

#### Bonus

* Add `role="presentation"` for layout tables
* Use descriptive link text (not “click here”)

---

### ⚙️ 8. Email Client Constraints (Design Reality)

#### Major Limitations

* Outlook = **Word rendering engine**
* Gmail clips emails >102KB
* Limited CSS support

#### Design Around:

* Inline CSS
* Tables (not divs)
* Avoid:

  * position, float
  * background-image (limited support)

---

### 🌙 9. Dark Mode Design


#### Problems

* Color inversion (Gmail, iOS)
* Logos disappearing

#### Solutions

* Transparent PNG logos
* Avoid pure black/white extremes
* Test in both modes

---

### 🧪 10. Conversion-Oriented Design Patterns

#### High-Converting Elements

* Urgency (timers, deadlines)
* Social proof (reviews, ratings)
* Personalization (name, behavior)
* Product recommendations

#### Psychological Triggers

* FOMO
* Scarcity
* Authority
* Reciprocity

---

### ⚡ Quick Design Checklist (Pre-Send)

**Layout**

* ✅ Single-column or mobile-friendly
* ✅ Clear hierarchy

**Typography**

* ✅ ≥14px body
* ✅ Safe fonts + fallbacks

**CTA**

* ✅ Visible above the fold
* ✅ Button (not image)

**Images**

* ✅ Optimized + ALT text
* ✅ Works without images

**Accessibility**

* ✅ Contrast OK
* ✅ Logical reading order

**Compatibility**

* ✅ Tested (Gmail, Outlook, iOS)
* ✅ <102KB (avoid clipping)
