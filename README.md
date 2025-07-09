# Website

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

## Installation

```bash
npm install
```

## Local Development
Starts the development server.
```bash
npm run start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

## Build
Bundles your website into static files for production.
```bash
npm run build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

## Serve
Serves the built website locally.
```bash
npm run serve
```
## Deployment

Not using SSH:

```bash
set GIT_USER=<Your GitHub username>
npm run deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
