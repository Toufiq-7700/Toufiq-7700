# Customization Guide

This guide will help you customize `dark.svg` and `light.svg` with your personal information.

Both files have a `<!-- VARIABLES -->` section near the top. You can edit the text and color values in this section to update the banner.

## How to replace avatar

The avatar uses an animated ASCII art portrait.
Because SVG doesn't support running a script to convert images, we have provided an editable text block in the SVG.

1. Convert your `avatar.png` to ASCII art (using any online image-to-ASCII converter, max width 40-50 chars).
2. Open `dark.svg` and `light.svg` in a text editor.
3. Find the `<!-- ASCII PORTRAIT -->` group.
4. Replace the text inside the `<tspan>` tags with your generated ASCII art. 
   - Make sure to use `<tspan x="..." dy="1.2em">` for each new line to keep it structured.

## How to update skills

The skills are listed as "glowing pills" in the SVG.
Find the `<!-- SKILLS -->` section in the SVG files.

1. Each skill is enclosed in a `<g class="skill-pill">` group.
2. Edit the `<text>` element inside this group to change the skill name.
3. To add more skills, duplicate a `<g class="skill-pill">` block, adjust its `transform="translate(x, y)"` position, and update the text.

## How to change colors

Near the top of both `dark.svg` and `light.svg`, there is a `<style>` block containing CSS variables.

Example from `dark.svg`:
```css
:root {
  --bg-color: #030712;
  --card-bg: #0F172A;
  --border-color: rgba(255,255,255,0.08);
  --primary-text: #F8FAFC;
  --secondary-text: #94A3B8;
  --accent-1: #7C3AED;
  --accent-2: #22D3EE;
  --accent-3: #10B981;
}
```

Update these hex codes to change the color palette. 

## How to edit typing animation

The typing animation cycles through your roles.
Find the `<!-- TYPING ANIMATION ROLES -->` section in the SVG.

1. You will see `<text>` elements with SMIL `<animate>` or `<set>` tags that control their visibility.
2. Edit the text content for the roles (e.g., change "Software Engineer" to "Frontend Developer").
3. Ensure the animation timings (`begin`, `dur`) match if you change the number of roles.

## How to add social links

Social icons are located at the bottom right.
Find the `<!-- SOCIALS -->` section.

1. Each social link is an `<a>` tag containing an `<svg>` icon path.
2. Update the `href` attribute to point to your profiles.
3. To add a new link, copy an existing `<a>` block, adjust its `transform="translate(x, 0)"`, and replace the SVG `<path>` with the new icon's path data.
