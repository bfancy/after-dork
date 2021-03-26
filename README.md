# after-dork
a robust, elegant d(a|o)rk theme for Zola.

![after-dork screenshot](https://github.com/getzola/after-dark/blob/master/screenshot.png?raw=true)

## contents

- [installation](#installation)
- [options](#options)
  - [top menu](#top-menu)
  - [title](#title)

## installation
first download this theme to your `themes` directory:

```bash
cd themes
git clone https://github.com/bfancy/after-dork.git
```
and then enable it in your `config.toml`:

```toml
theme = "after-dork"
```

this theme requires your index section (`content/_index.md`) to be paginated to work:

```toml
paginate_by = 5
```

the posts should therefore be in directly under the `content` folder.

the theme requires tags and categories taxonomies to be enabled in your `config.toml`:

```toml
taxonomies = [
    # you can enable/disable RSS
    {name = "categories", feed = true},
    {name = "tags", feed = true},
]
```

if you want to paginate taxonomies pages, you will need to overwrite the templates
as it only works for non-paginated taxonomies by default.


## options

### top-menu
set a field in `extra` with a key of `after_dork_menu`:

```toml
after_dork_menu = [
    {url = "$BASE_URL", name = "home"},
    {url = "$BASE_URL/categories", name = "categories"},
    {url = "$BASE_URL/tags", name = "tags"},
    {url = "https://duckduckgo.com", name = "DDG"},
]
```

if you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

### title
the site title is shown on the homepage. As it might be different from the `<title>`
element that the `title` field in the config represents, you can set the `after_dork_title`
instead.

## original
this template is based on the Zola template https://github.com/getzola/after-dark
