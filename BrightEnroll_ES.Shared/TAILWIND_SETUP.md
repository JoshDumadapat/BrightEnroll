# Tailwind CSS Setup for BrightEnroll ES

## Quick Start (CDN - Current Setup)

The project is currently using Tailwind CSS via CDN, which is the quickest way to get started. No build process required!

### Current Setup

- ? Tailwind CSS is loaded via CDN in `App.razor` and `index.html`
- ? Custom configuration is included inline
- ? Dashboard is converted to use Tailwind utility classes
- ? Bootstrap has been removed

### Usage

Just use Tailwind CSS utility classes directly in your Razor components:

```razor
<div class="bg-white rounded-lg shadow-md p-6">
    <h1 class="text-2xl font-bold text-gray-900">Hello World</h1>
</div>
```

## Production Setup (Recommended)

For production, it's recommended to build Tailwind CSS to reduce file size and improve performance.

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation Steps

1. **Install dependencies:**
   ```bash
   cd BrightEnroll_ES.Shared
   npm install
   ```

2. **Build Tailwind CSS:**
   ```bash
   npm run build:css
   ```

3. **For development with auto-rebuild:**
   ```bash
   npm run watch:css
   ```

4. **Update your HTML files to use the built CSS:**
   
   Change:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   
   To:
   ```html
   <link rel="stylesheet" href="_content/BrightEnroll_ES.Shared/app.min.css" />
   ```

### Build Configuration

The project includes:
- `package.json` - npm scripts for building Tailwind
- `tailwind.config.js` - Tailwind configuration
- `app.css` - Source CSS with Tailwind directives

### Custom Tailwind Configuration

The Tailwind config includes:
- Custom primary color palette
- Custom font family (Inter)
- Content paths configured for Razor files

### Migration Notes

The following files have been migrated to Tailwind:
- ? `Dashboard.razor` - Fully converted to Tailwind utility classes
- ? `dashboard.css` - Removed (no longer needed)

### Tailwind Utility Classes Used

Common patterns in the Dashboard:

| Old CSS Class | New Tailwind Classes |
|--------------|----------------------|
| `.dashboard-container` | `flex min-h-screen bg-gray-100` |
| `.dashboard-sidebar` | `w-48 bg-white border-r border-gray-200 fixed h-screen` |
| `.stat-card` | `bg-white rounded-xl p-5 shadow-sm` |
| `.nav-item.active` | `bg-blue-50 text-blue-600 border-l-blue-600` |

## Common Tailwind Patterns for Blazor

### Buttons
```razor
<button class="bg-blue-600 hover:bg-blue-700 text-white font-semibold py-2 px-4 rounded-lg transition-colors">
    Click Me
</button>
```

### Cards
```razor
<div class="bg-white rounded-xl shadow-sm p-6 hover:shadow-md transition-shadow">
    <!-- Content -->
</div>
```

### Forms
```razor
<input type="text" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent" />
```

### Responsive Design
```razor
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
    <!-- Responsive grid -->
</div>
```

## Resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Tailwind CSS Cheat Sheet](https://nerdcave.com/tailwind-cheat-sheet)
- [Tailwind CSS Components](https://tailwindui.com/components)

## Need Help?

If you encounter any issues:
1. Make sure Tailwind CSS is loading (check browser console)
2. Verify the content paths in `tailwind.config.js`
3. Clear browser cache if styles aren't updating
4. Check that class names are spelled correctly (Tailwind is case-sensitive)
