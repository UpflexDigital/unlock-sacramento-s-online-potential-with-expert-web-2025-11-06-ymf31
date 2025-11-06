# Upflex Digital Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Upflex Digital landing page. This guide assumes you have basic familiarity with HTML and CSS but are new to web development.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Customizations](#common-customizations)
7. [Troubleshooting](#troubleshooting)

---

## Getting Started

### Prerequisites

Before you begin customizing this landing page, you'll need:

- A text editor (we recommend [VS Code](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), or [Notepad++](https://notepad-plus-plus.org/))
- Basic understanding of HTML tags and structure
- A web browser to preview your changes
- File explorer/finder access to your project folder

### File Structure

Your project should be organized like this:

```
project-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy policy - create this)
├── terms.html          (Terms of service - create this)
└── blog.html           (Blog page - referenced in footer)
```

### How to Edit and Preview

1. **Open the file**: Right-click on `index.html` → Open with → Your text editor
2. **Make changes**: Edit the HTML content or CSS
3. **Save the file**: Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)
4. **Preview**: Open `index.html` in your web browser to see changes

---

## Updating Text Content

This section shows you exactly where and how to update all text on your landing page.

### Understanding HTML Structure

Before making changes, understand this basic HTML structure:

```html
<h1>This is a heading</h1>           <!-- Large title text -->
<p>This is a paragraph</p>           <!-- Body text -->
<span>This is inline text</span>     <!-- Text within a line -->
```

When you see these tags in the code, the text between the opening tag (`<`) and closing tag (`>`) is what displays on your page.

---

### 1. Header/Navigation Section

**Location**: Lines 47-79 in the provided HTML

#### Company Name

Find this code in the header:

```html
<span class="text-xl font-bold text-white hidden sm:block">Upflex Digital</span>
```

**To change it:**
- Replace `Upflex Digital` with your company name
- Example: `<span class="text-xl font-bold text-white hidden sm:block">Your Company Name</span>`

#### Navigation Menu Items

Find this section:

```html
<a href="#features" class="text-gray-300 hover:text-white...">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white...">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white...">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white...">FAQ</a>
<a href="#about" class="text-gray-300 hover:text-white...">About</a>
```

**To change menu items:**
- Replace the text between `>` and `</a>` with your desired menu item
- Example: `<a href="#features" class="...">Our Services</a>`

**⚠️ Important**: Keep the `href="#"` part the same—these are anchor links that jump to different sections.

#### "Get Started" Button Text

Find this code (appears twice—once for desktop, once for mobile):

```html
<a href="https://upflexdigital.com" class="button-hover px-6 py-2...">
    Get Started
</a>
```

**To change it:**
- Replace `Get Started` with your desired text
- Example: `Get Your Free Quote`

---

### 2. Hero Section (Main Banner)

**Location**: Lines 81-115

#### Main Headline

Find this code:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
    Unlock Sacramento's <span class="gradient-text">Online Potential</span> with Expert Web Design
</h1>
```

**To change it:**
- Replace the entire text with your headline
- Keep the `<span class="gradient-text">` tags around the words you want in purple/pink gradient
- Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
    Transform Your <span class="gradient-text">Business Online</span> Today
</h1>
```

#### Subheading (Subtitle)

Find this code:

```html
<p class="text-lg md:text-xl text-gray-300 max-w-3xl mx-auto mb-8 leading-relaxed">
    Future-proof your business with captivating web design tailored to your unique needs. We create stunning, high-performance websites that drive engagement and deliver measurable results for Sacramento businesses.
</p>
```

**To change it:**
- Replace the entire paragraph text
- Keep the class attributes the same
- Example:
```html
<p class="text-lg md:text-xl text-gray-300 max-w-3xl mx-auto mb-8 leading-relaxed">
    Your custom subheading text goes here. Describe your value proposition clearly and concisely.
</p>
```

#### Hero Buttons

Find this code:

```html
<a href="https://upflexdigital.com" class="button-hover px-8 py-4...">
    Start Your Web Journey <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**To change button text:**
- Replace `Start Your Web Journey` with your desired text
- The `<i class="fas fa-arrow-right...">` part adds the arrow icon—keep it or remove it
- Example: `<a href="...">Get Started Now <i class="fas fa-arrow-right ml-2"></i></a>`

---

### 3. Features Section

**Location**: Lines 117-185

#### Section Title

Find this code:

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Powerful Features Built for Success
</h2>
```

**To change it:**
- Replace `Powerful Features Built for Success` with your title
- Example: `Our Web Design Services`

#### Section Subtitle

Find this code:

```html
<p class="text-lg text-gray-300 max-w-2xl mx-auto">
    Our comprehensive web design solutions are engineered to deliver exceptional results and drive your business forward.
</p>
```

**To change it:**
- Replace the paragraph text with your description

#### Individual Feature Cards

Each feature card has three parts you can customize:

**Feature 1: User Experience Focus**

```html
<h3 class="text-xl md:text-2xl font-bold mb-3">User Experience Focus</h3>
<p class="text-gray-300 leading-relaxed mb-4">
    We prioritize intuitive navigation and engaging interfaces...
</p>
<ul class="space-y-2 text-sm text-gray-400">
    <li><i class="fas fa-check text-purple-400 mr-2"></i>Intuitive Navigation Design</li>
    <li><i class="fas fa-check text-purple-400 mr-2"></i>User Testing & Optimization</li>
    <li><i class="fas fa-check text-purple-400 mr-2"></i>Conversion Rate Optimization</li>
</ul>
```

**To customize:**

1. **Change the title**: Replace `User Experience Focus`
2. **Change the description**: Replace the paragraph text
3. **Change the bullet points**: Replace each list item text while keeping `<li>` and `</li>` tags

**Example:**
```html
<h3 class="text-xl md:text-2xl font-bold mb-3">Fast & Reliable</h3>
<p class="text-gray-300 leading-relaxed mb-4">
    Lightning-fast loading speeds and 99.9% uptime guarantee...
</p>
<ul class="space-y-2 text-sm text-gray-400">
    <li><i class="fas fa-check text-purple-400 mr-2"></i>Sub-2 Second Load Times</li>
    <li><i class="fas fa-check text-purple-400 mr-2"></i>Global CDN Network</li>
    <li><i class="fas fa-check text-purple-400 mr-2"></i>99.9% Uptime SLA</li>
</ul>
```

**Repeat this process for Feature 2 and Feature 3** (Mobile Responsiveness and Secure Hosting).

---

### 4. Benefits Section

**Location**: Lines 187-246

#### Section Title & Subtitle

Find and update similar to Features section:

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Transform Your Business with Real Results
</h2>
```

#### Individual Benefit Cards

Each benefit card contains:

```html
<h3 class="text-xl font-bold mb-2">Enhanced User Engagement</h3>
<p class="text-gray-300 text-sm leading-relaxed mb-3">
    Keep visitors captivated with interactive elements...
</p>
<ul class="space-y-1 text-xs text-gray-400">
    <li><i class="fas fa-arrow-right text-purple-400 mr-2"></i>40% Increase in Session Duration</li>
    <li><i class="fas fa-arrow-right text-purple-400 mr-2"></i>Interactive Content Elements</li>
    <li><i class="fas fa-arrow-right text-purple-400 mr-2"></i>Higher Conversion Rates</li>
</ul>
```

**To customize:**
- Update the title, description, and bullet points following the same pattern as Features

---

### 5. Call-to-Action (CTA) Section

**Location**: Lines 248-265

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-6 tracking-tight">
    Ready to Elevate Your Online Presence?
</h2>
<p class="text-lg md:text-xl text-gray-300 max-w-2xl mx-auto mb-10">
    Join hundreds of Sacramento businesses that have transformed their digital presence. Let's create something extraordinary together.
</p>
<a href="https://upflexdigital.com" class="button-hover...">
    Get Your Free Consultation <i class="fas fa-calendar ml-2"></i>
</a>
```

**To customize:**
- Update the heading, paragraph, and button text

---

### 6. Testimonials Section

**Location**: Lines 267-350

#### Section Title

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    What Our Clients Say
</h2>
```

#### Individual Testimonials

Each testimonial card contains:

```html
<p class="text-gray-300 mb-6 leading-relaxed text-sm md:text-base">
    "Upflex Digital completely transformed our online presence..."
</p>
<div class="flex items-center space-x-4">
    <div class="w-12 h-12 bg-gradient-to-br from-purple-500 to-pink-500 rounded-full...">
        <i class="fas fa-user text-white"></i>
    </div>
    <div>
        <p class="font-bold text-white">Sarah Mitchell</p>
        <p class="text-sm text-gray-400">CEO, Mitchell & Co Real Estate</p>
    </div>
</div>
```

**To update testimonials:**

1. **Replace the quote**: Update the paragraph text with the actual testimonial
2. **Replace the name**: Change `Sarah Mitchell`
3. **Replace the title/company**: Change `CEO, Mitchell & Co Real Estate`

**Note**: The star rating (`<i class="fas fa-star"></i>`) appears 5 times for a 5-star review. Keep these as-is unless you want to change the rating.

---

### 7. FAQ Section

**Location**: Lines 352-455

#### Section Title

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    Frequently Asked Questions
</h2>
```

#### Individual FAQ Items

Each FAQ item has a question and answer:

```html
<button class="faq-question w-full p-6 flex items-center justify-between...">
    <span class="text-lg font-semibold text-left">How long does it typically take to build a website?</span>
    <i class="faq-icon fas fa-chevron-down text-purple-400..."></i>
</button>
<div class="faq-answer hidden px-6 pb-6 text-gray-300 leading-relaxed border-t border-gray-700">
    <p class="mb-3">
        The timeline for website development typically ranges from 4 to 12 weeks...
    </p>
    <ul class="space-y-2 mb-3 text-sm">
        <li><i class="fas fa-check text-purple-400 mr-2"></i><strong>Simple Websites:</strong> 4-6 weeks</li>
        <li><i class="fas fa-check text-purple-400 mr-2"></i><strong>Medium Websites:</strong> 6-10 weeks</li>
    </ul>
</div>
```

**To update FAQ:**

1. **Change the question**: Replace text in the `<span>` tag
2. **Change the answer**: Replace text in the `<div class="faq-answer">` section
3. **Update bullet points**: Modify list items while keeping the `<li>` tags

**Important**: Keep the button and div structure intact—this is what makes the accordion expand/collapse functionality work.

---

### 8. About Us Section

**Location**: Lines 457-510

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 tracking-tight">
    About Upflex Digital
</h2>
<p class="text-lg text-gray-300">
    Transforming Sacramento businesses through innovative web design and digital strategy
</p>
<p class="text-gray-300 leading-relaxed text-lg mb-6">
    Founded in 2018, Upflex Digital emerged from a simple yet powerful vision...
</p>
```

**To customize:**
- Update the heading, subtitle, and all paragraph text
- The statistics at the bottom (500+, 98%, 7 Yrs) can be updated by changing the numbers and labels

---

### 9. Final CTA Section

**Location**: Lines 512-536

```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-6 tracking-tight">
    Ready to Transform Your Digital Presence?
</h2>
<p class="text-lg text-gray-300 mb-10 max-w-2xl mx-auto">
    Contact us today for a free consultation...
</p>
```

**To customize:**
- Update heading, paragraph, and button text

---

### 10. Footer Section

**Location**: Lines 538-620

#### Company Name & Description

```html
<span class="text-xl font-bold text-white">Upflex Digital</span>
<p class="text-gray-400 text-sm mb-4">
    Transforming Sacramento businesses through innovative web design and digital solutions.
</p>
```

**To customize:**
- Update company name and description

#### Footer Links

```html
<a href="#features" class="text-gray-400 hover:text-purple-400...">Web Design</a>
<a href="#features" class="text-gray-400 hover:text-purple-400...">Web Development</a>
<a href="blog.html" class="text-gray-400 hover:text-purple-400...">Blog</a>
<a href="privacy.html" class="text-gray-400 hover:text-purple-400...">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-purple-400...">Terms of Service</a>
```

**To customize:**
- Update link text between `>` and `</a>`
- Update href values (we'll cover this in the Links section below)

#### Contact Information

```html
<a href="mailto:info@upflexdigital.com" class="hover:text-purple-400...">info@upflexdigital.com</a>
<p class="text-gray-400">
    <i class="fas fa-map-marker-alt text-purple-400 mr-2"></i>
    Sacramento, California
</p>
```

**To customize:**
- Replace email address with your email
- Replace location with your location

#### Copyright Text

```html
<p class="text-gray-400 text-sm text-center md:text-left mb-4 md:mb-0">
    &copy; 2025 Upflex Digital. All rights reserved.
</p>
```

**To customize:**
- Replace company name and update year if needed

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first CSS framework used throughout this landing page. Instead of writing custom CSS, you add pre-built classes to HTML elements.

### Understanding Tailwind Classes

Tailwind classes are descriptive and tell you exactly what they do:

| Class | What It Does |
|-------|--------------|
| `text-white` | Makes text white |
| `bg-gray-900` | Makes background dark gray |
| `p-8` | Adds padding (internal spacing) |
| `mb-6` | Adds margin-bottom (space below element) |
| `rounded-lg` | Adds rounded corners |
| `hover:text-purple-400` | Changes text to purple when you hover over it |
| `md:text-5xl` | On medium screens and up, makes text extra large |
| `lg:px-8` | On large screens and up, adds left/right padding |

### Responsive Design Classes

This landing page uses responsive design, meaning it looks good on phones, tablets, and desktops. Tailwind uses prefixes for different screen sizes:

- **No prefix** (`text-4xl`): Applies on all screen sizes
- **`sm:`** (`sm:flex`): Applies on small screens and up (640px+)
- **`md:`** (`md:text-5xl`): Applies on medium screens and up (768px+)
- **`lg:`** (`lg:text-6xl`): Applies on large screens and up (1024px+)

**Example**: `text-4xl md:text-5xl lg:text-6xl`
- Small phones: 4xl size
- Tablets: 5xl size
- Desktop: 6xl size

### Common Customizations

#### 1. Change Text Color

Find a text element you want to change:

```html
<p class="text-gray-300">Your text here</p>
```

**Current color**: `text-gray-300` (light gray)

**To change to different colors:**

```html
<!-- White text -->
<p class="text-white">Your text here</p>

<!-- Purple text -->
<p class="text-purple-400">Your text here</p>

<!-- Pink text -->
<p class="text-pink-500">Your text here</p>

<!-- Red text -->
<p class="text-red-500">Your text here</p>
```

**Available color options**: `gray-`, `purple-`, `pink-`, `red-`, `blue-`, `green-`, `yellow-`, `orange-` followed by intensity (100, 200, 300, 400, 500, 600, 700, 800, 900)

#### 2. Change Background Color

```html
<!-- Original: dark gray background -->
<section class="bg-gray-900">

<!-- Change to: purple background -->
<section class="bg-purple-900">

<!-- Change to: black background -->
<section class="bg-black">
```

#### 3. Change Button Colors

Find button code:

```html
<a href="#" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white...">
    Button Text
</a>
```

**The gradient (`from-purple-600 to-pink-600`) creates the purple-to-pink effect.**

**To change to solid colors:**

```html
<!-- Solid purple button -->
<a href="#" class="px-8 py-4 bg-purple-600 text-white...">Button Text</a>

<!-- Solid blue button -->
<a href="#" class="px-8 py-4 bg-blue-600 text-white...">Button Text</a>

<!-- Solid gradient (blue to purple) -->
<a href="#" class="px-8 py-4 bg-gradient-to-r from-blue-600 to-purple-600 text-white...">Button Text</a>
```

#### 4. Change Spacing (Padding & Margins)

**Padding** (space inside an element):

```html
<!-- Original: p-8 (medium padding on all sides) -->
<div class="p-8">Content</div>

<!-- Large padding -->
<div class="p-12">Content</div>

<!-- Small padding -->
<div class="p-4">Content</div>

<!-- Different padding on different sides -->
<div class="px-8 py-4">Content</div>  <!-- 8 units left/right, 4 units top/bottom -->
```

**Margin** (space outside an element):

```html
<!-- Original: mb-6 (margin-bottom of 6 units) -->
<h2 class="mb-6">Heading</h2>

<!-- Larger margin below -->
<h2 class="mb-12">Heading</h2>

<!-- Margin on all sides -->
<div class="m-8">Content</div>

<!-- Margin top and bottom -->
<div class="my-8">Content</div>
```

#### 5. Change Text Size

```html
<!-- Original: text-4xl md:text-5xl lg:text-6xl -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">Heading</h1>

<!-- Make smaller -->
<h1 class="text-2xl md:text-3xl lg:text-4xl">Heading</h1>

<!-- Make larger -->
<h1 class="text-5xl md:text-6xl lg:text-7xl">Heading</h1>
```

**Text size options**: `text-xs`, `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`, `text-7xl`

#### 6. Change Border Colors

```html
<!-- Original: purple border on hover -->
<div class="border border-gray-700 hover:border-purple-500">

<!-- Change to pink border -->
<div class="border border-gray-700 hover:border-pink-500">

<!-- Make border thicker -->
<div class="border-2 border-gray-700 hover:border-purple-500">
```

#### 7. Change Rounded Corners

```html
<!-- Original: slightly rounded -->
<div class="rounded-lg">

<!-- More rounded -->
<div class="rounded-xl">

<!-- Fully rounded (circle) -->
<div class="rounded-full">

<!-- Slightly rounded -->
<div class="rounded">

<!-- No rounding -->
<div class="rounded-none">
```

### Maintaining Responsive Design

**Important**: When modifying classes, always include responsive prefixes:

❌ **Wrong** - Only shows on desktop:
```html
<h1 class="text-6xl">Heading</h1>
```

✅ **Right** - Works on all screen sizes:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">Heading</h1>
```

### Testing Your Changes

After modifying Tailwind classes:

1. Save your file (`Ctrl+S` or `Cmd+S`)
2. Refresh your browser (`F5` or `Cmd+R`)
3. Test on different screen sizes:
   - Right-click → Inspect → Toggle device toolbar (or press `Ctrl+Shift+M`)
   - Test on phone, tablet, and desktop sizes

---

## Fixing and Managing Links

This section shows you how to update, fix, and manage all links on your landing page.

### Understanding Links

Links in HTML use the `<a>` tag with an `href` attribute:

```html
<a href="https://example.com">Click Me</a>
```

- `<a>` = anchor tag (creates the link)
- `href="..."` = the URL the link goes to
- `Click Me` = the text that appears on your page

### Types of Links on This Page

#### 1. **Internal Links** (jump to sections on the same page)

These use `#` followed by a section ID:

```html
<a href="#features">Features</a>
```

This links to:
```html
<section id="features">
```

**These links should NOT be changed** unless you rename the sections.

#### 2. **External Links** (go to other websites)

```html
<a href="https://upflexdigital.com">Get Started</a>
```

**These need to be updated with your actual website URL.**

#### 3. **Email Links**

```html
<a href="mailto:info@upflexdigital.com">Email Us</a>
```

**These need to be updated with your actual email address.**

#### 4. **File Links** (go to other HTML files in your project)

```html
<a href="privacy.html">Privacy Policy</a>
```

**These link to files in your project folder.**

---

### All Links That Need Updating

Here are every link in your landing page that likely needs customization:

#### In the Header (Navigation)

**Location**: Lines 47-79

```html
<!-- Desktop Menu Links - These are fine, they're internal -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="#about">About</a>

<!-- "Get Started" Button - UPDATE THIS -->
<a href="https://upflexdigital.com" class="button-hover px-6 py-2...">
    Get Started
</a>
```

**To fix the Get Started button:**

Replace `https://upflexdigital.com` with your website URL:

```html
<!-- If your website is www.yoursite.com -->
<a href="https://www.yoursite.com" class="button-hover px-6 py-2...">
    Get Started
</a>

<!-- Or if you want it to go to a contact form on your site -->
<a href="https://www.yoursite.com/contact" class="button-hover px-6 py-2...">
    Get Started
</a>

<!-- Or if you want it to open an email -->
<a href="mailto:info@yourcompany.com" class="button-hover px-6 py-2...">
    Get Started
</a>
```

#### In the Hero Section

**Location**: Lines 95-107

```html
<!-- Primary CTA Button - UPDATE THIS -->
<a href="https://upflexdigital.com" class="button-hover px-8 py-4...">
    Start Your Web Journey <i class="fas fa-arrow-right ml-2"></i>
</a>

<!-- Learn More Button - This is fine (internal link) -->
<a href="#features" class="button-hover px-8 py-4...">
    Learn More <i class="fas fa-chevron-down ml-2"></i>
</a>
```

**To fix:**

```html
<a href="https://www.yoursite.com" class="button-hover px-8 py-4...">
    Start Your Web Journey <i class="fas fa-arrow-right ml-2"></i>
</a>
```

#### In the CTA Section (Middle of Page)

**Location**: Lines 248-265

```html
<!-- UPDATE THIS -->
<a href="https://upflexdigital.com" class="button-hover inline-block px-10 py-4...">
    Get Your Free Consultation <i class="fas fa-calendar ml-2"></i>
</a>
```

**To fix:**

```html
<a href="https://www.yoursite.com/consultation" class="button-hover inline-block px-10 py-4...">
    Get Your Free Consultation <i class="fas fa-calendar ml-2"></i>
</a>
```

#### In the Mobile Menu

**Location**: Lines 69-77

```html
<!-- UPDATE THIS -->
<a href="https://upflexdigital.com" class="button-hover px-6 py-2...">
    Get Started
</a>
```

**To fix (same as desktop):**

```html
<a href="https://www.yoursite.com" class="button-hover px-6 py-2...">
    Get Started
</a>
```

#### In the Final CTA Section

**Location**: Lines 512-536

```html
<!-- Two buttons here - UPDATE BOTH -->
<a href="https://upflexdigital.com" class="button-hover px-10 py-4...">
    Start Your Project <i class="fas fa-arrow-right ml-2"></i>
</a>

<a href="mailto:info@upflexdigital.com" class="button-hover px-10 py-4...">
    Email Us <i class="fas fa-envelope ml-2"></i>
</a>
```

**To fix:**

```html
<!-- Update the website URL -->
<a href="https://www.yoursite.com" class="button-hover px-10 py-4...">
    Start Your Project <i class="fas fa-arrow-right ml-2"></i>
</a>

<!-- Update the email address -->
<a href="mailto:your-email@yourcompany.com" class="button-hover px-10 py-4...">
    Email Us <i class="fas fa-envelope ml-2"></i>
</a>
```

#### In the Footer

**Location**: Lines 538-620

```html
<!-- Footer Services Links - These are fine (internal) -->
<a href="#features">Web Design</a>
<a href="#features">Web Development</a>
<a href="#features">Mobile Optimization</a>
<a href="#features">SEO Services</a>
<a href="#features">Hosting & Support</a>

<!-- Footer Company Links -->
<a href="#about">About Us</a>              <!-- Internal - fine -->
<a href="#testimonials">Testimonials</a>   <!-- Internal - fine -->
<a href="blog.html">Blog</a>               <!-- UPDATE THIS -->
<a href="#faq">FAQ</a>                     <!-- Internal - fine -->
<a href="#" class="...">Contact</a>        <!-- UPDATE THIS -->

<!-- Footer Legal Links -->
<a href="privacy.html">Privacy Policy</a>  <!-- UPDATE THIS (create file) -->
<a href="terms.html">Terms of Service</a>  <!-- UPDATE THIS (create file) -->

<!-- Footer Contact Links - UPDATE THESE -->
<a href="mailto:info@upflexdigital.com">info@upflexdigital.com</a>
```

---

### Step-by-Step: Fix All Links

**Step 1**: Open `index.html` in your text editor

**Step 2**: Find and replace all instances of `https://upflexdigital.com` with your website URL

Use your editor's Find & Replace feature:
- **Windows**: Press `Ctrl+H`
- **Mac**: Press `Cmd+Option+F`

In the Find field: `https://upflexdigital.com`
In the Replace field: `https://www.yoursite.com` (or your actual URL)

Click "Replace All"

**Step 3**: Find and replace all instances of `info@upflexdigital.com` with your email

In the Find field: `info@upflexdigital.com`
In the Replace field: `your-email@yourcompany.com`

Click "Replace All"

**Step 4**: Update the blog link

Find this line:
```html
<a href="blog.html">Blog</a>
```

Replace with:
```html
<!-- Option 1: If blog is in same folder -->
<a href="blog.html">Blog</a>

<!-- Option 2: If blog is on external website -->
<a href="https://www.yoursite.com/blog">Blog</a>

<!-- Option 3: If you don't have a blog yet, remove or change to # -->
<a href="#">Blog</a>
```

**Step 5**: Update the Contact link in footer

Find this line:
```html
<a href="#" class="...">Contact</a>
```

Replace with:
```html
<!-- Option 1: If contact form is on your site -->
<a href="https://www.yoursite.com/contact">Contact</a>

<!-- Option 2: If you want email contact -->
<a href="mailto:your-email@yourcompany.com">Contact</a>

<!-- Option 3: If you want a phone number -->
<a href="tel:+1-555-123-4567">Contact</a>
```

**Step 6**: Save your file

Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)

**Step 7**: Test all links

Open your page in a browser and click every link to make sure they work.

---

### Common Link Issues and Solutions

#### Issue: Link goes to wrong page

**Solution**: Double-check the URL spelling

```html
<!-- Wrong -->
<a href="https://www.yoursite.com">Click</a>  <!-- Missing https:// -->

<!-- Right -->
<a href="https://www.yoursite.com">Click</a>
```

#### Issue: Internal link doesn't work (jumping to section fails)

**Solution**: Make sure the `id` matches the `href`

```html
<!-- This won't work - mismatched names -->
<a href="#features">Go to Features</a>
<section id="feature">  <!-- Should be "features" not "feature" -->

<!-- This will work -->
<a href="#features">Go to Features</a>
<section id="features">
```

#### Issue: Email link doesn't open email client

**Solution**: Make sure you used `mailto:`

```html
<!-- Wrong -->
<a href="your-email@yourcompany.com">Email</a>

<!-- Right -->
<a href="mailto:your-email@yourcompany.com">Email</a>
```

#### Issue: Link opens in same tab instead of new tab

**Solution**: Add `target="_blank"` to open in new tab

```html
<!-- Opens in same tab -->
<a href="https://example.com">Link</a>

<!-- Opens in new tab -->
<a href="https://example.com" target="_blank">Link</a>
```

---

## Adding Privacy and Terms Pages

This section shows you how to create and link your Privacy Policy and Terms of Service pages.

### Why You Need These Pages

- **Legal requirement**: Most jurisdictions require privacy policies if you collect user data
- **Trust**: Customers want to know how you handle their information
- **SEO**: Search engines favor sites with proper legal documentation
- **Professional appearance**: Shows you're a legitimate business

### Step 1: Create the Privacy Policy Page

**Step 1a**: Create a new file

1. Open your text editor
2. Go to File → New File
3. Save it as `privacy.html` in the same folder as your `index.html`

**Step 1b**: Add the basic HTML structure

Copy and paste this template into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Upflex Digital">
    <meta name="author" content="Upflex Digital">
    <title>Privacy Policy | Upflex Digital</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header/Navigation (Copy from index.html) -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-code text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-white hidden sm:block">Upflex Digital</a>
            </div>
            <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-16 md:py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-8 tracking-tight">Privacy Policy</h1>
            <div class="prose prose-invert max-w-none space-y-6">
                <p class="text-gray-300 text-lg">Last Updated: January 2025</p>

                <h2 class="text-2xl font-bold mt-8 mb-4">1. Introduction</h2>
                <p class="text-gray-300 leading-relaxed">
                    Upflex Digital ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">2. Information We Collect</h2>
                <p class="text-gray-300 leading-relaxed">We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="text-gray-300 leading-relaxed space-y-2 ml-6">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, and other information you provide through contact forms</li>
                    <li><strong>Device Information:</strong> Browser type, IP address, and operating system</li>
                    <li><strong>Usage Data:</strong> Pages visited, time spent on pages, and links clicked</li>
                </ul>

                <h2 class="text-2xl font-bold mt-8 mb-4">3. How We Use Your Information</h2>
                <p class="text-gray-300 leading-relaxed">We use the information we collect in the following ways:</p>
                <ul class="text-gray-300 leading-relaxed space-y-2 ml-6">
                    <li>To respond to your inquiries and provide customer service</li>
                    <li>To send promotional communications (with your consent)</li>
                    <li>To improve our website and services</li>
                    <li>To analyze website usage and trends</li>
                    <li>To comply with legal obligations</li>
                </ul>

                <h2 class="text-2xl font-bold mt-8 mb-4">4. Cookies and Tracking Technologies</h2>
                <p class="text-gray-300 leading-relaxed">
                    Our website may use cookies and similar tracking technologies to enhance your experience. You can control cookie preferences through your browser settings.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">5. Third-Party Links</h2>
                <p class="text-gray-300 leading-relaxed">
                    Our Site may contain links to third-party websites. We are not responsible for the privacy practices of other websites. We encourage you to review their privacy policies.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">6. Data Security</h2>
                <p class="text-gray-300 leading-relaxed">
                    We implement appropriate technical and organizational measures to protect your personal information. However, no method of transmission over the Internet is 100% secure.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">7. Your Rights</h2>
                <p class="text-gray-300 leading-relaxed">Depending on your location, you may have the right to:</p>
                <ul class="text-gray-300 leading-relaxed space-y-2 ml-6">
                    <li>Access your personal data</li>
                    <li>Correct inaccurate data</li>
                    <li>Request deletion of your data</li>
                    <li>Opt-out of marketing communications</li>
                </ul>

                <h2 class="text-2xl font-bold mt-8 mb-4">8. Contact Us</h2>
                <p class="text-gray-300 leading-relaxed">
                    If you have questions about this Privacy Policy, please contact us at:
                </p>
                <p class="text-gray-300 leading-relaxed">
                    Email: <a href="mailto:info@upflexdigital.com" class="text-purple-400 hover:text-purple-300">info@upflexdigital.com</a><br>
                    Address: Sacramento, California
                </p>

                <p class="text-gray-400 text-sm mt-12 pt-8 border-t border-gray-700">
                    <strong>Disclaimer:</strong> This is a template privacy policy. Please consult with a legal professional to ensure compliance with applicable laws in your jurisdiction.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 Upflex Digital. All rights reserved.
                </p>
                <div class="mt-4 space-x-4">
                    <a href="index.html" class="text-gray-400 hover:text-purple-400 text-sm">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-purple-400 text-sm">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-purple-400 text-sm">Terms</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 1c**: Customize the privacy policy

1. Replace `info@upflexdigital.com` with your email
2. Replace `Sacramento, California` with your location
3. Update the "Last Updated" date
4. Add or modify the sections to match your actual data practices
5. Replace company name throughout if needed

**Step 1d**: Save the file

Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)

