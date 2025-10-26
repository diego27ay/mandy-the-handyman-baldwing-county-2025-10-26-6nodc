# Mandy the Handyman Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, customizing, and updating the Mandy the Handyman landing page. This guide is designed for beginners with no prior coding experience.

---

## Table of Contents

1. [Overview](#overview)
2. [Understanding the Structure](#understanding-the-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Troubleshooting Common Issues](#troubleshooting-common-issues)
8. [Best Practices](#best-practices)

---

## Overview

This landing page is built with:
- **HTML5** - The structure and content
- **Tailwind CSS** - A utility-first CSS framework for styling
- **Font Awesome Icons** - Professional icons throughout the page
- **Vanilla JavaScript** - Interactive features like mobile menu and FAQ accordion

**File Structure You'll Need:**
```
project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy - you'll create this)
├── terms.html (terms of service - you'll create this)
└── blog.html (optional blog section)
```

---

## Understanding the Structure

### What Each Section Does

The landing page is organized into clear, distinct sections. Understanding these will help you know where to make changes:

| Section | Location in Code | Purpose |
|---------|-----------------|---------|
| **Header Navigation** | Lines 51-83 | Main menu and mobile menu |
| **Hero Section** | Lines 85-118 | Eye-catching introduction with call-to-action buttons |
| **Features Section** | Lines 120-181 | Three main service offerings |
| **Benefits Section** | Lines 183-264 | Six reasons to choose the business |
| **Testimonials Section** | Lines 266-328 | Customer reviews with ratings |
| **About Us Section** | Lines 330-370 | Company story and statistics |
| **FAQ Section** | Lines 372-480 | Frequently asked questions |
| **CTA Section** | Lines 482-497 | Final call-to-action before footer |
| **Footer** | Lines 499-575 | Contact info, links, and copyright |

### Key Concepts

**Responsive Design**: This page automatically adjusts for different screen sizes using Tailwind's responsive prefixes:
- `sm:` - Small screens (640px and up)
- `md:` - Medium screens (768px and up)
- `lg:` - Large screens (1024px and up)

**Semantic HTML**: The page uses meaningful HTML tags (`<header>`, `<section>`, `<footer>`) that help both browsers and search engines understand the content.

---

## Updating Text Content

### How to Edit Text (Beginner Guide)

**Step 1: Open the File**
1. Right-click on `index.html`
2. Select "Open with" → Choose a text editor (Notepad, Visual Studio Code, Sublime Text, etc.)
3. The entire HTML code will display

**Step 2: Find the Text You Want to Change**
- Use **Ctrl+F** (Windows) or **Cmd+F** (Mac) to open the Find dialog
- Type the text you want to find
- Press Enter to locate it

**Step 3: Edit the Text**
- Click where you want to make changes
- Delete the old text
- Type the new text
- **Do NOT delete HTML tags** (the `<` and `>` symbols)

**Step 4: Save**
- Press **Ctrl+S** (Windows) or **Cmd+S** (Mac)
- Refresh your browser to see changes

---

### Specific Sections to Update

#### 1. **Header/Navigation - Company Name**

**Location**: Line 54-58

**Current Code:**
```html
<span class="text-2xl font-bold text-gray-900 hidden sm:inline">Mandy the Handyman</span>
<span class="text-xl font-bold text-gray-900 sm:hidden">Mandy</span>
```

**What to Change**: Replace "Mandy the Handyman" with your business name

**Example - Change to "ABC Home Services":**
```html
<span class="text-2xl font-bold text-gray-900 hidden sm:inline">ABC Home Services</span>
<span class="text-xl font-bold text-gray-900 sm:hidden">ABC</span>
```

**Why Two Lines?**
- First line shows on larger screens (full name)
- Second line shows on small phone screens (shorter name)
- This prevents the menu from looking crowded on mobile devices

---

#### 2. **Hero Section - Main Headline**

**Location**: Lines 93-96

**Current Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight">
    Mandy the Handyman
</h1>
```

**What to Change**: Replace with your main headline

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight">
    ABC Home Services
</h1>
```

**Note**: The size changes based on screen size (text-4xl on small screens, text-6xl on large screens)

---

#### 3. **Hero Section - Subtitle**

**Location**: Lines 97-99

**Current Code:**
```html
<h2 class="text-2xl md:text-3xl font-semibold text-blue-100">
    🔧 Reliable Handyman Services in Fairhope, Daphne
</h2>
```

**What to Change**: Update the location and service description

**Example:**
```html
<h2 class="text-2xl md:text-3xl font-semibold text-blue-100">
    🔧 Professional Services in Your Area
</h2>
```

**Tip**: The emoji (🔧) is optional. You can replace it with any emoji or remove it entirely.

---

#### 4. **Hero Section - Description**

**Location**: Lines 100-103

**Current Code:**
```html
<p class="text-lg md:text-xl text-blue-100 leading-relaxed max-w-2xl">
    Professional home maintenance and repair services you can trust. From general maintenance to electrical repairs and installations, we're here to keep your home in perfect condition.
</p>
```

**What to Change**: Replace with your service description

**Example:**
```html
<p class="text-lg md:text-xl text-blue-100 leading-relaxed max-w-2xl">
    We provide comprehensive home services including plumbing, electrical work, and general repairs. Our experienced team is ready to help with any project, big or small.
</p>
```

---

#### 5. **Features Section - Service Cards**

**Location**: Lines 150-181

The page has three feature cards. Here's how to update each one:

**Feature 1: General Home Maintenance**

**Location**: Lines 150-165

**Current Code:**
```html
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">
    <div class="bg-gradient-to-r from-blue-100 to-purple-100 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-home text-blue-600 text-3xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3">General Home Maintenance</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Keep your home in pristine condition with our comprehensive maintenance services. From drywall repair and painting to door adjustments and weatherproofing, we handle all the details that keep your home functioning perfectly and looking beautiful.
    </p>
    <ul class="space-y-2 text-gray-700">
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i>Drywall repair and patching</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i>Interior and exterior painting</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i>Door and window repairs</li>
    </ul>
</div>
```

**What You Can Change**:
1. **Title** (Line 155): "General Home Maintenance"
2. **Description** (Lines 156-158): The paragraph text
3. **Bullet Points** (Lines 159-162): The three service items

**Example - Change to Plumbing Services:**
```html
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">
    <div class="bg-gradient-to-r from-blue-100 to-purple-100 w-16 h-16 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-water text-blue-600 text-3xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-3">Plumbing Services</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Professional plumbing solutions for all your needs. From leak repairs to fixture installation, we ensure your plumbing systems work perfectly and efficiently.
    </p>
    <ul class="space-y-2 text-gray-700">
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i>Leak detection and repair</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i>Fixture installation</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-3"></i>Drain cleaning</li>
    </ul>
</div>
```

**Icon Change Note**: The icon is `fas fa-water`. Visit [fontawesome.com](https://fontawesome.com) to find other icons. Replace `fa-water` with any icon name you find.

---

#### 6. **Benefits Section - Six Benefits**

**Location**: Lines 219-264

Each benefit follows this pattern:

**Current Example (Benefit 1):**
```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-12 w-12 rounded-lg bg-blue-600">
            <i class="fas fa-check-circle text-white text-xl"></i>
        </div>
    </div>
    <div>
        <h3 class="text-xl font-bold text-gray-900 mb-2">Trusted Local Expert</h3>
        <p class="text-gray-600 leading-relaxed">
            Serving Fairhope and Daphne with professional handyman services for years. We're your neighbors, and we take pride in delivering quality work that builds lasting relationships with our community.
        </p>
    </div>
</div>
```

**What to Change**:
1. **Title**: "Trusted Local Expert"
2. **Description**: The paragraph text
3. **Icon** (optional): Change `fa-check-circle` to another icon

**Example - Change to Custom Benefit:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-2">Same-Day Service Available</h3>
<p class="text-gray-600 leading-relaxed">
    We understand emergencies happen. That's why we offer same-day emergency service for urgent repairs. Call us today for immediate assistance.
</p>
```

---

#### 7. **Testimonials Section - Customer Reviews**

**Location**: Lines 293-328

**Current Example (Testimonial 1):**
```html
<div class="testimonial-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">
    <div class="flex items-center mb-4">
        <i class="fas fa-star star-color"></i>
        <i class="fas fa-star star-color"></i>
        <i class="fas fa-star star-color"></i>
        <i class="fas fa-star star-color"></i>
        <i class="fas fa-star star-color"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "Mandy came to our house to install ceiling fans in our bedroom and living room. He was professional, punctual, and did an excellent job. The fans look great and work perfectly. We highly recommend his services!"
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Mitchell</p>
        <p class="text-gray-600 text-sm">Homeowner, Fairhope</p>
    </div>
</div>
```

**What to Change**:
1. **Review Text** (Line 302): The customer's quote (keep the quotation marks)
2. **Customer Name** (Line 305): "Sarah Mitchell"
3. **Customer Title** (Line 306): "Homeowner, Fairhope"
4. **Stars** (Lines 297-301): Keep all five stars or remove some for lower ratings

**Example - Add New Testimonial:**
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Outstanding service! The team fixed our plumbing issue quickly and professionally. Highly recommended!"
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-bold text-gray-900">John Anderson</p>
    <p class="text-gray-600 text-sm">Business Owner, Downtown</p>
</div>
```

---

#### 8. **About Us Section**

**Location**: Lines 346-360

**Current Code:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-8 tracking-tight">
    About Mandy the Handyman
</h2>

<div class="space-y-6">
    <p class="text-lg text-gray-700 leading-relaxed">
        Mandy the Handyman was founded on a simple principle: every homeowner deserves access to honest, reliable, and professional handyman services...
    </p>
    
    <p class="text-lg text-gray-700 leading-relaxed">
        Our mission is to be the most trusted handyman service in Baldwin County...
    </p>
</div>
```

**What to Change**:
1. **Title**: "About Mandy the Handyman"
2. **First Paragraph**: Company history and background
3. **Second Paragraph**: Mission statement

**Example:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-8 tracking-tight">
    About ABC Home Services
</h2>

<div class="space-y-6">
    <p class="text-lg text-gray-700 leading-relaxed">
        ABC Home Services was established in 2010 with a commitment to providing exceptional service to homeowners throughout the region. Our founder started with a simple vision: make quality home repairs accessible and affordable for everyone.
    </p>
    
    <p class="text-lg text-gray-700 leading-relaxed">
        Today, we're proud to serve thousands of satisfied customers. Our mission is to be your trusted partner for all your home service needs, delivering reliability, quality, and professional expertise on every project.
    </p>
</div>
```

---

#### 9. **About Stats Section**

**Location**: Lines 362-379

These are the numbers displayed on the right side of the About section:

**Current Code:**
```html
<div class="bg-white rounded-lg p-6 shadow-md">
    <div class="text-4xl font-bold text-blue-600 mb-2">500+</div>
    <p class="text-gray-700 font-semibold">Happy Customers Served</p>
</div>
```

**What to Change**: The number and label

**Example:**
```html
<div class="bg-white rounded-lg p-6 shadow-md">
    <div class="text-4xl font-bold text-blue-600 mb-2">2000+</div>
    <p class="text-gray-700 font-semibold">Projects Completed</p>
</div>
```

---

#### 10. **FAQ Section**

**Location**: Lines 415-480

Each FAQ item has a question and answer:

**Current Example:**
```html
<div class="faq-item bg-white rounded-lg shadow-md border border-gray-100 overflow-hidden">
    <button class="faq-question w-full px-6 py-5 text-left flex items-center justify-between hover:bg-gray-50 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-bold text-gray-900">What areas do you serve?</span>
        <i class="faq-icon fas fa-chevron-down text-blue-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 py-4 bg-gray-50 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            We proudly serve Fairhope, Daphne, and the surrounding areas of Baldwin County...
        </p>
    </div>
</div>
```

**What to Change**:
1. **Question** (Line 419): "What areas do you serve?"
2. **Answer** (Line 424): The response text

**Example - Add New FAQ:**
```html
<div class="faq-item bg-white rounded-lg shadow-md border border-gray-100 overflow-hidden">
    <button class="faq-question w-full px-6 py-5 text-left flex items-center justify-between hover:bg-gray-50 transition-colors duration-300 cursor-pointer">
        <span class="text-lg font-bold text-gray-900">Do you offer emergency services?</span>
        <i class="faq-icon fas fa-chevron-down text-blue-600 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 py-4 bg-gray-50 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            Yes! We offer 24/7 emergency service for urgent repairs. Contact us immediately for assistance with any emergency situation.
        </p>
    </div>
</div>
```

---

#### 11. **Footer Section - Contact Information**

**Location**: Lines 550-560

**Current Code:**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:mandymanservices@outlook.com" class="text-gray-400 hover:text-white transition-colors duration-300">mandymanservices@outlook.com</a>
</li>
<li class="flex items-start">
    <i class="fas fa-map-marker-alt text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span class="text-gray-400">Fairhope & Daphne, AL</span>
</li>
<li class="flex items-start">
    <i class="fas fa-globe text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="https://mandythehandyman.com/" class="text-gray-400 hover:text-white transition-colors duration-300">mandythehandyman.com</a>
</li>
```

**What to Change**:
1. **Email**: Replace `mandymanservices@outlook.com`
2. **Location**: Replace "Fairhope & Daphne, AL"
3. **Website**: Replace `https://mandythehandyman.com/`

**Example:**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:info@abcservices.com" class="text-gray-400 hover:text-white transition-colors duration-300">info@abcservices.com</a>
</li>
<li class="flex items-start">
    <i class="fas fa-map-marker-alt text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span class="text-gray-400">Your City, Your State</span>
</li>
<li class="flex items-start">
    <i class="fas fa-globe text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="https://www.yourbusiness.com/" class="text-gray-400 hover:text-white transition-colors duration-300">www.yourbusiness.com</a>
</li>
```

---

#### 12. **Footer - Company Description**

**Location**: Lines 527-531

**Current Code:**
```html
<p class="text-sm text-gray-400 leading-relaxed">
    Professional handyman services in Fairhope and Daphne. Your trusted local expert for home maintenance and repairs.
</p>
```

**What to Change**: Update to reflect your business

**Example:**
```html
<p class="text-sm text-gray-400 leading-relaxed">
    ABC Home Services provides comprehensive home repair and maintenance solutions. Your trusted partner for quality service and professional expertise.
</p>
```

---

### Quick Reference: Text Update Checklist

- [ ] Header logo/company name (2 places)
- [ ] Hero section headline
- [ ] Hero section subtitle
- [ ] Hero section description
- [ ] Feature 1 title and description
- [ ] Feature 2 title and description
- [ ] Feature 3 title and description
- [ ] All bullet points in features
- [ ] All six benefits (titles and descriptions)
- [ ] All four testimonials (quotes, names, titles)
- [ ] About section (title and two paragraphs)
- [ ] About section stats (4 numbers)
- [ ] All FAQ questions and answers
- [ ] Footer contact information
- [ ] Footer company description

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind Basics

Tailwind CSS uses **utility classes** - small, single-purpose classes that you combine to create designs. Instead of writing custom CSS, you add class names to HTML elements.

**Example - Making Text Larger:**
```html
<!-- Small text (default) -->
<h1 class="text-lg">Hello</h1>

<!-- Medium text -->
<h1 class="text-2xl">Hello</h1>

<!-- Large text -->
<h1 class="text-4xl">Hello</h1>
```

### Common Tailwind Classes Used in This Page

#### **Text Size Classes**
```
text-sm      = Small (14px)
text-base    = Normal (16px)
text-lg      = Large (18px)
text-xl      = Extra Large (20px)
text-2xl     = 24px
text-3xl     = 30px
text-4xl     = 36px
text-5xl     = 48px
text-6xl     = 60px
```

**How to Use**: Replace any `text-*` class with another size.

**Example - Make Hero Title Smaller:**
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight">
    Mandy the Handyman
</h1>

<!-- Modified (smaller on all screens) -->
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold leading-tight tracking-tight">
    Mandy the Handyman
</h1>
```

---

#### **Text Weight Classes (Boldness)**
```
font-light      = Thin
font-normal     = Regular
font-semibold   = Semi-bold
font-bold       = Bold
font-extrabold  = Extra bold
```

**Example - Make Navigation Links Bolder:**
```html
<!-- Original -->
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Services</a>

<!-- Modified (bolder) -->
<a href="#features" class="text-gray-700 hover:text-blue-600 font-bold transition-colors duration-300">Services</a>
```

---

#### **Color Classes**

Colors follow the pattern: `[property]-[color]-[intensity]`

**Text Colors:**
```
text-white
text-gray-900      = Dark gray/almost black
text-gray-600      = Medium gray
text-gray-400      = Light gray
text-blue-600      = Blue
text-green-500     = Green
```

**Background Colors:**
```
bg-white
bg-gray-50         = Very light gray
bg-gray-900        = Very dark gray
bg-blue-600        = Blue
bg-green-500       = Green
```

**Example - Change Feature Card Background:**
```html
<!-- Original (white background) -->
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">

<!-- Modified (light gray background) -->
<div class="feature-card bg-gray-50 rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">
```

---

#### **Spacing Classes (Padding & Margin)**

Padding adds space inside an element. Margin adds space outside.

```
p-4   = Padding of 16px on all sides
p-6   = Padding of 24px on all sides
p-8   = Padding of 32px on all sides

m-4   = Margin of 16px on all sides
m-6   = Margin of 24px on all sides
m-8   = Margin of 32px on all sides

px-4  = Horizontal padding (left & right)
py-4  = Vertical padding (top & bottom)

mx-auto = Center horizontally
```

**Example - Add More Padding to Feature Cards:**
```html
<!-- Original (32px padding) -->
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">

<!-- Modified (48px padding) -->
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-12 border border-gray-100">
```

---

#### **Responsive Classes (Mobile, Tablet, Desktop)**

The `md:` and `lg:` prefixes make styles apply only on certain screen sizes:

```
text-4xl          = On all screens
md:text-5xl       = On medium screens and up (768px+)
lg:text-6xl       = On large screens and up (1024px+)
```

**Example - Understand Responsive Text:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Mandy the Handyman
</h1>
```

This means:
- On phones: 36px text (text-4xl)
- On tablets: 48px text (text-5xl)
- On desktops: 60px text (text-6xl)

**Example - Make Text Larger on Mobile:**
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">

<!-- Modified (larger on mobile) -->
<h1 class="text-5xl md:text-5xl lg:text-6xl font-bold">
```

---

#### **Shadow Classes**

Shadows add depth:
```
shadow-sm    = Small shadow
shadow-md    = Medium shadow (used throughout this page)
shadow-lg    = Large shadow
shadow-xl    = Extra large shadow
```

**Example - Make Cards Have Larger Shadows:**
```html
<!-- Original -->
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">

<!-- Modified (larger shadow on hover) -->
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-2xl p-8 border border-gray-100">
```

---

#### **Border Radius (Rounded Corners)**

```
rounded      = Slightly rounded
rounded-lg   = More rounded
rounded-xl   = Very rounded
rounded-full = Completely circular
```

**Example - Make Feature Cards More Rounded:**
```html
<!-- Original -->
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">

<!-- Modified (more rounded) -->
<div class="feature-card bg-white rounded-2xl shadow-md hover:shadow-xl p-8 border border-gray-100">
```

---

#### **Display & Layout Classes**

```
hidden       = Hide element (display: none)
block        = Full width block
inline       = Inline element
flex         = Flexbox layout
grid         = Grid layout
```

**Example - Hide Element on Mobile:**
```html
<!-- Original (shows on all screens) -->
<div class="flex justify-center items-center">

<!-- Modified (hides on small screens) -->
<div class="hidden lg:flex justify-center items-center">
```

---

### Common Customization Scenarios

#### **Scenario 1: Change Primary Color from Blue to Green**

The page uses blue (`text-blue-600`, `bg-blue-600`) throughout. To change to green:

**Find and Replace:**
1. Press **Ctrl+H** (Windows) or **Cmd+H** (Mac) to open Find & Replace
2. Find: `blue-600`
3. Replace with: `green-600`
4. Click "Replace All"

**Example - Before and After:**
```html
<!-- Before -->
<div class="bg-gradient-to-r from-blue-600 to-purple-600 p-2 rounded-lg">

<!-- After -->
<div class="bg-gradient-to-r from-green-600 to-purple-600 p-2 rounded-lg">
```

---

#### **Scenario 2: Make Feature Cards Smaller**

**Original:**
```html
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-8 border border-gray-100">
```

**Modified (smaller padding and text):**
```html
<div class="feature-card bg-white rounded-xl shadow-md hover:shadow-xl p-6 border border-gray-100">
    <div class="bg-gradient-to-r from-blue-100 to-purple-100 w-14 h-14 rounded-lg flex items-center justify-center mb-4">
        <i class="fas fa-home text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">General Home Maintenance</h3>
```

**Changes Made:**
- `p-8` → `p-6` (less padding inside)
- `w-16 h-16` → `w-14 h-14` (smaller icon box)
- `text-3xl` → `text-2xl` (smaller icon)
- `mb-6` → `mb-4` (less space below icon)
- `text-2xl` → `text-xl` (smaller heading)

---

#### **Scenario 3: Make Buttons Larger**

**Original Button:**
```html
<a href="https://mandythehandyman.com/" class="cta-button bg-white text-blue-600 px-8 py-3 rounded-lg font-bold text-lg hover:shadow-lg transition-all duration-300 text-center">
    Get Started Today
</a>
```

**Modified (larger):**
```html
<a href="https://mandythehandyman.com/" class="cta-button bg-white text-blue-600 px-12 py-4 rounded-lg font-bold text-xl hover:shadow-lg transition-all duration-300 text-center">
    Get Started Today
</a>
```

**Changes Made:**
- `px-8` → `px-12` (more horizontal padding)
- `py-3` → `py-4` (more vertical padding)
- `text-lg` → `text-xl` (larger text)

---

#### **Scenario 4: Change Hero Section Background Color**

**Original:**
```html
<section class="hero-gradient text-white py-20 md:py-32 lg:py-40">
```

The `hero-gradient` class is defined in the `<style>` section (lines 23-25):
```css
.hero-gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

**To Change Color:**
1. Find the `.hero-gradient` CSS (around line 24)
2. Replace the hex colors with new ones

**Example - Change to Red Gradient:**
```css
.hero-gradient {
    background: linear-gradient(135deg, #ff6b6b 0%, #ee5a6f 100%);
}
```

**Color References:**
- Blue: `#667eea`
- Purple: `#764ba2`
- Red: `#ff6b6b`
- Green: `#10b981`
- Orange: `#f97316`

Find more colors at [tailwindcss.com/docs/customizing-colors](https://tailwindcss.com/docs/customizing-colors)

---

#### **Scenario 5: Adjust Section Spacing**

**Original:**
```html
<section class="py-16 md:py-24 bg-gray-50">
```

**Modified (more space):**
```html
<section class="py-20 md:py-32 bg-gray-50">
```

**Modified (less space):**
```html
<section class="py-12 md:py-20 bg-gray-50">
```

**Spacing Values:**
- `py-8` = 32px vertical padding
- `py-12` = 48px vertical padding
- `py-16` = 64px vertical padding
- `py-20` = 80px vertical padding
- `py-24` = 96px vertical padding

---

### Tailwind Class Reference Table

| Purpose | Classes | Examples |
|---------|---------|----------|
| Text Size | `text-*` | `text-sm`, `text-lg`, `text-2xl`, `text-4xl` |
| Text Weight | `font-*` | `font-light`, `font-bold`, `font-extrabold` |
| Text Color | `text-*` | `text-white`, `text-gray-900`, `text-blue-600` |
| Background | `bg-*` | `bg-white`, `bg-gray-50`, `bg-blue-600` |
| Padding | `p-*`, `px-*`, `py-*` | `p-4`, `px-6`, `py-8` |
| Margin | `m-*`, `mx-*`, `my-*` | `m-4`, `mx-auto`, `my-6` |
| Border Radius | `rounded-*` | `rounded-lg`, `rounded-xl`, `rounded-full` |
| Shadow | `shadow-*` | `shadow-md`, `shadow-lg`, `shadow-xl` |
| Display | `hidden`, `block`, `flex`, `grid` | Combined with `md:`, `lg:` |
| Responsive | `md:`, `lg:`, `sm:` | `md:text-5xl`, `lg:flex` |

---

## Fixing and Managing Links

### Understanding Links on This Page

Links are HTML elements that direct users to different pages or external websites. They use the `<a>` tag with an `href` attribute.

**Basic Link Structure:**
```html
<a href="destination">Link Text</a>
```

- `href` = Where the link goes
- `Link Text` = What users see and click

---

### Current Links in the Page

#### **Navigation Menu Links (Header)**

**Location**: Lines 60-64 (Desktop Menu) and Lines 71-77 (Mobile Menu)

**Current Code:**
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Services</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">FAQ</a>
<a href="#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
```

**What These Do:**
- `#features` - Jumps to Features section on the same page
- `#benefits` - Jumps to Benefits section
- `#testimonials` - Jumps to Testimonials section
- `#faq` - Jumps to FAQ section
- `#about` - Jumps to About section

**These Links Are Working Correctly** ✓ - No changes needed unless you rename sections.

---

#### **Hero Section CTA Buttons**

**Location**: Lines 104-113

**Current Code:**
```html
<a href="https://mandythehandyman.com/" class="cta-button bg-white text-blue-600 px-8 py-3 rounded-lg font-bold text-lg hover:shadow-lg transition-all duration-300 text-center">
    Get Started Today
</a>
<a href="#features" class="cta-button border-2 border-white text-white px-8 py-3 rounded-lg font-bold text-lg hover:bg-white hover:text-blue-600 transition-all duration-300 text-center">
    Learn More
</a>
```

**What These Do:**
- First button: Goes to external website `https://mandythehandyman.com/`
- Second button: Jumps to Features section

**NEEDS UPDATING** ⚠️ - Change the external URL to your business website.

**How to Fix:**
1. Find the line: `href="https://mandythehandyman.com/"`
2. Replace with your website URL
3. Example: `href="https://www.yourbusiness.com/"`

---

#### **Mobile Menu Contact Button**

**Location**: Line 78

**Current Code:**
```html
<a href="https://mandythehandyman.com/" class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition-colors duration-300 text-center">Contact Us</a>
```

**NEEDS UPDATING** ⚠️ - Change to your website URL.

**How to Fix:**
```html
<a href="https://www.yourbusiness.com/" class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition-colors duration-300 text-center">Contact Us</a>
```

---

#### **Footer Links - Quick Links Column**

**Location**: Lines 535-540

**Current Code:**
```html
<li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Services</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a></li>
```

**These Links Are Working Correctly** ✓ - They jump to sections on the same page.

---

#### **Footer Links - Resources Column**

**Location**: Lines 545-549

**Current Code:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
<li><a href="#about" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a></li>
```

**NEEDS UPDATING** ⚠️ - These files don't exist yet:
- `privacy.html` - Needs to be created
- `terms.html` - Needs to be created
- `blog.html` - Optional, can be removed if not needed

---

#### **Footer Contact Links**

**Location**: Lines 555-568

**Current Code:**
```html
<li class="flex items-start">
    <i class="fas fa-envelope text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="mailto:mandymanservices@outlook.com" class="text-gray-400 hover:text-white transition-colors duration-300">mandymanservices@outlook.com</a>
</li>
<li class="flex items-start">
    <i class="fas fa-map-marker-alt text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <span class="text-gray-400">Fairhope & Daphne, AL</span>
</li>
<li class="flex items-start">
    <i class="fas fa-globe text-blue-500 mr-3 mt-1 flex-shrink-0"></i>
    <a href="https://mandythehandyman.com/" class="text-gray-400 hover:text-white transition-colors duration-300">mandythehandyman.com</a>
</li>
```

**NEEDS UPDATING** ⚠️ - Change all three:
1. Email address
2. Location
3. Website URL

---

### Step-by-Step: Fix All Broken Links

#### **Step 1: Update External Website Links**

**Find these two lines:**

Line 107:
```html
<a href="https://mandythehandyman.com/" class="cta-button bg-white text-blue-600 px-8 py-3 rounded-lg font-bold text-lg hover:shadow-lg transition-all duration-300 text-center">
```

Line 78:
```html
<a href="https://mandythehandyman.com/" class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition-colors duration-300 text-center">Contact Us</a>
```

Line 568:
```html
<a href="https://mandythehandyman.com/" class="text-gray-400 hover:text-white transition-colors duration-300">mandythehandyman.com</a>
```

Line 490:
```html
<a href="https://mandythehandyman.com/" class="cta-button inline-block bg-blue-600 text-white px-10 py-4 rounded-lg font-bold text-lg hover:bg-blue-700 hover:shadow-lg transition-all duration-300">
```

**Replace all four with your website URL:**

**Example: If your website is `https://www.abchomeservices.com/`**

```html
<!-- Line 107 -->
<a href="https://www.abchomeservices.com/" class="cta-button bg-white text-blue-600 px-8 py-3 rounded-lg font-bold text-lg hover:shadow-lg transition-all duration-300 text-center">

<!-- Line 78 -->
<a href="https://www.abchomeservices.com/" class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition-colors duration-300 text-center">Contact Us</a>

<!-- Line 568 -->
<a href="https://www.abchomeservices.com/" class="text-gray-400 hover:text-white transition-colors duration-300">www.abchomeservices.com</a>

<!-- Line 490 -->
<a href="https://www.abchomeservices.com/" class="cta-button inline-block bg-blue-600 text-white px-10 py-4 rounded-lg font-bold text-lg hover:bg-blue-700 hover:shadow-lg transition-all duration-300">
```

---

#### **Step 2: Update Email Address**

**Find this line (Line 559):**
```html
<a href="mailto:mandymanservices@outlook.com" class="text-gray-400 hover:text-white transition-colors duration-300">mandymanservices@outlook.com</a>
```

**Replace with your email:**

**Example: If your email is `info@abcservices.com`**

```html
<a href="mailto:info@abcservices.com" class="text-gray-400 hover:text-white transition-colors duration-300">info@abcservices.com</a>
```

**Important**: You need TWO changes:
1. In the `href="mailto:..."` part
2. In the visible text

---

#### **Step 3: Update Location**

**Find this line (Line 563):**
```html
<span class="text-gray-400">Fairhope & Daphne, AL</span>
```

**Replace with your location:**

**Example:**
```html
<span class="text-gray-400">Your City, Your State</span>
```

---

### Understanding Different Link Types

#### **Type 1: Internal Links (Same Page)**
Links that jump to sections on the current page use `#` followed by the section ID.

```html
<a href="#features">Go to Features</a>
```

The section must have a matching `id`:
```html
<section id="features">
    <!-- Content -->
</section>
```

**This page already has all the IDs set up correctly** ✓

---

#### **Type 2: External Links (Different Website)**
Links to other websites use full URLs.

```html
<a href="https://www.example.com/">Visit Example</a>
```

**Remember**: Always include `https://` at the beginning.

---

#### **Type 3: Email Links**
Links that open the user's email client.

```html
<a href="mailto:info@example.com">Send Email</a>
```

---

#### **Type 4: File Links (Same Folder)**
Links to other HTML files in the same folder.

```html
<a href="privacy.html">Privacy Policy</a>
```

This assumes `privacy.html` is in the same folder as `index.html`.

---

### Link Update Checklist

- [ ] Line 107: Hero CTA button - Update website URL
- [ ] Line 78: Mobile menu contact button - Update website URL
- [ ] Line 490: Footer CTA section - Update website URL
- [ ] Line 559: Footer email - Update email address
- [ ] Line 563: Footer location - Update location
- [ ] Line 568: Footer website link - Update website URL
- [ ] Line 565: Footer website text - Update website name
- [ ] Line 545: Privacy Policy link - Create privacy.html file
- [ ] Line 546: Terms of Service link - Create terms.html file
- [ ] Line 547: Blog link - Create blog.html or remove link

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

Privacy and Terms pages are important for:
- **Legal Protection**: Explain how you handle customer data
- **Trust**: Show customers you're a legitimate business
- **Legal Compliance**: Required in many jurisdictions
- **Professionalism**: Professional businesses always have these pages

---

### Step 1: Create the Privacy Policy Page

**Step 1A: Create a New File**

1. Open your text editor
2. Click **File** → **New File**
3. Copy the code below
4. Click **File** → **Save As**
5. Name it: `privacy.html`
6. Save it in the **same folder** as `index.html`

**Step 1B: Privacy Policy HTML Code**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Mandy the Handyman">
    <meta name="author" content="Mandy the Handyman">
    <title>Privacy Policy - Mandy the Handyman</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="bg-gradient-to-r from-blue-600 to-purple-600 p-2 rounded-lg">
                    <i class="fas fa-hammer text-white text-2xl"></i>
                </div>
                <span class="text-2xl font-bold text-gray-900 hidden sm:inline">Mandy the Handyman</span>
                <span class="text-xl font-bold text-gray-900 sm:hidden">Mandy</span>
            </div>

            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Services</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Testimonials</a>
            </div>

            <div class="md:hidden">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium">Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-white rounded-xl shadow-md p-8 md:p-12">
                <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
                
                <div class="space-y-8 text-gray-700 leading-relaxed">
                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                        <p>
                            Mandy the Handyman ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                        <p class="mb-4">We may collect information about you in a variety of ways. The information we may collect on the site includes:</p>
                        <ul class="list-disc list-inside space-y-2 ml-4">
                            <li><strong>Personal Data:</strong> Name, email address, phone number, and address when you contact us for services</li>
                            <li><strong>Device Information:</strong> Browser type, IP address, and operating system</li>
                            <li><strong>Usage Data:</strong> Pages visited, time spent on pages, and links clicked</li>
                            <li><strong>Location Data:</strong> General location information to provide local services</li>
                        </ul>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Your Information</h2>
                        <p class="mb-4">We use the information we collect in the following ways:</p>
                        <ul class="list-disc list-inside space-y-2 ml-4">
                            <li>To provide and maintain our services</li>
                            <li>To process service requests and send related information</li>
                            <li>To respond to your inquiries and comments</li>
                            <li>To improve our website and services</li>
                            <li>To send promotional communications (with your consent)</li>
                            <li>To comply with legal obligations</li>
                        </ul>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Disclosure of Your Information</h2>
                        <p>
                            We do not sell, trade, or rent your personal information to third parties. We may share your information only when necessary to provide our services or as required by law. We may disclose your information when required by law or in response to valid requests by public authorities.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Security of Your Information</h2>
                        <p>
                            We use appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet is 100% secure.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Cookies and Tracking Technologies</h2>
                        <p>
                            Our website may use cookies and similar tracking technologies to enhance your experience. You can control cookie settings through your browser preferences. Note that disabling cookies may affect website functionality.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Your Rights</h2>
                        <p class="mb-4">Depending on your location, you may have the following rights:</p>
                        <ul class="list-disc list-inside space-y-2 ml-4">
                            <li>Right to access your personal data</li>
                            <li>Right to correct inaccurate data</li>
                            <li>Right to request deletion of your data</li>
                            <li>Right to opt-out of marketing communications</li>
                        </ul>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Third-Party Links</h2>
                        <p>
                            Our website may contain links to third-party websites. We are not responsible for the privacy practices of external sites. We encourage you to review their privacy policies before providing personal information.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Contact Us</h2>
                        <p>
                            If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                        </p>
                        <div class="mt-4 p-4 bg-gray-50 rounded-lg">
                            <p><strong>Email:</strong> mandymanservices@outlook.com</p>
                            <p><strong>Address:</strong> Fairhope & Daphne, AL</p>
                        </div>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Changes to This Privacy Policy</h2>
                        <p>
                            We may update this Privacy Policy from time to time. The date of the last update will be noted at the bottom of this page. Your continued use of the website following the posting of revised Privacy Policy means that you accept and agree to the changes.
                        </p>
                    </div>

                    <div class="border-t border-gray-200 pt-8 mt-8">
                        <p class="text-sm text-gray-600">
                            <strong>Last Updated:</strong> <span id="update-date">January 2025</span>
                        </p>
                    </div>
                </div>

                <!-- Back to Home Button -->
                <div class="mt-12">
                    <a href="index.html" class="inline-block bg-blue-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-blue-700 transition-colors duration-300">
                        Back to Home
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-500 text-sm">
                &copy; <span id="year">2025</span> Mandy the Handyman. All rights reserved.
            </p>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

**Step 2A: Create a New File**

1. Open your text editor
2. Click **File** → **New File**
3. Copy the code below
4. Click **File** → **Save As**
5. Name it: `terms.html`
6. Save it in the **same folder** as `index.html`

**Step 2B: Terms of Service HTML Code**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Mandy the Handyman">
    <meta name="author" content="Mandy the Handyman">
    <title>Terms of Service - Mandy the Handyman</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="bg-gradient-to-r from-blue-600 to-purple-600 p-2 rounded-lg">
                    <i class="fas fa-hammer text-white text-2xl"></i>
                </div>
                <span class="text-2xl font-bold text-gray-900 hidden sm:inline">Mandy the Handyman</span>
                <span class="text-xl font-bold text-gray-900 sm:hidden">Mandy</span>
            </div>

            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Services</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Testimonials</a>
            </div>

            <div class="md:hidden">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium">Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="bg-white rounded-xl shadow-md p-8 md:p-12">
                <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
                
                <div class="space-y-8 text-gray-700 leading-relaxed">
                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                        <p>
                            By accessing and using this website and our services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                        <p class="mb-4">Permission is granted to temporarily download one copy of the materials (information or software) on Mandy the Handyman's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                        <ul class="list-disc list-inside space-y-2 ml-4">
                            <li>Modify or copy the materials</li>
                            <li>Use the materials for any commercial purpose or for any public display</li>
                            <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                            <li>Remove any copyright or other proprietary notations from the materials</li>
                            <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                        </ul>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                        <p>
                            The materials on Mandy the Handyman's website are provided on an 'as is' basis. Mandy the Handyman makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                        <p>
                            In no event shall Mandy the Handyman or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Mandy the Handyman's website, even if Mandy the Handyman or an authorized representative has been notified orally or in writing of the possibility of such damage.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                        <p>
                            The materials appearing on Mandy the Handyman's website could include technical, typographical, or photographic errors. Mandy the Handyman does not warrant that any of the materials on its website are accurate, complete, or current. Mandy the Handyman may make changes to the materials contained on its website at any time without notice.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                        <p>
                            Mandy the Handyman has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Mandy the Handyman of the site. Use of any such linked website is at the user's own risk.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                        <p>
                            Mandy the Handyman may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                        <p>
                            These terms and conditions are governed by and construed in accordance with the laws of the State of Alabama, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Service Terms</h2>
                        <p class="mb-4">When booking services with Mandy the Handyman:</p>
                        <ul class="list-disc list-inside space-y-2 ml-4">
                            <li>A consultation and estimate are required before work begins</li>
                            <li>Payment terms will be discussed and agreed upon before service</li>
                            <li>Cancellations must be made 24 hours in advance</li>
                            <li>We are not responsible for damage to existing structures unless caused by our negligence</li>
                            <li>All work is performed to industry standards and building codes</li>
                        </ul>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Limitation of Liability</h2>
                        <p>
                            In no case shall Mandy the Handyman, its directors, officers, or employees be liable for any indirect, incidental, special, consequential, or punitive damages resulting from your use of the website or services, even if advised of the possibility of such damages.
                        </p>
                    </div>

                    <div>
                        <h2 class="text-2xl font-bold text-gray-900 mb-4">11. Contact Information</h2>
                        <p>
                            If you have any questions about these Terms of Service, please contact us at:
                        </p>
                        <div class="mt-4 p-4 bg-gray-50 rounded-lg">
                            <p><strong>Email:</strong> mandymanservices@outlook.com</p>
                            <p><strong>Address:</strong> Fairhope & Daphne, AL</p>
                        </div>
                    </div>

                    <div class="border-t border-gray-200 pt-8 mt-8">
                        <p class="text-sm text-gray-600">
                            <strong>Last Updated:</strong> <span id="update-date">January 2025</span>
                        </p>
                    </div>
                </div>

                <!-- Back to Home Button -->
                <div class="mt-12">
                    <a href="index.html" class="inline-block bg-blue-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-blue-700 transition-colors duration-300">
                        Back to Home
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-500 text-sm">
                &copy; <span id="year">2025</span> Mandy the Handyman. All rights reserved.
            </p>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

---

### Step 3: Verify Links Are Working

**Test the Links:**

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - should open `privacy.html`
4. Click on "Terms of Service" - should open `terms.html`
5. Click "Back to Home" button - should return to `index.html`

**If Links Don't Work:**
- Make sure all three files (`index.html`, `privacy.html`, `terms.html`) are in the **same folder**
- Check that filenames match exactly (lowercase, with `.html` extension)
- Refresh the browser page

---

### Step 4: Customize the Policy Pages

**To Update Contact Information on Both Pages:**

1. **In `privacy.html`** - Find and replace:
   - Email: `mandymanservices@outlook.com`
   - Location: `Fairhope & Daphne, AL`

2. **In `terms.html`** - Find and replace:
   - Email: `mandymanservices@outlook.com`
   - Location: `Fairhope & Daphne, AL`
   - State: `Alabama` (Line 153)

---

### Step 5: Customize Policy Content

Both pages contain template content that should be customized for your business:

**Privacy Policy - Update:**
- Section 1: Company name and description
- Section 2: Types of data you collect
- Section 3: How you use the data
- Section 10: Contact information

**Terms of Service - Update:**
- Section 8: Governing Law (your state)
- Section 9: Service Terms (your specific terms)
- Section 11: Contact information

---

### Optional: Add Blog Page

**If you want a blog page:**

1. Create a new file called `blog.html`
2. The footer already links to it (Line 547)
3. Use a similar structure to the privacy/terms pages

**Note**: If you don't want a blog, remove or hide the blog link in the footer:

**Find this line (Line 547):**
```html
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
```

**Delete or comment it out:**
```html
<!-- <li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li> -->
```

---

### File Structure After Completion

Your folder should now look like:
```
project-folder/
├── index.html (main landing page)
├── privacy.html (privacy policy)
├── terms.html (terms of service)
└── blog.html (optional)
```

---

## Troubleshooting Common Issues

### Issue 1: Changes Don't Appear When I Refresh

**Problem**: You edited the HTML but the changes don't show in the browser.

**Solution**:
1. Make sure you **saved the file** (Ctrl+S or Cmd+S)
2. **Hard refresh** the browser:
   - Windows: Press **Ctrl+Shift+R**
   - Mac: Press **Cmd+Shift+R**
3. Or clear browser cache:
   - Open browser settings
   - Find "Clear browsing data"
   - Select "Cached images and files"
   - Click Clear

---

### Issue 2: Links Don't Work

**Problem**: Clicking a link does nothing or shows an error.

**Solution**:
1. **Check the file path** - Make sure the file exists in the same folder
2. **Check the filename** - Ensure it's spelled correctly and matches exactly
3. **Check the href** - Make sure there are no typos in the link
4. **For external links** - Verify the URL starts with `https://`

**Example - Correct vs Incorrect:**
```html
<!-- Correct -->
<a href="privacy.html">Privacy</a>

<!-- Incorrect (won't work) -->
<a href="Privacy.html">Privacy</a>  <!-- Wrong capitalization -->
<a href="privacy.htm">Privacy</a>   <!-- Wrong extension -->
<a href="privacy">Privacy</a>        <!-- Missing extension -->
```

---

### Issue 3: Mobile Menu Doesn't Work

**Problem**: The hamburger menu on mobile doesn't open/close.

**Solution**:
1. Check that JavaScript is enabled in your browser
2. Make sure you haven't deleted the JavaScript code at the bottom (Lines 583-616)
3. Check browser console for errors:
   - Press F12 to open Developer Tools
   - Click "Console" tab
   - Look for red error messages

---

### Issue 4: Styling Looks Wrong

**Problem**: Colors, spacing, or layout looks off.

**Solution**:
1. **Check Tailwind CDN** - Make sure the Tailwind link is present (Line 15):
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
2. **Check Font Awesome** - Make sure the icon link is present (Line 16):
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
   ```
3. **Check for typos** in class names
4. **Hard refresh** the browser (Ctrl+Shift+R)

---

### Issue 5: Text Overlaps or Looks Crowded

**Problem**: Text is overlapping or the layout looks cramped.

**Solution**:
1. Check if you accidentally deleted spacing classes (like `p-8`, `mb-4`)
2. Increase padding: Change `p-4` to `p-6` or `p-8`
3. Increase margins: Change `mb-2` to `mb-4` or `mb-6`
4. Check responsive classes - make sure `md:` and `lg:` classes are present

---

### Issue 6: Images or Icons Don't Show

**Problem**: Icons appear as broken images or don't display.

**Solution**:
1. **For Font Awesome icons** - Check that the CDN link is included (Line 16)
2. **Check icon names** - Visit [fontawesome.com](https://fontawesome.com) to verify icon names
3. **Icon format** - Make sure you're using `fas` (solid) or `fab` (brand):
   ```html
   <!-- Correct -->
   <i class="fas fa-hammer"></i>
   
   <!-- Incorrect -->
   <i class="fa-hammer"></i>  <!-- Missing 'fas' -->
   ```

---

### Issue 7: Website Looks Different on Mobile

**Problem**: The layout breaks or looks wrong on phones.

**Solution**:
1. Check that responsive classes are present (`md:`, `lg:`)
2. Make sure you didn't delete `hidden` or `flex` classes
3. Test in browser's mobile view:
   - Press F12 to open Developer Tools
   - Click the mobile phone icon
   - Select a device to test

---

### Issue 8: Colors Look Different Than Expected

**Problem**: The colors don't match what you intended.

**Solution**:
1. **Verify color names** - Check Tailwind color names at [tailwindcss.com](https://tailwindcss.com/docs/customizing-colors)
2. **Use Find & Replace** - To change all instances of a color:
   - Press Ctrl+H (or Cmd+H)
   - Find: `blue-600`
   - Replace with: `green-600`
3. **Check for custom CSS** - Look in the `<style>` section (Lines 18-48) for custom colors

---

### Issue 9: Form/Contact Button Doesn't Send Messages

**Problem**: Clicking "Contact Us" doesn't send a message.

**Solution**:
This landing page doesn't have a built-in contact form. The buttons link to your external website where the contact form should be.

**To Fix:**
1. Make sure the website URL is correct (should be your actual website)
2. Your website needs to have a contact form set up
3. Or, create a contact form page

---

### Issue 10: Footer Year Doesn't Update

**Problem**: The copyright year shows "2025" but it should be current year.

**Solution**:
The year should update automatically. If it doesn't:
1. Check that JavaScript is enabled
2. Make sure the script at the bottom (Lines 583-616) is intact
3. Hard refresh the browser

---

### Quick Troubleshooting Checklist

- [ ] Saved the file (Ctrl+S or Cmd+S)
- [ ] Hard refreshed browser (Ctrl+Shift+R or Cmd+Shift+R)
- [ ] Checked file names for typos
- [ ] Verified all three CDN links are present (Tailwind, Font Awesome)
- [ ] Checked that HTML tags aren't accidentally deleted
- [ ] Verified class names are spelled correctly
- [ ] Checked responsive prefixes (`md:`, `lg:`) are present
- [ ] Tested in different browsers
- [ ] Checked browser console for errors (F12)
- [ ] Verified all files are in the same folder

---

## Best Practices

### 1. Always Back Up Your Files

**Before making major changes:**
1. Right-click on `index.html`
2. Select "Copy"
3. Right-click in the folder
4. Select "Paste"
5. Rename to `index-backup.html`

**This way, if something breaks, you have the original to restore.**

---

### 2. Make One Change at a Time

**Don't change multiple things at once:**
- Edit one text section
- Save and test
- Then move to the next change

**This helps you identify what broke if something goes wrong.**

---

### 3. Use Consistent Formatting

**Keep spacing consistent:**
```html
<!-- Good - consistent spacing -->
<div class="space-y-4">
    <p>Item 1</p>
    <p>Item 2</p>
    <p>Item 3</p>
</div>

<!-- Confusing - inconsistent spacing -->
<div class="space-y-4">
    <p>Item 1</p>
<p>Item 2</p>
    <p>Item 3</p>
</div>
```

---

### 4. Keep Links Updated

**Maintain a list of all links:**
- External website URL
- Email address
- Phone number (if added)
- Social media profiles

**Update all of them consistently across the site.**

---

### 5. Test Regularly

**Test after each change:**
1. Save the file
2. Refresh the browser
3. Check on mobile view (F12 → mobile icon)
4. Click all links to verify they work
5. Check that text is readable

---

### 6. Use Semantic HTML

**Use meaningful tags:**
```html
<!-- Good -->
<header>Navigation</header>
<section id="features">Features</section>
<footer>Footer content</footer>

<!-- Avoid -->
<div>Navigation</div>
<div id="features">Features</div>
<div>Footer content</div>
```

---

### 7. Keep Styling Consistent

**Maintain consistent color scheme:**
- Use the same blue throughout (blue-600)
- Use the same gray for text (gray-700)
- Use the same spacing values (p-8, mb-4)

---

### 8. Document Your Changes

**Keep a simple change log:**
```
Changes Made:
- Updated business name to ABC Services (1/15/2025)
- Changed email to info@abc.com (1/15/2025)
- Added new testimonial from John Smith (1/16/2025)
- Updated feature descriptions (1/16/2025)
```

---

### 9. SEO Best Practices

**For better search engine visibility:**
1. Keep meta description relevant (Line 7)
2. Use descriptive heading text
3. Include keywords naturally in content
4. Add alt text to images (if you add any)
5. Use semantic HTML tags

---

### 10. Mobile-First Approach

**Always test on mobile:**
1. Open browser DevTools (F12)
2. Click mobile phone icon
3. Test all functionality
4. Ensure text is readable
5. Check that buttons are clickable

---

### 11. Accessibility Considerations

**Make your site accessible to everyone:**
1. Use descriptive link text (not "Click Here")
2. Include `alt` text for images
3. Use sufficient color contrast
4. Use semantic HTML tags
5. Test with keyboard navigation

**Example - Good vs Bad Link Text:**
```html
<!-- Good - descriptive -->
<a href="privacy.html">Read our Privacy Policy</a>

<!-- Bad - not descriptive -->
<a href="privacy.html">Click Here</a>
```

---

### 12. Performance Tips

**Keep your site fast:**
1. Use the CDN links (already included)
2. Don't add too many custom fonts
3. Optimize images if you add any
4. Minimize custom CSS
5. Keep JavaScript minimal

---

### 13. Security Practices

**Protect your business:**
1. Use `https://` for all external links
2. Don't include sensitive information in HTML
3. Regularly update contact information
4. Use strong passwords for file access
5. Keep backups of important files

---

### 14. Version Control (Optional)

**If you know Git, use it:**
```bash
git init
git add .
git commit -m "Initial landing page"
git commit -m "Updated business name and contact info"
```

This allows you to track all changes and revert if needed.

---

### 15. Future Enhancements

**Consider adding:**
- Contact form (with backend processing)
- Blog section
- Photo gallery
- Online booking system
- Customer testimonials section
- Service pricing table
- Team member profiles
- FAQ video section
- Live chat support

---

## Quick Reference Guide

### File Locations for Common Updates

| What to Update | File | Line(s) | How |
|---|---|---|---|
| Company name | index.html | 54, 55, 56 | Replace text |
| Main headline | index.html | 93-96 | Replace text |
| Hero description | index.html | 100-103 | Replace text |
| Feature titles | index.html | 155, 166, 177 | Replace text |
| Testimonials | index.html | 293-328 | Replace text |
| About section | index.html | 346-360 | Replace text |
| Footer email | index.html | 559 | Replace email |
| Footer location | index.html | 563 | Replace location |
| Footer website | index.html | 565, 568 | Replace URL |
| CTA buttons | index.html | 107, 490 | Replace URL |
| Primary color | index.html | Use Find & Replace | Change `blue-600` |

---

### Common Tailwind Classes

| Purpose | Classes |
|---------|---------|
| Large text | `text-4xl`, `text-5xl`, `text-6xl` |
| Bold text | `font-bold`, `font-extrabold` |
| Padding | `p-4`, `p-6`, `p-8`, `p-12` |
| Margin | `m-4`, `m-6`, `m-8`, `mx-auto` |
| Background | `bg-white`, `bg-gray-50`, `bg-blue-600` |
| Text color | `text-white`, `text-gray-700`, `text-blue-600` |
| Rounded | `rounded-lg`, `rounded-xl`, `rounded-2xl` |
| Shadow | `shadow-md`, `shadow-lg`, `shadow-xl` |
| Responsive | `md:text-5xl`, `lg:flex`, `hidden md:block` |

---

### File Checklist

Before launching:
- [ ] `index.html` - Main landing page
- [ ] `privacy.html` - Privacy policy
- [ ] `terms.html` - Terms of service
- [ ] All files in same folder
- [ ] All links tested and working
- [ ] Contact information updated
- [ ] Company name updated throughout
- [ ] Mobile view tested
- [ ] All text proofread
- [ ] Backup created

---

## Conclusion

This landing page is now ready for customization and maintenance. Remember:

1. **Start small** - Make one change at a time
2. **Test often** - Verify changes work before moving on
3. **Back up regularly** - Keep copies of working versions
4. **Keep it updated** - Regularly review and refresh content
5. **Monitor performance** - Check how visitors interact with your site

For more help with Tailwind CSS, visit [tailwindcss.com](https://tailwindcss.com)
For more Font Awesome icons, visit [fontawesome.com](https://fontawesome.com)

Good luck with your website!