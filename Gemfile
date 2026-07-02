source "https://rubygems.org"

# This pins your local build to the exact same Jekyll/plugin versions
# GitHub Pages uses on their servers, so what you see locally is what
# ships. Run `bundle install` once, then `bundle exec jekyll serve`.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Windows/JRuby support (harmless to leave in on other platforms)
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]
