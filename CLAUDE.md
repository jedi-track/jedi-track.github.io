# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based website using the Minimal Mistakes theme, specifically adapted as a template for citizen science environmental monitoring projects. The site showcases the "jedi-track" group as an example of how to document environmental actions and data collection campaigns.

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Serve the site locally (with auto-reload)
bundle exec jekyll serve

# Build the site for production
bundle exec jekyll build
```

### GitHub Pages
The site is configured to use GitHub Pages with the `github-pages` gem, which automatically handles deployment when pushed to the main branch.

## Site Architecture - Citizen Science Template

### Core Configuration
- `_config.yml`: Configured for "jedi-track - Science Citoyenne" with environmental focus
- `Gemfile`: Standard Jekyll dependencies for GitHub Pages
- Navigation adapted for citizen science activities

### Page Structure
- **Homepage (`index.html`)**: Team presentation, mission, study area, and latest news
- **Campaigns (`_pages/campagnes.md`)**: Documentation of data collection campaigns, methodology, and results
- **Local Impact (`_pages/impact.md`)**: Problems identified, solutions proposed, and actions with decision-makers
- **Join Us (`_pages/rejoignez-nous.md`)**: How to participate, training calendar, and contact information

### Content Strategy
The site demonstrates how to:
- Present environmental monitoring data professionally
- Document scientific methodologies for citizen science
- Show real impact on local policy decisions
- Engage community participation in environmental monitoring

### Sample Content Included
- **4 blog posts** covering different aspects of citizen science campaigns
- **Realistic data** (air quality, water quality, biodiversity monitoring)
- **Training and methodology** documentation
- **Policy engagement** examples and results

### Theme Integration
Uses `mmistakes/minimal-mistakes` with:
- Environmental branding (jedi-track theme)
- Professional presentation suitable for municipal presentations
- Clear navigation for different stakeholder groups (citizens, officials, scientists)
- Contact information and social media integration

### Jekyll Plugins
- `jekyll-paginate`: Blog post pagination
- `jekyll-sitemap`: SEO optimization
- `jekyll-feed`: RSS feed for updates
- `jemoji`: Emoji support for accessibility and engagement
- `jekyll-algolia`: Search functionality (configured but may need API key)
- `jekyll-include-cache`: Performance optimization

## Site Structure and Navigation

### Navigation Configuration
- Main navigation is defined in `_data/navigation.yml`
- Key sections: Accueil (/), Nos campagnes (/campagnes/), Impact local (/impact/), Rejoignez-nous (/rejoignez-nous/), Actualités (/actualites/)

### Page Types and Permalinks
- **Static pages**: Located in `_pages/` with custom permalinks defined in frontmatter
- **Campaign pages**: Use pattern `/campagnes/{campaign-name}/` for consistency
- **Blog posts**: Located in `_posts/` with date-based URLs, accessible via `/actualites/`

### Content Organization
- **Team presentation**: README.md serves as the main team page with member profiles
- **Campaign documentation**: Individual pages under `/campagnes/` with embedded images and interactive content
- **Resource management**: PDFs and downloadable content should be placed in `/assets/docs/`
- **Images**: Campaign images stored in `/Images/` directory, referenced with `?raw=true` parameter

### Link Consistency Guidelines
- Always use `{{ '/path/' | relative_url }}` for internal links
- Campaign links must match the permalink defined in the target page
- Ensure navigation URLs correspond to existing pages or redirect properly

## Development Guidelines

### Content Updates
- ALWAYS prefer editing existing files over creating new ones
- When adding new campaigns, follow the established pattern: create page in `_pages/` with `/campagnes/{name}/` permalink, then add link in `campagnes.md`
- Maintain link consistency - verify all internal links work after making changes
- Use Jekyll's `relative_url` filter for all internal links to ensure proper URL generation

### Image and Asset Management
- Campaign images should be stored in `/Images/` directory
- Use `?raw=true` parameter when referencing images from GitHub
- For downloadable resources (PDFs), use `/assets/docs/` directory structure
- Always provide meaningful alt text for images for accessibility

### Multi-language Considerations
- Site is currently in French - maintain consistency in language use
- Date formats should follow French conventions (dd/mm/yyyy)
- Navigation and page titles should remain in French unless specifically requested otherwise

## Template Usage

This template serves as a starting point for environmental groups wanting to:
1. Document their citizen science activities professionally
2. Present data and results to local authorities
3. Recruit new volunteers and participants
4. Share methodologies with other citizen science groups

### Key Customization Points
- Update site title, description, and contact information in `_config.yml`
- Replace "jedi-track" branding with your group's identity in both config and content
- Adapt team presentation in README.md with actual member information
- Modify campaign pages in `_pages/` to reflect your group's specific activities
- Update navigation structure in `_data/navigation.yml` based on your focus areas
- Replace sample campaign content with real data and methodologies
- Ensure all PDF links in resource pages point to actual files or are marked as "coming soon"