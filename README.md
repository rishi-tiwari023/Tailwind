# Tailwind CSS - Utility-First CSS Framework

A comprehensive guide and reference for Tailwind CSS implementation, featuring installation methods, project structure, and build configurations.

## 🎨 What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework that provides low-level utility classes to build custom designs directly in your markup. Instead of writing custom CSS, you compose your designs using pre-built classes like `flex`, `pt-4`, `text-center`, and `rotate-90`.

### Key Benefits
- **Utility-First**: Build complex components from a constrained set of primitive utilities
- **Responsive Design**: Built-in responsive variants for every utility
- **Component-Friendly**: Works seamlessly with modern frameworks
- **Customizable**: Fully customizable through configuration
- **Small Bundle Size**: Automatically removes unused CSS in production

## 🚀 Installation Methods

### Method 1: Using Package Manager (Recommended)

#### With npm
```bash
# Initialize project (if not already done)
npm init -y

# Install Tailwind CSS
npm install -D tailwindcss

# Generate configuration file
npx tailwindcss init
```
### Method 2: CDN (Development Only)
```html
<script src="https://cdn.tailwindcss.com"></script>
```
⚠️ **Note**: CDN build is much larger and not optimized for production use.

## 📁 Project Structure

```
tailwind-project/
├── src/
│   ├── input.css          # Main CSS file with Tailwind directives
│   ├── components/        # Reusable component styles
│   └── assets/           # Images, fonts, etc.
├── dist/
│   ├── output.css        # Compiled CSS output
│   └── assets/          # Processed assets
├── public/              # Static files
│   └── index.html       # HTML files
├── tailwind.config.js   # Tailwind configuration
├── package.json         # Project dependencies
└── README.md           # Project documentation
```

## ⚙️ Configuration

### Basic tailwind.config.js
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
## 🎯 CSS Input File (src/input.css)
## 🔨 Build Commands

### Development Build
```bash
# Watch for changes and rebuild
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

### Production Build
```bash
# Single build with optimization
npx tailwindcss -i ./src/input.css -o ./dist/output.css
```

### Package.json Scripts
```json
{
  "scripts": {
    "build-css": "tailwindcss -i ./src/input.css -o ./dist/output.css",
    "watch-css": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch",
    "build-css-prod": "NODE_ENV=production tailwindcss -i ./src/input.css -o ./dist/output.css --minify"
  }
}
```
## 🔧 Advanced Features

### JIT (Just-In-Time) Mode
Modern Tailwind CSS uses JIT mode by default, enabling:
- Dynamic class generation
- Smaller development builds
- All variants enabled by default

### Responsive Design
```html
<div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4">
    Responsive width
</div>
```

### Dark Mode
```javascript
// tailwind.config.js
module.exports = {
  darkMode: 'class', // or 'media'
  // ... rest of config
}
```

```html
<div class="bg-white dark:bg-gray-800 text-black dark:text-white">
    Dark mode support
</div>
```

## 📦 Popular Plugins

```bash
# Forms plugin
npm install -D @tailwindcss/forms

# Typography plugin
npm install -D @tailwindcss/typography

# Aspect ratio plugin
npm install -D @tailwindcss/aspect-ratio

# Line clamp plugin
npm install -D @tailwindcss/line-clamp
```
## 🚀 Performance Tips

1. **Purge unused CSS**: Ensure proper content paths in config
2. **Use production build**: Always minify for production
3. **Optimize images**: Use responsive images with Tailwind classes
4. **Bundle analysis**: Monitor your CSS bundle size

## 📚 Resources

- [Official Documentation](https://tailwindcss.com/docs)
- [Tailwind UI Components](https://tailwindui.com/)
- [Headless UI](https://headlessui.dev/)
- [Heroicons](https://heroicons.com/)
- [Tailwind Play](https://play.tailwindcss.com/)

## 🤝 Contributing

Feel free to submit issues and pull requests to improve this guide!

## 📄 License
This project is open source and available under the [MIT License](LICENSE).

---

Made by Rishi Tiwari with ❤️ and Tailwind CSS