---

### Step 2: Create the Terms of Service Page

**Step 2a**: Create a new file

1. Open your text editor
2. Go to File → New File
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2b**: Add the HTML structure

Copy and paste this template into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Upflex Digital">
    <meta name="author" content="Upflex Digital">
    <title>Terms of Service | Upflex Digital</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header/Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-code text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-white hidden sm:block">Upflex Digital</a>
            </div>
            <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Terms of Service Content -->
    <section class="py-16 md:py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-8 tracking-tight">Terms of Service</h1>
            <div class="prose prose-invert max-w-none space-y-6">
                <p class="text-gray-300 text-lg">Last Updated: January 2025</p>

                <h2 class="text-2xl font-bold mt-8 mb-4">1. Agreement to Terms</h2>
                <p class="text-gray-300 leading-relaxed">
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">2. Use License</h2>
                <p class="text-gray-300 leading-relaxed">
                    Permission is granted to temporarily download one copy of the materials (information or software) on Upflex Digital's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="text-gray-300 leading-relaxed space-y-2 ml-6">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold mt-8 mb-4">3. Disclaimer</h2>
                <p class="text-gray-300 leading-relaxed">
                    The materials on Upflex Digital's website are provided on an 'as is' basis. Upflex Digital makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">4. Limitations</h2>
                <p class="text-gray-300 leading-relaxed">
                    In no event shall Upflex Digital or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Upflex Digital's website.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">5. Accuracy of Materials</h2>
                <p class="text-gray-300 leading-relaxed">
                    The materials appearing on Upflex Digital's website could include technical, typographical, or photographic errors. Upflex Digital does not warrant that any of the materials on its website are accurate, complete, or current. Upflex Digital may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">6. Links</h2>
                <p class="text-gray-300 leading-relaxed">
                    Upflex Digital has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Upflex Digital of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">7. Modifications</h2>
                <p class="text-gray-300 leading-relaxed">
                    Upflex Digital may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">8. Governing Law</h2>
                <p class="text-gray-300 leading-relaxed">
                    These terms and conditions are governed by and construed in accordance with the laws of California and you irrevocably submit to the exclusive jurisdiction of the courts located in Sacramento, California.
                </p>

                <h2 class="text-2xl font-bold mt-8 mb-4">9. Contact Information</h2>
                <p class="text-gray-300 leading-relaxed">
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p class="text-gray-300 leading-relaxed">
                    Email: <a href="mailto:info@upflexdigital.com" class="text-purple-400 hover:text-purple-300">info@upflexdigital.com</a><br>
                    Address: Sacramento, California
                </p>

                <p class="text-gray-400 text-sm mt-12 pt-8 border-t border-gray-700">
                    <strong>Disclaimer:</strong> This is a template terms of service. Please consult with a legal professional to ensure compliance with applicable laws in your jurisdiction.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-950 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 Upflex Digital. All rights reserved.
                </p>
                <div class="mt-4 space-x-4">
                    <a href="index.html" class="text-gray-400 hover:text-purple-400 text-sm">Home</a>
                    <a href="privacy.html" class="text-gray-400 hover:text-purple-400 text-sm">Privacy</a>
                    <a href="terms.html" class="text-gray-400 hover:text-purple-400 text-sm">Terms</a>
                </div>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 2c**: Customize the terms of service

