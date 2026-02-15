# Gloria Pu — Personal Portfolio Website

An editorial-driven personal portfolio website for DJ/Curator/Artist Gloria Pu, built with refined aesthetics inspired by high-end fashion lookbooks (Acne Studios, The Row, early Raf Simons).

## Design Philosophy

**Editorial + Soft Luxury + Restrained Elegance**

- Large typography with oversized serif headings
- Minimal animations and controlled interactions
- Textured quality with grain/noise overlays
- Printshop aesthetic with flat design
- 90% neutral colors + 8% greens + 2% pink/red accents

## Color Palette

### Core Neutrals
- **Ivory**: `#F6F1E7` (page background)
- **Warm Gray**: `#E6E0D6` (divider sections)
- **Ink**: `#121212` (main text)

### Brand Anchors
- **Fairway Green**: `#1F3D2B` (brand color, large titles)
- **Olive**: `#4A5A3A` (hover states, captions)
- **Denim**: `#2F4A64` (links, small highlights)

### Accents
- **Dusty Pink**: `#D9B2B0` (photos, highlights, brand objects)
- **Ox Blood**: `#6A1F2B` (minimal CTA contrast)

## Typography

- **Display Serif**: Cormorant Garamond (headings)
  - H1: 64-80px (hero)
  - H2: 32-40px (section titles)
  
- **Text Sans**: Inter (body text)
  - Body: 16-18px (line-height 1.6)
  - Caption: 12-13px (uppercase labels)

## Structure

1. **Hero Section**: Full-screen visual statement with large typography
2. **About**: Editorial text block with narrative identity (200-300 words)
3. **Gigs Archive**: Photo grid with hover details (event, city, year)
4. **Music**: Embedded Spotify playlists and SoundCloud tracks
5. **Gallery**: Masonry grid for lifestyle visual storytelling
6. **Contact**: Simple form + direct email link

## Customization Guide

### 1. Replace Personal Information

Search and replace in `index.html`:
- "GLORIA PU" → Your name
- "DJ / Curator / Artist" → Your roles
- "Music as Atmosphere." → Your tagline
- "hello@gloriapu.me" → Your email

### 2. Update About Section

Replace the three paragraphs in the About section with your own narrative (aim for 200-300 words total).

### 3. Add Your Gig Photos

Replace the Unsplash image URLs in the Gigs section:
```html
<img src="YOUR_IMAGE_URL" alt="Performance Description">
<h3>Event Name</h3>
<div class="gig-meta">City / Year</div>
```

### 4. Embed Your Music

#### Spotify:
1. Go to your Spotify playlist
2. Click "..." → Share → Copy Embed Code
3. Replace the iframe in the "Spotify Curations" section

#### SoundCloud:
1. Go to your SoundCloud track
2. Click "Share" → Embed
3. Copy the embed code
4. Replace the iframe in the "SoundCloud Mixes" section
5. Update color parameter to `color=%231f3d2b` for brand consistency

### 5. Update Gallery Images

Replace the Unsplash URLs in the Gallery section with your high-resolution lifestyle photos.

### 6. Contact Form Backend

The contact form currently shows a success message without sending data. To make it functional:

**Option A: Use a form service (easiest)**
- Formspree: https://formspree.io
- Basin: https://usebasin.com
- Update the form action: `<form action="https://formspree.io/f/YOUR_ID" method="POST">`

**Option B: Build your own backend**
- Add server-side code (Node.js, Python, PHP)
- Handle form submission via API
- Send email notifications

## Local Development

Simply open `index.html` in a web browser:

```bash
open index.html
```

Or use a local server for better preview:

```bash
# Python
python -m http.server 8000

# Node.js (if you have http-server)
npx http-server

# Then open http://localhost:8000
```

## Deployment Options

### Option 1: Netlify (Recommended)
1. Create account at https://netlify.com
2. Drag and drop the `dj-portfolio` folder
3. Your site will be live in seconds
4. Add custom domain in settings

### Option 2: Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the project directory
3. Follow the prompts

### Option 3: GitHub Pages
1. Create a GitHub repository
2. Push your code
3. Enable GitHub Pages in repository settings
4. Your site will be at `username.github.io/repo-name`

### Option 4: Traditional hosting
- Upload `index.html` to any web host via FTP
- Works with Bluehost, HostGator, etc.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome)

## Performance

The site is optimized for performance:
- Single HTML file (no external dependencies except fonts)
- Minimal JavaScript (vanilla JS, no frameworks)
- CSS custom properties for theming
- Responsive images from Unsplash CDN
- Lazy loading for iframes

## Accessibility

- Semantic HTML5 elements
- Proper heading hierarchy
- Keyboard navigation support
- Focus states on interactive elements
- Alt text on images (update with your descriptions)
- Color contrast meets WCAG AA standards

## Credits

- **Design**: Based on Gloria Pu PRD
- **Fonts**: Google Fonts (Cormorant Garamond, Inter)
- **Placeholder Images**: Unsplash
- **Icons**: SVG patterns generated inline

## License

Feel free to use this template for your personal portfolio. Replace all content with your own.

---

**Questions or need help?** Feel free to customize this further to match your personal brand!
