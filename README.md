# RABIKS Email Signature — Template 1 (With Photo)

HTML email signature for **Szymon Rabikowski, CEO** at Rabiks Sp. z o.o.

## Preview

Horizontal layout (1094 × 288px) featuring:
- Blue sidebar with geometric hexagon pattern + person photo
- Name, title, social links, partner logos
- Contact information (phone, email, NIP, REGON, KRS)
- Company addresses (HQ + branch offices)
- Legal disclaimer (Polish)

## Design Specs

| Property | Value |
|----------|-------|
| Primary Color | `#4875FB` (Rabiks Blue) |
| Text Color | `#383838` |
| Heading Font | Krona One (Google Fonts) |
| Body Font | Krub (Google Fonts) |
| Fallback Font | Arial, Helvetica, sans-serif |
| Signature Width | 1094px |
| Signature Height | ~300px |

## Files

```
├── signature.html              # Main HTML email signature
└── images/
    ├── sidebar-composite.png   # Blue sidebar + geometric pattern + photo (composite)
    ├── rabiks-logo.png         # Rabiks logo (blue, with tagline)
    ├── partner-logos.png       # Streamsoft + Dell Technologies logos
    ├── facebook.png            # Facebook icon (dark gray)
    ├── instagram.png           # Instagram icon (dark gray)
    ├── person-photo.png        # Original person photo
    ├── geometric-pattern.png   # Geometric hexagon pattern (PNG)
    ├── geometric-pattern.svg   # Geometric hexagon pattern (SVG source)
    ├── white-rabiks-logo.png   # White Rabiks logo (PNG)
    ├── white-rabiks-logo.svg   # White Rabiks logo (SVG source)
    ├── facebook.svg            # Facebook icon (SVG source)
    └── instagram.svg           # Instagram icon (SVG source)
```

## Usage

### Option 1: Self-hosted images
1. Upload the `images/` folder to your web server
2. In `signature.html`, find-and-replace `images/` with your full URL path (e.g., `https://yourdomain.com/email-assets/`)
3. Copy the HTML and paste it into your email client's signature settings

### Option 2: GitHub-hosted images (quick setup)
1. Push this repo to GitHub
2. Use raw GitHub URLs for images:
   ```
   https://raw.githubusercontent.com/YOUR_USERNAME/REPO_NAME/main/images/sidebar-composite.png
   ```
3. Replace all `images/` paths in `signature.html` with the full raw URLs

## Email Client Compatibility

- ✅ Gmail (Web, iOS, Android)
- ✅ Outlook (2016+, 365, Web)
- ✅ Apple Mail
- ✅ Yahoo Mail
- ✅ Thunderbird
- ✅ Samsung Mail

## Technical Notes

- Table-based layout for maximum email client compatibility
- All CSS is inline (required for email clients)
- MSO conditional comments for Outlook desktop rendering
- Google Fonts with Arial fallback for clients that don't support `@import`
- Complex visual elements (blue sidebar, geometric pattern, photo) are pre-composited as a single PNG image — this is the most reliable approach for email
- Social icons converted from SVG to PNG (SVG not supported by most email clients)
- Non-breaking hyphens (`&#8209;`) used in postal codes to prevent line breaks

## Customization

To change the person's details, edit `signature.html`:
- **Name**: Search for "Szymon" and "Rabikowski"
- **Title**: Search for "CEO"
- **Contact**: Update phone, email, NIP, REGON, KRS values
- **Addresses**: Update the company address and branch office sections
- **Photo**: Replace `images/sidebar-composite.png` (regenerate the composite with the new photo)
- **Social links**: Update the `href` values on the Facebook and Instagram `<a>` tags