1. Replace `info@upflexdigital.com` with your email
2. Replace `Sacramento, California` with your location
3. Update the "Last Updated" date
4. Modify sections to match your actual business practices
5. Replace company name throughout if needed

**Step 2d**: Save the file

Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)

---

### Step 3: Link the Pages to Your Main Page

The footer already has links to `privacy.html` and `terms.html`, so they should automatically work. However, let's verify and ensure they're correct.

**Step 3a**: Open your `index.html` file

**Step 3b**: Find the footer section (around line 600)

Look for these lines:

```html
<a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a>
```

These links are already correct! They point to the files you just created.

**Step 3c**: Verify the links work

1. Save all three files (`index.html`, `privacy.html`, `terms.html`) in the same folder
2. Open `index.html` in your browser
3. Scroll to the footer
4. Click "Privacy Policy" - you should see the privacy page
5. Click "Terms of Service" - you should see the terms page
6. Click "← Back to Home" on either policy page to return to the main page

---

### Step 4: Add Privacy/Terms Links to Header (Optional)

If you want to add links to your Privacy Policy and Terms of Service in the main navigation menu, follow these steps:

**Step 4a**: Open `index.html`

**Step 4b**: Find the desktop navigation menu (around line 60)

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white...">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white...">Benefits</a>
    <a href="#testimonials" class="text-gray-300 hover:text-white...">Testimonials</a>
    <a href="#faq" class="text-gray-300 hover:text-white...">FAQ</a>
    <a href="#about" class="text-gray-300 hover:text-white...">About</a>
