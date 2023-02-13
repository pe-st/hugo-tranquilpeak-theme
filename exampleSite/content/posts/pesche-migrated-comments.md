---
title: 'Article with Migrated Comments'
date: 2023-02-13T17:00:00+01:00
draft: false
categories:
- tranquilpeak
- features
tags:
- cactus-comments
summary: Demonstrate how comments can be migrated to Hugo/tranquilpeak as front matter.
comments:
- time: 2023-02-13T18:00:00+01:00
  name: Pesche
  site: https://pesche.schlau.ch
  mail: me@me.me
  text: |-
    Comment with all supported fields:

    - `name` (mandatory)
    - `time`
    - `site`
    - `mail`
    - `text` (mandatory)

    Notice that you can use Markdown in the `text`,
    and multi-line texts are easy in YAML with the `|-`
    block indicator
- time: 2023-02-13T18:05:00+01:00
  name: Pesche
  mail: me@me.me
  text: |-
    Comment with email address but without site

    Notice (when hovering over the name) how the email address is
    obfuscated as simple spam protection by prefixing the domain
    with `REMOVE.`.
- time: 2023-02-13T18:10:00+01:00
  name: Pesche
  site: https://pesche.schlau.ch
  text: |-
    Comment with site and without email address
- time: 2023-02-13T18:15:00+01:00
  name: Pesche
  text: |-
    Comment without site and without email address
- name: Pesche
  text: |-
    Comment without date/time, site and email address
- time: 2023-02-14
  name: Pesche
  text: |-
    Comment with date only (no time)
---

When you migrate a blog to Hugo and have also comments to migrate,
you can add them as list in the front matter:

```
---
(front matter as usual)
- time: (ISO time stamp when the comment was saved, optional)
  name: (name of the commenter)
  site: (site URL, optional)
  mail: (email address of the commenter, optional)
  text: (comment itself, can contain Markdown)
```

Look at the [source of this post](https://github.com/pe-st/hugo-tranquilpeak-theme/blob/pesche/exampleSite/content/posts/pesche-migrated-comments.md) to see some more examples of comments.
They should be rendered below, using the same style as new comments entered
using cactus comments.

