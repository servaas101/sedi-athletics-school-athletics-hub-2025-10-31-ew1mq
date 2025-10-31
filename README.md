# Sedi Athletics Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting](#troubleshooting)

---

## Overview

This README provides comprehensive guidance for maintaining and customizing the Sedi Athletics landing page. The page is built with:

- **HTML5** for structure
- **Tailwind CSS** for styling (via CDN)
- **Font Awesome** for icons
- **Vanilla JavaScript** for interactivity

**No build tools or installations are required** — you can edit the file directly in any text editor and see changes immediately in your browser.

---

## Project Structure

Your landing page (`index.html`) contains these main sections:

```
index.html
├── Header & Navigation (sticky, responsive)
├── Hero Section (gradient background, CTAs)
├── Features Section (5 feature cards)
├── Benefits Section (3 benefit cards with icons)
├── About Us Section (company description)
├── Testimonials Section (4 testimonial cards)
├── CTA Section (call-to-action with background image)
├── FAQ Section (expandable accordion)
├── Footer (links, contact, social media)
└── JavaScript (mobile menu, FAQ toggle, smooth scroll)
```

---

## Updating Text Content

### Understanding the Structure

Text content in HTML is placed between opening and closing tags. For example:

```html
<h1>This is a heading</h1>
<p>This is a paragraph</p>
```

To update text, simply replace the content between the tags while keeping the tags themselves intact.

### Key Sections to Update

#### 1. **Page Title & Meta Description**

**Location:** Lines 7-8 in the `<head>` section

**Current Code:**
```html
<meta name="description" content="Sedi Athletics - School Athletics Hub. Track every race. Celebrate every champion. Central results hub with verified data and easy uploads.">
<title>Sedi Athletics — School Athletics Hub | Track Every Race</title>
```

**How to Update:**
- The `content=""` attribute in the meta description appears in search results
- The `<title>` appears in browser tabs and search results
- Keep descriptions under 160 characters for search engines

**Example Update:**
```html
<meta name="description" content="Your School Name Athletics - Manage races, track results, celebrate champions.">
<title>Your School Name Athletics | Track Every Race</title>
```

#### 2. **Header Navigation Text**

**Location:** Lines 33-43 (desktop menu) and Lines 51-59 (mobile menu)

**Current Code:**
```html
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
```

**How to Update:**
- Change the text between `>` and `</a>` to rename menu items
- Keep the `href="#"` attributes intact — they link to sections below

**Example:**
```html
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Our Features</a>
```

#### 3. **Hero Section (Main Banner)**

**Location:** Lines 65-88

**Current Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
    Sedi Athletics — School Athletics Hub
</h1>
<p class="text-xl md:text-2xl font-light mb-4 text-purple-100 max-w-3xl mx-auto">
    Track every race. Celebrate every champion.
</p>
```

**How to Update:**
- Replace the heading text (h1) with your own main message
- Update the subheading (first p tag) with your tagline
- Update the description (second p tag) with your value proposition

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
    Lincoln High School Athletics
</h1>
<p class="text-xl md:text-2xl font-light mb-4 text-purple-100 max-w-3xl mx-auto">
    Excellence in Every Event
</p>
```

#### 4. **Features Section**

**Location:** Lines 104-176 (5 feature cards)

**Current Code (Example - Race Results):**
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Race Results</h3>
<p class="text-gray-600 leading-relaxed">
    Real-time race result tracking with automatic timing integration. Capture every finish line moment and instantly update your community.
</p>
```

**How to Update:**
- Change the `<h3>` text to rename features
- Change the `<p>` text to update feature descriptions
- Keep the icon code (`<i class="fas fa-...">`) unchanged if you want the same icons

**Example:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Live Race Updates</h3>
<p class="text-gray-600 leading-relaxed">
    See real-time updates as athletes cross the finish line. Parents and supporters get instant notifications.
</p>
```

#### 5. **Benefits Section**

**Location:** Lines 189-283 (3 benefit cards)

**Current Code (Example - Central Hub):**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Central Results Hub</h3>
<p class="text-gray-700 leading-relaxed mb-4">
    Consolidate all your athletics data in one unified platform...
</p>
```

**How to Update:**
- Replace heading and description text
- Update the bullet points in the `<ul>` lists below each benefit

**Example:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">One Complete Platform</h3>
<p class="text-gray-700 leading-relaxed mb-4">
    Manage all your school's athletic programs in a single, easy-to-use system...
</p>
```

#### 6. **About Us Section**

**Location:** Lines 288-325

**Current Code:**
```html
<p class="text-lg text-gray-700 leading-relaxed">
    Sedi Athletics was founded with a simple yet powerful vision...
</p>
```

**How to Update:**
- Replace the entire paragraph text with your school's story
- Keep the `<p>` tags intact
- You can add or remove paragraphs as needed

