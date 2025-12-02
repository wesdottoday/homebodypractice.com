# Homebody Practice Website

A simple, elegant Hugo site for Homebody Practice meditation business, built with custom branding inspired by lindsaymack.com and marybethlarue.com.

## Quick Start

```bash
# Run the development server
hugo server

# Build the site
hugo

# The built site will be in the /public directory
```

Visit `http://localhost:1313` to view the site locally.

## Site Structure

- **Home** - Main landing page with hero, about section, offerings preview, and CTA
- **About** - Detailed information about the practice
- **Offerings** - Details about meditation sessions and services

## Customizing Homepage Content

**All homepage text is configured in `hugo.toml`** - you don't need to edit the HTML files directly. Simply update the values in the configuration file:

### Hero Section
```toml
[params.hero]
  image = "hero-image.jpg"  # Optional - place your image in themes/homebody/static/images/
  headline = "Welcome to Homebody Practice"
  subheadline = "Meditation for real life"
  description = "A space for remembering connection..."
```

The hero section displays as a full viewport height/width image on the homepage. The navigation remains visible over the image with a semi-transparent background. If no image is specified, it falls back to a gradient background.

### About Section
```toml
[params.about]
  headline = "About"
  content = "Your about content here..."
```

### Offerings Section
```toml
[params.offerings]
  headline = "Offerings"
  intro = "Grounded practices for everyday life."
  description = "Explore offerings designed..."
```

### CTA (Call-to-Action) Section
```toml
[params.cta]
  headline = "Let's Connect"
  content = "Interested in learning more..."
  button_text = "Get in Touch"
  button_link = "mailto:hello@homebodypractice.com"
```

## Brand Specifications

The theme uses the Homebody brand guidelines from the spec sheet:

### Typography
- **Headings**: Cormorant Garamond (serif) - organic, calligraphic feel
- **Body**: Karla (sans-serif) - humanist, rounded, readable

### Colors (Cool Cozy Neutrals)
- Deep Espresso (#2B241E) - main text
- Soft Clay (#C9B5A3) - grounding neutral
- Warm Birch (#E8E1D8) - background
- Pale Olive (#B8BBA4) - cool balance
- Muted Mineral Blue (#99A8B2) - cool balance
- Ochre/Coral accents - vitality

### Design Principles
- Warm, grounded, relational, handcrafted
- Generous spacing and white space
- Natural light aesthetic
- Calm and tactile feel
- Lowercase or title case (avoiding all caps)

## Design Inspiration

This theme incorporates design patterns from:
- **Lindsay Mack** (lindsaymack.com): Clean centered hero, clear navigation, newsletter CTAs
- **Mary Beth LaRue** (marybethlarue.com): Personal welcome sections, mission-focused content, warm storytelling

## Editing Pages

### About Page
Edit `content/about.md` to update the About page content.

### Offerings Page
Edit `content/offerings.md` to update the Offerings page content.

Both pages support:
- A title
- An intro (optional subtitle/tagline)
- Markdown content

## File Locations

```
.
├── hugo.toml                  # Main configuration (edit homepage content here!)
├── content/
│   ├── about.md              # About page content
│   └── offerings.md          # Offerings page content
└── themes/homebody/
    ├── layouts/
    │   ├── index.html        # Homepage template
    │   ├── _default/
    │   │   ├── baseof.html   # Base template
    │   │   └── single.html   # Single page template
    │   └── partials/
    │       ├── header.html   # Site header/navigation
    │       └── footer.html   # Site footer
    └── static/
        └── css/
            └── style.css     # All styles
```

## Next Steps

1. Update the email address in `hugo.toml` under `params.cta.button_link`
2. Customize the homepage content by editing the values in `hugo.toml`
3. Add your content to `content/about.md`
4. Add your offerings to `content/offerings.md`
5. Consider adding images to enhance the visual design
6. Update `baseURL` in `hugo.toml` when you're ready to deploy

## Deployment

The built site in `/public` can be deployed to:
- Netlify
- Vercel
- GitHub Pages
- Any static hosting service

Simply run `hugo` to build, then upload the `/public` directory.
