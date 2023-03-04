---
title: "About this folder"
date: "2023-02-28 23:05:28"
draft: false
slug: "about-this-folder"
---

![Posts 폴더 소개](Posts/attachments/about-this-folder.png)

The **Posts** folder is a folder that is intended for use when creating a blog in the future. Note that when a file is created in this folder, it uses a special template which was created using the feature of a plugin called [Templater](https://obsidian.md/plugins?id=templater-obsidian).

```yaml
---
title: "File Name"
date: "YYYY-MM-DD HH:mm:ss"
publish: true
slug: ""
tags: []
---
```

The above template is the result of the file `Templates/Templater/New Post Template`. Each [frontmatter](https://nextjs.org/docs/advanced-features/using-mdx#frontmatter) attribute has the following meanings:

- `title`
    - The title of the document
    - Set to be the same as the file name
    - Intended to be used as the title of the browser tab in the blog
- `date`
    - The time the document was created
- `publish`
    - Whether to publish the document on the blog
- `slug`
    - The last part of URL of this document
- `tags`
    - The list of tags for this document
    - Tags defined here will also appear in Obsidian's tag feature
    - Intended to be used when listing posts by tag on the blog in the future
