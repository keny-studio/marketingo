## $${\color{red}Email \ coding}$$ - tricks, traps and snippets



### 🧱 Layout & Structure Hacks

### 1. Table-Based Layout (Still king 👑)

* Use `<table>` instead of divs
* Nest tables for complex layouts
* Always include:

```html
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" border="0">
```

---

### 2. Ghost Tables (for Outlook)

* Helps control width in Outlook (which ignores max-width)

```html
<!--[if mso]>
<table width="600" align="center"><tr><td>
<![endif]-->

<!-- Your content -->

<!--[if mso]>
</td></tr></table>
<![endif]-->
```

---

### 3. Hybrid (Spongy) Layout

* Combine fixed + fluid widths
* Use:

```css
max-width: 600px;
width: 100%;
```

* Works without media queries in some clients

---

### 🎯 Outlook-Specific Hacks (MSO)

### 4. Conditional Comments

* Target only Outlook (MSO engine)

```html
<!--[if mso]>
<p>This only shows in Outlook</p>
<![endif]-->
```

---

### 5. VML for Background Images

* Outlook doesn’t support CSS `background-image`

```html
<v:rect xmlns:v="urn:schemas-microsoft-com:vml" fill="true" stroke="false">
  <v:fill type="tile" src="image.jpg" />
  <v:textbox>
    Content here
  </v:textbox>
</v:rect>
```

---

### 6. Force Font Fallbacks

Outlook ignores web fonts:

```css
font-family: Arial, sans-serif;
```

---

### 📱 Responsive Design Hacks

### 7. Mobile Targeting with Media Queries

```css
@media only screen and (max-width: 600px) {
  .container { width: 100% !important; }
}
```

---

### 8. Gmail App Hack (No `<style>` support workaround)

* Inline critical styles
* Use `!important` aggressively

---

### 9. Hide/Show Content

```css
.mobile-hide {
  display: none;
  max-height: 0;
  overflow: hidden;
}
```

---

### 🎨 Styling Hacks

### 10. Inline CSS (Mandatory)

* Most clients strip `<style>`
* Use tools like:

  * MJML
  * Premailer

---

### 11. Bulletproof Buttons

Use table instead of `<button>`:

```html
<table role="presentation">
  <tr>
    <td bgcolor="#007BFF" style="padding: 12px 24px;">
      <a href="#" style="color:#fff; text-decoration:none;">Click me</a>
    </td>
  </tr>
</table>
```

---

### 12. Line Height Fix (Outlook)

```css
line-height: 1.5;
mso-line-height-rule: exactly;
```

---

### 🖼️ Image Handling Hacks

### 13. Prevent Image Gaps

```css
img {
  display: block;
}
```

---

### 14. Retina Images

* Use double resolution:

```html
<img src="image@2x.png" width="300" style="width:300px;">
```

---

### 15. ALT Text Styling (when images blocked)

```html
<img src="..." alt="Important text" style="font-size:16px; color:#000;">
```

---

### 🧩 Spacing & Alignment Hacks

### 16. Spacer GIF (Old but reliable)

```html
<img src="spacer.gif" width="20" height="20">
```

---

### 17. Padding via Table Cells

```html
<td style="padding: 20px;">
```

---

### 🔠 Typography Hacks

### 18. Web Font Fallback Stack

```css
font-family: 'Roboto', Arial, sans-serif;
```

---

### 19. Fix Text Scaling (iOS)

```css
-webkit-text-size-adjust: 100%;
```

---

### 🧪 Debugging & Testing Hacks

### 20. Use Background Colors for Debugging

```html
<td style="background:red;">
```

---

### 21. Border Debugging

```css
border: 1px solid red;
```

---

### 22. Test Tools

* Litmus
* Email on Acid
* Real devices (especially Outlook 😅)

---

### ⚡ Deliverability & Safety Hacks

### 23. Avoid Spam Triggers

* Don’t overuse:

  * ALL CAPS
  * “FREE!!!”
* Balance text-to-image ratio

---

### 24. Preheader Hack

```html
<div style="display:none; max-height:0; overflow:hidden;">
  This is preheader text
</div>
```

---

### 25. Bulletproof Background Color

```html
<body bgcolor="#ffffff" style="background:#ffffff;">
```

---

### 🧠 Pro-Level Tricks

### 26. Min-width Hack (for Gmail)

```css
min-width: 100% !important;
```

---

### 27. Fix iOS Blue Links

```css
a[x-apple-data-detectors] {
  color: inherit !important;
  text-decoration: none !important;
}
```

---

### 28. Prevent Gmail Clipping (102KB limit)

* Keep HTML under ~100KB
* Remove comments + unnecessary code

---

### 🚀 Golden Rules (Always remember)

* Tables > Divs
* Inline CSS > `<style>`
* Outlook = special treatment
* Test everywhere (not just browser)
* Keep it simple & robust


### 📧 Text Preview (Preheader) 

The **text preview hack** controls the snippet shown next to the subject line in inboxes (Gmail, Apple Mail, Outlook, etc.).

---

#### 🎯 What is it?

* The **preheader** = preview text shown after the subject
* Pulled from the **first visible text in the email body**
* If not defined → random text like *“View in browser…”*

---

### ✅ Basic Preheader Hack

Place this **at the very top of your email body**:

```html
<div style="display:none; max-height:0; overflow:hidden;">
  Your preview text goes here. Make it compelling!
</div>
```

---

### 🚀 Advanced “Bulletproof” Preheader Hack

This version hides the text more reliably across clients:

```html
<div style="display:none !important; 
            visibility:hidden; 
            opacity:0; 
            color:transparent; 
            height:0; 
            width:0; 
            max-height:0; 
            max-width:0; 
            overflow:hidden; 
            mso-hide:all; 
            font-size:1px; 
            line-height:1px;">
  Your preview text goes here 👀
</div>
```
- Keep the preheader between 85–100 characters to ensure consistent display.
- Do not repeat the subject line.
- Match the hidden text color to the email background.


---

### 🧠 Inbox Control Trick (Spacing Hack)

Add invisible filler to **prevent unwanted text appearing after your preheader**:

```html
<div style="display:none; max-height:0; overflow:hidden;">
  Your preview text goes here
  &nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;
</div>
```

👉 This:

* Pushes away unwanted text like *“View in browser”*
* Keeps preview clean in Gmail & iOS Mail

---

### ✨ Pro Version (Used in production emails)

```html
<div style="display:none !important;
            visibility:hidden;
            opacity:0;
            color:transparent;
            height:0;
            width:0;
            max-height:0;
            max-width:0;
            overflow:hidden;
            mso-hide:all;
            font-size:1px;
            line-height:1px;">
  20% off ends tonight — don’t miss out
  &nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;&nbsp;&zwnj;
</div>
```

---

### 📏 Best Practices

#### ✍️ Length

* Ideal: **40–90 characters**
* Mobile: ~35–50 chars
* Desktop: ~75–100 chars

---

#### 🎯 Copywriting Tips

* Complement subject line (don’t repeat it)
* Add urgency or curiosity
* Examples:

  * *“Ends tonight — last chance to save”*
  * *“You forgot something in your cart”*
  * *“Here’s your exclusive access 👀”*

---

#### ⚠️ Common Mistakes

* ❌ Forgetting preheader → random text shows
* ❌ Too long → gets cut off
* ❌ Not hidden properly → visible in email body
* ❌ No spacing hack → messy preview

---

### 🧪 Testing Tip

Always test in:

* Gmail (web + app)
* iOS Mail
* Outlook (desktop + web)
