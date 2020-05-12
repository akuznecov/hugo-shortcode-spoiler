  * [Description](#description)
  * [Demo](#demo)
  * [Setup](#setup)
  * [Usage](#usage)
  * [Known issues](#known-issues)

#### Description

Spoiler shortcodes (also known as "cut tags") allow you to write text that some users may not want to see and hide until the reader chooses to see it.

#### Demo

[Demo post](https://hugo-shortcode-spoiler.zae.bz/posts/spoiler-demo/)

#### Setup

1. Download repository content and put into your Hugo site structure (into root or inside of theme)
1. Include `spoiler.css` and `spoiler.js` on your site via modification of `<head>` tag or with your theme properties.
1. Include JQuery on your site via modification of `<head>` tag. 
For example, `<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.slim.min.js"></script>`

#### Usage

Syntax is quite basic

##### Spoiler shortode without Markdown
https://gohugo.io/content-management/shortcodes/#shortcodes-without-markdown
```
{{< spoiler >}}
Hidden content!
{{< /spoiler >}}
```

##### Spoiler shortcode with Markdown
https://gohugo.io/content-management/shortcodes/#shortcodes-with-markdown
```
{{% spoiler %}}
- Hidden
- **content**
{{% /spoiler %}}
```
##### Nested spoiler
```
{{< spoiler >}}
Foo
{{% spoiler %}}
Bar
{{% /spoiler %}}
{{< /spoiler >}}
```

#### Known issues

* Nesting issue
* * Parent level spoiler should be non-markdown due to nature of Hugo markdown processing.
* * It also affect case with more than 2 levels - only latest level could be Markdown.
