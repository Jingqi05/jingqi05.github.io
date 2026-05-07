# 李景奇 — Personal Homepage

Personal website for **李景奇 (Jingqi Li)**, undergraduate student in Information Security at Tianjin Sino-German University of Applied Sciences. Research focuses on IoT security, embedded cryptography, and vehicular network authentication.

## Site Structure

| Path | Purpose |
|------|---------|
| `_data/profile.yml` | Personal info, bio, education, experience, awards |
| `_data/display.yml` | Show/hide homepage sections |
| `_data/navigation.yml` | Navbar pages |
| `_data/authors.yml` | Collaborator names and profile links |
| `_publications/YEAR/` | Add publication entries (Markdown) |
| `_projects/YEAR/` | Add project entries (Markdown) |
| `_news/` | Add news/announcements (Markdown) |
| `assets/images/photos/` | Profile photo |
| `assets/images/covers/` | Cover images for publications and projects |
| `assets/css/global.css` | Custom styles |
| `assets/CV/cv.pdf` | CV file |

## Local Preview

```bash
cd jingqi.github.io-main
bundle install
bundle exec jekyll serve
```

Then open http://127.0.0.1:4000/

## Template

Based on [academic-homepage](https://github.com/luost26/academic-homepage) by luost26.
