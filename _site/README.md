# How About No - Teenager Blog

A black-themed Jekyll blog website with a teenager-y aesthetic, featuring blog posts, art gallery, random stuff, and comments section.

## Features

- 🎨 **Black Theme**: Dark, modern design perfect for late-night blogging
- 📝 **Blog Posts**: Easy-to-write markdown blog posts
- 🖼️ **Art Gallery**: Dedicated space for showcasing artwork (coming soon)
- 💭 **Random Stuff**: Section for miscellaneous thoughts and content
- 💬 **Comments**: Integrated Cusdis commenting system
- 📱 **Responsive**: Works great on all devices
- ⚡ **Fast**: Optimized Jekyll site with minimal dependencies

## Setup Instructions

### Prerequisites
- Ruby (2.7 or higher)
- Bundler gem

### Installation

1. **Clone or download this repository**
   ```bash
   git clone <your-repo-url>
   cd howaboutno
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Set up Cusdis (for comments)**
   - Go to [cusdis.com](https://cusdis.com)
   - Create an account and get your App ID
   - Replace `YOUR_CUSDIS_APP_ID` in the following files:
     - `_layouts/post.html`
     - `comments.html`

4. **Run the development server**
   ```bash
   bundle exec jekyll serve
   ```

5. **Open your browser**
   - Navigate to `http://localhost:4000`

## Customization

### Adding New Blog Posts
1. Create a new markdown file in the `_posts` directory
2. Use the format: `YYYY-MM-DD-title.md`
3. Include the front matter:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: 2024-01-15 10:00:00 -0000
   author: "Your Name"
   tags: [tag1, tag2, tag3]
   excerpt: "Brief description of your post"
   ---
   ```

### Customizing the Theme
- Edit `assets/css/style.css` to modify colors, fonts, and styling
- Update `_config.yml` to change site settings
- Modify `_layouts/default.html` for structural changes

### Adding Content to Art and Stuff Pages
- Edit `art.html` and `stuff.html` to add your content
- Replace the "Coming Soon" sections with your actual content

## File Structure

```
howaboutno/
├── _config.yml          # Jekyll configuration
├── _layouts/            # HTML layouts
│   ├── default.html     # Main layout
│   └── post.html        # Blog post layout
├── _posts/              # Blog posts (markdown files)
├── assets/              # CSS, JS, and other assets
│   ├── css/
│   │   └── style.css    # Main stylesheet
│   └── js/
│       └── main.js      # JavaScript functionality
├── index.html           # Homepage
├── art.html             # Art gallery page
├── stuff.html           # Random stuff page
├── comments.html        # Comments page
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Deployment

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to repository Settings > Pages
3. Select "GitHub Actions" as the source
4. Create `.github/workflows/jekyll.yml`:
   ```yaml
   name: Jekyll site CI
   on:
     push:
       branches: [ main ]
     pull_request:
       branches: [ main ]
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
       - uses: actions/checkout@v3
       - uses: actions/setup-ruby@v3
         with:
           ruby-version: '3.1'
           bundler-cache: true
       - run: bundle exec jekyll build --destination ./_site
       - uses: actions/deploy-pages@v2
   ```

### Netlify
1. Connect your GitHub repository to Netlify
2. Set build command: `bundle exec jekyll build`
3. Set publish directory: `_site`

## Customization Tips

- **Colors**: Update CSS variables in `:root` section of `style.css`
- **Fonts**: Change the Google Fonts import in `_layouts/default.html`
- **Navigation**: Modify the nav links in `_layouts/default.html`
- **Social Links**: Add social media links to the footer

## Support

If you need help:
1. Check the [Jekyll documentation](https://jekyllrb.com/docs/)
2. Look at the [Cusdis documentation](https://cusdis.com/docs)
3. Create an issue in this repository

## License

This project is open source and available under the [MIT License](LICENSE).

---

Made with 💀 and caffeine by a teenager who stays up too late coding.
