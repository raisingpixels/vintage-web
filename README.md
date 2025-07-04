# Vintage Web Hugo Theme

A nostalgic Hugo theme inspired by late 90s/early 2000s web design with modern functionality. Experience the charm of classic operating system interfaces with contemporary web standards.

![Theme Preview](https://github.com/raisingpixels/vintage-web-hugo-theme/blob/master/images/screenshot.png?raw=true)

## Features

✨ **Retro Design Elements**
- Classic window-style interface with title bars and controls
- 90s-inspired color palette and typography
- Retro status bar and browser chrome effects
- Blinking text and marquee animations
- Vintage button styling and form controls

🎮 **Interactive Features**
- Functional window controls (minimize, maximize, close)
- Konami code easter egg (↑↑↓↓←→←→BA)
- Keyboard navigation shortcuts
- Interactive image galleries with lightbox
- Copy-to-clipboard for code blocks

📱 **Modern Functionality**
- Fully responsive design
- SEO optimized with structured data
- Fast loading with optimized assets
- Accessibility features
- RSS feeds and social sharing
- Multiple post list views (list, grid, archive)

🎨 **Content Support**
- Complete Markdown support (thoroughly tested with the [Hugo Theme Development Template](https://github.com/raisingpixels/hugo-theme-dev-template))
- Syntax highlighting for code
- Image galleries and media embedding
- Table of contents generation
- Categories, tags, and series support
- Featured images and post metadata

## Installation

### Option 1: Git Submodule (Recommended)

```bash
git submodule add https://github.com/raisingpixels/vintage-web-hugo-theme.git themes/vintage-web-hugo-theme
```

### Option 2: Git Clone

```bash
git clone https://github.com/raisingpixels/vintage-web-hugo-theme.git themes/vintage-web-hugo-theme
```

### Option 3: Download

Download the latest release and extract to your `themes/vintage-web-hugo-theme` directory.

## Configuration

Add the theme to your `hugo.toml`:

```toml
theme = "vintage-web-hugo-theme"
```

### Basic Configuration

```toml
baseURL = "https://yoursite.com"
languageCode = "en-us"
title = "Your Vintage Website"
theme = "vintage-web-hugo-theme"

# Pagination
[pagination]
  pagerSize = 10
  path = "page"

# Taxonomies
[taxonomies]
  category = "categories"
  tag = "tags"
  series = "series"

# Menu
[[menu.main]]
  name = "Home"
  url = "/"
  weight = 10

[[menu.main]]
  name = "Posts"
  url = "/posts/"
  weight = 20

[[menu.main]]
  name = "About"
  url = "/about/"
  weight = 30

# Theme Parameters
[params]
  # Site Description
  description = "A nostalgic journey through the early web"
  author = "Your Name"

  # Retro Features
  show_browser_chrome = true
  show_status_bar = true
  show_sidebar = true
  show_welcome_message = true
  welcome_message = "Welcome to our vintage web experience!"

  # Content Display
  show_featured_sections = true
  show_stats = true
  show_retro_elements = true
  show_sharing = true

  # Footer Options
  show_retro_footer = true
  show_build_info = false

  # Sidebar Options
  show_sidebar_stats = true
  show_retro_sidebar = true
  sidebar_content = "Welcome to our retro corner of the internet!"

  # Social Links
  [params.social]
    twitter = "username"
    github = "username"
    linkedin = "username"
    email = "you@example.com"
    mastodon = "https://mastodon.social/@username"
    youtube = "channelname"
    instagram = "username"

  # SEO and Analytics
  google_analytics = "G-XXXXXXXXXX"

  # Repository (for edit links)
  repo_url = "https://github.com/username/repo"
  edit_page = true
```

## Content Structure

### Front Matter Options

#### Posts (`content/posts/`)

```yaml
---
title: "Your Post Title"
date: 2024-01-01T10:00:00Z
draft: false
description: "Post description for SEO"
author: "Author Name"
categories: ["category1", "category2"]
tags: ["tag1", "tag2", "tag3"]
series: ["series-name"]
featured_image: "https://example.com/image.jpg"
toc: true
weight: 1
---
```

#### Pages (`content/about.md`, etc.)

```yaml
---
title: "About"
date: 2024-01-01T10:00:00Z
draft: false
description: "About page description"
---
```

### Special Content Types

The theme includes comprehensive test content showcasing:

- **Typography Showcase** - All heading levels, text formatting, quotes
- **Media Content** - Images, videos, audio, galleries, responsive media
- **Code Examples** - Syntax highlighting, multiple languages
- **Tables and Lists** - Data tables, ordered/unordered lists
- **Interactive Elements** - Forms, buttons, navigation

## Customization

### Theme Colors

Override CSS custom properties in your site's CSS:

```css
:root {
  --bg-primary: #F5E6E8;
  --bg-secondary: #E8D5D7;
  --bg-window: #F0F0F0;
  --text-primary: #000000;
  --text-link: #0000EE;
  --highlight: #316AC5;
}
```

### Custom CSS

Add custom styles in your `hugo.toml`:

```toml
[params]
  custom_css = """
    .custom-style {
      background: linear-gradient(45deg, #ff00ff, #00ffff);
    }
  """
```

### Custom JavaScript

Add custom JavaScript:

```toml
[params]
  custom_js = """
    console.log('Custom JavaScript loaded!');
  """
```

## Content Creation Tips

### Image Optimization

- Use responsive images with appropriate alt text
- Featured images work best at 1200x600 pixels
- Gallery images should be consistent in aspect ratio

### Code Blocks

Use fenced code blocks with language specification:

````markdown
```javascript
function retroFunction() {
  console.log('Welcome to 1999!');
}
```
````

### Series Organization

Group related posts using the `series` front matter:

```yaml
series: ["hugo-tutorial", "web-development"]
```

## Development

### Testing with exampleSite

The theme includes a complete exampleSite with vintage 90s content to showcase all features:

```bash
# Navigate to the exampleSite directory
cd exampleSite

# Serve the site locally
hugo server

# Or serve with drafts and future posts
hugo server --buildDrafts --buildFuture
```

The exampleSite will be available at `http://localhost:1313` and includes:
- Retro homepage with authentic 90s styling
- HTML tutorial blog post with vintage code examples
- Y2K survival guide with period-appropriate warnings
- Animated GIF collection showcase
- About page with team profiles and tech specs
- Interactive guestbook with sample entries

### Local Development

```bash
hugo server --theme=vintage-web-hugo-theme --buildDrafts
```

### Building for Production

```bash
hugo --theme=vintage-web-hugo-theme --minify
```

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Graceful degradation for older browsers
- Mobile responsive design
- Progressive enhancement approach

## Accessibility

- Semantic HTML structure
- ARIA labels where appropriate
- Keyboard navigation support
- High contrast color schemes
- Screen reader friendly

## Performance

- Optimized CSS and JavaScript
- Image lazy loading
- Minified assets in production
- Efficient Hugo templating
- Fast loading times

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This theme is released under the MIT License. See [LICENSE](LICENSE) for details.

## Credits

- Inspired by classic operating system interfaces
- Built with [Hugo](https://gohugo.io)
- Fonts from Google Fonts
- Icons from Unicode emoji set

## Support

- 📖 [Documentation](https://github.com/raisingpixels/vintage-web-hugo-theme/blob/master/README.md)
- 🐛 [Issues](https://github.com/raisingpixels/vintage-web-hugo-theme/issues)

---

Made with 💾 by [raisingpixels](https://github.com/raisingpixels)

*Remember: This site is Y2K compliant and best viewed in 1024x768! 🖥️*
