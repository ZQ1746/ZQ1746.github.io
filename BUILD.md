# Building the Personal Website

This website is built using Jekyll and the Academic Pages template.

## Prerequisites

- Ruby 3.2+
- Bundler

## Quick Start

### Option 1: Local Build (Recommended)

1. Install bundler if not already installed:
   ```bash
   gem install --user-install bundler
   export PATH="$HOME/.local/share/gem/ruby/3.2.0/bin:$PATH"
   ```

2. Configure bundle to install gems locally:
   ```bash
   bundle config set --local path 'vendor/bundle'
   ```

3. Install dependencies:
   ```bash
   bundle install
   ```

4. Build the site:
   ```bash
   bundle exec jekyll build
   ```

5. Serve the site locally:
   ```bash
   bundle exec jekyll serve -H localhost --port 4000
   ```

   The site will be available at http://localhost:4000

### Option 2: Using Docker

If you prefer using Docker:

1. Build and run with Docker Compose:
   ```bash
   chmod -R 777 .
   docker compose up
   ```

   The site will be available at http://localhost:4000

## Deployment

This site is designed to be deployed on GitHub Pages. Simply push your changes to the `master` branch, and GitHub Pages will automatically build and deploy your site.

## Customization

To customize your site:

1. Edit `_config.yml` to update site-wide settings (name, bio, social links, etc.)
2. Update `_data/navigation.yml` to modify the top navigation menu
3. Add your content in the `_pages`, `_posts`, `_publications`, `_talks`, etc. directories
4. Replace images in the `images` folder with your own

## Build Verification

The site has been successfully built and tested. All pages render correctly:
- Homepage (about page)
- Publications
- Talks
- Teaching
- Portfolio
- Blog Posts
- CV

## Troubleshooting

If you encounter permission issues when installing gems:
1. Use `--user-install` flag: `gem install --user-install bundler`
2. Configure bundle to install locally: `bundle config set --local path 'vendor/bundle'`

If Jekyll server doesn't start:
1. Make sure port 4000 is not already in use
2. Check that all dependencies are installed: `bundle install`
