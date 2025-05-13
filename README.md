# ✨ Sesame CSS Framework

Sesame is a modern, lightweight CSS framework designed to provide a robust and easily customizable foundation for your web development projects. It includes a universal reset, a powerful system for theming with CSS Custom Properties, and sensible base styles for common HTML elements and form controls.

Whether you prefer linking via CDN for quick use or downloading the files for more control, Sesame helps you get started quickly while allowing deep customization.

## 🚀 Features

- **Comprehensive Reset:** Builds upon best practices from popular resets (like Normalize.css) with an effective universal reset for cross-browser consistency.
- **CSS Custom Properties (Variables):** Theme your entire project effortlessly by overriding well-defined variables for colors, spacing, typography, borders, and more.
- **Responsive Foundation:** Includes basic responsive adjustments, particularly for typography, to ensure your base looks good on various devices.
- **Base Element Styling:** Provides clean, accessible default styles for standard HTML elements (headings, paragraphs, lists, links, forms, etc.).
- **Modern Form Resets:** Offers detailed and consistent styling for form controls across different browsers.
- **Utility Classes (Planned/In sesame-styles.css):** Lightweight utility classes for common design patterns like Glassmorphism and Skeuomorphism (Mention this if you plan to include sesame-styles.css).

## 📦 Installation & Usage

Sesame can be included in your project via CDN or by downloading the files.

### Option 1: Via CDN (Recommended for quick start and production)

Use the free jsDelivr CDN to link the files directly in the `<head>` of your HTML documents. Using version numbers is highly recommended for stability.

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/gh/ctrlcat0x/sesame@latest/base.css"
/>
```

Finding the latest version: Check the GitHub repository releases or the jsDelivr page for Sesame to find the latest recommended version tag. Use the `@latest` version tag to always get the updated version in production.

### Option 2: Download Files

You can download the `base.css` file (and `sesame-styles.css` if available) directly from the GitHub repository and host it yourself or include it in your project's build process.

#### 1. Download `base.css` from the main branch or a specific release tag.

#### 2. Save the file in your project's CSS directory (e.g., `/css`).

#### 3. Link the file in your HTML:

```html
<link rel="stylesheet" href="/css/base.css" />
```

### Usage Example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Project</title>

    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/gh/ctrlcat0x/sesame@[VERSION]/base.css"
    />
    <!-- Link your custom stylesheet AFTER Sesame's files -->
    <link rel="stylesheet" href="/path/to/your/my-custom-styles.css" />

    <style>
      /* Your custom overrides or page-specific styles here */
    </style>
  </head>
  <body>
    <!-- Your content here -->
  </body>
</html>
```

## 🎨 Customization (Theming with CSS Variables)

Sesame is built to be easily themed using CSS Custom Properties. You can override the default variables defined in `:root` by simply redefining them in your own CSS file that is linked _after_ the Sesame CSS files.

```css
/* my-custom-styles.css */

:root {
  /* --- Color Overrides --- */
  --back-color: #1e1e1e; /* Darker background */
  --text-color: #e0e0e0; /* Slightly darker text */
  --primary-color: #00aaff; /* Bright blue primary color */
  --accent: #333; /* Darker accent */
  --selection-back: var(
    --primary-color
  ); /* Use the new primary color for selection */
  --selection-text: #fff; /* White selection text */

  /* --- Typography Overrides --- */
  --base-font-size: 17px; /* Larger base font size */
  --font-family: "Roboto Slab", serif; /* Change font family */
  --font-weight: 400; /* Change font weight */
  --line-height: 1.6; /* Increase line height */

  /* --- Spacing Overrides --- */
  --gap: 0.8rem;
  --gap-big: 1.2rem;

  /* --- Border/Radius Overrides --- */
  --border: 1px solid var(--accent);
  --corner-radius: 0.5rem;
}

/* Your project-specific styles below the variable overrides */
h1 {
  border-bottom: var(--border); /* This will use your new border variable */
  padding-bottom: var(--gap-xs); /* Example using a spacing variable */
}

.my-feature-box {
  background-color: var(--back-color); /* Uses your overridden background */
  color: var(--text-color); /* Uses your overridden text color */
  padding: var(--gap-big); /* Uses your overridden big gap */
  border-radius: var(--corner-radius); /* Uses your overridden radius */
}
```

Refer to the `base.css` file to see the full list of customizable variables.

## 👋 Contributing

We welcome contributions to the Sesame CSS Framework! If you have suggestions for improvements, bug fixes, or new features (like additional utility classes or components), please feel free to:

- Open an Issue to discuss ideas or report bugs.
- Fork the repository and submit a Pull Request with your changes.

Please ensure your code adheres to standard CSS practices and consider the framework's goal of being lightweight and customizable.

## 📄 License

Anyone may use this for any sort of bussiness or individual applications.

© 2025 ctrlcat0x
