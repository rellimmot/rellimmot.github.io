# Jekyll Site Modernization Documentation

This document details the modernization changes made to this Jekyll site (last updated: January 2026).

## Overview

This site was modernized from an outdated Jekyll 3.x configuration to current best practices while maintaining compatibility with GitHub Pages.

## Changes Made

### 1. Configuration Syntax Updates

**File**: `_config.yml`

**Deprecated → Modern**:
- `plugins_dir` → `plugins`
- `whitelist` → `allowlist`

**Added**:
- `jekyll-include-cache` plugin (required by Minimal Mistakes theme)

### 2. Analytics Removed

**File**: `_config.yml`

**What Changed**:
- Removed Google Universal Analytics (UA-107095408-1) - discontinued July 2023
- Simplified analytics configuration to disabled state
- Removed unused GA4 configuration placeholders

**Why**: The site doesn't require analytics tracking.

### 3. Comments System Migration

**File**: `_config.yml`

**What Changed**:
- Migrated from Facebook Comments to giscus (GitHub Discussions-based)
- Removed Staticman configuration (unused)

**Why**: Facebook deprecated their comments plugin in 2021. Giscus is modern, privacy-friendly, and GitHub-native.

### 4. Social Profiles Cleanup

**File**: `_config.yml`

**What Changed**:
- Removed empty social profile fields (20+ unused fields)
- Kept active profiles: email, GitHub, Facebook
- Added comment for future social profile additions

**Why**: Cleaner configuration, easier maintenance.

### 5. Dependency Updates

**File**: `Gemfile`

**What Changed**:
- Added explicit `webrick` dependency (required for Ruby 3.0+)
- Added `jekyll-include-cache` to plugins list
- Cleaned up and modernized Gemfile structure
- Ran `bundle update` to update all dependencies

**Result**: All dependencies updated to latest GitHub Pages compatible versions.

## Setup Instructions

### Prerequisites

- Ruby 3.0 or higher (tested with Ruby 3.2.0)
- Bundler gem installed

### Initial Setup

```bash
# Install dependencies
bundle install

# Build the site
bundle exec jekyll build

# Serve locally (http://localhost:4000)
bundle exec jekyll serve
```

### Setting Up giscus Comments

The site is configured for giscus comments, but requires manual setup:

1. **Enable GitHub Discussions**:
   - Go to https://github.com/rellimmot/rellimmot.github.io/settings
   - Scroll to "Features" section
   - Check "Discussions"

2. **Install giscus App**:
   - Visit https://github.com/apps/giscus
   - Click "Install"
   - Select your repository

3. **Configure giscus**:
   - Visit https://giscus.app
   - Enter your repository: `rellimmot/rellimmot.github.io`
   - Choose "Discussion title contains page pathname"
   - Select or create a "Comments" category
   - Copy the generated `repo_id` and `category_id`

4. **Update _config.yml**:
   ```yaml
   comments:
     provider: "giscus"
     giscus:
       repo_id: "R_xxx"  # Replace with your repo_id
       category_name: "Comments"
       category_id: "DIC_xxx"  # Replace with your category_id
       discussion_term: "pathname"
       reactions_enabled: '1'
       theme: "preferred_color_scheme"
   ```

5. **Enable Comments on Posts**:
   - Comments are controlled per-post via front matter
   - Edit post to add `comments: true` or update defaults in `_config.yml`

### Deployment

The site auto-deploys via GitHub Pages when you push to master:

```bash
git add .
git commit -m "Your commit message"
git push origin master
```

Visit https://www.rellimmot.com after 1-2 minutes to see changes.

## Current Configuration

### Jekyll & Theme Versions
- Jekyll: 3.10.0 (via github-pages gem v232)
- Theme: Minimal Mistakes 4.27.3
- Ruby: 3.2.0+
- Theme Skin: default

### Active Plugins
- jekyll-paginate
- jekyll-sitemap
- jekyll-gist
- jekyll-feed
- jemoji
- jekyll-include-cache

