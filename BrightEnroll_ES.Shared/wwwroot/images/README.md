# Images Folder

## Current Images in BrightEnroll

### 1. **brighthenlogo.png** ? ADDED
- BrightEnroll logo with graduation cap
- Transparent PNG
- Used across Landing, Login, and Dashboard pages

### 2. **kid.png** ? ADDED
- Image of child (for login page background)
- Used on the left side of the login page
- PNG format

### 3. **user-avatar.png** (OPTIONAL)
- User profile avatar image
- If not present, dashboard shows a gradient placeholder
- Recommended size: 80x80px or larger

## Current Location
`BrightEnroll_ES.Shared\wwwroot\images\`

## Files Currently in Folder
- ? brighthenlogo.png (17 KB)
- ? kid.png (462 KB)
- ?? README.md

## Usage in Code
These images are referenced in:
- `Pages\LandingPage.razor` - Uses brighthenlogo.png
- `Pages\LoginPage.razor` - Uses brighthenlogo.png and kid.png
- `Pages\Dashboard.razor` - Uses brighthenlogo.png and gradient avatar

## File Paths in Code
```html
<img src="images/brighthenlogo.png" />
<img src="images/kid.png" />
```

## Status
? All required images are present and configured!
