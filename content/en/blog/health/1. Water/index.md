---
date: 2024-01-04
title: "Book 1: Water"
linkTitle: "Water"
description: >
  Discussing the importance of water and its presence in everyday life. Including tips on intake, moisture, showering, and more.
author: Me
resources:
  - src: "**.{png,jpg}"
    title: "Image #:counter"
    params:
      byline: "Photo: DALL-E"
---

**This is a typical blog post that includes images.**

The front matter specifies the date of the blog post, its title, a short description that will be displayed on the blog landing page, and its author.

Here's an image (`featured-water.png`) that includes a byline and a caption.
{{< imgproc water Fill "600x300" >}}
Why doesnt this work.
{{< /imgproc >}}



The front matter of this post specifies properties to be assigned to all image resources:

```
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
  params:
    byline: "Photo: Riona MacNamara / CC-BY-CA"
```

To include the image in a page, specify its details like this:

```
{{< imgproc water Fill "600x300" >}}
Fetch and scale an image in the upcoming Hugo 0.43.
{{< /imgproc >}}
```

The image will be rendered at the size and byline specified in the front matter.
