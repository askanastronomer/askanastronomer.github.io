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
