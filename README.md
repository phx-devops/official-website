# Phoenix DevOps Official Website

[![Hugo](https://img.shields.io/badge/Hugo-0.157.0-blue.svg)](https://gohugo.io)
[![Node.js](https://img.shields.io/badge/Node.js-24.14.0-green.svg)](https://nodejs.org)
[![Go](https://img.shields.io/badge/Go-1.26.1-blue.svg)](https://golang.org)
[![Cloudflare Workers](https://img.shields.io/badge/Cloudflare-Workers-orange.svg)](https://workers.cloudflare.com)

The official website for Phoenix DevOps, a leading provider of DevOps, AI operations, and cloud infrastructure services. Built with Hugo and deployed on Cloudflare Workers.

## 🌟 About Phoenix DevOps

[Phoenix DevOps](https://www.phxdevops.com) specializes in:
- **DevOps Consulting & Implementation**
- **AI Infrastructure & LLM Operations**
- **Cloud Architecture & Migration**
- **Security-First Development (DevSecOps)**
- **CI/CD Pipeline Design**
- **Monitoring & Observability Solutions**
- **Training & Certification Programs**

## 🛠️ Tech Stack

- **Static Site Generator**: [Hugo](https://gohugo.io) v0.157.0
- **Theme**: [Universal Theme](https://themes.gohugo.io/hugo-universal-theme/)
- **Deployment**: [Cloudflare Workers](https://workers.cloudflare.com)
- **Analytics**: Google Analytics (G-W108NZ6XSN)
- **Build Tools**: Node.js 24.14.0, Go 1.26.1, Dart Sass 1.98.0

## 📁 Project Structure

```
official-website/
├── archetypes/          # Content templates
├── assets/             # SCSS, JS, and other assets
├── content/            # Site content (Markdown files)
│   ├── about/          # About pages
│   ├── blog/           # Blog posts and articles
│   ├── contact.md      # Contact information
│   ├── faq.md          # Frequently asked questions
│   ├── marketing/      # Marketing pages
│   ├── services/       # Service offerings
│   └── training/       # Training programs
├── data/               # YAML data files for dynamic content
├── i18n/               # Internationalization files
├── layouts/            # Custom Hugo layouts
├── public/             # Generated static files (auto-generated)
├── static/             # Static assets (images, CSS, JS)
├── themes/             # Hugo themes
├── build.sh            # Build script for Cloudflare deployment
├── config.toml         # Hugo configuration
├── hugo.toml           # Additional Hugo configuration
└── wrangler.toml       # Cloudflare Workers configuration
```

## 🚀 Quick Start

### Prerequisites

- [Hugo](https://gohugo.io/getting-started/installing/) v0.157.0 or later
- [Node.js](https://nodejs.org/) v24.14.0 or later
- [Go](https://golang.org/dl/) v1.26.1 or later
- [Wrangler CLI](https://developers.cloudflare.com/workers/wrangler/install-and-update/) (for deployment)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/phx-devops/official-website.git
   cd official-website
   ```

2. **Install dependencies**
   ```bash
   # The build script handles most dependencies
   chmod +x build.sh
   ```

3. **Start the development server**
   ```bash
   hugo server -D
   ```

4. **Open your browser**
   Navigate to `http://localhost:1313`

### Building for Production

```bash
# Build the site
hugo --minify

# Or use the build script (used by Cloudflare)
./build.sh
```

## 📝 Content Management

### Adding Blog Posts

1. Create a new Markdown file in `content/blog/`:
   ```bash
   hugo new blog/your-post-title.md
   ```

2. Edit the generated file with your content, front matter, and metadata.

### Content Front Matter

Example front matter for blog posts:
```yaml
---
title: "Your Post Title"
date: 2026-03-30
description: "Brief description of the post"
author: "phx-devops"
categories: ["DevOps", "AI"]
weight: 10
---
```

### Data Files

Dynamic content is managed through YAML files in the `data/` directory:
- `carousel/` - Homepage carousel items
- `clients/` - Client testimonials
- `features/` - Service features
- `testimonials/` - Customer testimonials

## 🚢 Deployment

The site is automatically deployed to Cloudflare Workers using GitHub Actions or manual deployment:

```bash
# Deploy to Cloudflare Workers
wrangler deploy
```

### Build Configuration

- **Build Command**: `./build.sh`
- **Assets Directory**: `./public`
- **404 Handling**: Custom 404 page

## 🔧 Development Workflow

1. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Update content in `content/`
   - Modify layouts in `layouts/`
   - Add assets in `assets/`

3. **Test locally**
   ```bash
   hugo server -D
   ```

4. **Build and preview**
   ```bash
   hugo --minify
   ```

5. **Commit and push**
   ```bash
   git add .
   git commit -m "Add your changes"
   git push origin feature/your-feature-name
   ```

6. **Create a pull request**

## 📊 Analytics & Monitoring

- **Google Analytics**: Integrated with tracking ID `G-W108NZ6XSN`
- **Performance**: Monitored via Cloudflare Analytics
- **SEO**: Optimized with meta tags, structured data, and sitemaps

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request with a clear description

### Content Guidelines

- Use clear, concise language
- Include relevant code examples where applicable
- Add proper front matter to all content files
- Optimize images for web (under 500KB)
- Follow the existing content structure

## 📞 Contact & Support

- **Website**: [https://www.phxdevops.com](https://www.phxdevops.com)
- **Email**: [support@phxdevops.com](mailto:support@phxdevops.com)
- **GitHub Issues**: For technical issues and feature requests

## 📄 License

This project is proprietary. All rights reserved by Phoenix DevOps.

## 🙏 Acknowledgments

- [Hugo Universal Theme](https://themes.gohugo.io/hugo-universal-theme/) - The theme powering this site
- [Cloudflare Workers](https://workers.cloudflare.com) - Hosting and deployment platform
- [Hugo](https://gohugo.io) - Static site generator