**Example:**
```html
<p class="text-lg text-gray-700 leading-relaxed">
    Lincoln High School has been a leader in athletics for over 50 years...
</p>
```

#### 7. **Testimonials Section**

**Location:** Lines 342-426 (4 testimonial cards)

**Current Code (Example):**
```html
<p class="text-gray-700 mb-6 leading-relaxed text-base">
    "Sedi Athletics has completely transformed how we manage our school's track and field program..."
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-semibold text-gray-900">Coach Michael Thompson</p>
    <p class="text-gray-600 text-sm">Head Track & Field Coach, Riverside High School</p>
</div>
```

**How to Update:**
- Replace the quote text in the first `<p>` tag
- Update the name in the `font-semibold` line
- Update the title/role in the last `<p>` tag

**Example:**
```html
<p class="text-gray-700 mb-6 leading-relaxed text-base">
    "This platform has helped us track our athletes' progress like never before..."
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-semibold text-gray-900">Sarah Johnson</p>
    <p class="text-gray-600 text-sm">Athletic Director, Lincoln High School</p>
</div>
```

#### 8. **FAQ Section**

**Location:** Lines 476-560 (5 FAQ items)

**Current Code (Example):**
```html
<button class="faq-question w-full p-6 flex items-center justify-between hover:bg-gray-50 transition-colors duration-300 cursor-pointer">
    <h3 class="text-lg font-semibold text-gray-900 text-left">
        How easy is it to migrate our existing data to Sedi Athletics?
    </h3>
    <i class="fas fa-chevron-down faq-icon text-purple-600 text-xl"></i>
</button>
<div class="faq-answer hidden border-t border-gray-200 p-6 bg-gray-50">
    <p class="text-gray-700 leading-relaxed">
        Migration is seamless and straightforward...
    </p>
</div>
```

**How to Update:**
- Change the question text in the `<h3>` tag
- Change the answer text in the `<p>` tag inside `faq-answer`
- The `hidden` class and icon will work automatically

**Example:**
```html
<h3 class="text-lg font-semibold text-gray-900 text-left">
    How do I upload race results?
</h3>
```

#### 9. **Footer Content**

**Location:** Lines 576-650

**Current Code (Example - Brand Section):**
```html
<span class="text-xl font-bold text-white">Sedi Athletics</span>
<p class="text-gray-400 mb-4">
    Empowering schools to celebrate athletic excellence through modern technology.
</p>
```

**How to Update:**
- Replace the brand name
- Update the tagline/description
- Update footer links and contact information

**Example:**
```html
<span class="text-xl font-bold text-white">Lincoln High Athletics</span>
<p class="text-gray-400 mb-4">
    Celebrating student athletes and building champions since 1975.
</p>
```

---

## Modifying Tailwind CSS Classes

### What Are Tailwind CSS Classes?

Tailwind CSS uses utility classes to style elements. Instead of writing traditional CSS, you add class names directly to HTML elements. For example:

```html
<div class="bg-white p-8 rounded-lg shadow-md">
    Content here
</div>
```

This means:
- `bg-white` = white background
- `p-8` = padding (spacing inside)
- `rounded-lg` = slightly rounded corners
- `shadow-md` = medium shadow effect

### Understanding Responsive Classes

This landing page uses responsive design, meaning it looks good on phones, tablets, and desktops. Tailwind uses prefixes for this:

- `md:` = applies on medium screens and larger (tablets)
- `lg:` = applies on large screens and larger (desktops)

**Example:**
```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
    Responsive Heading
</h1>
```

This means:
- **Mobile:** 2xl font size
- **Tablet (md):** 4xl font size
- **Desktop (lg):** 6xl font size

### Common Tailwind Classes Used in This Landing Page

#### **Colors**

| Class | What It Does |
|-------|-------------|
| `bg-white` | White background |
| `bg-gray-50` | Very light gray background |
| `bg-gray-900` | Very dark gray/almost black background |
| `text-white` | White text |
| `text-gray-700` | Dark gray text |
| `text-purple-600` | Purple text |
| `text-pink-600` | Pink text |

**How to Change Colors:**

Find a section you want to modify. For example, the hero section uses:

```html
<section class="hero-gradient text-white py-24 md:py-32 lg:py-40">
```

The `hero-gradient` class is defined in the `<style>` section (lines 15-18):

```css
.hero-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

**To change the gradient:**

1. Find this style section
2. Replace the color codes:
   - `#667eea` = first color (currently purple)
   - `#764ba2` = second color (currently darker purple)

