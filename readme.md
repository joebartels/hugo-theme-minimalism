## Hugo Theme: Minimalism

Intended to be very simple, easy to look at, while functional at the same time.

### Preview
![preview](https://github.com/joebartels/hugo-theme-minimalism/blob/master/wiki-assets/list-preview-1.gif?raw=true)


### Disclaimer
This theme has some rough edges that I will smooth out over time. Some known TODOs are:
- [ ] fix google analytics support
- [ ] fix disqus support
- [ ] fix gitub, npm, and linkedin links (need better design)
- [ ] needs some minor changes for better mobile support

### 3rd Party Support
- Google Analytics support
- Disqus support
- Highlight.js

### Installation
git clone
```bash
cd <your-project>/themes
git clone --depth 1 https://github.com/joebartels/hugo-theme-minimalism
```

Specify theme
From inside your config file (config.toml, config.json, or config.yml)
```
# config.toml
theme = "hugo-theme-minos"
```

### Configuration
Specifying your github, linkedin, and npm links:
```toml
[params]
  githubUrl = "https://github.com/georgeharrison"
  linkedinUrl = "https://linkedin.com/georgeharrison"
  npmUrl = "https://npmjs.org/georgeharrison"
```

Specifying the items in the main navigation menu:
```toml
[[menu.main]]
  name = "Articles"
  identifier = "articles"
  url = "/article/"
  weight = 90

[[menu.main]]
  name = "About"
  identifier = "about"
  url = "/about/"
  weight = 100
```

### Customization
Each js library and stylesheet that gets loaded lives inside its own partial so if you want to omit a library or customize the tag in any way it's very easy to do. 

For example if you don't want to use highlight.js, place a blank file here: __layouts/partials/foot/js_highlightjs.html__  

Or if you want to use a different CSS Reset, create a partial here: __layouts/partials/head/css_reset.html__  

This pattern exists for all the `<head></head>` includes and those above the `</body>` tag.
