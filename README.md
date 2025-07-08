# KAWAIININJA UI Kits Portfolio

A dark, cyberpunk-inspired portfolio website showcasing premium UI kits. Built with pure HTML/CSS using the official KAWAIININJA theme system.

## 🎨 Design Features

- **Dark Theme**: Pure black background with subtle transparency layers
- **Cyberpunk Aesthetic**: Neon accents in pink/cyan with glowing effects
- **Kawaii Elements**: Soft animations and playful design touches
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- **Fast Loading**: No external dependencies, optimized for GitHub Pages

## 🛠️ Tech Stack

- **HTML5**: Semantic, accessible markup
- **CSS3**: Custom dark theme with CSS variables
- **No Frameworks**: Pure vanilla code, no Bootstrap/Tailwind
- **No JavaScript**: Static site, perfect for GitHub Pages

## 📁 Project Structure

```
portfolio/
├── index.html          # Main portfolio page
├── style.css          # KAWAIININJA dark theme styles
├── ui/                # UI kit preview images
│   ├── midnight-bubble-kit.png
│   ├── neon-dashboard-kit.png
│   ├── cyber-forms-kit.png
│   ├── kawaii-dark-kit.png
│   ├── glitch-ui-kit.png
│   └── terminal-theme-kit.png
├── README.md          # This file
└── LICENSE           # MIT License
```

## 🎯 Adding New UI Kits

To add a new UI kit to the portfolio:

### 1. Add Preview Image

- Create a preview image (recommended: 800x600px)
- Save as `./ui/your-kit-name.png`
- Use PNG format for best quality

### 2. Update HTML

Add a new kit card in the `kits-grid` section:

```html
<div class="kit-card">
  <div class="kit-image">
    <img
      src="./ui/your-kit-name.png"
      alt="Your Kit Name Preview"
      loading="lazy"
    />
    <div class="kit-badge new">New</div>
  </div>
  <div class="kit-content">
    <h3 class="kit-title">Your Kit Name</h3>
    <p class="kit-description">
      Brief description of your UI kit and its features.
    </p>
    <div class="kit-features">
      <span class="feature-tag">Feature 1</span>
      <span class="feature-tag">Feature 2</span>
      <span class="feature-tag">Feature 3</span>
    </div>
    <a
      href="https://gumroad.com/l/your-kit-slug"
      target="_blank"
      class="gumroad-button"
    >
      <span>Buy on Gumroad</span>
      <svg
        class="button-icon"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
      >
        <path d="M7 17L17 7M17 7H7M17 7V17" />
      </svg>
    </a>
  </div>
</div>
```

### 3. Badge Options

Available badge styles:

- `new` - Pink badge for new releases
- `popular` - Cyan badge for bestsellers
- `essential` - Green badge for must-have kits
- `kawaii` - Pink badge for cute designs
- `experimental` - Purple badge for cutting-edge
- `dev` - Yellow badge for developer tools

## 🚀 GitHub Pages Deployment

### Option 1: Direct Upload

1. Create a new repository on GitHub
2. Upload all files to the repository
3. Go to Settings → Pages
4. Select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Your site will be available at `https://yourusername.github.io/repository-name`

### Option 2: Using Git

```bash
# Initialize git repository
git init
git add .
git commit -m "Initial portfolio setup"

# Connect to GitHub repository
git remote add origin https://github.com/yourusername/repository-name.git
git branch -M main
git push -u origin main

# Enable GitHub Pages in repository settings
```

## 🎨 Customization

### Colors

The theme uses CSS variables for easy customization:

```css
:root {
  --text-accent: #06b6d4; /* Main accent color */
  --color-cyan-400: #22d3ee; /* Secondary accent */
  --bg-white-02: rgba(255, 255, 255, 0.02); /* Card backgrounds */
}
```

### Branding

Update the following elements:

- `brand-title`: Your brand name
- `brand-subtitle`: Your tagline
- `footer-text`: Copyright information
- `footer-links`: Social media links

## 📱 Mobile Optimization

The portfolio is fully responsive with:

- Flexible grid layouts
- Touch-friendly button sizes
- Optimized font scaling
- Mobile-first approach

## 🔧 Browser Support

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support
- Mobile browsers: Full support

## 📊 Performance

- **Lighthouse Score**: 95+ (Performance, Accessibility, Best Practices, SEO)
- **Load Time**: < 1 second on fast connections
- **File Size**: < 50KB total (excluding images)

## 🎁 What's Included

- ✅ Responsive HTML structure
- ✅ Complete CSS theme system
- ✅ 6 example UI kit showcases
- ✅ Gumroad integration ready
- ✅ GitHub Pages optimized
- ✅ SEO-friendly markup
- ✅ Accessible design
- ✅ No external dependencies

## 📝 License

MIT License - Feel free to use this for your own UI kit portfolio!

## 🤝 Support

For questions about customization or deployment:

- Check GitHub Issues for common problems
- Review the HTML/CSS for implementation details
- Test locally before deploying to GitHub Pages

---

**Built with 🖤 by KAWAIININJA**
