# README.md - Maintenance & Customization Guide

## Welcome to Your Landing Page Documentation

This guide will help you maintain and customize your **"Wear Your Vow"** landing page. Whether you're updating text, fixing links, or adding new pages, this documentation provides step-by-step instructions tailored to your specific HTML structure.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Navigation Menu Updates](#navigation-menu-updates)
7. [Troubleshooting](#troubleshooting)
8. [Best Practices](#best-practices)

---

## Getting Started

### What You Have

Your landing page is built with:
- **HTML5** - The structure and content
- **Tailwind CSS** - The styling system (loaded via CDN)
- **Font Awesome** - Icons throughout the page
- **Vanilla JavaScript** - Interactive features like mobile menu and accordion

### Files You'll Need

```
project-folder/
├── index.html          (Your main landing page)
├── privacy.html        (Create this file)
├── terms.html          (Create this file)
├── blog.html           (Optional - mentioned in footer)
└── README.md           (This file)
```

### How to Edit Your Page

1. **Open** `index.html` in a text editor (VS Code, Notepad++, or even Notepad)
2. **Find** the section you want to change (use Ctrl+F or Cmd+F to search)
3. **Edit** the text or code
4. **Save** the file (Ctrl+S or Cmd+S)
5. **Refresh** your browser to see changes (F5 or Cmd+R)

---

## Updating Text Content

### Understanding the Structure

Your page is organized into clear sections. Each section has an **ID** that makes it easy to find:

```html
<section id="home">        <!-- Hero Section -->
<section id="features">    <!-- Features Section -->
<section id="benefits">    <!-- Benefits Section -->
<section id="about">       <!-- About Section -->
<section id="testimonials"><!-- Testimonials Section -->
<section id="faq">         <!-- FAQ Section -->
<section id="contact">     <!-- Contact Section -->
```

### Section-by-Section Updates

#### 1. **Announcement Bar** (Top of Page)

**Location:** Lines 69-73

**Current Code:**
```html
<div class="bg-gray-900 text-white py-3 px-4 text-center text-sm md:text-base">
    <p class="flex items-center justify-center gap-2">
        <i class="fas fa-truck"></i>
        Fast Worldwide Shipping (5 days delivery) | 100% Satisfaction Guarantee
    </p>
</div>
```

**How to Update:**
- Find the text "Fast Worldwide Shipping (5 days delivery) | 100% Satisfaction Guarantee"
- Replace it with your message
- Keep the `<i class="fas fa-truck"></i>` icon (or change it if you want a different icon)

**Example:**
```html
<!-- Change to: -->
Free Shipping on Orders Over $50 | Limited Time Offer
```

---

#### 2. **Header/Logo** (Navigation Bar)

**Location:** Lines 76-82

**Current Code:**
```html
<a href="#" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
    <i class="fas fa-crown mr-2"></i>Miguel
</a>
```

**How to Update:**
- Replace "Miguel" with your brand name
- Keep `<i class="fas fa-crown mr-2"></i>` or choose a different icon from [Font Awesome](https://fontawesome.com/icons)

**Example:**
```html
<!-- Change to: -->
<i class="fas fa-star mr-2"></i>Your Brand Name
```

---

#### 3. **Hero Section** (Main Banner)

**Location:** Lines 119-135

**Current Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 tracking-tight leading-tight">
    Wear Your Vow: Samurai Stillness, Hip-Hop Grit
</h1>
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed font-light">
    Cinematic tees with meaning. Made by Miguel.
</p>
```

**How to Update:**
- Change the `<h1>` text to your main headline
- Change the `<p>` text to your tagline/subtitle
- The classes control styling (keep them unless you want to redesign)

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 tracking-tight leading-tight">
    Your Amazing Product Here
</h1>
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed font-light">
    Your compelling tagline goes here.
</p>
```

---

#### 4. **Features Section** (Three Feature Cards)

**Location:** Lines 161-207

Each feature card follows this pattern:

**Current Code (Feature 1):**
```html
<div class="feature-card bg-white border border-gray-200 rounded-lg p-8 hover:shadow-xl transition-all duration-300">
    <div class="mb-6">
        <div class="inline-flex items-center justify-center w-16 h-16 bg-gray-900 rounded-lg">
            <i class="fas fa-book text-white text-2xl"></i>
        </div>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">
        Lore-driven Designs
    </h3>
    <p class="text-gray-600 leading-relaxed">
        Each design tells a story...
    </p>
</div>
```

**How to Update:**

1. **Change the Icon:**
   - Find the `<i class="fas fa-book...">` 
   - Replace `fa-book` with another icon from [Font Awesome Icons](https://fontawesome.com/icons)
   - Examples: `fa-star`, `fa-heart`, `fa-rocket`, `fa-gem`

2. **Change the Heading:**
   - Replace "Lore-driven Designs" with your feature name

3. **Change the Description:**
   - Replace the paragraph text with your feature description

**Complete Example:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-lg p-8 hover:shadow-xl transition-all duration-300">
    <div class="mb-6">
        <div class="inline-flex items-center justify-center w-16 h-16 bg-gray-900 rounded-lg">
            <i class="fas fa-rocket text-white text-2xl"></i>
        </div>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">
        Fast Performance
    </h3>
    <p class="text-gray-600 leading-relaxed">
        Lightning-quick load times and smooth interactions designed to keep your users engaged.
    </p>
</div>
```

---

#### 5. **Benefits Section** (With Images)

**Location:** Lines 223-350

Each benefit has a heading, description, and bullet points:

**Current Code (Example - Cinematic Tees):**
```html
<h3 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 mb-4">
    Cinematic Tees
</h3>
<p class="text-gray-600 text-lg leading-relaxed mb-6">
    Our designs are visual masterpieces...
</p>
<ul class="space-y-3 mb-6">
    <li class="flex items-start gap-3">
        <i class="fas fa-check text-gray-900 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700">Premium quality fabrics with vibrant, long-lasting prints</span>
    </li>
    <!-- More list items -->
</ul>
```

**How to Update:**

1. **Change the Heading:**
   ```html
   <h3>Your New Heading</h3>
   ```

2. **Change the Description:**
   ```html
   <p class="text-gray-600 text-lg leading-relaxed mb-6">
       Your new description text goes here.
   </p>
   ```

3. **Update Bullet Points:**
   ```html
   <li class="flex items-start gap-3">
       <i class="fas fa-check text-gray-900 mt-1 flex-shrink-0"></i>
       <span class="text-gray-700">Your bullet point text here</span>
   </li>
   ```

4. **Change the Image:**
   Look for the `<img>` tag:
   ```html
   <img src="https://images.unsplash.com/photo-1556740714-a8395b3bf30f?w=800&h=600&fit=crop&q=80" 
        alt="Cinematic tees showcase" 
        class="benefit-image w-full h-auto rounded-lg shadow-lg object-cover">
   ```
   
   Replace the URL with your image URL (see [Image URLs section](#updating-image-urls))

---

#### 6. **About Section**

**Location:** Lines 358-391

**Current Code:**
```html
<div class="bg-gray-50 p-8 md:p-12 rounded-lg border border-gray-200">
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Journey</h3>
    <p class="text-gray-700 leading-relaxed text-lg">
        Miguel Gastin started this brand...
    </p>
</div>
```

**How to Update:**
- Change the `<h3>` heading
- Replace the paragraph text with your company story

---

#### 7. **Testimonials Section**

**Location:** Lines 410-485

Each testimonial card has:

**Current Code (Example):**
```html
<div class="testimonial-card bg-white p-8 rounded-lg border border-gray-200 hover:shadow-lg transition-all duration-300">
    <div class="flex items-center gap-4 mb-4">
        <div class="w-12 h-12 bg-gray-900 rounded-full flex items-center justify-center text-white font-bold">
            JM
        </div>
        <div>
            <h4 class="font-bold text-gray-900">James Mitchell</h4>
            <p class="text-sm text-gray-600">Creative Director</p>
        </div>
    </div>
    <div class="flex gap-1 mb-4">
        <i class="fas fa-star star-rating"></i>
        <i class="fas fa-star star-rating"></i>
        <!-- More stars -->
    </div>
    <p class="text-gray-700 leading-relaxed">
        "The lore-driven designs completely changed..."
    </p>
</div>
```

**How to Update:**

1. **Change the Initials (Avatar):**
   ```html
   <div class="w-12 h-12 bg-gray-900 rounded-full flex items-center justify-center text-white font-bold">
       JM  <!-- Change to customer's initials -->
   </div>
   ```

2. **Change the Name:**
   ```html
   <h4 class="font-bold text-gray-900">James Mitchell</h4>
   <!-- Change to actual customer name -->
   ```

3. **Change the Title:**
   ```html
   <p class="text-sm text-gray-600">Creative Director</p>
   <!-- Change to customer's title/role -->
   ```

4. **Adjust Star Rating:**
   Each `<i class="fas fa-star star-rating"></i>` is one star. Copy/paste to add more or delete to remove.

5. **Update the Quote:**
   ```html
   <p class="text-gray-700 leading-relaxed">
       "Your testimonial text here..."
   </p>
   ```

---

#### 8. **FAQ Section**

**Location:** Lines 516-630

Each FAQ item has:

**Current Code (Example):**
```html
<div class="accordion-item border border-gray-200 rounded-lg overflow-hidden">
    <button class="accordion-button w-full px-6 py-4 md:px-8 md:py-6 bg-gray-50 hover:bg-gray-100 transition-colors duration-300 flex items-center justify-between text-left focus:outline-none focus:ring-2 focus:ring-gray-900 focus:ring-offset-2" onclick="toggleAccordion(this)">
        <span class="text-lg md:text-xl font-semibold text-gray-900">What makes your tees cinematic?</span>
        <i class="accordion-icon fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
    </button>
    <div class="accordion-content bg-white">
        <div class="px-6 py-4 md:px-8 md:py-6 border-t border-gray-200 text-gray-700 leading-relaxed">
            <p class="mb-3">
                Our cinematic tees are designed...
            </p>
            <p>
                Every design goes through...
            </p>
        </div>
    </div>
</div>
```

**How to Update:**

1. **Change the Question:**
   ```html
   <span class="text-lg md:text-xl font-semibold text-gray-900">Your question here?</span>
   ```

2. **Change the Answer:**
   ```html
   <div class="accordion-content bg-white">
       <div class="px-6 py-4 md:px-8 md:py-6 border-t border-gray-200 text-gray-700 leading-relaxed">
           <p class="mb-3">
               Your answer paragraph 1.
           </p>
           <p>
               Your answer paragraph 2.
           </p>
       </div>
   </div>
   ```

3. **To Add More FAQs:**
   Copy the entire `<div class="accordion-item">...</div>` block and paste it below

---

#### 9. **Contact Section**

**Location:** Lines 639-699

**Current Code (Email):**
```html
<a href="mailto:contact@miguelgastin.com" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">
    contact@miguelgastin.com
</a>
```

**How to Update:**
- Replace `contact@miguelgastin.com` with your actual email address

**Form Fields:**
The form has four fields that you can customize by changing the `placeholder` text:

```html
<input type="text" id="name" name="name" required class="..." placeholder="Your name">
<input type="email" id="email" name="email" required class="..." placeholder="your@email.com">
<input type="text" id="subject" name="subject" required class="..." placeholder="How can we help?">
<textarea id="message" name="message" rows="5" required class="..." placeholder="Tell us more..."></textarea>
```

---

#### 10. **Footer**

**Location:** Lines 705-780

**Logo in Footer:**
```html
<h3 class="text-xl font-bold text-white mb-4 flex items-center gap-2">
    <i class="fas fa-crown"></i>Miguel
</h3>
```
Change "Miguel" to your brand name.

**Footer Description:**
```html
<p class="text-gray-400 leading-relaxed mb-6">
    Cinematic tees with meaning. Blending samurai philosophy with hip-hop culture...
</p>
```
Update this text to describe your brand.

**Footer Links:**
```html
<a href="#home" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
```
These links already work if you have the sections with matching IDs.

**Copyright Year:**
```html
&copy; <span id="year">2024</span> Miguel Gastin. All rights reserved.
```
The year updates automatically, but you can change "Miguel Gastin" to your name/brand.

---

### Updating Image URLs

Your page uses images from Unsplash (a free image service). To change them:

**Find Image Tags:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Cinematic tees hero image" 
     class="w-full h-full object-cover">
```

**Where to Find Images:**
1. Visit [Unsplash.com](https://unsplash.com)
2. Search for an image
3. Right-click the image → "Copy image link"
4. Paste it in place of the old URL

**Example:**
```html
<!-- Old: -->
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80"

<!-- New: -->
<img src="https://images.unsplash.com/photo-1505228395891-9a51e7e86e81?w=1600&h=900&fit=crop&q=80"
```

**Important:** Always keep the `alt` attribute (the descriptive text) for accessibility.

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS, you use pre-made classes. Your page loads Tailwind from a CDN (Content Delivery Network), so you don't need to install anything.

### Common Tailwind Classes in Your Page

#### **Text Styling**

```html
<!-- Text Size -->
text-sm          <!-- Small text -->
text-base        <!-- Normal text -->
text-lg          <!-- Large text -->
text-xl          <!-- Extra large -->
text-2xl         <!-- 2x large -->
text-3xl, text-4xl, text-5xl, text-6xl  <!-- Heading sizes -->

<!-- Text Weight (Boldness) -->
font-light       <!-- Thin text -->
font-normal      <!-- Regular text -->
font-semibold    <!-- Semi-bold -->
font-bold        <!-- Bold text -->

<!-- Text Color -->
text-white       <!-- White text -->
text-gray-900    <!-- Dark gray text -->
text-gray-700    <!-- Medium gray text -->
text-gray-600    <!-- Light gray text -->
text-gray-400    <!-- Very light gray text -->

<!-- Text Alignment -->
text-center      <!-- Center text -->
text-left        <!-- Left align text -->
text-right       <!-- Right align text -->
```

#### **Spacing (Padding & Margin)**

```html
<!-- Padding (space inside) -->
p-4              <!-- Padding on all sides -->
px-4             <!-- Padding left and right -->
py-4             <!-- Padding top and bottom -->
px-6 py-2        <!-- Different padding for x and y -->

<!-- Margin (space outside) -->
m-4              <!-- Margin on all sides -->
mx-auto          <!-- Center horizontally -->
mb-4             <!-- Margin bottom -->
mb-6             <!-- Larger margin bottom -->
gap-2            <!-- Space between flex items -->
gap-4, gap-8     <!-- Larger gaps -->
```

#### **Colors**

```html
<!-- Background Colors -->
bg-white         <!-- White background -->
bg-gray-50       <!-- Very light gray -->
bg-gray-900      <!-- Dark gray/black -->
bg-gray-800      <!-- Dark gray -->

<!-- Text Colors (already shown above) -->
text-white, text-gray-900, etc.

<!-- Border Colors -->
border-gray-200  <!-- Light gray border -->
border-gray-800  <!-- Dark border -->
```

#### **Sizing & Layout**

```html
<!-- Width -->
w-full           <!-- 100% width -->
w-12, w-16       <!-- Fixed widths -->

<!-- Height -->
h-full           <!-- 100% height -->
h-12, h-16       <!-- Fixed heights -->

<!-- Display -->
flex             <!-- Flexbox layout -->
grid             <!-- Grid layout -->
hidden           <!-- Hide element -->
block            <!-- Display as block -->
inline-flex      <!-- Inline flexbox -->

<!-- Responsive Classes (Mobile First) -->
md:flex          <!-- Flex on medium screens and up -->
md:grid          <!-- Grid on medium screens and up -->
lg:text-6xl      <!-- Text size changes on large screens -->
sm:px-6          <!-- Padding changes on small screens -->
```

#### **Borders & Shadows**

```html
<!-- Borders -->
border           <!-- 1px border -->
border-gray-200  <!-- Light gray border -->
rounded-lg       <!-- Rounded corners (large) -->
rounded          <!-- Slightly rounded corners -->

<!-- Shadows -->
shadow-sm        <!-- Small shadow -->
shadow-lg        <!-- Large shadow -->
hover:shadow-xl  <!-- Extra large shadow on hover -->
```

#### **Transitions & Animations**

```html
<!-- Transitions (smooth changes) -->
transition-all   <!-- Transition all properties -->
transition-colors<!-- Transition only colors -->
duration-300     <!-- 300ms duration -->
duration-300 ease<!-- With easing function -->

<!-- Hover Effects -->
hover:text-gray-900  <!-- Change on hover -->
hover:bg-gray-100    <!-- Background change on hover -->
hover:shadow-xl      <!-- Shadow on hover -->

<!-- Focus Effects (for form inputs) -->
focus:outline-none       <!-- Remove default outline -->
focus:ring-2             <!-- Add ring/outline -->
focus:ring-gray-900      <!-- Ring color -->
focus:border-transparent <!-- Remove border -->
```

### How to Modify Classes

#### **Example 1: Change Button Color**

**Current Code:**
```html
<a href="https://stripe.com/shop" class="btn-primary bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold hover:bg-gray-800">
    Buy Now
</a>
```

**Change the background color from dark gray to blue:**
```html
<!-- Replace bg-gray-900 with bg-blue-600 -->
<a href="https://stripe.com/shop" class="btn-primary bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700">
    Buy Now
</a>
```

**Available Tailwind Colors:**
- `gray`, `blue`, `red`, `green`, `yellow`, `purple`, `pink`, `indigo`, `cyan`, `teal`, `orange`
- Followed by intensity: `50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`
- Example: `bg-blue-500`, `bg-red-700`, `text-green-600`

---

#### **Example 2: Increase Padding**

**Current Code:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-lg p-8 hover:shadow-xl transition-all duration-300">
```

**Increase padding from 8 to 12:**
```html
<!-- Replace p-8 with p-12 -->
<div class="feature-card bg-white border border-gray-200 rounded-lg p-12 hover:shadow-xl transition-all duration-300">
```

**Padding Scale:**
- `p-2`, `p-4`, `p-6`, `p-8`, `p-10`, `p-12`, `p-16`, `p-20`

---

#### **Example 3: Change Text Size**

**Current Code:**
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Our Features
</h2>
```

**Make text smaller on mobile:**
```html
<!-- Replace text-3xl with text-2xl -->
<h2 class="text-2xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Our Features
</h2>
```

**What the responsive classes mean:**
- `text-2xl` - Mobile size (small screens)
- `md:text-4xl` - Medium screens and up
- `lg:text-5xl` - Large screens and up

---

#### **Example 4: Change Grid Columns**

**Current Code:**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-6 lg:gap-8">
    <!-- 3 feature cards -->
</div>
```

**Change from 3 columns to 2 columns on medium screens:**
```html
<!-- Replace md:grid-cols-3 with md:grid-cols-2 -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-8 md:gap-6 lg:gap-8">
    <!-- Now displays 1 column on mobile, 2 on medium, 3 on large -->
</div>
```

---

#### **Example 5: Change Hover Effect**

**Current Code:**
```html
<div class="feature-card bg-white border border-gray-200 rounded-lg p-8 hover:shadow-xl transition-all duration-300">
```

**Make the hover effect less dramatic:**
```html
<!-- Replace hover:shadow-xl with hover:shadow-md -->
<div class="feature-card bg-white border border-gray-200 rounded-lg p-8 hover:shadow-md transition-all duration-300">
```

**Shadow Options:**
- `shadow-sm` - Smallest shadow
- `shadow-md` - Medium shadow
- `shadow-lg` - Large shadow
- `shadow-xl` - Extra large shadow
- `shadow-2xl` - Largest shadow

---

### Responsive Design Breakpoints

Your page uses these responsive breakpoints:

```
Mobile:    Default (no prefix)
Small:     sm:    (640px and up)
Medium:    md:    (768px and up)
Large:     lg:    (1024px and up)
XL:        xl:    (1280px and up)
2XL:       2xl:   (1536px and up)
```

**Example:**
```html
<div class="text-sm md:text-base lg:text-lg">
    This text is:
    - Small on mobile
    - Medium on tablets (768px+)
    - Large on desktops (1024px+)
</div>
```

---

### Common Customization Scenarios

#### **Scenario 1: Make Sections Narrower**

**Current Code:**
```html
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
```

**Make it narrower (max-w-4xl = narrower, max-w-5xl = wider):**
```html
<!-- Replace max-w-7xl with max-w-5xl -->
<div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
```

---

#### **Scenario 2: Add More Vertical Space**

**Current Code:**
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

**Add more padding (vertical space):**
```html
<!-- Replace py-24 with py-32 (on medium screens) -->
<section id="features" class="py-16 md:py-32 bg-white">
```

---

#### **Scenario 3: Change Background Color**

**Current Code:**
```html
<section id="benefits" class="py-16 md:py-24 bg-gray-50">
```

**Change to white:**
```html
<!-- Replace bg-gray-50 with bg-white -->
<section id="benefits" class="py-16 md:py-24 bg-white">
```

---

## Fixing Broken Links

### Understanding Links in Your Page

Your page has three types of links:

1. **Internal Links** - Jump to sections on the same page
2. **External Links** - Go to other websites
3. **Page Links** - Go to other HTML files in your project

---

### All Links in Your Page

#### **Navigation Menu Links** (Lines 84-92)

```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#home" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Home</a>
    <a href="#features" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Features</a>
    <a href="#benefits" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Benefits</a>
    <a href="#about" class="nav-link text-gray-700 hover:text-gray-900 font-medium">About</a>
    <a href="#testimonials" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Testimonials</a>
    <a href="#faq" class="nav-link text-gray-700 hover:text-gray-900 font-medium">FAQ</a>
    <a href="#contact" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Contact</a>
</nav>
```

**Status:** ✅ These work correctly (they match section IDs)

---

#### **"Buy Now" / "Shop Now" Links** (Multiple Locations)

**Locations:**
- Line 97 (Header)
- Line 104 (Mobile menu)
- Line 141 (Hero section)
- Line 354 (CTA section)
- And more...

**Current Code:**
```html
<a href="https://stripe.com/shop" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition-all duration-300 shadow-lg">
    Shop Now
</a>
```

**Status:** ⚠️ This points to Stripe's generic shop page. You need to update this.

**How to Fix:**

1. **If you have a Stripe store:**
   ```html
   <!-- Replace with your actual Stripe shop link -->
   <a href="https://your-store.stripe.com" class="btn-primary...">
   ```

2. **If you have a Shopify store:**
   ```html
   <a href="https://your-store.myshopify.com" class="btn-primary...">
   ```

3. **If you have a custom shop page:**
   ```html
   <a href="shop.html" class="btn-primary...">
   ```

4. **If you have WooCommerce/WordPress:**
   ```html
   <a href="https://yourwebsite.com/shop" class="btn-primary...">
   ```

**To Update All "Shop Now" Links at Once:**

Use Find & Replace in your text editor:
1. Press `Ctrl+H` (Windows) or `Cmd+H` (Mac)
2. Find: `https://stripe.com/shop`
3. Replace with: `https://your-actual-shop-url.com`
4. Click "Replace All"

---

#### **Logo Link** (Line 77)

**Current Code:**
```html
<a href="#" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
    <i class="fas fa-crown mr-2"></i>Miguel
</a>
```

**Status:** ⚠️ The `href="#"` doesn't go anywhere

**How to Fix:**

**Option 1 - Go to home section:**
```html
<a href="#home" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
```

**Option 2 - Go to top of page:**
```html
<a href="index.html" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
```

---

#### **Footer Links** (Lines 720-760)

**Quick Links Section:**
```html
<a href="#home" class="text-gray-400 hover:text-white transition-colors duration-300">Home</a>
<a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#about" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a>
<a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a>
```

**Status:** ✅ These work correctly

---

#### **Resources Section Links** (Lines 753-760)

**Current Code:**
```html
<a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a>
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
<a href="https://stripe.com/shop" class="text-gray-400 hover:text-white transition-colors duration-300">Shop</a>
```

**Status:** ⚠️ These need files to exist

- `privacy.html` - Needs to be created
- `terms.html` - Needs to be created
- `blog.html` - Optional (can be removed if not needed)
- `https://stripe.com/shop` - Needs to be updated

---

#### **Contact Section Email Link** (Line 651)

**Current Code:**
```html
<a href="mailto:contact@miguelgastin.com" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">
    contact@miguelgastin.com
</a>
```

**How to Update:**
1. Replace `contact@miguelgastin.com` with your email
2. Keep the `mailto:` prefix

**Example:**
```html
<a href="mailto:your-email@yoursite.com" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">
    your-email@yoursite.com
</a>
```

---

#### **Footer Contact Email** (Line 767)

**Current Code:**
```html
<a href="mailto:contact@miguelgastin.com" class="text-gray-400 hover:text-white transition-colors duration-300">
    contact@miguelgastin.com
</a>
```

**Update this too** with your actual email.

---

### Step-by-Step: Fix All Links

#### **Step 1: Find All Links**

Use Find feature (`Ctrl+F` or `Cmd+F`) to search for:
- `href="https://stripe.com/shop"` - Update all instances
- `href="mailto:contact@miguelgastin.com"` - Update both instances
- `href="#"` - Update the logo link

#### **Step 2: Update Shop Links**

```html
<!-- BEFORE: -->
<a href="https://stripe.com/shop" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition-all duration-300 shadow-lg">
    Shop Now
</a>

<!-- AFTER (Example with Shopify): -->
<a href="https://my-store.myshopify.com/products" class="btn-primary bg-white text-gray-900 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition-all duration-300 shadow-lg">
    Shop Now
</a>
```

#### **Step 3: Update Email Links**

```html
<!-- BEFORE: -->
<a href="mailto:contact@miguelgastin.com">contact@miguelgastin.com</a>

<!-- AFTER: -->
<a href="mailto:your-email@example.com">your-email@example.com</a>
```

#### **Step 4: Update Logo Link**

```html
<!-- BEFORE: -->
<a href="#" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">

<!-- AFTER: -->
<a href="#home" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
```

---

### Testing Your Links

After updating links:

1. **Save the file** (Ctrl+S or Cmd+S)
2. **Refresh the browser** (F5 or Cmd+R)
3. **Click each link** to verify it works
4. **Check mobile menu** links work on small screens

---

## Linking Privacy and Terms Pages

### Why You Need These Pages

Privacy Policy and Terms of Service are legal pages that protect you and your customers. They're also required by law in many jurisdictions if you collect user data or sell products.

### Creating the Files

#### **Step 1: Create privacy.html**

1. Open your text editor
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`
4. Add this basic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Wear Your Vow">
    <title>Privacy Policy | Wear Your Vow</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <a href="index.html" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
                    <i class="fas fa-crown mr-2"></i>Miguel
                </a>
                <a href="index.html" class="text-gray-600 hover:text-gray-900">← Back to Home</a>
            </div>
        </div>
    </header>

    <!-- Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>
                    At Miguel Gastin, we are committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site or when you choose to participate in various activities related to the Site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase products from the Site.</li>
                    <li>Data From Social Networks: User information from social networks, including your name, your social network username, location, gender, birth date, email address, profile picture, and public data for contacts.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Generate a personal profile about you so that future visits to the Site will be personalized as possible.</li>
                    <li>Increase the efficiency and operation of the Site.</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site.</li>
                    <li>Notify you of updates to the Site.</li>
                    <li>Process your transactions and send related information.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p>
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>By Law or to Protect Rights: If we believe the release of information is necessary to comply with the law.</li>
                    <li>Third-Party Service Providers: We may share your information with third parties that perform services for us or on our behalf.</li>
                    <li>Marketing Communications: With your permission, we may share your information with our marketing partners.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to protect your personal information. However, despite our efforts, no security system is impenetrable.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:contact@miguelgastin.com" class="text-blue-600 hover:text-blue-800">contact@miguelgastin.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    &copy; <span id="year">2024</span> Miguel Gastin. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

---

#### **Step 2: Create terms.html**

1. Create a new file
2. Save it as `terms.html` in the same folder as `index.html`
3. Add this basic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Wear Your Vow">
    <title>Terms of Service | Wear Your Vow</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <a href="index.html" class="text-2xl font-bold text-gray-900 hover:text-gray-700 transition-colors duration-300">
                    <i class="fas fa-crown mr-2"></i>Miguel
                </a>
                <a href="index.html" class="text-gray-600 hover:text-gray-900">← Back to Home</a>
            </div>
        </div>
    </header>

    <!-- Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Miguel Gastin's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modifying or copying the materials</li>
                    <li>Using the materials for any commercial purpose or for any public display</li>
                    <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                    <li>Removing any copyright or other proprietary notations from the materials</li>
                    <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>
                    The materials on Miguel Gastin's website are provided on an 'as is' basis. Miguel Gastin makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>
                    In no event shall Miguel Gastin or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Miguel Gastin's website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Miguel Gastin's website could include technical, typographical, or photographic errors. Miguel Gastin does not warrant that any of the materials on its website are accurate, complete, or current. Miguel Gastin may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>
                    Miguel Gastin has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Miguel Gastin of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>
                    Miguel Gastin may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Us</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    Email: <a href="mailto:contact@miguelgastin.com" class="text-blue-600 hover:text-blue-800">contact@miguelgastin.com</a>
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    &copy; <span id="year">2024</span> Miguel Gastin. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

---

### Customizing Your Privacy & Terms Pages

#### **Update the Company Name**

In both `privacy.html` and `terms.html`, replace:
- `Miguel Gastin` with your company name
- `contact@miguelgastin.com` with your email
- `Wear Your Vow` with your brand name

**Example - In privacy.html:**
```html
<!-- BEFORE: -->
<title>Privacy Policy | Wear Your Vow</title>
<a href="index.html" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-crown mr-2"></i>Miguel
</a>

<!-- AFTER: -->
<title>Privacy Policy | Your Brand Name</title>
<a href="index.html" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-crown mr-2"></i>Your Brand Name
</a>
```

---

#### **Update the Email Address**

Search for `contact@miguelgastin.com` and replace with your email:

```html
<!-- BEFORE: -->
Email: <a href="mailto:contact@miguelgastin.com" class="text-blue-600 hover:text-blue-800">contact@miguelgastin.com</a>

<!-- AFTER: -->
Email: <a href="mailto:your-email@yoursite.com" class="text-blue-600 hover:text-blue-800">your-email@yoursite.com</a>
```

---

#### **Update the Copyright Year**

Both files have a script that automatically updates the year:

```html
<p class="text-gray-400 text-sm">
    &copy; <span id="year">2024</span> Miguel Gastin. All rights reserved.
</p>

<script>
    document.getElementById('year').textContent = new Date().getFullYear();
</script>
```

This will automatically show the current year, so you don't need to update it manually.

---

#### **Customize the Content**

The sample text is generic. Customize it for your business:

**In privacy.html - Update:**
- Section 2: "Information We Collect" - List what data you actually collect
- Section 3: "Use of Your Information" - Explain how you use it
- Section 4: "Disclosure of Your Information" - Who you share data with

**In terms.html - Update:**
- Section 1: "Agreement to Terms" - Your specific terms
- Section 5: "Accuracy of Materials" - Your policies
- Section 8: "Governing Law" - Your jurisdiction

---

### Linking These Pages to index.html

The links are already in your `index.html`, but let's verify they're correct:

#### **Footer Links** (Already Correct)

**Location:** Lines 753-760 in index.html

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
```

✅ These links will work once you create `privacy.html` and `terms.html`

---

#### **Optional: Add Links to Navigation**

If you want to add Privacy/Terms to the main navigation menu:

**Location:** Lines 84-92 in index.html

**Current Code:**
```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#home" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Home</a>
    <a href="#features" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Features</a>
    <!-- ... other links ... -->
</nav>
```

**Add these lines:**
```html
<a href="privacy.html" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Privacy</a>
<a href="terms.html" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Terms</a>
```

---

### File Structure After Creating Pages

Your project folder should now look like:

```
project-folder/
├── index.html          (Your main landing page)
├── privacy.html        (Privacy Policy page)
├── terms.html          (Terms of Service page)
├── blog.html           (Optional - if you want a blog)
└── README.md           (This documentation)
```

---

### Testing Your Links

1. **Save all files** (Ctrl+S or Cmd+S)
2. **Open index.html** in your browser
3. **Scroll to footer** and click "Privacy Policy"
   - Should go to privacy.html
   - Should see "Back to Home" link
4. **Click "Back to Home"** - Should return to index.html
5. **Repeat for Terms of Service**
6. **Test on mobile** - Use browser's mobile view (F12 → responsive mode)

---

## Navigation Menu Updates

### Current Navigation Structure

Your page has two navigation menus:

1. **Desktop Menu** (Lines 84-92) - Visible on medium screens and up
2. **Mobile Menu** (Lines 106-117) - Visible on small screens

---

### Desktop Navigation

**Location:** Lines 84-92

```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#home" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Home</a>
    <a href="#features" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Features</a>
    <a href="#benefits" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Benefits</a>
    <a href="#about" class="nav-link text-gray-700 hover:text-gray-900 font-medium">About</a>
    <a href="#testimonials" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Testimonials</a>
    <a href="#faq" class="nav-link text-gray-700 hover:text-gray-900 font-medium">FAQ</a>
    <a href="#contact" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Contact</a>
</nav>
```

**How to Add a Menu Item:**

```html
<!-- Add this line: -->
<a href="#your-section" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Your Label</a>
```

**Example - Add a "Blog" link:**
```html
<a href="blog.html" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Blog</a>
```

---

### Mobile Navigation

**Location:** Lines 106-117

```html
<nav class="mobile-menu hidden md:hidden pb-4 border-t border-gray-200">
    <a href="#home" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Home</a>
    <a href="#features" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Features</a>
    <!-- ... other links ... -->
</nav>
```

**Important:** Keep the mobile menu in sync with the desktop menu.

**How to Add a Menu Item to Mobile:**

```html
<a href="#your-section" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Your Label</a>
```

---

### Step-by-Step: Add a New Menu Item

#### **Step 1: Add to Desktop Menu**

Find line 84 and add your link:

```html
<nav class="hidden md:flex items-center gap-8">
    <a href="#home" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Home</a>
    <a href="#features" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Features</a>
    <a href="#benefits" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Benefits</a>
    <a href="#about" class="nav-link text-gray-700 hover:text-gray-900 font-medium">About</a>
    <a href="#testimonials" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Testimonials</a>
    <a href="#faq" class="nav-link text-gray-700 hover:text-gray-900 font-medium">FAQ</a>
    <a href="#contact" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Contact</a>
    <!-- ADD YOUR NEW LINK HERE: -->
    <a href="blog.html" class="nav-link text-gray-700 hover:text-gray-900 font-medium">Blog</a>
</nav>
```

#### **Step 2: Add to Mobile Menu**

Find line 106 and add the same link:

```html
<nav class="mobile-menu hidden md:hidden pb-4 border-t border-gray-200">
    <a href="#home" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Home</a>
    <a href="#features" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Features</a>
    <a href="#benefits" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Benefits</a>
    <a href="#about" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">About</a>
    <a href="#testimonials" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Testimonials</a>
    <a href="#faq" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">FAQ</a>
    <a href="#contact" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Contact</a>
    <!-- ADD YOUR NEW LINK HERE: -->
    <a href="blog.html" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 transition-colors duration-300 rounded">Blog</a>
</nav>
```

#### **Step 3: Test**

1. Save the file
2. Refresh browser
3. Test on desktop - new link appears in menu
4. Test on mobile - new link appears when you click the hamburger menu

---

### Removing a Menu Item

To remove a menu item, delete the entire `<a>` line from BOTH the desktop and mobile menus.

**Example - Remove "About":**

```html
<!-- DELETE THIS FROM BOTH MENUS: -->
<a href="#about" class="nav-link text-gray-700 hover:text-gray-900 font-medium">About</a>
```

---

## Troubleshooting

### Problem: Links Don't Work

**Symptom:** Clicking a link does nothing or shows a 404 error

**Solutions:**

1. **Check the href matches a section ID:**
   ```html
   <!-- Navigation link: -->
   <a href="#features">Features</a>
   
   <!-- Must have matching section: -->
   <section id="features">...</section>
   ```

2. **Check file names are correct:**
   ```html
   <!-- If linking to privacy.html -->
   <a href="privacy.html">Privacy</a>
   
   <!-- File must be named exactly: privacy.html (lowercase, no spaces) -->
   ```

3. **Check file is in same folder as index.html:**
   ```
   Correct:
   ├── index.html
   ├── privacy.html
   
   Wrong:
   ├── index.html
   └── pages/
       └── privacy.html
   ```

---

### Problem: Text Changes Don't Show

**Symptom:** You changed text but it doesn't appear on the page

**Solutions:**

1. **Save the file** - Press Ctrl+S (Windows) or Cmd+S (Mac)
2. **Hard refresh browser** - Press Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
3. **Clear browser cache** - Close and reopen browser
4. **Check you edited the right file** - Make sure you're editing `index.html`

---

### Problem: Styling Looks Wrong

**Symptom:** Classes don't work or styling is broken

**Solutions:**

1. **Don't remove Tailwind classes** - Only modify class names, don't delete them
   ```html
   <!-- WRONG - Removes all styling: -->
   <div class="">Content</div>
   
   <!-- RIGHT - Keeps styling: -->
   <div class="text-2xl font-bold text-gray-900">Content</div>
   ```

2. **Use valid Tailwind classes** - Check [Tailwind docs](https://tailwindcss.com/docs)
   ```html
   <!-- WRONG - Not a real class: -->
   <div class="text-huge">Content</div>
   
   <!-- RIGHT - Real class: -->
   <div class="text-6xl">Content</div>
   ```

3. **Keep responsive prefixes** - Don't remove `md:` or `lg:` prefixes
   ```html
   <!-- WRONG - Removes responsive design: -->
   <div class="text-2xl text-4xl">Content</div>
   
   <!-- RIGHT - Responsive: -->
   <div class="text-2xl md:text-4xl">Content</div>
   ```

---

### Problem: Mobile Menu Doesn't Work

**Symptom:** Hamburger menu doesn't open on mobile

**Solutions:**

1. **Check JavaScript is not broken** - Look in browser console (F12) for errors
2. **Don't modify the JavaScript** - The code at the bottom of `index.html` handles the menu
3. **Test on real mobile device** - Some mobile browsers behave differently
4. **Check viewport meta tag** exists:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

---

### Problem: Images Don't Load

**Symptom:** Images show broken icon or don't appear

**Solutions:**

1. **Check image URL is correct:**
   ```html
   <!-- WRONG - URL broken: -->
   <img src="https://images.unsplash.com/photo-invalid-id?w=800">
   
   <!-- RIGHT - Valid URL: -->
   <img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=800">
   ```

2. **Use HTTPS URLs** - Don't use HTTP (without the 's')
   ```html
   <!-- WRONG: -->
   <img src="http://images.unsplash.com/...">
   
   <!-- RIGHT: -->
   <img src="https://images.unsplash.com/...">
   ```

3. **Check image file exists** - If using local images:
   ```
   ├── index.html
   ├── images/
   │   └── my-image.jpg
   ```
   
   Then use:
   ```html
   <img src="images/my-image.jpg">
   ```

---

### Problem: Form Doesn't Submit

**Symptom:** Contact form shows error or doesn't send

**Solutions:**

1. **Check all required fields are filled:**
   ```html
   <!-- These fields are required: -->
   <input type="text" id="name" name="name" required>
   <input type="email" id="email" name="email" required>
   <input type="text" id="subject" name="subject" required>
   <textarea id="message" name="message" required></textarea>
   ```

2. **Note:** The form currently logs to console - it doesn't actually send emails. To enable email sending, you need a backend service like:
   - Formspree (formspree.io)
   - EmailJS (emailjs.com)
   - Your own server

3. **To use Formspree:**
   ```html
   <!-- Change the form tag to: -->
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
       <!-- Keep all fields the same -->
   </form>
   ```

---

### Problem: Layout Breaks on Mobile

**Symptom:** Page looks weird on phone or tablet

**Solutions:**

1. **Don't remove responsive classes:**
   ```html
   <!-- WRONG - Breaks on mobile: -->
   <div class="md:flex">Content</div>
   
   <!-- RIGHT - Works on mobile: -->
   <div class="grid grid-cols-1 md:grid-cols-2">Content</div>
   ```

2. **Test on actual devices** - Use browser's mobile view (F12 → Responsive Design Mode)
3. **Check viewport meta tag:**
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

---

## Best Practices

### 1. Always Backup Before Major Changes

Before making significant changes:
1. Save a copy of `index.html` as `index-backup.html`
2. Make your changes
3. If something breaks, you can restore from backup

---

### 2. Test After Every Change

After editing:
1. Save the file
2. Refresh the browser
3. Check on desktop and mobile
4. Click all links to verify they work

---

### 3. Use Find & Replace Carefully

When using Find & Replace:
1. Preview the changes first
2. Replace one at a time initially
3. Use "Replace All" only when confident

**Example - Replace all "Miguel" with "Your Name":**
1. Press Ctrl+H (Find & Replace)
2. Find: `Miguel`
3. Replace with: `Your Name`
4. Click "Replace" once to preview
5. If correct, click "Replace All"

---

### 4. Keep Consistent Styling

When adding new sections:
1. Use the same Tailwind classes as existing sections
2. Match the color scheme (grays, blacks, whites)
3. Keep the same spacing and padding
4. Use the same font sizes for similar elements

**Example - Add a new feature card:**
```html
<!-- Copy existing feature card structure: -->
<div class="feature-card bg-white border border-gray-200 rounded-lg p-8 hover:shadow-xl transition-all duration-300">
    <div class="mb-6">
        <div class="inline-flex items-center justify-center w-16 h-16 bg-gray-900 rounded-lg">
            <i class="fas fa-star text-white text-2xl"></i>
        </div>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-3">
        Your Feature Name
    </h3>
    <p class="text-gray-600 leading-relaxed">
        Your feature description.
    </p>
</div>
```

---

### 5. Maintain Mobile Responsiveness

Always include responsive classes:

```html
<!-- GOOD - Responsive: -->
<div class="text-2xl md:text-4xl lg:text-5xl">Heading</div>

<!-- BAD - Not responsive: -->
<div class="text-5xl">Heading</div>
```

---

### 6. Use Semantic HTML

Use proper HTML tags:

```html
<!-- GOOD - Semantic: -->
<header>Navigation</header>
<section id="features">Features</section>
<footer>Footer</footer>

<!-- AVOID - Non-semantic: -->
<div class="header">Navigation</div>
<div class="features">Features</div>
<div class="footer">Footer</div>
```

---

### 7. Keep Code Organized

Maintain consistent indentation:

```html
<!-- GOOD - Easy to read: -->
<div class="container">
    <h1>Title</h1>
    <p>Content</p>
</div>

<!-- BAD - Hard to read: -->
<div class="container">
<h1>Title</h1>
<p>Content</p>
</div>
```

---

### 8. Document Your Changes

Add comments when making significant changes:

```html
<!-- Updated: Changed from 3 columns to 2 columns on 2024-01-15 -->
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
    <!-- Cards -->
</div>
```

---

### 9. Validate Your HTML

Use [W3C HTML Validator](https://validator.w3.org/) to check for errors:
1. Go to validator.w3.org
2. Upload your HTML file
3. Fix any reported errors

---

### 10. Optimize Images

Before uploading images:
1. Compress images (use [TinyPNG](https://tinypng.com/))
2. Use appropriate formats (JPEG for photos, PNG for graphics)
3. Include `alt` text for accessibility
4. Use correct dimensions (don't load 4000px images for 400px display)

---

## Quick Reference

### File Locations for Common Updates

| What to Update | Location | Line |
|---|---|---|
| Announcement bar text | Announcement Bar | 73 |
| Brand name/logo | Header Navigation | 77 |
| Hero title | Hero Section | 122 |
| Hero subtitle | Hero Section | 126 |
| Feature 1 icon | Features Section | 167 |
| Feature 1 title | Features Section | 172 |
| Feature 1 description | Features Section | 175 |
| Benefit 1 image | Benefits Section | 232 |
| Benefit 1 title | Benefits Section | 236 |
| About text | About Section | 368 |
| Testimonial 1 quote | Testimonials | 438 |
| FAQ question 1 | FAQ Section | 528 |
| FAQ answer 1 | FAQ Section | 534 |
| Contact email | Contact Section | 651 |
| Footer text | Footer | 714 |

---

## Additional Resources

### Learning Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **Font Awesome Icons:** https://fontawesome.com/icons
- **HTML Basics:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **CSS Basics:** https://developer.mozilla.org/en-US/docs/Web/CSS
- **Unsplash Images:** https://unsplash.com/

### Tools

- **Text Editors:** 
  - VS Code (free, recommended)
  - Sublime Text
  - Atom
  
- **Browser Developer Tools:** Press F12 in any browser
  
- **HTML Validator:** https://validator.w3.org/

- **Responsive Design Tester:** https://responsively.app/

---

## Getting Help

### Common Questions

**Q: Can I use this template for commercial purposes?**
A: Yes, but customize it with your own content and branding.

**Q: How do I add more sections?**
A: Copy an existing section, update the ID and content, add it to the navigation menu.

**Q: Can I change the colors?**
A: Yes, replace Tailwind color classes (e.g., `bg-gray-900` → `bg-blue-600`).

**Q: How do I add a blog?**
A: Create a `blog.html` file and link to it from the navigation menu.

**Q: Is this mobile-friendly?**
A: Yes, it's fully responsive and mobile-optimized.

---

## Summary

You now have everything you need to maintain and customize your landing page:

✅ **Update Text** - Find and replace content in each section
✅ **Modify Styling** - Change Tailwind CSS classes
✅ **Fix Links** - Update href attributes to correct URLs
✅ **Create Policy Pages** - Add privacy.html and terms.html
✅ **Manage Navigation** - Add/remove menu items
✅ **Troubleshoot Issues** - Use the troubleshooting guide

**Next Steps:**
1. Update all text with your brand information
2. Replace placeholder images with your own
3. Update all links to your actual URLs
4. Create privacy.html and terms.html files
5. Test everything on desktop and mobile
6. Deploy your website

Good luck with your landing page! 🚀