**Example - Change to blue/teal:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #0084ff 0%, #00d4ff 100%);
}
```

#### **Spacing (Padding & Margins)**

| Class | Spacing Amount |
|-------|---|
| `p-4` | Padding: 1 unit (16px) |
| `p-6` | Padding: 1.5 units (24px) |
| `p-8` | Padding: 2 units (32px) |
| `mb-4` | Margin bottom: 1 unit |
| `mb-6` | Margin bottom: 1.5 units |
| `mb-16` | Margin bottom: 4 units (64px) |
| `space-x-2` | Horizontal spacing between children: 0.5 unit |
| `space-y-4` | Vertical spacing between children: 1 unit |

**How to Adjust Spacing:**

Example: Feature cards currently have `p-8` (32px padding):

```html
<div class="feature-card bg-white rounded-xl shadow-md p-8 hover:shadow-xl">
```

To reduce padding to 24px, change to `p-6`:

```html
<div class="feature-card bg-white rounded-xl shadow-md p-6 hover:shadow-xl">
```

#### **Typography (Text Styling)**

| Class | What It Does |
|-------|-------------|
| `text-xl` | Extra large text |
| `text-2xl` | 2x large text |
| `text-4xl` | 4x large text |
| `font-bold` | Bold text |
| `font-semibold` | Semi-bold text |
| `font-light` | Light text |
| `tracking-tight` | Tight letter spacing |
| `leading-relaxed` | Relaxed line spacing |

**How to Change Text Size:**

Example: The main heading in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
```

To make it slightly smaller on mobile:

```html
<h1 class="text-3xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
```

#### **Shadows & Borders**

| Class | Effect |
|-------|--------|
| `shadow-md` | Medium shadow |
| `shadow-lg` | Large shadow |
| `shadow-xl` | Extra large shadow |
| `rounded-lg` | Slightly rounded corners |
| `rounded-xl` | More rounded corners |
| `border` | 1px border |
| `border-t` | Top border only |
| `border-gray-200` | Light gray border |

**How to Add More Shadow:**

Feature cards currently have `shadow-md`:

```html
<div class="feature-card bg-white rounded-xl shadow-md p-8">
```

To make them stand out more, change to `shadow-lg`:

```html
<div class="feature-card bg-white rounded-xl shadow-lg p-8">
```

#### **Transitions & Hover Effects**

| Class | Effect |
|-------|--------|
| `transition-all` | Smooth animation |
| `duration-300` | 300ms animation speed |
| `hover:text-purple-600` | Changes text color on hover |
| `hover:shadow-xl` | Adds shadow on hover |
| `hover:scale-105` | Slightly enlarges on hover |
| `hover:translate-y-[-8px]` | Moves up on hover |

**How to Modify Hover Effects:**

Buttons currently scale up 5% on hover:

```html
<a class="btn-primary bg-white text-purple-600 px-8 py-4 rounded-lg font-bold text-lg hover:shadow-xl transition-all duration-300 inline-block">
```

The `hover:shadow-xl` adds extra shadow. To also change color on hover, add this class:

```html
<a class="btn-primary bg-white text-purple-600 px-8 py-4 rounded-lg font-bold text-lg hover:shadow-xl hover:text-pink-600 transition-all duration-300 inline-block">
```

### Grid & Layout Classes

| Class | Purpose |
|-------|---------|
| `grid` | Creates a grid layout |
| `grid-cols-1` | 1 column (mobile) |
| `md:grid-cols-2` | 2 columns on tablets |
| `lg:grid-cols-3` | 3 columns on desktops |
| `gap-6` | 1.5 unit spacing between items |
| `gap-8` | 2 unit spacing between items |
| `flex` | Creates flexible layout |
| `justify-between` | Spreads items apart |
| `items-center` | Centers items vertically |

**Example: Feature Cards Grid**

Current code (lines 123-124):

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-6">
```

This means:
- **Mobile:** 1 column
- **Tablet:** 2 columns
- **Desktop:** 5 columns
- Gap between items: 1.5 units

To show 3 columns on tablets instead:

```html
<div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5 gap-6">
```

### Practical Example: Customizing a Section Background

**Current testimonials section (line 330):**

```html
<section id="testimonials" class="py-24 md:py-32 bg-white">
```

**To change to light gray background:**

```html
<section id="testimonials" class="py-24 md:py-32 bg-gray-50">
```

**To add a gradient background:**

1. First, add a custom style in the `<style>` section
2. Then use it in the class

Add this to the `<style>` section (around line 18):

```css
.testimonial-section-bg {
    background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
}
```

Then update the section:

```html
<section id="testimonials" class="py-24 md:py-32 testimonial-section-bg">
```

### Troubleshooting Tailwind Changes

**Problem:** Changes aren't showing up

**Solution:** 
- Make sure you're using the correct class name (check spelling)
- Clear your browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Hard refresh the page (Ctrl+F5 or Cmd+Shift+R)

**Problem:** Layout breaks on mobile

**Solution:**
- Check that you have mobile-first classes: `grid-cols-1` for mobile, then `md:` and `lg:` for larger screens
- Don't remove responsive prefixes

---

## Fixing and Managing Links

### Understanding Links in HTML

Links are created with the `<a>` tag:

```html
<a href="https://example.com">Click Here</a>
```

Breaking this down:
- `<a>` = anchor (link) tag
- `href=""` = where the link goes
- The text between `>` and `</a>` = what users see

### Types of Links in This Landing Page

#### **1. Internal Navigation Links (Within the Page)**

These use `#` followed by a section ID:

