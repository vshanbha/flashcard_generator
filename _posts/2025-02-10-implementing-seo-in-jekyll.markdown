---
layout: post
title:  "Implementing SEO in Jekyll: Quick Start"
date:   2025-02-10 19:29:48 UTC
author: vshanbha
categories: jekyll seo update
description: "A comprehensive guide to implementing SEO in Jekyll using jekyll-seo-tag and jekyll-sitemap plugins. Learn how to optimize your Jekyll site for search engines."
---

Search Engine Optimization (SEO) is crucial for ensuring your Jekyll site ranks well in search results. This guide walks through implementing SEO using Jekyll's built-in capabilities and popular plugins.

## Prerequisites

This Jekyll site already has the necessary plugins installed in `_config.yml` and can be used as a quick start template to [create a new Blog](https://github.com/new?template_name=github_jekyll_pages_demo&template_owner=vshanbha):
```yaml
plugins:
  - jekyll-seo-tag
  - jekyll-sitemap
```

## Implementation Steps
### 1. SEO Configuration
Add or update the following settings in your `_config.yml`:

```yaml
# SEO Settings
title: Your awesome title
logo: "/assets/logos/logo.svg"
description: >- # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
author: vshanbha
lang: en
social:
  name: Your Name
  links:
    - https://github.com/yourhandle # if applicable
    - https://twitter.com/yourhandle # if applicable
    - https://linkedin.com/in/yourprofile # if applicable
```
### 2. Creating robots.txt
Create a `robots.txt` file in your site's root directory with content like below:

```txt
User-agent: *
Allow: /
Sitemap: https://vshanbha.github.io/github_jekyll_pages_demo/sitemap.xml
```
The sitemap.xml is automatically genearted by the Jekyll build, just ensure that the Domain name (`vshanbha.github.io`) and project root (`github_jekyll_pages_demo`) are correctly modified to suit your own site deployment location.

### 3. More Information about SEO plugin
This template already has the SEO Tag and Sitemap plugins installed so just the above two changes should be sufficient. If you need to do more with SEO go through the relevant documentation of the Jekyll SEO tag and Sitemap plguins. Also the theme in use by this site has many useful features. Check the [Readme]({% link README.md %}) page for details.
- [Jekyll SEO Tag Documentation](https://github.com/jekyll/jekyll-seo-tag)
- [Jekyll Sitemap Documentation](https://github.com/jekyll/jekyll-sitemap)

## Verification Steps
After implementation, verify your SEO setup:

- Meta Tags: View your page source to ensure meta tags are generated correctly
- Sitemap: Verify sitemap.xml is accessible at /sitemap.xml
- Testing: Use Google's Rich Results Test tool to validate your implementation
### Benefits
This implementation provides:

- Proper meta tags for search engine optimization
- Social sharing meta tags (Open Graph)
- Automatically generated XML sitemap
- Crawler guidance through robots.txt
### Best Practices
- Titles: Keep page titles under 60 characters
- Descriptions: Write meta descriptions between 150-160 characters
- Images: Always include relevant alt text for images
- URLs: Use clean, descriptive URLs for pages and posts

### Monitoring
After implementation, monitor your site's performance using:

- Google Search Console
- Google Analytics
- Bing Webmaster Tools

### Troubleshooting
If meta tags aren't generating:

Verify plugins are properly installed
Check for proper Jekyll build output
Ensure `{% raw %}{% seo %}{% endraw %}` tag is placed correctly
Clear Jekyll cache and rebuild

## Conclusion
With these implementations, your Jekyll site is now optimized for search engines. Remember to regularly update your content and monitor your SEO performance for best results.