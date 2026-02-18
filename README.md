# Codestitch + CloudCannon Starter Kit

A fork of the [Codestitch Intermediate Website Kit (Less)](https://github.com/CodeStitchOfficial/Intermediate-Website-Kit-LESS) converted to use [CloudCannon](https://cloudcannon.com/) as the CMS instead of Decap CMS. Built with Eleventy (11ty), Nunjucks templating, and Less preprocessing.

This project is a companion to the blog post: **[CloudCannon Review: The Best Visual CMS for Static Sites](https://vikboyechko.com/blog/cloudcannon-visual-cms-static-sites/)**

## What's Different from the Original Kit

- **CloudCannon CMS** replaces Decap CMS for content management
- **Visual editing** enabled on pages via `data-editable` attributes
- **CloudCannon config** (`cloudcannon.config.yml`) defines collections, build settings, and editor behavior
- Blog posts are managed through CloudCannon's blog editor instead of Decap's markdown editor
- Everything else remains the same: Eleventy, Nunjucks, Less, and the Codestitch component library

## Quick Start

1. Fork or clone this repository
2. Run `npm install`
3. Run `npm start` to start the dev server
4. To use with CloudCannon, [create a site](https://cloudcannon.com/) and connect this repo

## How Visual Editing Works

CloudCannon visual editing is enabled through data attributes on HTML elements:

- `data-editable="source"` - Edit text directly in the source HTML
- `data-editable="text"` - Edit text stored in front matter
- `data-editable="image"` - Swap images stored in front matter

See the [blog post](https://vikboyechko.com/blog/cloudcannon-visual-cms-static-sites/) for a full walkthrough with code examples.

## Project Structure

```
src/
├── _data/           # Global data (client.js)
├── _includes/
│   ├── components/  # Header, footer
│   └── layouts/     # base.html, post.html
├── admin/           # Decap CMS config (unused with CloudCannon)
├── assets/          # CSS, JS, images, fonts, Less files
├── config/          # Eleventy plugin configs
├── content/
│   ├── blog/        # Markdown blog posts
│   └── pages/       # HTML pages
├── index.html       # Homepage
├── robots.html      # Generates robots.txt
└── sitemap.html     # Generates sitemap.xml
cloudcannon.config.yml  # CloudCannon configuration
```

## Hosting Options

- **CloudCannon hosted** - CloudCannon builds and hosts the site (recommended for full visual editing support)
- **Headless mode** - CloudCannon as CMS only, with Netlify or another service handling builds and hosting

## Credits

- [Codestitch](https://www.codestitch.app/) for the original website kit and component library
- [CloudCannon](https://cloudcannon.com/) for the visual CMS platform
- [Eleventy](https://www.11ty.dev/) for the static site generator
