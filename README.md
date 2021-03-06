Lasso.js CLI
========================================

This utility provides support for running the [Lasso.js](https://github.com/lasso-js/lasso) from the command-line.

# Installation

```bash
npm install lasso-cli --global
```

# Usage

A simple usage that writes out a JavaScript bundle and a CSS bundle to the `static/` directory that includes all of the required dependencies is shown below:

```bash
lasso foo.js style.less --main main.js --name my-page
```

With additional options:
```bash
lasso jquery.js style.less \
    --main main.js \                         # Entry JavaScript module for the browser
    --name my-page \                         # Give the page bundle files a name
    --out static                             # Output directory
    --url-prefix http://mycdn/static/ \      # URL prefix
    --fingerprint \                             # Include fingerprints
    --html \                                 # Head and body HTML
    --minify \                               # Minify JavaScript and CSS
    --inject-into index.html \               # Inject HTML markup into a static HTML file
    --plugin my-plugin \                     # Enable a custom plugin
    --transform my-transform                 # Enable a custom output transform
```

Alternatively, you can create a JSON configuration file and use that instead:

```bash
lasso --config lasso-config.json
```

For additional help from the command line, you can run the following command:

```bash
lasso --help
```
