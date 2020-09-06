🌐 opensource-website
=================



Spencer Lander's personal website based on framework provied by Embark Studios

## About

This is a static site made using Vue.js.

Project data is provided by a small JSON file, but in the future this should be grabbed from an API.

All non-project data and text is hardcoded for now, but in the future this should be provided by a CMS.

I should also add routing, multiple pages, and all sorts of other things

Banner image: https://www.maxpixel.net/Flat-Web-Computer-Banner-Gray-Banner-Design-Idea-2833953

## Possible future additions

accordion: https://codepen.io/Fatal7x/pen/eZOYNK


### Adding or Changing Projects

The site's data comes from `data.json`. You can add a new project by adding its info to this file.

```javascript
{
  // Make sure the name is exactly the same as the GitHub repo name
  "name": "texture-synthesis",
  // The most important part
  "emoji": "🎨",
  // Add tags that you find relevant, as a comma-separated array
  "tags": ["rust"],
  // Short description to display on the card
  "description": "Example-based texture synthesis written in Rust",
  
  // The following fields are only required if the project will be featured:
  "featured": true,
  // Longer description, displayed on the featured card
  "extendedDescription": "A light Rust API for Multiresolution Stochastic Texture Synthesis, a non-parametric example-based algorithm for image generation.",
  // URL to an image to display on the featured card
  "featureImage": "www.example.com"
}
```

### Adding or Changing Category Sections

You can insert a section showing all projects with a specified tag by putting the following into `index.html`:

```html
<!-- Replace "rust" with your tag -->
<project-category
  tag="rust"
  v-bind:projects="projectsWithTag('rust')"
></project-category>
```

## License

Licensed under either of

* Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
* MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.