### Features
- Pagination: 5 posts per page
- Collections: Portfolio
- Archives: Liquid-based (GitHub Pages compatible)
- Markdown: Kramdown with Rouge syntax highlighting

## Troubleshooting

### Build Errors

**"cannot load such file -- webrick"**
```bash
bundle add webrick
```

**"Liquid Exception: Included file '_includes/xxx' not found"**
- Ensure `jekyll-include-cache` is in both `plugins` and `allowlist` sections of `_config.yml`
- Run `bundle install` to ensure the plugin is installed

### Local Preview Issues

**Changes not appearing**:
- Restart Jekyll server (it doesn't auto-reload `_config.yml`)
- Clear browser cache
- Check `exclude` list in `_config.yml`

**Port 4000 already in use**:
```bash
# Kill existing process
pkill -f jekyll

# Or use different port
bundle exec jekyll serve --port 4001
```

### Deployment Issues

**Site not updating on GitHub Pages**:
- Check GitHub Actions tab for build errors
- Verify you pushed to the correct branch (master)
- GitHub Pages can take 1-5 minutes to rebuild

**404 errors on deployed site**:
- Check `url` and `baseurl` in `_config.yml`
- Verify file paths are correct (case-sensitive on GitHub Pages)

### Comments Not Showing

**giscus comments not appearing**:
1. Verify GitHub Discussions is enabled
2. Check `repo_id` and `category_id` are correct
3. Ensure `comments: true` in post front matter
4. Check browser console for JavaScript errors
5. Verify giscus app is installed for the repository

## File Structure

```
.
├── _config.yml          # Main configuration
├── Gemfile              # Ruby dependencies
├── Gemfile.lock         # Locked dependency versions
├── _posts/              # Blog posts
├── _pages/              # Static pages
├── _portfolio/          # Portfolio items
├── assets/              # CSS, JS, images
│   ├── images/
│   └── js/
├── _includes/           # Reusable HTML components
├── _layouts/            # Page templates
└── _sass/               # Sass stylesheets
```

## Future Considerations

### Optional Enhancements

1. **Migrate to Jekyll 4.x**:
   - Requires GitHub Actions workflow (not supported by default GitHub Pages)
   - Provides performance improvements and new features
   - More complex deployment setup

2. **Asset Pipeline Modernization**:
   - Current: jQuery 3.2.1 in assets/js/vendor
   - Theme includes newer jQuery 3.6.0
   - Consider removing custom jQuery copy

3. **Theme Updates**:
   - Current: Minimal Mistakes 4.27.3
   - Monitor for updates: https://github.com/mmistakes/minimal-mistakes
   - Test updates in development before deploying

4. **Social Profiles**:
   - Add Twitter/X, LinkedIn, or other platforms as needed
   - Edit `author` section in `_config.yml`

### Maintenance Schedule

- **Quarterly**: Run `bundle update` and test build
- **Annually**: Review theme updates and deprecated features
- **As Needed**: Update social profiles, add new features

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Minimal Mistakes Documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [giscus Documentation](https://giscus.app)
- [Kramdown Syntax](https://kramdown.gettalong.org/syntax.html)

## Support

For issues or questions:
- Jekyll: https://talk.jekyllrb.com
- Minimal Mistakes: https://github.com/mmistakes/minimal-mistakes/discussions
- GitHub Pages: https://github.com/orgs/community/discussions/categories/pages

## Change Log

### 2026-01-31 - Major Modernization
- Updated deprecated config syntax (plugins_dir, whitelist)
- Removed Google Universal Analytics
- Migrated to giscus comments system
- Cleaned up social profiles
- Updated all dependencies via bundle update
- Added documentation (this file)
- Updated README.md

### Historical
- Site originally created with Jekyll 3.x
- Theme: Minimal Mistakes
- Last major update before modernization: Unknown
