# bitcoder.net

Welcome! This repo contains the code behind [bitcoder.net](https://bitcoder.net/). Where you can see [Jekyll](https://github.com/jekyll/jekyll) in action, a cool [Ruby Gem](https://rubygems.org/search?query=jekyll) to transform your plain text into static websites. Also, I used [Forty template](https://html5up.net/forty) from [HTML5 UP](https://html5up.net/). Give some love to their [Sponsors](https://github.com/jekyll/jekyll#sponsors)

![bitcoder.net](assets/images/wide-jg.jpg "Guillermo Garcia")

# Installation

## Pre-requisites

- [Ruby +2.4.0](https://www.ruby-lang.org/en/downloads/)

  **Mac users**: Do not try to update/modify your OS installed Ruby version.

- [RubyGems](https://rubygems.org/pages/download)
- [GCC](https://gcc.gnu.org/install/) and [Make](https://www.gnu.org/software/make/)

  **Mac users**: You will need to install `xcode-select`. Follow [this path](https://jekyllrb.com/docs/installation/macos/).

You can [follow these instructions](https://jekyllrb.com/docs/installation/) depending on your platform.

## Setup

> Install dependencies

```shell
$ bundle install
```

> Run Jekyll in development mode

```shell
$ bundle exec jekyll serve --watch --livereload
```

> :warning: In case you are using Github Pages and you update the repository dependencies with `bundle update`, make sure it accomplishes the current github-pages dependencies [version requirements](https://pages.github.com/versions/). Anyway, it uses the [github pages gem](https://github.com/github/pages-gem).

# Build

Only in case you are deploying to a different service than [GithUb Pages](https://jekyllrb.com/docs/github-pages/). Otherwise pushing your code to main branch will trigger a build automatically.

```shell
$ bundle exec jekyll build
```

Repository licensed under a [Creative Commons Attribution 4.0 International License](http://choosealicense.com/licenses/cc-by-4.0/).
