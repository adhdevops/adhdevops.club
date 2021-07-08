# Development for ADHDevOps.club

## Requirements

Install Hugo using Homebrew for MacOS or Linux:

```console
brew install hugo
```

[See the Hugo docs](https://gohugo.io/getting-started/installing/)
for other installation options.

Note: the version of Hugo used for deployment is listed in
[netlify.toml](../netlify.toml).

## Fork and clone the repo

If you're not a part of the ADHDevOps GitHub team,
it's easier to **fork the repo before cloning it** for local development.

When cloning the repo from here or from your fork,
be sure to use the `--recurse-submodules` flag
to ensure that the site theme gets cloned as well.

```console
git clone --recurse-submodules git://github.com/{YOUR_NAME}/adhdevops.club.git
```

## Run the site locally

Run Hugo locally from the repo base directory:

```console
cd adhdevops.club
hugo serve
```

If you're working on a page or blog post with `draft: true` in the front matter,
you will need to run `hugo serve -D` to render your draft.

If you're making significant changes to the theme,
you may want to run `hugo serve --disableFastRender` to avoid caching issues.
