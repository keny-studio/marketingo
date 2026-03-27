## $${\color{red}MJML \ - \ Mailjet \ Markup \ Language}$$

### 🧠 What is MJML?

* Framework for responsive email HTML
* Compiles to table-based HTML (email-safe)
* Developed by Mailjet

---

### 🏗️ Basic Structure

```xml
<mjml>
  <mj-head>
    <!-- styles, fonts, metadata -->
  </mj-head>
  <mj-body>
    <!-- content -->
  </mj-body>
</mjml>
```

---

### 🧱 Layout Components

#### 📦 Sections & Columns

![Image](https://images.openai.com/static-rsc-4/RkdPbvuP7gAtok9MHePdo7vIR8_CCPXWOl93uqqaKT30fRtMRnqSofwHa9TzeMoNHgXu_Bj4j8oddUvOA0I6D6dqfRhTNHtBk-te6IYFU_MxxM7C6ca90ZufAd0RBN3kbHtq38u_E49tqPZ2uwE9cHPNlX0fXPpDMM5OWmdH8LyX9RoVJCD1cdUMV4XXz_9e?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/OaeJ_GoPOc93Cz4TmD4BUh1oRdfnK_MZrkbzGf4s-zxXbQ_9uiK4KgcLFpeaQFXCm0Afgq_PqsOmlsLMRLVYV-dUp_DSW1AGpIOhwSFdg0qxrJ27WfFqnlBRZUQEbNe-suYfoLqOSV9JGwq3HXNiUS3-JDTPG0iHZZR_VLjmOJ22Yy5X_8rzdhAsZ-71hvBc?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/RkdPbvuP7gAtok9MHePdo7vIR8_CCPXWOl93uqqaKT30fRtMRnqSofwHa9TzeMoNHgXu_Bj4j8oddUvOA0I6D6dqfRhTNHtBk-te6IYFU_MxxM7C6ca90ZufAd0RBN3kbHtq38u_E49tqPZ2uwE9cHPNlX0fXPpDMM5OWmdH8LyX9RoVJCD1cdUMV4XXz_9e?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/bXDcK9i42G80VKAQRB9n0wdfCbSpAIaSVA_oWWsg4ztRDfXiOS0WjOvq_9i-bum3LJTuvMhpOYWicL8yuqONq4JEI6nC5G3566u0p-DzK5ei_XPcMYTTnWae2tFSbJuVScYocqQoWo-rEjsfcxRde6IsqDdtMCQqEpn7643fP9g-u32NBfRYzezhG5SRM6AF?purpose=fullsize)

```xml
<mj-section>
  <mj-column>
    <mj-text>Column 1</mj-text>
  </mj-column>
  <mj-column>
    <mj-text>Column 2</mj-text>
  </mj-column>
</mj-section>
```

**Key Rules:**

* `mj-section` = row
* `mj-column` = column
* Columns stack on mobile automatically

---

### 🧩 Core Components

#### 📝 Text

```xml
<mj-text font-size="16px" color="#333333">
  Hello World
</mj-text>
```

---

#### 🖼️ Image

```xml
<mj-image src="image.jpg" alt="Description" width="300px" />
```

---

#### 🔘 Button

```xml
<mj-button href="https://example.com" background-color="#F45E43">
  Click Me
</mj-button>
```

---

#### 📏 Divider

```xml
<mj-divider border-color="#dddddd" />
```

---

#### 🧱 Spacer

```xml
<mj-spacer height="20px" />
```

---

### 🎨 Styling & Attributes

#### Global Styles

```xml
<mj-head>
  <mj-attributes>
    <mj-text font-family="Arial" color="#000000" />
    <mj-button border-radius="4px" />
  </mj-attributes>
</mj-head>
```

---

#### Inline Styling

```xml
<mj-text padding="10px" align="center">
  Styled Text
</mj-text>
```

---

### 📱 Responsive Behavior

* Mobile-first by default
* Columns stack vertically
* No media queries needed (MJML handles it)

---

### 🧩 Advanced Components

#### 🧠 Hero Section

![Image](https://images.openai.com/static-rsc-4/Xq0kHkyw6pkgcMP-RA09VnTa6pzciTUmFdhXgd3kuNFNdrP8aE9t2G3-1Re5TCOq_PtR4suZWL7KL7jwxWXdKs-WlpYDjZKIhfLX4SCIlvmNqVLUY1uM8iAkxJ3f0HkyPUa9X7ZS24XeTOPfdDpvnMZzOq0nNktSyWtY2fi8zVVJWYsp1YDUvVXZmZA3ZoBZ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/j6N-FXTEgN1RkNTBC-Q4XaPKiJFqhEPcIz_FEKwujZFRo125NzfSTdN3f8q6xhOjDPAOftvyRSh_88vfrRokaonpae4ckhVsz24eHjwsyAbuA8Xzqouqd6zt2OPyRYlwxgcg2HZ6ysyFGmGz6CRtwBk-XJO1a8kREu0M5IEaIhNVVS45HlQQ2cguaJILiwnO?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Xq0kHkyw6pkgcMP-RA09VnTa6pzciTUmFdhXgd3kuNFNdrP8aE9t2G3-1Re5TCOq_PtR4suZWL7KL7jwxWXdKs-WlpYDjZKIhfLX4SCIlvmNqVLUY1uM8iAkxJ3f0HkyPUa9X7ZS24XeTOPfdDpvnMZzOq0nNktSyWtY2fi8zVVJWYsp1YDUvVXZmZA3ZoBZ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/7Ycs_uiXGIfoqYa4Sno7jkCDn3Kujs2wwFKgHH0vcXIS7nXubjo10BvHcHTFH0jMJgNyQYwcnr8PGMS44y7bXEMCzsGUYnFcNwIhAAH38SwQY4FVuByfb7pZ0rX9JWh-iOYg00WlksXKQTohpUoJxHSymrJmP5XMOaeb9DhM4gfewzCZc5Jt36rNBjWqPBI6?purpose=fullsize)

```xml
<mj-hero mode="fixed-height" height="300px" background-url="bg.jpg">
  <mj-text color="#ffffff">Hero Text</mj-text>
</mj-hero>
```

---

#### 📑 Navbar

```xml
<mj-navbar>
  <mj-navbar-link href="#">Home</mj-navbar-link>
  <mj-navbar-link href="#">About</mj-navbar-link>
</mj-navbar>
```

---

#### 🖼️ Carousel

```xml
<mj-carousel>
  <mj-carousel-image src="1.jpg" />
  <mj-carousel-image src="2.jpg" />
</mj-carousel>
```

⚠️ Limited support in email clients

---

#### 📊 Table

```xml
<mj-table>
  <tr>
    <td>Item</td>
    <td>Price</td>
  </tr>
</mj-table>
```

---

### 🧾 Full Example Template

```xml
<mjml>
  <mj-head>
    <mj-attributes>
      <mj-text font-family="Arial" />
    </mj-attributes>
  </mj-head>
  <mj-body>

    <mj-section>
      <mj-column>
        <mj-text font-size="20px">Welcome 👋</mj-text>
        <mj-button href="#">Get Started</mj-button>
      </mj-column>
    </mj-section>

  </mj-body>
</mjml>
```

---

### ⚠️ Email Dev Best Practices (MJML)

* Always add:

  * `alt` for images
  * inline-friendly styles
* Keep width ≤ **600px**
* Test in:

  * Gmail
  * Outlook
  * Apple Mail
* Avoid:

  * complex nesting
  * unsupported components (carousel, video)

---

### 🧰 Useful Tools

* MJML CLI:

```bash
mjml input.mjml -o output.html
```

* Integrations:

  * VS Code plugin
  * Webpack loader
  * Gulp plugin

---

### 💡 Pro Tips

* Use `mj-wrapper` for grouped sections
* Use `mj-group` to prevent stacking (advanced)
* Use `mj-raw` for custom HTML
* Use partials/components for reuse
