# GitHub Profile Banner

A premium, pure SVG GitHub profile hero banner featuring an animated ASCII portrait, glassmorphism design, and SMIL animations. 

## Features

- **Pure SVG**: No external CSS or JS dependencies. Everything is embedded.
- **SMIL Animations**: Smooth typing effects, floating animations, blinking cursor, and particle effects natively in SVG.
- **Dark/Light Mode**: Full support for GitHub's native theme switching using the `<picture>` element.
- **ASCII Portrait**: Animated ASCII art placeholder for your avatar.
- **Dynamic Greeting**: Animated typing text highlighting roles/skills.

## Usage

To use this banner in your GitHub Profile README, copy the following HTML into your `README.md`:

```html
<a href="https://github.com/YourUsername">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="./light.svg">
    <img alt="GitHub Profile Banner" src="./light.svg" width="100%">
  </picture>
</a>
```

Make sure to replace `YourUsername` with your actual GitHub username.

## Customization

To customize the banner with your own information, name, skills, and ASCII art, please see the [Customization Guide](docs/customization.md).

## Project Structure

```text
github-profile-banner/
├── dark.svg
├── light.svg
├── README.md
├── assets/
│   ├── avatar.png
│   ├── social/
│   └── icons/
└── docs/
    └── customization.md
```
