---
title: 'Using Cactus Comments'
date: 2023-02-13T16:00:00+01:00
draft: false
categories:
- tranquilpeak
- features
tags:
- cactus-comments
summary: Demo of integrated Cactus Comments
commentSlug: cactus-comments
---

Prerequisites: you must enable Cactus Comments and set the site name as registered with Cactus Comments.

```
[params]
  [params.comment]
    [params.comment.cactus]
      enable = true
      siteName = "YOUR_SITE_NAME"
```

Then you just have to set `commentSlug: my-slug` in the front matter of an article
where you want to allow comments. The `commentSlug` is the name of the chatroom
as described in the [Cactus Documentation](https://cactus.chat/docs/integrations/hugo/).

Note that you don't need the shortcode mentioned for the
[Hugo Integration](https://cactus.chat/docs/integrations/hugo/) when Cactus is integrated in the theme.

For the curious: the source of the Cactus integration in the theme is in
[cactus.html](https://github.com/pe-st/hugo-tranquilpeak-theme/blob/pesche/layouts/partials/post/cactus.html), which is called from [comments.html](https://github.com/pe-st/hugo-tranquilpeak-theme/blob/pesche/layouts/partials/post/comments.html) when Cactus is enabled in the site configuration.

The difference between using a shortcode and integration within the theme:

- with the shortcode the comments appear directly below the article content,
  above the navigation elements
- with the theme integration the comments appear below the navigation elements

Compare the two screenshots below for this difference:

{{< image classes="fancybox fig-50" thumbnail-width="100%" src="./cactus-with-shortcode.png" title="Cactus integrated by placing the shortcode in the article" >}}
{{< image classes="fancybox fig-50" thumbnail-width="100%" src="./cactus-with-theme.png" title="Cactus integrated in the theme's layout" >}}
{{< image classes="clear" >}}

Below you can try out Cactus Comments.
