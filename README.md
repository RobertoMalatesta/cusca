# CUSCA

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Donate](https://img.shields.io/badge/donate-paypal-blue.svg?style=flat-square)](https://paypal.me/wdiazux)

A theme for [Ghost 2.x](https://ghost.org).

**What that mean CUSCA?**

Is the abbreviation for Cuscatlán, it was the name of El Salvador before the conquest and means "the land of precious things" in Nahuatl.

---

## Introduction

Cusca was development using [Foundation](http://foundation.zurb.com), and other libraries:

- [Shuffle](https://vestride.github.io/Shuffle/)
- [Fancybox](http://fancyapps.com/fancybox/3/)
- [FontAwesome](http://fontawesome.io)
- [Prism.js](http://prismjs.com)
- [Node Vibrant](https://github.com/akfish/node-vibrant)
- [Particles.js](https://vincentgarreau.com/particles.js/)
- [Ghost Search](https://github.com/HauntedThemes/ghost-search)
  
## Installation

Inside the Ghost themes folder (content/themes) you have to clone the repository or download the last version:

:anchor: [Last release](https://github.com/wdiazux/cusca/releases/latest)

```bash
git clone https://github.com/wdiazux/cusca.git
```

:warning: **Important:**

You will need to enable the Ghost Public API and Subscribers, both option are in the Labs in the Admin panel. You also can [Read how to do it on my blog](https://www.wdiaz.org/how-to-enable-the-public-api-on-ghost/).

## Setup

### Disqus

Inside the `post.hbs` file you need to replace `[your-disqus-name]` with your Disqus name:

```javascript
(function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.async = true;
    s.src = 'https://[your-disqus-name].disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
})();
```

Do the same for `partials/loop.hbs`:

```html
<script id="dsq-count-scr" src="//[your-disqus-name].disqus.com/count.js" async></script>
```

### Social Icons

Inside the `partials/footer.hbs` file replace `[your-user]` with your user names for each social network:

```html
<li>
    <a href="https://www.youtube.com/[your-user]" target="_blank" rel="noopener" title="Youtube"><i class="fab fa-youtube"></i></a>
</li>
<li>
    <a href="https://www.facebook.com/[your-user]" target="_blank" rel="noopener" title="Facebook"><i class="fab fa-facebook-f"></i></a>
</li>
<li>
    <a href="https://twitter.com/[your-user]" target="_blank" rel="noopener" title="Twitter"><i class="fab fa-twitter"></i></a>
</li>
<li>
    <a href="https://www.instagram.com/[your-user]" target="_blank" rel="noopener" title="Instagram"><i class="fab fa-instagram"></i></a>
</li>
<li>
    <a href="https://github.com/[your-user]" target="_blank" rel="noopener" title="Github"><i class="fab fa-github-alt"></i></a>
</li>
<li>
    <a href="https://www.linkedin.com/in/[your-user]" target="_blank" rel="noopener" title="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
</li>
```

### Google Analytics

Inside the `partials/google_analytics.hbs` file replace `[your-ga-id]` with your google analytics id:

```javascript
window.ga=window.ga||function(){(ga.q=ga.q||[]).push(arguments)};ga.l=+new Date;
ga('create', '[your-ga-id]', 'auto');
ga('send', 'pageview');
```

## Modify the theme

You need to run a ghost instance in the port 2368 it is the default ghost port,
the theme was development using Webpack, so first you need to install it and
their dependencies with this command:

``` bash
npm install
```

Then you have four commands provided by the Webpack configuration file:
* `npm run dev` to compile files in development.
* `npm run start` for live development.
* `npm run build:prod` to build a production environment.
* `npm run test` to test the theme with gscan.

If you are looking to modify the style or something in the scripts, the source
files are in the `src` directory `assets` is the destination directory and it
shouldn't be modified.
This version use Typescript for javascript and SASS to generate CSS.

## Copyright & License

- Copyright (c) 2017-2019 William Diaz - Released under the [MIT license](LICENSE).
This version is using the MIT license and the libraries are also MIT or compatibles with it.
