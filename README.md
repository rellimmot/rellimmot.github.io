# [relliMmoT](https://www.rellimmot.com/)

Personal website and project log built with Jekyll and hosted on GitHub Pages.

## Quick Start

### Prerequisites

- Ruby 3.0 or higher (tested with Ruby 3.2.0)
- Bundler: `gem install bundler`

### Local Development

```bash
# Install dependencies
bundle install

# Build the site
bundle exec jekyll build

# Serve locally at http://localhost:4000
bundle exec jekyll serve

# Serve with live reload
bundle exec jekyll serve --livereload
```

### Deployment

The site automatically deploys to https://www.rellimmot.com when you push to the master branch.

```bash
git add .
git commit -m "Your changes"
git push origin master
```

GitHub Pages will rebuild the site in 1-2 minutes.

## Tech Stack

- **Static Site Generator**: Jekyll 3.10.0
- **Theme**: [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) 4.27.3
- **Hosting**: GitHub Pages
- **Comments**: giscus (GitHub Discussions-based)

## Project Structure

```
.
├── _config.yml          # Main configuration
├── _posts/              # Blog posts
├── _pages/              # Static pages (About, Archive, etc.)
├── _portfolio/          # Portfolio items
├── assets/              # Images, CSS, JavaScript
├── Gemfile              # Ruby dependencies
└── MODERNIZATION.md     # Detailed modernization notes
```

## Documentation

- [MODERNIZATION.md](MODERNIZATION.md) - Detailed documentation of recent updates, setup instructions, and troubleshooting

## Troubleshooting

### Common Issues

**"cannot load such file -- webrick"**
```bash
bundle add webrick
```

**Changes to `_config.yml` not showing**
- Restart the Jekyll server (config changes require restart)

**Port 4000 already in use**
```bash
pkill -f jekyll
# Or use a different port
bundle exec jekyll serve --port 4001
```

See [MODERNIZATION.md](MODERNIZATION.md) for more troubleshooting help.

## License

Content is copyright Thomas George Miller. Theme is MIT licensed.
