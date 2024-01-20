# Portfolio Website

- Install ruby v3.3
- Install node v20
- Install project dependencies
  - `bundle install`
  - `npm install`
- Serve the website with `npm run serve`

## Adding a project

- Add an entry in `_data/settings.yaml`
- Create a directory matching the `url` attribute of the project in `assets/images/projects`
- Add a thumbnail image named `thumb.png` for the home page, and any other relevant images for the main project page
- Create a `html` page matching the `url` attribute in the `projects` directory at the root of the repo
- Add the following block to the top of the page
```
---
layout: project
title: <Name of the project>
---
```
- Add images with `{% include image.html image_url="/assets/images/projects/<url>/thumb.png" name="<name>" %}`

## Editing global CSS

For common CSS, create sections in the `assets/css/main.css` and apply tailwind classes with the `@apply` marker.

E.g.
```css
h1 {
  @apply text-6xl font-bold mb-4
}
```