</div>
```

**Step 4c**: Add the new links

Add these lines at the end, before the closing `</div>`:

```html
<a href="privacy.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Privacy</a>
<a href="terms.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Terms</a>
```

Your updated menu should look like:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white...">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white...">Benefits</a>
    <a href="#testimonials" class="text-gray-300 hover:text-white...">Testimonials</a>
    <a href="#faq" class="text-gray-300 hover:text-white...">FAQ</a>
    <a href="#about" class="text-gray-300 hover:text-white...">About</a>
    <a href="privacy.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Privacy</a>
    <a href="terms.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Terms</a>
</div>
```

**Step 4d**: Add to mobile menu (optional)

Find the mobile menu section (around line 69):

```html
<div class="mobile-menu hidden absolute top-full left-0 right-0 bg-gray-800...">
    <div class="flex flex-col space-y-4 px-4 py-6">
        <a href="#features">Features</a>
        <a href="#benefits">Benefits</a>
        <a href="#testimonials">Testimonials</a>
        <a href="#faq">FAQ</a>
        <a href="#about">About</a>
```

Add these lines before the "Get Started" button:

```html
        <a href="privacy.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Privacy</a>
        <a href="terms.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Terms</a>
```

**Step 4e**: Save and test

1. Save `index.html`
2. Refresh your browser
3. Check that the new links appear in the navigation menu
4. Click them to verify they work