```html
<a href="#features">Features</a>
```

This links to:

```html
<section id="features" class="py-24 md:py-32 bg-gray-50">
```

**Key Point:** The `href="#features"` must match the `id="features"` exactly.

#### **2. External Links (Outside the Page)**

These use full URLs starting with `http://` or `https://`:

```html
<a href="https://sediathleticssports.co.za">Get Started</a>
```

#### **3. Email Links**

These use `mailto:`:

```html
<a href="mailto:info@sediathleticssports.co.za">Email Us</a>
```

### All Links in Your Landing Page

#### **Header Navigation**

**Location:** Lines 33-43 (desktop) and 51-59 (mobile)

| Link Text | Current URL | Type | Purpose |
|-----------|------------|------|---------|
| Features | `#features` | Internal | Scrolls to Features section |
| Benefits | `#benefits` | Internal | Scrolls to Benefits section |
| Testimonials | `#testimonials` | Internal | Scrolls to Testimonials section |
| FAQ | `#faq` | Internal | Scrolls to FAQ section |
| Get Started | `https://sediathleticssports.co.za` | External | Main CTA button |

#### **Hero Section**

**Location:** Lines 82-92

| Link Text | Current URL | Purpose |
|-----------|------------|---------|
| Launch Your Hub | `https://sediathleticssports.co.za` | Primary CTA |
| Explore Features | `#features` | Scroll to features |

#### **CTA Section**

**Location:** Lines 456-470

| Link Text | Current URL | Purpose |
|-----------|------------|---------|
| Launch Your Hub Now | `https://sediathleticssports.co.za` | Main CTA |

#### **Footer**

**Location:** Lines 576-650

| Link Text | Current URL | Purpose |
|-----------|------------|---------|
| Features | `#features` | Internal navigation |
| Benefits | `#benefits` | Internal navigation |
| Testimonials | `#testimonials` | Internal navigation |
| FAQ | `#faq` | Internal navigation |
| Blog | `blog.html` | External page |
| Privacy Policy | `privacy.html` | External page |
| Terms of Service | `terms.html` | External page |
| Contact Us | `https://sediathleticssports.co.za` | External link |
| Facebook | `#` | Social media (placeholder) |
| Twitter | `#` | Social media (placeholder) |
| Instagram | `#` | Social media (placeholder) |
| LinkedIn | `#` | Social media (placeholder) |
| Email | `mailto:info@sediathleticssports.co.za` | Email link |
| Website | `https://sediathleticssports.co.za` | External link |

### Step-by-Step: Update All Links

#### **Step 1: Update the Main Website URL**

This URL appears multiple times throughout the page. Search for `sediathleticssports.co.za` and replace it with your own domain.

**Locations to update:**

1. **Line 43** (desktop menu Get Started button):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">Get Started</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">Get Started</a>
```

2. **Line 59** (mobile menu Get Started button):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">Get Started</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">Get Started</a>
```

3. **Line 87** (hero section primary button):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">Launch Your Hub</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">Launch Your Hub</a>
```

4. **Line 467** (CTA section button):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">Launch Your Hub Now</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">Launch Your Hub Now</a>
```

5. **Line 620** (footer Get Started button):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">Get Started</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">Get Started</a>
```

6. **Line 633** (footer Contact Us link):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">Contact Us</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">Contact Us</a>
```

7. **Line 641** (footer website link):
```html
<!-- BEFORE -->
<a href="https://sediathleticssports.co.za" class="...">sediathleticssports.co.za</a>

<!-- AFTER -->
<a href="https://yourschool.edu" class="...">yourschool.edu</a>
```

**Pro Tip:** Use Find & Replace (Ctrl+H or Cmd+H in most editors) to replace all instances at once:
- Find: `sediathleticssports.co.za`
- Replace with: `yourschool.edu`

#### **Step 2: Update Email Address**

**Location:** Line 636

```html
<!-- BEFORE -->
<a href="mailto:info@sediathleticssports.co.za">info@sediathleticssports.co.za</a>

<!-- AFTER -->
<a href="mailto:info@yourschool.edu">info@yourschool.edu</a>
```

#### **Step 3: Update Social Media Links**

**Location:** Lines 602-611 (footer social icons)

```html
<!-- BEFORE -->
<a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- AFTER -->
<a href="https://facebook.com/yourschoolname" class="text-gray-400 hover:text-purple-400 transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

Replace each social media link:

- **Facebook:** `https://facebook.com/yourschoolname`
- **Twitter:** `https://twitter.com/yourschoolhandle`
- **Instagram:** `https://instagram.com/yourschoolname`
- **LinkedIn:** `https://linkedin.com/company/yourschoolname`

