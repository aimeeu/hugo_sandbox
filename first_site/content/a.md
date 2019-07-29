---
title: "Title of Page A"
date: 2019-07-24T10:51:40-05:00
draft: true
author: aimeeu
tags: ["tag1", "tag2", "tag3"]
categories: ["cat1"]
moods: ["Happy", "Upbeat"]
myVar: "myValue"
color: "blue"
---

# This is the heading


This is the 'A' markdown file. It's in the *content* root directory.

# Custom Shortcode
## Single Word Example
[Hugo Docs Example](https://gohugo.io/templates/shortcode-templates/#single-word-example-year)

```html
 {{</* year */>}}

```
This is year {{< year >}}

## Custom Shortcode with Named Parameters
Add the custom shortcode to the page:

```
 {{</* myshortcodeNameParms name="Aimee" color="blue" */>}}

```

{{< myshortcodeNameParms name="Aimee" color="blue">}}

## Custom Shortcode with Positional Parameters

```
 {{</* myshortcodePosParms Aimee orange */>}}

```

{{< myshortcodePosParms Aimee orange>}}

## Custom Shortcode with Tags
Shortcode can also pull text enclosed within the tags. 
[Hugo Docs](https://gohugo.io/templates/shortcode-templates/#paired-example-highlight) call this Paired.
Named or positional parameters can also be included.


```
{{</* shortCodeWithTags  color="purple" */>}}
    This is the text inside the shortcode tags
{{</* /shortCodeWithTags */>}}

```

{{< shortCodeWithTags color="purple" >}}
    This is the text inside the shortcode tags
{{< /shortCodeWithTags >}}


### Shortcodes Without Markdown
The < character indicates that the shortcode's inner content does not need further rendering.
```
{{</* shortCodeWithTags */>}}
    This is the **bold text** inside the shortcode tags
{{</* /shortCodeWithTags */>}}

```

{{< shortCodeWithTags color="red">}}
    This is the **bold text** inside the shortcode tags with '<'
{{< /shortCodeWithTags >}}


### Including Markdown Inside Tags
hortcodes with Markdown
Hugo 0.55  changed how the % delimiter works. 
Shortcodes using the % as the outer-most delimiter will now be fully rendered when sent to the content renderer
 (e.g. Blackfriday for Markdown), meaning they can be part of the generated table of contents, footnotes, etc.


Change the '<' to '%' to include Markdown inside the tags.

The % characters indicates that the shortcode's inner content needs further processing by the page's rendering processor (i.e. Markdown), needed to get the bold text in the example below:

```html
{{%/* myshortcode */%}}
Hello **World!**
{{%/* /myshortcode */%}}
```

{{% myshortcode %}}Hello **World!**{{% /myshortcode %}}


# YouTube Example

Embed a YouTube video using a Hugo shortcode:

```
 {{</* youtube id */>}}

```

Embedded video:

{{< youtube id="2xkNJL4gJ9E" autoplay="false" >}}