---

### Important Reminders About Legal Pages

⚠️ **These are templates only!**

The privacy policy and terms of service templates provided are starting points. You should:

1. **Consult a lawyer** - Have a legal professional review your policies
2. **Customize thoroughly** - Update all company information, contact details, and business practices
3. **Keep them current** - Update when your business practices change
4. **Make them accessible** - Ensure they're easy to find (footer is good)
5. **Match your business** - If you collect data, explain how; if you don't, remove that section

---

## Common Customizations

This section covers the most common changes people make to landing pages.

### 1. Change Company Colors

The landing page uses purple and pink as primary colors. To change them:

**Find all color classes:**

In your text editor, use Find & Replace (`Ctrl+H` or `Cmd+Option+F`):

| To Change | Find | Replace With |
|-----------|------|--------------|
| Purple buttons | `from-purple-600 to-pink-600` | `from-blue-600 to-cyan-600` |
| Purple hover | `hover:border-purple-500` | `hover:border-blue-500` |
| Purple text | `text-purple-400` | `text-blue-400` |
| Purple background | `bg-purple-900` | `bg-blue-900` |

**Example**: To change from purple/pink to blue/cyan:

1. Press `Ctrl+H` (Windows) or `Cmd+Option+F` (Mac)
2. Find: `from-purple-600 to-pink-600`
3. Replace: `from-blue-600 to-cyan-600`
4. Click "Replace All"

