---
title: Plugin types
published: true
lang: en
position: 10
---

# Plugin types

## Overview

Scully uses a plugin system which allows users to define new ways for Scully to pre-render an application.  
There are five main types of plugins which allow code to be injected into various stages of the Scully process lifecycle:

<div class="docs-toc no-spacing"></div>

- [Plugin types](#plugin-types)
  - [Overview](#overview)
    - [`router`](#router)
    - [`render`](#render)
    - [`fileHandler`](#filehandler)
    - [`routeDiscoveryDone`](#routediscoverydone)
    - [`allDone`](#alldone)

#### [`router`](/docs/Reference/plugins/types/router)

`router` plugins teach Scully how to get the required data to be pre-render pages from the route-params.

#### [`render`](/docs/Reference/plugins/types/render)

`render` plugins are used to transform the rendered HTML.  
After the Angular application renders, the HTML content is passed to a `render` plugin where it can be further modified.

#### [`fileHandler`](/docs/Reference/plugins/types/fileHandler)

`fileHandler` plugins are used by the [`contentFolder`](/docs/Reference/plugins/built-in-plugins/contentFolder) plugin during the render process. The [`contentFolder`](/docs/Reference/plugins/built-in-plugins/contentFolder) plugin processes the folders for markdown files or other file type the folders may contain. The render process processes any existing `fileHandler` plugin for any file extension type.

#### [`routeDiscoveryDone`](/docs/Reference/plugins/types/routeDiscoveryDone)

`routeDiscoveryDone` plugins are called automatically after all routes have been collected and all router plugins have finished.

#### [`allDone`](/docs/Reference/plugins/types/allDone)

`allDone` plugins are like `routeDiscoveryDone` plugins, except they are called _after_ Scully finishes executing all its processes.
