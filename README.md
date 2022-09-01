# Living With Plagues: New Narratives for a World in Distress

**Edited by Michael Loriaux, Published by Northwestern University Libraries and the Buffett Institute for Global Affairs**

This repository contains the Markdown and [Hugo](https://gohugo.io/) source files for the [website](https://plagues.buffett.northwestern.edu/).

## Updating the site

> This site is configured to automatically build and deploy new versions of the site to AWS with every new commit to the `main` branch.

All of the content for the website is located in the `content` folder, which contains:

- `essays`: long-form writings
- `impressions-and-reflections`: vignettes
- `static/files/`: PDF files with filenames that match their markdown counterparts

Each essay is available in English and in French. The files are organized using the [translation by filename](https://gohugo.io/content-management/multilingual/#translation-by-filename) method in Hugo.

### Item Metadata

Each content item has descriptive metadata in YAML format at the top of each Markdown file, wrapped in `---`. Here's an example:

```yml
---
title: "A Story of Confinement: Before, During and After"
author:
    given_name: Éva
    middle_name: 
    family_name: Abouahi
    display_name: Éva Abouahi
    bio: "Éva Abouahi is a philosophy professor based in Reims. She is working on a dissertation on the idea of salvation in the work of Jean-Paul Sartre under the direction of Marc Crépon and  Jean-François Louette."
doi: 10.21985/n2-0xzd-th89
alt: Photo of Éva Abouahi
image: abouahi.jpg
keywords:
    - plauges
bg_img: 'white'
hero:
    title: The angel of death striking a door during the plague of Rome
    src: abouahi.jpg
    alt: The angel of death striking a door during the plague of Rome
    url: https://wellcomecollection.org/works/wwraaugh
    creator: Jules-Elie Delaunay
    license: CC BY 4.0
    license_url: https://creativecommons.org/licenses/by/4.0/
---
```

Each article has a hero image that has some properties, such as `title`, `src`, `alt` and license information. **All images used in the site are available under a permissive Creative Commons license. 

### Article Text

I used [Pandoc](https://pandoc.org/) to convert the manuscripts from Microsoft Word to Markdown for use in the site. The only "gotcha" I ran across was that Hugo does not process markdown superscripts, so I had to manually change superscripts to the `html` tags (`<sup>`), for example: `Today's date is June 4<sup>th</sup>, 2020.`

The PDFs were made in Microsoft Word (by exporting to PDF) due to my lack of LaTeX templating skills at the time. If you make PDFs for future essays, Microsoft Word is fine. 