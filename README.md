# gatsby-universal

[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

A ~~simple~~ and *opinionated* setup for using Gatsby v2 with Redux, tag-agnostic styled-components, page transitions, scroll events with `IntersectionObserver`.

## Usage

```bash
# Installation
gatsby new my-site https://github.com/fabe/gatsby-universal

# To develop
yarn develop

# To build
yarn build

# To test SSR (for Lighthouse etc.)
yarn ssr

# To format JS (precommit)
yarn prettier
```

## Lighthouse scores on Netlify

![](https://i.imgur.com/jSG7hSz.png)

## Folder structure
```bash
├── README.md
├── gatsby-browser.js
├── gatsby-config.js
├── gatsby-node.js
├── gatsby-ssr.js
├── package.json
├── src
│   ├── actions
│   ├── components
│   │   ├── head # All meta tags etc.
│   │   │   └── head.js
│   │   ├── io # Intersection Observer component, uses render props
│   │   │   └── io.js
│   │   ├── layout # Layout component
│   │   │   ├── layout.css.js # .css.js for component's styled-components
│   │   │   └── layout.js
│   │   └── transition # Page Transition component, can be used with any other
│   │       └── transition.js
│   ├── constants
│   ├── containers
│   ├── helpers
│   │   ├── agnosticStyled.js # Tag-agnostic styled-component
│   │   ├── mediaTemplates.js # Creates media queries for styled-components
│   │   └── toFallbackStyleString.js # Creates fallback styles for no-js page transitions
│   ├── images
│   ├── pages
│   ├── reducers
│   ├── reset.css.js # Global CSS
│   ├── selectors
│   └── store
└── yarn.lock
```

## Author

* Fabian Schultz ([@fschultz\_](https://twitter.com/fschultz_)) - [Stink Studios](https://stinkstudios.com)
