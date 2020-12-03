[![Build Status](https://travis-ci.org/VersBinarii/hermit_zola.svg?branch=master)](https://travis-ci.org/VersBinarii/hermit_zola)

# Hermit 

> this is a port of the [Hermit theme](https://github.com/Track3/hermit) for [Zola](https://www.getzola.org/)

> this is a fork of https://github.com/VersBinarii/hermit_zola

Hermit is a  minimal & fast Zola theme for bloggers.

![screenshot](hermit_zola.png)

[View demo](https://pawndev-hermit-zola.netlify.app/)

## Installation

First download the theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/pawndev/hermit_zola
```
and then enable it in your `config.toml`:

```toml
theme = "hermit_zola"
```

## Configuration

```toml
[extra]
home_subtitle = "Some profound and catchy statement"

footer_copyright = ' &#183; <a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank" rel="noopener">CC BY-NC 4.0</a>'

hermit_menu = [
    { link = "/posts", name = "Posts" },
    { link = "/about", name = "About" }
]

hermit_social = [
    { name = "twitter", link = "https://twitter.com" },
    { name = "github", link = "https://github.com" },
    { name = "email", link = "mailto:author@domain.com" }
]

[extra.author]
name = "The Author"
email = "author@domain.com"

[extra.google_analytics]
enable = false
id = "UA-4XXXXXXX-X"
```

### Table of content
Table of content can be enabled by adding 
```
[extra]
toc=true
```
to the page front matter. Icon will then appear above the page title that will
allow to toggle the ToC.

### Changes from the original

#### highlightjs

You can enable highlightjs to replace the built-in syntax high lighting.
But, make sure to disable the built-in syntax highlighting.
In your config.toml


```toml
highlight_code = false

[extra.highlightjs]
enable = true
```

You can change the highlightjs theme with this:

```toml
highlight_code = false

[extra.highlightjs]
enable = false
theme = "vs2015"
```

For all themes, see: https://unpkg.com/browse/highlightjs-badge@0.1.9/highlightjs/styles/

#### clipboard

You can enable the display of a button to copy the content of a pre>code tag.

##### Custom buttom

This will display a "copy" button on the bottom of each pre tag.
Only when highlightjs is disable.

```toml
highlight_code = true
       
[extra.highlightjs]
enable = false
```

##### With highlightjs

Enable it in the highlightjs config block.

```toml
highlight_code = false

[extra.highlightjs]
enable = true
clipboard = true
```

#### Jupyter notebook

You can display a jupyter notebook from a ipynb file. Only if you have enable highlightjs

```toml
highlight_code = false

[extra.highlightjs]
enable = true
clipboard = true
theme = "vs2015"
notebook = true
```

#### Featured image

You can add a background image when you set an extra variable in a page section:

```toml
+++
title="Test bg image"
date=2020-10-14
draft=false

[taxonomies]
tags=["test", "image"]

[extra]
featuredImg = "https://picsum.photos/1024/768/?random"
+++
```

#### Shortcodes

##### Figure

This theme provide a `figure` shortcode. You can use it like this:

```
{{ figure(src="https://via.placeholder.com/1600x800",
          class="big"
          caption_position="center",
          caption="figure-big",
          caption_style="font-style: italic;") }}
```

- src: The url of the image
- class: Can be "big" | "left" | "right" (default to "") This define how to display the image
- caption_position: Can be "center" | "left" | "right" (default to "center")
- caption: string, describe the image
- caption_style: Custom CSS style to apply to caption

##### image

This theme provide a `image` shortcode. You can use it like this:

```
{{ image(src="https://via.placeholder.com/1600x800", class="boulou" alt="Hello Friend", style="border-radius: 8px;") }}
```

- src: The url of the image
- class: You can apply class to the current img
- alt: The alt of the image
- style: Custom CSS style to apply on the img element

#### Fix footnotes css

In an article you can do footnotes like this:

```markdown
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.[^1]

> An apple is a sweet, edible fruit produced by an apple tree (Malus pumila). Apple trees are cultivated worldwide, and are the most widely grown species in the genus Malus. The tree originated in Central Asia, where its wild ancestor, Malus sieversii, is still found today. Apples have been grown for thousands of years in Asia and Europe, and were brought to North America by European colonists. Apples have religious and mythological significance in many cultures, including Norse, Greek and European Christian traditions.[^2]

[^1]: From [https://www.lipsum.com/](https://www.lipsum.com/)

[^2]: From [https://en.wikipedia.org/wiki/Apple](https://en.wikipedia.org/wiki/Apple)
```

#### Themes

You can switch to a darker theme by setting de `extra.accent_color` variable.
There is 2 themes actually:

```toml
[extra]
accent_color = "dark" # Or "grey", which is the default value
```

## License

[MIT](LICENSE)

Thanks to [Track3](https://github.com/Track3) for creating the original!
Thanks to [VersBinarii](https://github.com/VersBinarii) for making the zola port !