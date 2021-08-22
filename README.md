# jeromeciarkowski.github.io

# TODO
* Learn GitHub Pages, jekyll
    * gem theme
    * only content, no theme
* README.md
    * First Setup
    * Commands
* Change Root URL to JeromeCiarkowski.com
    * https://github.com/JeromeCiarkowski/jeromeciarkowski.github.io/settings/pages
* Add Repository License
* Migrate WordPress website to jekyll
* https://mmistakes.github.io/minimal-mistakes/docs/configuration/
    * reCAPTCHA
    * atom_feed
    * Google Analytics or Google Search Console
    * Follow buttons near footer
* https://mmistakes.github.io/minimal-mistakes/docs/layouts/#custom-sidebar-navigation-menu
    * Neat but unnecessary
* Terms and Conditions
* Last but not least
    * Manually review every single line

https://web.chaehni.ch/web/blog-thumbnails/

# Docker
[GitHub Pages](https://pages.github.com/) and [jekyll](https://github.com/jekyll/jekyll) are built with Ruby and Gems. Like any build technology, dependencies exist and are a headache. Let us not suffer!

## Pull the Repository, Change Directory
```zsh
git clone git@github.com:JeromeCiarkowski/jeromeciarkowski.github.io.git
cd jeromeciarkowski.github.io
```

## Build the Website
```zsh
docker container run --rm --volume $PWD:/srv/jekyll jekyll/jekyll jekyll build
docker container exec $(docker container ls -aqf "name=blog") jekyll build --verbose 
```

## Serve the Website
```zsh
docker container run --name blog --volume $PWD:/srv/jekyll -p 4000:4000 -it jekyll/jekyll jekyll serve --livereload
```

## Restart the Container
```zsh
docker container restart blog
```

## Remove the Container
```zsh
docker container rm $(docker container ls -aqf "name=blog")
```

# CNAME
JeromeCiarkowski.com CNAME jeromeciarkowski.github.io