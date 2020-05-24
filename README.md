[![Build Status][build-img]][build-url]
[![Demo][demo-img]][demo-url]

# Hallo

> A single-page theme to introduce yourself.
>
> [Zola][zola] port of [hallo-hugo][hallo-hugo].

![Screenshot](screenshot.png)

## Original

This is a port of the original [hallo-hugo][hallo-hugo] theme for Hugo ([License][upstream-license]).

## Installation

The easiest way to install this theme is to either clone it ...

```
git clone https://github.com/janbaudisch/zola-hallo.git themes/hallo
```

... or to use it as a submodule.

```
git submodule add https://github.com/janbaudisch/zola-hallo.git themes/hallo
```

Either way, you will have to enable the theme in your `config.toml`.

```toml
theme = "hallo"
```

### Introduction

The introduction text is made in `content/_index.md`.

```markdown
+++
+++
Hallo is a single-page theme to introduce yourself. Add a portrait, an introduction, several links, and you're set. Create a partial called introduction.html on your own site to replace this standard introduction. Create a file called portrait.jpg in static/images to replace the standard portrait.
```

## Options

Example `config.toml`

```toml
base_url = "https://zola-hallo.janbaudisch.dev"
title = "Hallo"

compile_sass = true

highlight_code = false

build_search_index = false

[extra]
greeting = "Hello!"

iam = "I am"

links = [
    { title = "E-Mail", url = "mailto:mail@example.org", iconset = "fas", icon = "envelope" },
    { title = "GitHub", url = "https://github.com", icon = "github" },
    { title = "Twitter", url = "https://twitter.com", icon = "twitter" }
]

[extra.author]
name = "Hallo"

[extra.theme]
background = "#6FCDBD"
foreground = "#FFF"
hover = "#333"
```

### Author

The given name will be used for the 'I am ...' text.

Default: `Hallo`

```toml
[extra.author]
name = "Hallo"
```

### Greeting

The string will be used as a greeting.

Default: `Hello!`

```toml
[extra]
greeting = "Hello!"
```

### `iam`

This variable defines the `I am` text, which you may want to swap out for another language.

Default: `I am`

```toml
[extra]
iam = "I am"
```

### Links

Links show up below the introduction. They are styled with [Font Awesome][fontawesome], you may optionally choose the iconset (default is [brands][fontawesome-brands]).

```toml
[extra]
links = [
    { title = "E-Mail", url = "mailto:mail@example.org", iconset = "fas", icon = "envelope" },
    { title = "GitHub", url = "https://github.com", icon = "github" },
    { title = "Twitter", url = "https://twitter.com", icon = "twitter" }
]
```

### Theme

Change the colors used.

```toml
[extra.theme]
background = "#6FCDBD"
foreground = "#FFF" # text and portrait border
hover = "#333" # link hover
```

[build-img]: https://travis-ci.com/janbaudisch/zola-hallo.svg?branch=master
[build-url]: https://travis-ci.com/janbaudisch/zola-hallo
[demo-img]: https://img.shields.io/badge/demo-live-green.svg
[demo-url]: https://zola-hallo.janbaudisch.dev
[zola]: https://www.getzola.org
[hallo-hugo]: https://github.com/EmielH/hallo-hugo
[fontawesome]: https://fontawesome.com
[fontawesome-brands]: https://fontawesome.com/icons?d=gallery&s=brands&m=free
[upstream-license]: https://github.com/janbaudisch/zola-hallo/blob/master/upstream/LICENSE