#### **Step 4: Verify All Internal Links Work**

Test that section links work correctly:

1. Click on "Features" in the menu — should scroll to the Features section
2. Click on "Benefits" — should scroll to Benefits section
3. Click on "Testimonials" — should scroll to Testimonials section
4. Click on "FAQ" — should scroll to FAQ section

**If links don't work:**

Check that the `id` attribute in sections matches the `href`:

```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Must match this section ID -->
<section id="features" class="...">
```

### Adding New Links

To add a new link to your page:

```html
<a href="https://example.com" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">
    Link Text
</a>
```

Breaking this down:
- `href=""` = where the link goes
- `class=""` = styling (copy from similar links)
- Text between tags = what users see

**For internal links (within your page):**
```html
<a href="#section-id">Go to Section</a>
```

**For external links:**
```html
<a href="https://example.com">Visit Example</a>
```

**For email links:**
```html
<a href="mailto:email@example.com">Send Email</a>
```

---

## Adding Privacy and Terms Pages

### Understanding Page Structure

Your landing page is currently a single file: `index.html`

To add privacy and terms pages, you'll create two new HTML files:
- `privacy.html` (Privacy Policy)
- `terms.html` (Terms of Service)

These files already have placeholder links in your footer (lines 630-631), but the pages don't exist yet.

### Step-by-Step: Create Privacy Policy Page

#### **Step 1: Create a New File**

1. Open your text editor (Notepad, Visual Studio Code, etc.)
2. Create a new file
3. Save it as `privacy.html` in the same folder as your `index.html`

#### **Step 2: Add the HTML Structure**

Copy this template into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Sedi Athletics">
    <meta name="author" content="Sedi Athletics">
    <title>Privacy Policy - Sedi Athletics</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-running text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Sedi Athletics</a>
            </div>

            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Testimonials</a>
                <a href="index.html#faq" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">FAQ</a>
                <a href="https://sediathleticssports.co.za" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-lg font-semibold hover:shadow-lg transition-all duration-300">Get Started</a>
            </div>

            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300" aria-label="Toggle menu">
                <i class="fas fa-bars text-gray-900 text-xl"></i>
            </button>

            <div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white border-t border-gray-200 md:hidden">
                <div class="flex flex-col space-y-4 p-4">
                    <a href="index.html#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">Benefits</a>
                    <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">Testimonials</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">FAQ</a>
                    <a href="https://sediathleticssports.co.za" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-lg font-semibold text-center hover:shadow-lg transition-all duration-300">Get Started</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="bg-white rounded-xl shadow-md p-8 space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Sedi Athletics ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>Personal Data: Name, email address, phone number, school name, and other information you voluntarily provide.</li>
                        <li>Device Data: Browser type, IP address, operating system, and device identifiers.</li>
                        <li>Usage Data: Pages visited, time spent on pages, links clicked, and other usage information.</li>
                        <li>Athletic Data: Race results, athlete information, and performance data you upload to our platform.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Your Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>Create and manage your account.</li>
                        <li>Process your transactions and send related information.</li>
                        <li>Improve our website and services.</li>
                        <li>Send promotional communications (with your consent).</li>
                        <li>Respond to your inquiries and provide customer support.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Disclosure of Your Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We may share information we have collected about you in certain situations:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 mt-4">
                        <li>By Law or to Protect Rights: If required by law or if we believe in good faith that disclosure is necessary.</li>
                        <li>Third-Party Service Providers: We may share your information with vendors who assist us in operating our website and conducting our business.</li>
                        <li>Business Transfers: If we are involved in a merger, acquisition, or asset sale, your information may be transferred.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Security of Your Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your personal information, we cannot guarantee its absolute security.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:info@sediathleticssports.co.za" class="text-purple-600 hover:text-purple-800">info@sediathleticssports.co.za</a>
                    </p>
                </div>

                <div class="border-t border-gray-200 pt-8">
                    <p class="text-gray-600 text-sm">
                        Last Updated: January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-running text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">Sedi Athletics</span>
                    </div>
                    <p class="text-gray-400 mb-4">
                        Empowering schools to celebrate athletic excellence through modern technology.
                    </p>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-6">Product</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">FAQ</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-6">Company</h4>
                    <ul class="space-y-3">
                        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Blog</a></li>
                        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="https://sediathleticssports.co.za" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Contact Us</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-6">Get In Touch</h4>
                    <p class="text-gray-400 mb-2">
                        <i class="fas fa-envelope mr-2"></i>
                        <a href="mailto:info@sediathleticssports.co.za" class="hover:text-purple-400 transition-colors duration-300">info@sediathleticssports.co.za</a>
                    </p>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-400 text-sm mb-4 md:mb-0">
                        &copy; 2025 Sedi Athletics. All rights reserved.
                    </p>
                    <div class="flex space-x-6 text-sm">
                        <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy</a>
                        <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

