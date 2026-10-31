# Ruiyang Zhang — Personal Homepage

Source code for my personal academic homepage, built on the
[Minimal Light](https://github.com/yaoyao-liu/minimal-light) Jekyll theme
and hosted via GitHub Pages.

## Structure

```
.
├── _config.yml              # site-wide settings: name, affiliation, links, etc.
├── index.md                 # page content: About Me, News, Education, ...
├── _data/
│   ├── publications.yml     # publication entries (edit this to add a paper)
│   └── internships.yml      # internship entries (edit this to add one)
├── _includes/
│   ├── publications.md      # renders _data/publications.yml
│   ├── internship.md        # renders _data/internships.yml
│   └── services.md          # Academic Service section (edited directly)
├── _layouts/
│   └── homepage.html        # page shell (header, icons, footer) — from theme
├── _sass/, assets/          # theme styles, fonts, scripts — from theme
└── assets/files/            # CV PDF
```

## Updating content

- **New publication:** add an entry to the top of `_data/publications.yml`
  (a blank template is commented at the top of that file).
- **New internship:** add an entry to the top of `_data/internships.yml`
  (same pattern).
- **Everything else** (About Me, News, Education, Honor and Award, Work
  Experience, Academic Service, Teaching, Interest): edit the
  corresponding section directly in `index.md` (or `_includes/services.md`
  for Academic Service).

## Theme

This site uses the [Minimal Light](https://github.com/yaoyao-liu/minimal-light)
theme by Yaoyao Liu, used here under its original license (see `LICENSE`).
