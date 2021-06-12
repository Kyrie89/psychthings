
### Contribute a site example

To contribute a site:

1. Create a new yaml file in the [`src/site/_data/examples`](src/site/_data/examples) folder with a unique and descriptive name. Populate that file according to the structure shown below.
1. Add a thumbnail image to the [`src/site/img/examples`](src/site/img/examples) folder. (Image should be a jpeg 596px wide and 396px tall)
1. Submit a pull request

_example site yaml reference:_
```yaml
title: Your site title
description: A short description of the site.
link: The URL of this site
thumbnailurl: /img/examples/this-site-thumbnail.jpg
tools:
  - List
  - of
  - notable
  - tools
  - used
```

## Styling with TailwindCSS

This site uses [TailwindCSS](https://tailwindcss.com) to offer utility CSS classes and provide a rapid means to styling the site. This means that most styling can be done without writing any additional CSS. Instead, utility classes can be added directly to the HTML. This can provide some very rapid development and also offer surprising levels of familiarity for these used to working in this way (since the conventions and classes are not _per site_.)

While running/developing locally, the `npm run start` command will generate the site including the CSS pipeline from Tailwind.

### Global CSS utilities.

A small number of bespoke CSS rules are provided for efficiency of repeated or global classes. These reside in `src/css/tailwind.css` but these should be used sparingly, with most styling taking place in the HTML via Tailwind's utility classes.

### Dev vs prod

During a production build, the CSS pipeline includes a step to remove all unused CSS statements and compress the resultant CSS. For development efficiency, this step is not performed during local development via the `npm run start` command. You can preview an optimised production build by running these commands:

```bash

# Run a production build
npm run build

# Serve the build locally
npm run start
```