#### **Step 3: Customize the Privacy Policy**

Replace the placeholder content with your actual privacy policy. Key sections to customize:

1. **Introduction:** Add your school's name and specific details
2. **Information We Collect:** List what data your school collects
3. **Use of Your Information:** Explain how you use the data
4. **Disclosure:** Explain when you share data
5. **Contact Us:** Update with your school's contact information

**Example customization:**

```html
<p class="text-gray-700 leading-relaxed">
    Lincoln High School ("we," "us," "our," or "School") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our athletics website and use our services.
</p>
```

### Step-by-Step: Create Terms of Service Page

#### **Step 1: Create a New File**

1. Open your text editor
2. Create a new file
3. Save it as `terms.html` in the same folder as your `index.html`

#### **Step 2: Add the HTML Structure**

Copy this template into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Sedi Athletics">
    <meta name="author" content="Sedi Athletics">
    <title>Terms of Service - Sedi Athletics</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-running text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Sedi Athletics</a>
            </div>

            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Testimonials</a>
                <a href="index.html#faq" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">FAQ</a>
                <a href="https://sediathleticssports.co.za" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-lg font-semibold hover:shadow-lg transition-all duration-300">Get Started</a>
            </div>

            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-100 transition-colors duration-300" aria-label="Toggle menu">
                <i class="fas fa-bars text-gray-900 text-xl"></i>
            </button>

            <div class="mobile-menu hidden absolute top-full left-0 right-0 bg-white border-t border-gray-200 md:hidden">
                <div class="flex flex-col space-y-4 p-4">
                    <a href="index.html#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">Benefits</a>
                    <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">Testimonials</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300 py-2">FAQ</a>
                    <a href="https://sediathleticssports.co.za" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-lg font-semibold text-center hover:shadow-lg transition-all duration-300">Get Started</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="bg-white rounded-xl shadow-md p-8 space-y-8">
                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        By accessing and using this website and service, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on Sedi Athletics' website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials on Sedi Athletics' website are provided on an 'as is' basis. Sedi Athletics makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall Sedi Athletics or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Sedi Athletics' website, even if Sedi Athletics or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials appearing on Sedi Athletics' website could include technical, typographical, or photographic errors. Sedi Athletics does not warrant that any of the materials on its website are accurate, complete, or current. Sedi Athletics may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Sedi Athletics has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Sedi Athletics of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Sedi Athletics may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of South Africa, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Contact Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:info@sediathleticssports.co.za" class="text-purple-600 hover:text-purple-800">info@sediathleticssports.co.za</a>
                    </p>
                </div>

                <div class="border-t border-gray-200 pt-8">
                    <p class="text-gray-600 text-sm">
                        Last Updated: January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-running text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">Sedi Athletics</span>
                    </div>
                    <p class="text-gray-400 mb-4">
                        Empowering schools to celebrate athletic excellence through modern technology.
                    </p>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-6">Product</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">FAQ</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-6">Company</h4>
                    <ul class="space-y-3">
                        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Blog</a></li>
                        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="https://sediathleticssports.co.za" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Contact Us</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-semibold mb-6">Get In Touch</h4>
                    <p class="text-gray-400 mb-2">
                        <i class="fas fa-envelope mr-2"></i>
                        <a href="mailto:info@sediathleticssports.co.za" class="hover:text-purple-400 transition-colors duration-300">info@sediathleticssports.co.za</a>
                    </p>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-400 text-sm mb-4 md:mb-0">
                        &copy; 2025 Sedi Athletics. All rights reserved.
                    </p>
                    <div class="flex space-x-6 text-sm">
                        <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy</a>
                        <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

#### **Step 3: Customize the Terms of Service**

Replace placeholder content with your actual terms. Key sections:

1. **Agreement to Terms:** Your school's specific terms
2. **Use License:** How users can use your site
3. **Disclaimer:** Your liability disclaimers
4. **Limitations:** Liability limitations
5. **Contact Information:** Your school's contact details

### Verifying Links Work

After creating `privacy.html` and `terms.html`:

1. **In your browser**, navigate to your website
2. **Scroll to the footer**
3. **Click "Privacy Policy"** — should open `privacy.html`
4. **Click "Terms of Service"** — should open `terms.html`
5. **Click the logo or "Features" link** — should return to `index.html`

**If links don't work:**

Check that:
- File names match exactly (case-sensitive on some servers)
- Files are in the same folder as `index.html`
- Links use correct file names: `privacy.html`, `terms.html`

### File Structure After Adding Pages

```
your-folder/
├── index.html          (main landing page)
├── privacy.html        (new privacy policy)
├── terms.html          (new terms of service)
└── blog.html           (optional, for future use)
```

---

## Common Customizations

