---
title: How To Create Cards Using Tailwind (From Zero)
published: 2026-07-22
tags: ["ZeroToDev", "CSS", "Tailwind", "Style", "Card"]
category: DevNotes
draft: false
---

I Currently try making cards again, before i've done it with bootstrap though it is still confusing for me, now i try using tailwind and it seems more complicated than i anticipated. I decide to make a guide, so i can remember how to make it.

Also in order for me to make studying front end stuff easier, will definetly refer links here as well in order to see correct documentation. I will use my current project as a practice, this is my Digimon Catalog project with high hopes i can understand Tailwind better.


# THE STEPS


## 1. CREATE CARD WRAPPER

This is the place for the card, we will decide background color, corner curve, shadows and effects when cursor points at the card. For example:

```html

<div class="bg-white rounded-2xl shadow-md border border-gray-100 overflow-hidden hover:shadow-xl transition-all duration-300"> </div>

```

**Documentation Links:**
- bg-white: background color (Warna Latar Belakang) > https://tailwindcss.com/docs/background-color

- rounded-2xl: Curve corner (2x Extra large/16px) > https://tailwindcss.com/docs/border-radius

- shadow-md & hover:shadow-xl: Shadow Effect > https://tailwindcss.com/docs/box-shadow

- border border-gray-100: Thin lines in corners/Borders > https://tailwindcss.com/docs/border-width

- overflow-hidden: Making sure the content that is out of borders is cut (overflow) > https://tailwindcss.com/docs/overflow

- transition-all duration-300: Speed of animation (300ms) > https://tailwindcss.com/docs/transition-duration


## 2. ADD NEW AREA FOR PICTURES/IMAGES (IMAGE SECTION)

In my current project, the api does have an image data so i want the image to appear inside the card, that's why we are going to use div tag and use flexbox so image is always in the middle and propotional.


```html

<div class="p-4 bg-slate-50 flex justify-center items-center h-48">
    <img 
      src="https://digimon-api.vercel.app/images/agumon.jpg" 
      alt="Agumon" 
      class="max-h-full max-w-full object-contain hover:scale-105 transition-transform duration-300"
    />
  </div>

```

**Documentation Links:**
- p-4: Padding / Jarak dalam (16px) > https://tailwindcss.com/docs/padding

- flex justify-center items-center: Image position in the middle > https://tailwindcss.com/docs/justify-content

- h-48: Making sure the height of the image is locked at 192px > https://tailwindcss.com/docs/height

- object-contain: Making sure the picture is fit and propotional > https://tailwindcss.com/docs/object-fit

- hover:scale-105: Zoom picture when hover > https://tailwindcss.com/docs/scale

## 3. ADD AREA OF TEXT AND INFORMATION (CONTENT SECTION)

In this project, i also want to add text in the card for Digimon Name, as for levels i actually want it to appear in details page but i will put it here too as an example.

Example:

```html

<div class="p-5 text-center">
    <h3 class="text-xl font-bold text-gray-800 tracking-wide">
      Agumon
    </h3>

    <span class="inline-block mt-3 px-4 py-1 bg-blue-100 text-blue-700 text-xs font-bold rounded-full uppercase tracking-wider">
      Rookie
    </span>
  </div>

```

**Documentation Links:**
- text-xl: Size of text name (20px) > https://tailwindcss.com/docs/font-size

- font-bold: Bold text format > https://tailwindcss.com/docs/font-weight

- text-gray-800: Text color in dark grey > https://tailwindcss.com/docs/color

- inline-block mt-3: Badge position and Top Space (Margin Top 12px) > https://tailwindcss.com/docs/margin

- bg-blue-100 text-blue-700: Text background color and badge > https://tailwindcss.com/docs/colors

- rounded full: Badge shape in capsule/full circle > https://tailwindcss.com/docs/border-radius

- uppercase tracking-wider: Every letters is capital and there is space between letters > https://tailwindcss.com/docs/letter-spacing


## Final Code

Just an example:


```html
<div class="bg-white rounded-2xl shadow-md border border-gray-100 overflow-hidden hover:shadow-xl transition-all duration-300">
  <div class="p-4 bg-slate-50 flex justify-center items-center h-48">
    <img 
      src="https://digimon-api.vercel.app/images/agumon.jpg" 
      alt="Agumon" 
      class="max-h-full max-w-full object-contain hover:scale-105 transition-transform duration-300"
    />
  </div>

  <div class="p-5 text-center">
    <h3 class="text-xl font-bold text-gray-800 tracking-wide">Agumon</h3>
    <span class="inline-block mt-3 px-4 py-1 bg-blue-100 text-blue-700 text-xs font-bold rounded-full uppercase tracking-wider">
      Rookie
    </span>
  </div>
</div>
```