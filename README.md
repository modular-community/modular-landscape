# Modular Landscape

![Modular Landscape Logo](./images/modular-summit-hero-bg.png)

- [Modular Landscape](#modular-landscape)
  - [Interactive Version](#interactive-version)
  - [How to Run on your computer:](#how-to-run-on-your-computer)
  - [New Entries](#new-entries)
  - [Logos](#logos)
  - [Don't Use SVGs with Embedded Text](#dont-use-svgs-with-embedded-text)
  - [Corrections](#corrections)
  - [External Data](#external-data)
  - [Best Practices Badge](#best-practices-badge)
  - [Non-Updated Items](#non-updated-items)
  - [License](#license)
  - [Formats](#formats)
  - [Installation](#installation)
  - [Vulnerability reporting](#vulnerability-reporting)
  - [Adjusting the Landscape View](#adjusting-the-landscape-view)

The [Modular Landscape](https://landscape.modular.community) Project is intended as a map through modular technologies. This attempts to categorize most of the projects and product offerings in the modular ecosystem. There are many routes to deploying a blockchain, with Modular Landscape Projects representing a particularly well-traveled path.

The software for the interactive landscape has been extracted to https://github.com/modular-community/modular-landscape where it is used for other landscapes as well. This repo includes all of the data and images specific to the Modular landscapes.

## Interactive Version

Please see [landscape.modular.community](https://landscape.modular.community).

## How to Run on your computer:
**If you have node.js installed locally**, just run `./server.js` from the root directory of the project and open http://localhost:8001 once the site is updated.

It requires any node.js version 14+ to be installed, does not use any npm package. It is both a server and a site builder - after any change the new site is built.

**If you prefer to use Docker**, run `make serve-docker`. This will build and run a container serving the landscape at http://localhost:8001.

## New Entries

* We generally will only list a company's product in one box, to represent its major or best-known offering. We occasionally make exceptions for large companies. Note that if we allowed listing the same product or project in multiple boxes, the over 600 logos on the landscape would multiply to many times that many.
* We are unlikely to create a new category for products/projects as we'd rather find the best home with the current options.
* We are generally not including commercial versions of open source software. The exception is that we are showing all Certified Kubernetes implementations.
* Closed source products need to link to a clear description of your product; no stealth mode companies.
* Your project or company needs a logo and the logo needs to include the name.
* Crunchbase organization should be the company or organization that controls the software. That is normally the owner of the trademark, whether or not a trademark has been formally filed.

If you think your company or project should be included, please open a pull request to add it in alphabetical order to [landscape.yml](landscape.yml). For the logo, add an SVG to the `hosted_logos` directory and reference it there.

## Logos

The following rules will produce the most readable and attractive logos:

1. We require SVGs, as they are smaller, display correctly at any scale, and work on all modern browsers. If you only have the logo in another vector format (like AI or EPS), please open an issue and we'll convert it to an SVG for you, or you can often do it yourself at https://cloudconvert.com/. Note that you may need to zip your file to attach it to a GitHub issue. Please note that we require pure SVGs and will reject SVGs that contain embedded PNGs, since they have the same problems of being bigger and not scaling seamlessly. We also require that SVGs convert fonts to outlines so that they will render correctly whether or not a font is installed. See [Don't Use SVGs with Embedded Text](#dont-use-svgs-with-embedded-text) below.
1. Don't use reversed logos (i.e., with a non-white, non-transparent background color). If you only have a reversed logo, create an issue with it attached and we'll produce a non-reversed version for you.
1. Logos must include the company, product or project name in English. It's fine to also include words from another language. If you don't have a version of your logo with the name in it, please open an issue and we'll create one for you (and please specify the font).
1. Match the item name to the English words in the logos. So an Acme Rocket logo that shows "Rocket" should have product name "Rocket", while if the logo shows "Acme Rocket", the product name should be "Acme Rocket". Otherwise, logos looks out of place when you sort alphabetically.
1. Logos should include a company and/or product name but no tagline, which allows them to be larger and more readable. The only exception is if the only format that the logo is ever shown includes the tagline.
1. Google images is often the best way to find a good version of the logo (but ensure it's the up-to-date version). Search for [grpc logo filetype:svg](https://www.google.com/search?q=grpc+logo&tbs=ift:svg,imgo:1&tbm=isch) but substitute your project or product name for grpc.
1. Upload the SVG to the `hosted_logos` directory.

## Corrections

Please open a pull request with edits to [landscape.yml](landscape.yml). The file [processed_landscape.yml](processed_landscape.yml) is generated and so should never be edited directly.

If the error is with data from [Crunchbase](https://www.crunchbase.com/) you should open an account there and edit the data. If you don't like a project description, edit it in GitHub. If your project isn't showing the license correctly, you may need to paste the unmodified text of the license into a LICENSE file at the root of your project in GitHub, in order for GitHub to serve the license information correctly.

## External Data

The canonical source for all data is [landscape.yml](landscape.yml). Once a day, we download data for projects and companies from the following sources:

* Project info from GitHub
* Funding info from [Crunchbase](https://www.crunchbase.com/)
* Market cap data from Yahoo Finance
* CII Best Practices Badge [data](https://bestpractices.coreinfrastructure.org/)

The update server enhances the source data with the fetched data and saves the result in [processed_landscape.yml](processed_landscape.yml) and as a JSON [file](https://landscape.cncf.io/data/items.json), the latter of which is what the app loads to display data.

## Best Practices Badge

As explained at https://bestpractices.coreinfrastructure.org/:
>The Linux Foundation (LF) Core Infrastructure Initiative (CII) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice. The CII Best Practices Badge is inspired by the many badges available to projects on GitHub. Consumers of the badge can quickly assess which FLOSS projects are following best practices and as a result are more likely to produce higher-quality secure software.

The interactive landscape displays the status (or non-existence) of a badge for each open-source project. There's also a feature not available through the filter bar to see all items [with](https://landscape.cncf.io/card-mode/?bestpractices=yes) and [without](https://landscape.cncf.io/card-mode/?bestpractices=no) badges. Note that a passing badge is a requirement for projects to [graduate](https://github.com/cncf/toc/blob/main/process/graduation_criteria.md) in the CNCF.

For projects using a GitHub organisation, and the url used for the badge is the organisation not the repository, `url_for_bestpractices` needs to be specified in the projects section in the [landscape.yml](landscape.yml).


## License

This repository contains data received from [Crunchbase](http://www.crunchbase.com). This data is not licensed pursuant to the Apache License. It is subject to Crunchbase’s Data Access Terms, available at [https://data.crunchbase.com/docs/terms](https://data.crunchbase.com/docs/terms), and is only permitted to be used with Linux Foundation landscape projects.

Everything else is under the Apache License, Version 2.0, except for project and product logos, which are generally copyrighted by the company that created them, and are simply cached here for reliability. The trail map, static landscape, serverless landscape, and [landscape.yml](landscape.yml) file are alternatively available under the [Creative Commons Attribution 4.0 license](https://creativecommons.org/licenses/by/4.0/).

## Formats

The Modular Landscape is available in these formats:

* [PNG](https://landscape.modular.community/images/landscape.png)
* [PDF](https://landscape.modular.community/images/landscape.pdf)

## Installation

You can install and run locally with the following commands.

```bash
git clone https://github.com/modular-community/modular-landscape.git
cd modular-landscape
npm install -g yarn@latest
yarn
```

## Vulnerability reporting

Please open an [issue](https://github.com/modular-community/modular-landscape/issues/new).

## Adjusting the Landscape View
The file src/components/MainContent2.js describes the key elements of a
landscape big picture. It specifies where to put these sections: App Definition
and Development, Orchestration & Management, Runtime,  Provisioning, Cloud,
    Platform, Observability and Analysis, Special. Also it specifies where to
    locate the link to the serverless preview and an info with a QR code.

All these elements should have `top`, `left`, `width` and `height` properties to
position them. `rows` and `cols` specify how much columns or rows we expect in a
given horizontal or vertical section.

When we see that those elements can not fit the sections, we need to either increase
the width of all the horizontal sections, or increase height and amount of rows
in a single horizontal section and adjust the position of sections below.

Beside that, we have to adjust the width of a parent div (1620), the width in a
`src/components/BigPicture/FullscreenLandscape.js` (1640) and the width in a
`tools/renderLandscape.js` (6560, because of x4 zoom and margins)

Serverless has a same approach, files are
`src/components/BigPicture/ServerlessContent.js`,
  `src/components/BigPicture/FullscreenServerless.js` and
  `tools/renderLandscape.js`, with a full width of 3450 (because of x3 zoom and
      margins)

Sometimes the total height is changed too, then we need to adjust the height the
same way as we adjust the width.

We have an experimental `fitWidth` property, it is good when you want to get rid of
an extra space on the right of a section.

The best way to test that layout is ok, is to visit `/landscape` and
`/serverless`, and if it looks ok, run `PORT=3000 babel-node
tools/renderLandscape` and see the rendered png files, they are in `src/images`
folder