### 1. Changing the Hero Section Background Color

**Current code (line 14-16):**
```css
.hero-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

**Change to blue/cyan gradient:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #0084ff 0%, #00d4ff 100%);
}
```

**Change to green/teal gradient:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #00b894 0%, #00cec9 100%);
}
```

### 2. Changing Feature Card Icons

**Current code (example - line 129):**
```html
<i class="fas fa-flag-checkered text-white text-2xl"></i>
```

**To use a different icon**, visit [Font Awesome Icons](https://fontawesome.com/icons) and find your icon. Replace `fa-flag-checkered` with the new icon name.

**Examples:**
```html
<!-- Medal icon -->
<i class="fas fa-medal text-white text-2xl"></i>

<!-- Chart icon -->
<i class="fas fa-chart-line text-white text-2xl"></i>

<!-- Users icon -->
<i class="fas fa-users text-white text-2xl"></i>
```

### 3. Adding More Feature Cards

**Current structure (5 features):**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-5 gap-6">
    <!-- 5 feature cards here -->
</div>
```

**To add a 6th feature:**

1. Change the grid to accommodate 6 items:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
```

2. Copy an existing feature card and paste it before the closing `</div>`:
```html
<div class="feature-card bg-white rounded-xl shadow-md p-8 hover:shadow-xl transition-all duration-300">
    <div class="w-14 h-14 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center mb-4">
        <i class="fas fa-star text-white text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">New Feature</h3>
    <p class="text-gray-600 leading-relaxed">
        Description of your new feature goes here.
    </p>
</div>
```

### 4. Changing Button Colors

**Current primary button (line 87):**
```html
<a href="..." class="btn-primary bg-white text-purple-600 px-8 py-4 rounded-lg font-bold text-lg">
    Launch Your Hub
</a>
```

**To change button color:**

Change `bg-white` and `text-purple-600`:

```html
<!-- Blue button with white text -->
<a href="..." class="btn-primary bg-blue-600 text-white px-8 py-4 rounded-lg font-bold text-lg">
    Launch Your Hub
</a>

<!-- Green button with white text -->
<a href="..." class="btn-primary bg-green-600 text-white px-8 py-4 rounded-lg font-bold text-lg">
    Launch Your Hub
</a>
```

### 5. Adjusting Section Padding

**Current (line 104):**
```html
<section id="features" class="py-24 md:py-32 bg-gray-50">
```

**To reduce spacing:**
```html
<section id="features" class="py-16 md:py-24 bg-gray-50">
```

**To increase spacing:**
```html
<section id="features" class="py-32 md:py-40 bg-gray-50">
```

### 6. Adding a New Testimonial

**Find the testimonials section (line 342)** and copy an existing testimonial card:

```html
<div class="testimonial-card bg-white rounded-xl shadow-md p-8 border border-gray-200 hover:shadow-xl transition-all duration-300">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    <p class="text-gray-700 mb-6 leading-relaxed text-base">
        "Your testimonial quote goes here..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-semibold text-gray-900">Person Name</p>
        <p class="text-gray-600 text-sm">Their Title, School Name</p>
    </div>
