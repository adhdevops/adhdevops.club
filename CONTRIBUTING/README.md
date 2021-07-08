# Contributing to ADHDevOps.club

All content is written in
[Markdown](https://www.markdownguide.org/basic-syntax/).

Please check out the [project style guide](./STYLE_GUIDE.md),
which contains more detailed guidelines for authors.

If you'd like to join the ADHDevOps team to gain write access to the repository,
please open an issue to introduce yourself!

Otherwise, please fork the repository and open a PR against the `main` branch.

## Accessibility

Accessibility is a requirement.

It's impossible to achieve perfect accessibility for every individual need,
but it's important to strive to follow recommended practices
so that the site is accessible to the largest audience possible.

There some great
[articles on web accessibility from WebAIM](https://webaim.org/articles/).
Here are a few recommended reads for authors:

- [image alt-text guide](https://webaim.org/techniques/alttext/)
- [link description guide for accessibility](https://webaim.org/techniques/hypertext/)
- [guide to writing clearly and consistently](https://webaim.org/techniques/writing/)

These guides have great info for developers and designers:

- [introduction to semantic HTML structure](https://webaim.org/techniques/semanticstructure/)
- [introduction to accessible CSS](https://webaim.org/techniques/css/)
- [guide to contrast and color accessibility](https://webaim.org/articles/contrast/)
- [guide to accessible typefaces and fonts](https://webaim.org/techniques/fonts/)
- [guide to accessible text and typographical layout](https://webaim.org/techniques/textlayout/)

## Contribute design/layout/etc. improvements

The site's theme is a custom fork hosted at
[adhdevops/ezhil](https://github.com/adhdevops/ezhil).
If you have feedback or suggestions, please open an issue there!

## Contribute content

You don't need to be able to run the site locally to contribute content,
but it does help a lot.
Please see [DEVELOPMENT.md](./DEVELOPMENT.md) for instructions.

When in doubt, open an issue!


### Non-blog content

We'd love to publish content that's more timeless than a blog post!
We're also open to converting existing blog post advice into guides.

Please open an issue to describe what you'd like to see.

If you've cloned the site locally, you can generate a new page using Hugo:

```console
cd adhdevops.club
hugo new page-title.md
```

Hugo will create a new markdown file in `content/`
containing the following
[front matter](https://gohugo.io/content-management/front-matter/):

```yaml
---
title: "Page Title"
draft: true
# slug: "short-friendly-name"
# categories: [""]
# tags: [""]
---
```

### Contribute a new blog post

If you would like to draft a blog post to publish on the site,
please open a PR with the content you want to contribute.

If you've cloned the site locally, you can generate a new post using Hugo:

```console
cd adhdevops.club
hugo new posts/{year}/blog-post-title.md
```

Hugo will create a new markdown file in `content/posts/{year}/`

#### Blog post front matter

The new post you've generated will contain the following
[front matter](https://gohugo.io/content-management/front-matter/):

```yaml
---
title: "Blog Post Title"
date: yyyymmddT00:00:00
draft: true
# slug: "short-friendly-name"
# categories: [""]
# tags: [""]
# author:
#   name: Your Name
#   url: https://yourname.com
#   pronouns: "they/them"
---
```

Un-comment and fill out the other attributes, or delete the ones you don't use.
Note that the filename, post title, and
[url slug](https://gohugo.io/content-management/organization#paths-explained)
can each be set separately.

If your post is marked `draft: true`, be sure to run `hugo serve -D`.
The `-D` flag will render any drafts on your branch.

#### Summary and "read more" tag

The site's home page lists recent posts with a short summary of each.
That summary will also be used in link unfurls as commonly seen
on Twitter or Slack.

By default, new ADHDevOps blog posts generated with Hugo include
the `<!--more-->` tag as follows:

```markdown
... (front matter)
---

(First sentence or two here.)

<!--more-->

(The rest of the post.)
```

The summary is automatically pulled from the beginning of post contents,
starting after the front matter up until the `<!--more-->` tag.

Hugo can also use a `description` attribute set in the front matter,
if you prefer to use that.

```yaml
---
title: "Blog Post Title"
date: yyyy-mm-ddT00:00:00-00:00
description: |
  Multiple lines of text can go here to describe your blog post
  in a few sentences.
  It'll be visible in the recent posts list as well as in link unfurls
  when shared on social media or in chat applications.
---
```

The `|` character after `description:` allows you to use multiple lines,
as demonstrated in the above example.

#### Post publish date

When you run the `hugo new` command to generate the new blog post,
Hugo will automatically set the `date` attribute in the front matter
to the current time.

If some time has passed between creating the file and publishing,
you can update the publish date by editing it manually in the front matter.
