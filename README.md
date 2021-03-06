# michaelheyman.com

## Overview

[Jekyll](http://jekyllrb.com/) page that uses the [Phantom theme](http://jamigibbs.github.io/phantom/).

## How to Install

1. Run:

  ```bash
  gem install bundler
  bundle install
  bundle exec jekyll serve
  ```

  You may need to append your commands with `sudo` if you're getting a permissions error.

  _Don't have Jekyll yet? [Get `er installed then!](http://jekyllrb.com/docs/installation/)_

2. Visit in your browser at:

  `http://localhost:4000`

## Launching with Github Pages :rocket:

Jekyll + Github pages is a marriage made in heaven. You can [use your own custom domain name](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/) or use the default Github url (ie. http://username.github.io/repository) and not bother messing around with DNS settings.

## Setting up Google Domain with Github Pages

Follow [these instructions](https://dev.to/trentyang/how-to-setup-google-domain-for-github-pages-1p5) to configure Google Domain with Github Pages.

## Theme Features

### Navigation

Navigation can be customized in `_config.yml` under the `nav_item` key. Default settings:

```yaml
nav_item:
    - { url: '/', text: 'Home' }
    - { url: '/about', text: 'About' }
```

Set the `nav_enable` variable to false in `_config.yml` to disable navigation.

### Contact Form

You can display a contact form within the modal window template. This template is already setup to use the [Formspree](https://formspree.io) email system. You'll just want to add your email address to the form in `/_includes/contact-modal.html`.

Place the modal window template in any place you'd like the user to click for the contact form.
The template will display a link to click for the contact form modal window:

```liquid
{% include contact.html %}
{% include contact-modal.html %}
```

### Animation Effects

Animations with CSS classes are baked into the theme. To animate a section or element, simply add the animation classes:

```html
<div id="about-me" class="wow fadeIn">
  I'm the coolest!
</div>
```

For a complete list of animations, see the [animation list](http://daneden.github.io/animate.css/).

### Pagination

By default, pagination on the home page will activate after 10 posts. You can change this within `_config.yml`. You can add the pagination to other layouts with:

```liquid
  {% for post in paginator.posts %}
    {% include post-content.html %}
  {% endfor %}

  {% include pagination.html %}
```

Read more about the [pagination plugin](http://jekyllrb.com/docs/pagination/).
