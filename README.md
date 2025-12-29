# site

[Hugo]() static site with support for notes, blog posts, photos,
and workout data visualization.

## setup

```bash
# install hugo (macos)
brew install hugo

# run development server
cd site
hugo server -D
```

## content

create new content:

```bash
hugo new notes/my-note.md
hugo new blog/my-post.md
hugo new photos/my-gallery.md
```

## features

- light/dark theme toggle
- latex math support via katex
- workout stats display via shortcodes
- responsive design

## shortcodes

use in markdown:

```
{{< workout-stats >}}
{{< lifting-prs >}}
{{< recent-workouts >}}
```

## deployment

github actions workflow in `.github/workflows/deploy.yml` builds and deploys
to github pages on push to main.
