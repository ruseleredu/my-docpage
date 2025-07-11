---
sidebar_position: 2
---

# Translate your site

Let's translate to Portuguese (Brazil).

To enable Portuguese (Brazil) translation on your Docusaurus site, you’ll use its built-in i18n (internationalization) system. Here's a step-by-step guide to get you rolling:

## Configure i18n

Modify `docusaurus.config.js` to add support for the `pt-BR` locale:

```js title="docusaurus.config.js"
i18n: {
  defaultLocale: 'en',
  locales: ['en', 'pt-BR'],
  localeConfigs: {
    pt-BR: {
      htmlLang: 'pt-BR',
    },
  },
},
```
This sets up your site to support both English and Brazilian Portuguese.

## Add Locale Dropdown to Navbar
Let users switch languages:
```js title="docusaurus.config.js"
themeConfig: {
  navbar: {
    items: [
      {
        type: 'localeDropdown',
        position: 'right',
      },
    ],
  },
}

```

## Create Translation Files
Run this command to generate translation scaffolding:

```bash
npm run write-translations -- --locale pt-BR
```
This will create a folder like `i18n/pt-BR/` with JSON files for UI strings and plugin content.

##  Translate Markdown Docs

Copy your English docs into:

```bash
i18n/pt-BR/docusaurus-plugin-content-docs/current/
```
Then translate the `.md` files inside.

## SPreview Your Translated Site

Run the dev server with the locale:

```bash
npm run start -- --locale pt-BR
```

Your localized site is accessible at [http://localhost:3000/pt-BR/](http://localhost:3000/pt-BR/) and the `Getting Started` page is translated.

:::caution

In development, you can only use one locale at a time.

:::


## Build your localized site

Build your site for a specific locale:

```bash
npm run build -- --locale pt-BR
```

Or build your site to include all the locales at once:

```bash
npm run build
```
