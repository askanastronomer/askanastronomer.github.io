# Ask An Astronomer
(c) Stefano Meschiari, 2015

Repository for http://www.askanastronomer.org. MIT Licensed.

## About
The website is built using [Jekyll](http://jekyllrb.com) and [Poole](http://getpoole.com), and hosted on [Github Pages](https://pages.github.com).

### Forking
You can fork this repository and adapt it for your institution. The structure of the website should be very easy to customize:

* Each q&a resides in the _posts/ directory and is categorized into one of Black Holes & Cosmology, Galaxies, Stars, Planets, Others and FAQ.
* `index.html` is the front page.
* `_includes/sidebar.html` contains the sidebar.
* `public/css/aaa.css` contains the styles used throughout the website.
* `img` contains static images.
* `ask.md` embeds a Google Form.

# For authors
## Writing your answer
Please write your answer in plain text format. If you’d like to apply some formatting to your answer, please use the [Markdown syntax](https://help.github.com/articles/github-flavored-markdown/).

If you’ve never answered an Ask an Astronomer question before, please [browse the website](http://www.askanastronomer.org) and check out some of the questions and answers published there. Ideally, it should be accessible to the broadest possible audience, so keep your answer simple, focused, and as free of jargon as possible. When needed, either explain the jargon or provide a link (e.g. to a Wikipedia article).

Feel free to liberally sprinkle your answer with links to websites that address part of the question, or that work as supporting materials. In fact, if there’s a webpage out there that answers the question fully, linking to it can constitute the answer itself! Finally, if there are any images that you think should be displayed along the answer once it’s posted on the website, please include them in your email as URLs. 

## Submitting your answer
When you answer this question, please reply to the submitter AND cc me at askanastronomer AT astro.as.utexas.edu; don’t forget to include the original question. 

I will then publish the question on the AaA website; I will lightly edit the answer (if needed), add a nice image on top of it, and share it through the [Ask an Astronomer Facebook group](https://www.facebook.com/mcdaskanastronomer/?ref=hl). Feel free to share it further on your favorite social media channel.

## Editing posts (optional)
Once the answer is published, you can make still make edits to your answers if you'd like. If you are not already part of this repository, please send an email to askanastronomer@astro.as.utexas.edu.

Each answer is composed using [Markdown](https://help.github.com/articles/github-flavored-markdown/) and resides inside the _posts/ directory. To include a full-width picture in the answer, use the following format:

```
<div class="image">
<img src="http://address-to-my/image.png" alt="Short description">
<div class="caption">Long description. Credits: A, B, and C</div>
</div>
```

*Always* include credits and copyright information.

# For maintainers
## Getting started (assuming Mac OS X)
1. Install a package manager such as [Homebrew](http://brew.sh).
2. Install git, jekyll, and ImageMagick: `brew install git jekyll imagemagick`
3. Clone the AaA repository to your local machine: `git clone https://github.com/askanastronomer/askanastronomer.github.io.git`.

## Operating the website
This website is powered by Jekyll. A quick tutorial is available in the [home page](https://jekyllrb.com), but you should be able to operate the website using the following instructions.

Jekyll works by compiling files into static HTML pages. To start a live Jekyll server on your machine, type:
```
$ jekyll serve --watch
```

This command will build the static HTML pages, prepare a local web server for you to see the website with any modifications you have applied, and continue watching the directory such that any changes will trigger an automatic rebuild.

The output will list a server address, typically something like:
```
   Server address: http://127.0.0.1:4000/
```

You can browse to that address (`http://127.0.0.1:4000/`) to see a live local copy of the website.

## Adding new answers
You can add new answers by using one of the existing answers in `_posts/` as a template. The file name should include the date and a dash-separated short description, for instance:
```
cp 2016-02-29-planets-from-gas-and-dust.md 2016-07-16-how-do-galaxies-form.md
```

The answers themselves are written in plain-text [Markdown format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

The top of each answer contains a [YAML front matter](https://jekyllrb.com/docs/frontmatter/), a simple list of properties and values. For example:
```
---
layout: post
title: What proof do you have that planets are made from gas and dust?
author: Sam Factor
categories: planets
thumbnail: http://askanastronomer.org/img/ppdisk_thumb.jpg
---
```
The available categories are: `bhc` (black holes & cosmology), `stars`, `planets`, `galaxies`, `faq`, and `other`.

## Adding images
Images are stored in the `img/` folder. I typically save them as JPEG files, and create thumbnails that are ~300px wide. You can create thumbnails by using the `mogrify` command from ImageMagick (or any other tool you prefer):

```
cp img/my_image.jpg img/my_image_thumb.jpg
mogrify -resize 300 img/my_image_thumb.jpg
```

The address of the thumbnail should be listed in the front matter, using the full URL to askanastronomer.org.

The post image should be at the top of the answer, right under the front matter, as an HTML fragment:
```
<div class="image">
<img src="/img/my_image.jpg">
<div class="caption">Caption, taken from this <a href="http://address-of-source.com">Source</a>. Credit: NASA/ESA/ESO/HST/Etc.</div>
</div>
```
*Only* use images in the public domain and list source and any credits in the caption.

## Workflow
1. Get a new question in the Google Sheets spreadsheet.
2. Assign it to one of the experts, taking care to cycle through people. Asking for an answer in plain text (or even Markdown, if the author is willing) will make it easier for you to import it into the website.
3. Wait for an answer -- typical wait times are 1-2 weeks.
4. When you receive an answer:
  - Create a new file for the answer by cloning a past answer, e.g. `cp _posts/2016-01-01-old.md _posts/2016-07-01-new.md`.
  - Edit the front matter to reflect question, category, author and address of thumbnail.
  - Copy and paste the answer under the front matter.
  - Lightly edit as necessary, and add links where useful.
5. Open your web browser and navigate to the local Jekyll server; check if answer looks good. Note: the thumbnail will be broken until the modifications to the website is pushed back to the Git repository.
6. Push your modifications to the git repository, e.g.:
```bash
git status   # Check which files were modified
git add -A
git commit -m "Added answer by XYZ"
git push
```
7. Share it on social media and enjoy the likes!

