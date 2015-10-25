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
## Editing posts
You can make edits to your answers if you'd like. If you are not already part of this repository, please send an email to askanastronomer@astro.as.utexas.edu.

Each answer is composed using [Markdown](https://help.github.com/articles/github-flavored-markdown/) and resides inside the _posts/ directory. To include a full-width picture in the answer, use the following format:

```
<div class="image">
<img src="http://address-to-my/image.png" alt="Short description">
<div class="caption">Long description. Credits: A, B, and C</div>
</div>
```

*Always* include credits and copyright information.
