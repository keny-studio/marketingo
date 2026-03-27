## $${\color{red}Preflight \ in \ Email \ Marketing}$$

### 🧠 What is Preflight?

**Preflight** = a final validation process before sending an email campaign to ensure:

* ✅ correct rendering
* ✅ working functionality
* ✅ deliverability
* ✅ compliance

Think of it as **QA + testing + risk prevention**.

---

### 📧 1. Content & Copy Checks

#### ✅ Basics

* Subject line (length: **30–60 chars**)
* Preheader (complements subject, **40–100 chars**)
* From name & email (brand consistency)
* No placeholder text (`Lorem ipsum`, `{{name}}`)

#### ✅ Personalization

* Variables fallback:

  ```html
  {{ first_name | default: "there" }}
  ```
* No broken merge tags

#### ✅ Proofreading

* Grammar & spelling
* Tone consistency
* Correct links & CTA wording

---

### 🧩 2. HTML & Code Validation

#### ✅ Structure

* Table-based layout (NOT div-based)
* Inline CSS only
* Max width: **600–800px**

#### ✅ Compatibility

* Avoid:

  * `position`, `float`
  * external CSS
  * JavaScript ❌
* Use:

  * `<table>`
  * `<tr>`, `<td>`
  * inline styles

#### ✅ File Size

* Keep email under **~100 KB**

  * Gmail clipping limit ≈ **102 KB**

---

### 🎨 3. Design & Rendering

#### ✅ Cross-client Testing

Test in:

* Gmail (Web + Mobile)
* Outlook (Windows!)
* Apple Mail
* Yahoo Mail

#### ✅ Responsive Design

* Mobile-first approach
* Use:

  ```css
  @media screen and (max-width: 600px)
  ```

#### ✅ Images

* Use `alt` text
* Optimize size (<200 KB per image)
* Use absolute URLs
* Check blocked-image fallback

---

### 🔗 4. Links & Tracking

#### ✅ Links

* All links working (no 404)
* HTTPS only
* Correct UTM parameters:

  ```
  utm_source=email
  utm_medium=campaign
  utm_campaign=name
  ```

#### ✅ Buttons (CTA)

* Clickable area ≥ **44px height**
* Bulletproof buttons (HTML-based, not images)

---

### 📬 5. Deliverability Checks

#### ✅ Authentication

* SPF ✅
* DKIM ✅
* DMARC ✅

#### ✅ Spam Testing

* Avoid spam triggers:

  * “FREE!!!”, “BUY NOW!!!”
* Balanced text-to-image ratio (~60:40)

#### ✅ Sender Reputation

* Warmed-up domain/IP
* Clean list (no old/unengaged contacts)

---

# ⚙️ 6. Functional Testing

#### ✅ Test Sends

* Send to:

  * internal team
  * different email clients
* Check:

  * layout
  * links
  * personalization

#### ✅ Dynamic Content

* Conditional blocks:

  ```html
  {% if user.plan == "pro" %}
  ```
* Verify all scenarios render correctly

---

### 📱 7. Accessibility (WCAG Basics)

#### ✅ Readability

* Font size ≥ **14px**
* Line height: **1.4–1.6**

#### ✅ Contrast

* Text/background contrast ≥ **4.5:1**

#### ✅ Semantic fallback

* Use meaningful `alt` text
* Logical reading order

---

### ⚖️ 8. Legal & Compliance

#### ✅ Required Elements

* Unsubscribe link (visible!)
* Physical mailing address
* Privacy policy link

#### ✅ GDPR / CAN-SPAM

* Consent-based list
* Easy opt-out (1 click)

---

### 🧪 9. Final Checklist (Quick Scan)

**Before hitting SEND:**

* [ ] Subject & preheader optimized
* [ ] No broken personalization
* [ ] HTML validated (tables, inline CSS)
* [ ] Mobile responsive
* [ ] All links working + tracked
* [ ] Images optimized + alt text
* [ ] Spam test passed
* [ ] Test emails verified
* [ ] Unsubscribe + legal info included
* [ ] Email < 100 KB

---

### 🛠️ 10. Pro Tools for Preflight

* Litmus → rendering + QA
* Email on Acid → client previews
* Mailtrap → safe testing
* GlockApps → spam testing