Repeat for other color combinations.

### 2. Add Your Logo

The current logo is a code icon. To add your own logo:

**Find the logo code** (appears twice - header and footer):

```html
<div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
    <i class="fas fa-code text-white text-lg"></i>
</div>
```

**Option 1: Use an image file**

```html
<div class="w-10 h-10 flex items-center justify-center">
    <img src="logo.png" alt="Company Logo" class="w-full h-full object-contain">
</div>
```

Then add your `logo.png` file to your project folder.

**Option 2: Use a different icon**

Visit [FontAwesome Icons](https://fontawesome.com/search?o=r&m=free) and find an icon you like. Replace `fa-code` with the icon name:

```html
<!-- Shopping icon -->
<i class="fas fa-shopping-bag text-white text-lg"></i>

<!-- Briefcase icon -->
<i class="fas fa-briefcase text-white text-lg"></i>

<!-- Rocket icon -->
<i class="fas fa-rocket text-white text-lg"></i>

<!-- Star icon -->
<i class="fas fa-star text-white text-lg"></i>
```

### 3. Change Hero Background

The hero section has animated gradient circles. To change them:

**Find this code** (around line 83):

```html
<div class="absolute top-20 right-10 w-72 h-72 bg-purple-500 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-pulse"></div>
<div class="absolute -bottom-8 left-10 w-72 h-72 bg-pink-500 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-pulse"></div>
```

**To change colors:**

```html
<!-- Change to blue -->
<div class="absolute top-20 right-10 w-72 h-72 bg-blue-500 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-pulse"></div>

<!-- Change to green -->
<div class="absolute -bottom-8 left-10 w-72 h-72 bg-green-500 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-pulse"></div>
```

**To change size:**

Replace `w-72 h-72` with different sizes:
- `w-48 h-48` - smaller
- `w-96 h-96` - larger
- `w-full h-full` - full screen

### 4. Add More Features or Benefits

To add a fourth feature card:

**Find the Features section** (around line 117)

**Copy one complete feature card:**

```html
<div class="card-hover group p-8 bg-gradient-to-br from-gray-800 to-gray-900 rounded-xl border border-gray-700 hover:border-purple-500 transition-all duration-300 shadow-lg">
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg flex items-center justify-center mb-6 feature-icon">
        <i class="fas fa-mouse text-white text-2xl"></i>
    </div>
    <h3 class="text-xl md:text-2xl font-bold mb-3">User Experience Focus</h3>
    <p class="text-gray-300 leading-relaxed mb-4">
        We prioritize intuitive navigation...
    </p>
    <ul class="space-y-2 text-sm text-gray-400">
        <li><i class="fas fa-check text-purple-400 mr-2"></i>Intuitive Navigation Design</li>
        <li><i class="fas fa-check text-purple-400 mr-2"></i>User Testing & Optimization</li>
        <li><i class="fas fa-check text-purple-400 mr-2"></i>Conversion Rate Optimization</li>
    </ul>
</div>
```

**Paste it after the third feature**, then customize:

1. Change the icon: Replace `fa-mouse` with another icon
2. Change the title and description
3. Update the bullet points

**Update the grid layout:**

Find this line in the Features section:

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

Change `lg:grid-cols-3` to `lg:grid-cols-4` to fit 4 columns on large screens.

### 5. Modify Testimonials

To add a new testimonial or change existing ones:

**Find a testimonial card** (around line 282):

```html
<div class="card-hover p-8 bg-gradient-to-br from-gray-800 to-gray-900 rounded-xl border border-gray-700 hover:border-purple-500 transition-all duration-300 shadow-lg">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-300 mb-6 leading-relaxed text-sm md:text-base">
        "Your testimonial quote goes here..."
    </p>
    <div class="flex items-center space-x-4">
        <div class="w-12 h-12 bg-gradient-to-br from-purple-500 to-pink-500 rounded-full flex items-center justify-center">
            <i class="fas fa-user text-white"></i>
        </div>
        <div>
            <p class="font-bold text-white">Client Name</p>
            <p class="text-sm text-gray-400">Title, Company Name</p>
        </div>
    </div>
</div>
```

**To customize:**

1. Replace the quote text
2. Replace the client name
3. Replace the title and company

**To change star rating:**

Remove or add `<i class="fas fa-star"></i>` lines:
- 5 stars = 5 lines (excellent)
- 4 stars = 4 lines (very good)
- 3 stars = 3 lines (good)

### 6. Change Section Background Colors

Each section has a background color. To change:

**Find the section** you want to change:

```html
<!-- Features section - light gray background -->
<section id="features" class="py-16 md:py-24 bg-gray-800 bg-opacity-50">

<!-- Benefits section - dark background -->
<section id="benefits" class="py-16 md:py-24 bg-gray-900">
```

**To change:**

```html
<!-- Change to purple background -->
<section id="features" class="py-16 md:py-24 bg-purple-900">

<!-- Change to transparent -->
<section id="features" class="py-16 md:py-24 bg-transparent">

<!-- Change to blue with opacity -->
<section id="features" class="py-16 md:py-24 bg-blue-800 bg-opacity-30">
```

### 7. Add Social Media Icons

The footer has social media icons. To add more or change them:

**Find the social icons** (around line 560):

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="Facebook">
        <i class="fab fa-facebook-f"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="Twitter">
        <i class="fab fa-twitter"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="LinkedIn">
        <i class="fab fa-linkedin-in"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="Instagram">
        <i class="fab fa-instagram"></i>
    </a>
</div>
```

**To add your social links:**

```html
<a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To add more platforms:**

Find icons at [FontAwesome](https://fontawesome.com/search?o=r&m=free&s=brands) and add:

```html
<!-- YouTube -->
<a href="https://youtube.com/yourchannel" class="text-gray-400 hover:text-purple-400...">
    <i class="fab fa-youtube"></i>
</a>

<!-- TikTok -->
<a href="https://tiktok.com/@yourprofile" class="text-gray-400 hover:text-purple-400...">
    <i class="fab fa-tiktok"></i>
</a>

<!-- GitHub -->
<a href="https://github.com/yourprofile" class="text-gray-400 hover:text-purple-400...">
    <i class="fab fa-github"></i>
</a>
```

### 8. Change Font Sizes

To make text larger or smaller throughout:

**Headings (h1, h2, h3):**

```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">Heading</h1>

<!-- Make smaller -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">Heading</h1>

<!-- Make larger -->
<h1 class="text-5xl md:text-6xl lg:text-7xl">Heading</h1>
```

**Body text:**

```html
<!-- Original -->
<p class="text-lg md:text-xl">Paragraph</p>

<!-- Make smaller -->
<p class="text-base md:text-lg">Paragraph</p>

<!-- Make larger -->
<p class="text-xl md:text-2xl">Paragraph</p>
```

---

## Troubleshooting

### Issue: Changes aren't showing up

**Solution 1: Clear browser cache**
- Press `Ctrl+Shift+Delete` (Windows) or `Cmd+Shift+Delete` (Mac)
- Select "All time"
- Click "Clear data"

**Solution 2: Hard refresh**
- Press `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)

**Solution 3: Check file was saved**
- Look at the filename in your editor - unsaved files often show a dot or asterisk
- Press `Ctrl+S` or `Cmd+S` to save

### Issue: Text is cut off or overlapping

**Solution**: Check spacing classes

```html
<!-- Add more space -->
<div class="mb-8">Content</div>  <!-- Instead of mb-4 -->
<div class="p-8">Content</div>   <!-- Instead of p-4 -->
```

### Issue: Colors look wrong

**Solution**: Check color names are correct

❌ **Wrong:**
```html
<div class="bg-purpel-900">  <!-- Typo: "purpel" -->
```

✅ **Right:**
```html
<div class="bg-purple-900">  <!-- Correct spelling -->
```

### Issue: Mobile menu doesn't work

**Solution**: Check JavaScript is enabled

1. Right-click on the page
2. Select "Inspect" or "Inspect Element"
3. Go to the "Console" tab
4. Look for red error messages

If you see errors, the JavaScript might not be loading correctly.

### Issue: Links don't work

**Solution**: Check href values

❌ **Wrong:**
```html
<a href="www.example.com">Link</a>  <!-- Missing https:// -->
```

✅ **Right:**
```html
<a href="https://www.example.com">Link</a>
```

### Issue: Images don't display

**Solution**: Check file path

```html
<!-- If image is in same folder -->
<img src="image.png" alt="Description">

<!-- If image is in subfolder -->
<img src="images/image.png" alt="Description">

<!-- If image is from internet -->
<img src="https://example.com/image.png" alt="Description">
```

### Issue: Styling looks broken

**Solution**: Check all class names are spelled correctly

Tailwind only works if class names are exact. Common typos:

- `md:flex` (correct) vs `md-flex` (wrong)
- `text-white` (correct) vs `text-wh` (wrong)
- `bg-gray-900` (correct) vs `bg-grey-900` (wrong - it's "gray" not "grey")

### Issue: Animation is too fast or too slow

**Solution**: Modify animation classes

```html
<!-- Original - medium speed -->
<div class="animate-pulse">

<!-- Slower animation -->
<div class="animate-pulse" style="animation-duration: 3s;">

<!-- Faster animation -->
<div class="animate-pulse" style="animation-duration: 1s;">
```

### Issue: Page looks different on mobile

**Solution**: Check responsive classes

Always use responsive prefixes:

❌ **Wrong:**
```html
<h1 class="text-6xl">Heading</h1>  <!-- Too big on mobile! -->
```

✅ **Right:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">Heading</h1>
```

### Issue: Can't find where to edit something

**Solution**: Use Find function

1. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac)
2. Type the text you want to find
3. Press Enter to jump to it

---

## Best Practices for Maintenance

### Regular Updates

- **Monthly**: Review analytics and update testimonials
- **Quarterly**: Check all links are working
- **Annually**: Update copyright year and review content accuracy

### Before Publishing Changes

1. **Save your file** - `Ctrl+S` or `Cmd+S`
2. **Test in browser** - Refresh and check everything works
3. **Test on mobile** - Use browser's responsive design mode
4. **Test all links** - Click every link to verify
5. **Check spelling** - Use spell checker or read through carefully
6. **Backup** - Keep a copy of the original file

### Version Control

Keep backups of your files:

```
project-folder/
├── index.html (current version)
├── index-backup.html (previous version)
├── index-v1.html (original version)
```

### Security

- Keep email addresses and phone numbers current
- Regularly update privacy policy
- Use HTTPS (not HTTP) for all external links
- Don't store sensitive information in HTML

---

## Additional Resources

### Learning More

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [FontAwesome Icons](https://fontawesome.com/search?o=r&m=free)
- [CSS Tricks](https://css-tricks.com/)

### Tools

- [VS Code](https://code.visualstudio.com/) - Text editor
- [Responsively App](https://responsively.app/) - Test on multiple devices
- [Chrome DevTools](https://developer.chrome.com/docs/devtools/) - Debug issues
- [Lighthouse](https://developers.google.com/web/tools/lighthouse) - Performance testing

### Getting Help

- Check the [Tailwind CSS docs](https://tailwindcss.com/docs) for class reference
- Use browser DevTools (F12) to inspect elements
- Search for your issue online - someone has probably had it before!

---

## Conclusion

You now have a comprehensive guide for maintaining and customizing your Upflex Digital landing page. The key points to remember:

1. **Text updates** - Find the text between HTML tags and replace it
2. **Styling changes** - Modify Tailwind CSS classes while keeping responsive prefixes
3. **Link management** - Use Find & Replace to update multiple links at once
4. **Legal pages** - Create privacy.html and terms.html in your project folder
5. **Testing** - Always test changes in your browser before publishing

For questions or issues, refer to the Troubleshooting section or consult the provided resources. Happy customizing! 🚀