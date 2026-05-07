# Mintlify Styling Guide

This guide documents how to customize the Interhuman AI documentation using Mintlify's styling capabilities, including global settings, custom CSS/JS, and component styling.

## 1. Global Theme Settings (`docs.json`)

The primary configuration file `docs.json` controls the global theme, colors, and branding.

### Theme & Colors
Set the base theme and color palette. The `maple` theme is used to enable the sidebar layout preferences.
```json
{
  "theme": "maple",
  "colors": {
    "primary": "#BE9AFB",
    "light": "#CEB3FF",
    "dark": "#5A3BAF"
  }
}
```

### Branding
Configure the logo and favicon.
```json
{
  "favicon": "/favicon.svg",
  "logo": {
    "light": "/logo/light.svg",
    "dark": "/logo/dark.svg"
  }
}
```

## 2. Navigation Layout

The navigation layout is configured to use the **Sidebar Layout** which features:
*   **Search Bar:** Located at the top of the sidebar.
*   **Language Picker & Theme Toggle:** Located at the bottom of the sidebar.
*   **Top Navigation:** Managed via Tabs.

### Localization & Sidebar Trigger
To activate the full Sidebar Layout with the language picker in the sidebar footer, the `languages` configuration is used with multiple entries (e.g., `en` and `es`). This explicitly enables the multi-language UI mode.

### Example Configuration
```json
"navigation": {
  "languages": [
    {
      "language": "en",
      "tabs": [
        {
          "tab": "Documentation",
          "groups": [
            {
              "group": "Getting Started",
              "icon": "rocket",
              "pages": ["getting-started/introduction"]
            }
          ]
        }
      ]
    },
    {
      "language": "es",
      "tabs": [...]
    }
  ]
}
```

## 3. Custom CSS

You can fully customize the look and feel by adding a `style.css` file to the root of the repository. Class names defined here are available in all MDX files.

### Sidebar Title Styling
The sidebar group titles are customized by setting the heading font in `docs.json`.

## 4. Font Configuration

Fonts can be configured globally in `docs.json`. You can use external fonts (e.g., Google Fonts) or local font files.

### Configuration Example
This configuration sets "Switzer" as the global font, loading local files from the repository.
```json
{
  "fonts": {
    "heading": {
      "family": "Switzer",
      "source": "/fonts/switzer/Switzer-Bold.woff2",
      "format": "woff2",
      "weight": 800
    },
    "body": {
      "family": "Switzer",
      "source": "/fonts/switzer/Switzer-Regular.woff2",
      "format": "woff2",
      "weight": 400
    }
  }
}
```

## 5. Component Styling (MDX)

### Tailwind CSS
Mintlify supports Tailwind CSS v3 for styling HTML elements within MDX.
*   **Layout:** `w-full`, `aspect-video`, `block`, `hidden`
*   **Appearance:** `rounded-xl`, `border`
*   **Dark Mode:** `dark:hidden`, `dark:block`

### Inline Styles
For values not supported by Tailwind or custom overrides, use the `style` prop.
```jsx
<img style={{ width: '350px', margin: '12px auto' }} src="/path/image.jpg" />
```