</div>
```

Paste before the closing `</div>` of the testimonials grid and update the quote and person details.

### 7. Changing the CTA Section Background Image

**Current code (line 453):**
```html
<section class="py-24 md:py-32 bg-cover bg-center relative" style="background-image: url('https://images.unsplash.com/photo-1461896836934-ffe607ba8211?w=1200&h=600&fit=crop');">
```

**To use a different image:**

Replace the URL with another image:

```html
<section class="py-24 md:py-32 bg-cover bg-center relative" style="background-image: url('https://images.unsplash.com/photo-1461896836934-ffe607ba8211?w=1200&h=600&fit=crop');">
```

You can find free images at:
- [Unsplash](https://unsplash.com)
- [Pexels](https://pexels.com)
- [Pixabay](https://pixabay.com)

### 8. Changing Mobile Menu Behavior

The mobile menu currently shows/hides when you click the hamburger icon. The JavaScript is at the bottom of the file (lines 668-694).

To modify behavior, you can edit the JavaScript function, but this is advanced. For beginners, the current functionality is fine.

---

## Troubleshooting

### Issue: Page looks broken or styles aren't applied

**Solution:**

1. **Clear browser cache:**
   - Chrome: Ctrl+Shift+Delete (or Cmd+Shift+Delete on Mac)
   - Firefox: Ctrl+Shift+Delete
   - Safari: Develop > Empty Caches

2. **Hard refresh the page:**
   - Ctrl+F5 (or Cmd+Shift+R on Mac)

3. **Check for typos:**
   - Make sure class names are spelled correctly
   - Tailwind is case-sensitive

### Issue: Links aren't working

**Solution:**

1. **Check the href attribute:**
   ```html
   <!-- Correct -->
   <a href="https://example.com">Link</a>
   
   <!-- Wrong - missing https:// -->
   <a href="example.com">Link</a>
   ```

2. **For internal links, verify the ID matches:**
   ```html
   <!-- Navigation -->
   <a href="#features">Features</a>
   
   <!-- Must have matching ID -->
   <section id="features">
   ```

3. **Check file names are correct:**
   - File names are case-sensitive on some servers
   - `Privacy.html` ≠ `privacy.html`

### Issue: Mobile menu doesn't work

**Solution:**

1. **Check that JavaScript isn't disabled** in your browser
2. **Verify the mobile menu button exists** in your HTML
3. **Check browser console for errors:**
   - Press F12 to open Developer Tools
   - Look for red error messages

### Issue: Colors look different than expected

**Solution:**

1. **Check that you updated the correct class:**
   - `bg-` = background color
   - `text-` = text color
   - `border-` = border color

2. **Verify color names are correct:**
   - Valid: `purple-600`, `pink-600`, `gray-50`
   - Invalid: `purple`, `dark-blue`

3. **Check that you're using the right shade:**
   - `purple-50` (lightest) to `purple-900` (darkest)

### Issue: Text content doesn't update

**Solution:**

1. **Make sure you're editing the right file:**
   - Save changes to `index.html`
   - Not a backup or other file

2. **Save the file after editing:**
   - Ctrl+S (or Cmd+S on Mac)

3. **Refresh the browser:**
   - F5 or Ctrl+R

### Issue: Responsive design breaks on mobile

**Solution:**

1. **Don't remove responsive prefixes:**
   ```html
   <!-- Correct -->
   <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
   
   <!-- Wrong - missing mobile classes -->
   <div class="grid md:grid-cols-2 lg:grid-cols-3">
   ```

2. **Test on actual mobile devices or use browser DevTools:**
   - Press F12 and click the mobile device icon
   - Test different screen sizes

### Issue: Custom CSS doesn't work

**Solution:**

1. **Make sure you added CSS to the `<style>` section:**
   ```html
   <style>
       /* Your custom CSS here */
       .my-custom-class {
           color: red;
       }
   </style>
   ```

2. **Don't use external CSS files without linking them:**
   ```html
   <!-- This won't work without a link tag -->
   <style src="styles.css"></style>
   
   <!-- Correct way -->
   <link rel="stylesheet" href="styles.css">
   ```

### Issue: FAQ accordion doesn't expand

**Solution:**

1. **Check that JavaScript is enabled**
2. **Verify the FAQ structure is intact:**
   - Each FAQ item needs a `.faq-item` class
   - Each needs a `.faq-question` button
   - Each needs a `.faq-answer` div

3. **Check browser console for JavaScript errors:**
   - Press F12
   - Look for error messages in red

---

## Best Practices

### 1. Always Make Backups

Before making major changes:
1. Duplicate your `index.html` file
2. Rename it to `index-backup.html`
3. Make changes to the original

### 2. Test Changes Locally

1. Edit the HTML file
2. Save it
3. Open it in your browser
4. Test all functionality before uploading

### 3. Use Consistent Naming

When creating new files:
- Use lowercase: `privacy.html` (not `Privacy.html`)
- Use hyphens for spaces: `my-page.html` (not `my page.html`)
- Keep names descriptive: `blog-post-1.html`

### 4. Validate Your HTML

Use [HTML Validator](https://validator.w3.org/) to check for errors:
1. Go to the validator
2. Upload your HTML file
3. Fix any errors reported

### 5. Test on Multiple Browsers

Test your site on:
- Chrome
- Firefox
- Safari
- Edge
- Mobile browsers

### 6. Keep External URLs Updated

If you change your main website URL:
1. Use Find & Replace (Ctrl+H)
2. Find the old URL
3. Replace with the new URL
4. Test all links

---

## Getting Help

### Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **Font Awesome Icons:** https://fontawesome.com/icons
- **HTML Reference:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS

### Common Questions

**Q: Can I use this on my own domain?**
A: Yes! Upload the HTML files to your web server and they'll work on any domain.

**Q: Do I need to pay for anything?**
A: No. Tailwind CSS and Font Awesome are free via CDN. You only need to pay for web hosting.

**Q: Can I add more sections?**
A: Yes! Copy an existing section and modify it. Keep the same structure and classes.

**Q: How do I make it my own brand?**
A: Update colors in the `<style>` section, change text content, update links, and customize images.

---

## Summary

This README provides comprehensive guidance for:

✅ **Updating text content** in every section  
✅ **Modifying Tailwind CSS classes** for styling  
✅ **Fixing and managing all links** on the page  
✅ **Adding privacy and terms pages** with proper linking  
✅ **Common customizations** for quick changes  
✅ **Troubleshooting tips** for common issues  

**Remember:** Start with small changes, test thoroughly, and keep backups of your files. Happy customizing!