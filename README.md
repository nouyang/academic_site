# quickstart

```
$ gem install jekyll bundler

$ jekyll serve
Configuration file: /home/jade/Desktop/cat/academic_site/_config.yml
            Source: /home/jade/Desktop/cat/academic_site
       Destination: /home/jade/Desktop/cat/academic_site/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.225 seconds.
 Auto-regeneration: enabled for '/home/jade/Desktop/cat/academic_site'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

If run into permissions errors on gem install  --
Make sure in `.bashrc`
```
export GEM_HOME="$HOME/gems"
export PATH="$HOME/gems/bin:$PATH"
```

Then
```
source ~/.bashrc
```

# notes

28 May 2020: This site hosted at nrobot.dev

Forked from 
https://github.com/leonidk/new_website which is viewable at https://leonidk.com/

# updated website

This repo is built on a fork of **Jekyll Now** from [this repository](https://github.com/barryclark/jekyll-now). **Jekyll** is a static site generator that's perfect for GitHub hosted blogs ([Jekyll Repository](https://github.com/jekyll/jekyll))

The website design is just a modification of [Jon Barron's website](https://jonbarron.info/) and is converted for my own use, re-purposing my old markdown posts. **Feel free to use template for your own purposes**, but please respect copyright for all the images/content in my `images`, `pdfs`, `_posts` folders. 



## issues
* In general, jekyll will try to build a full page for every post. I skip that by forcing `permalink: /`. This creates multiple entries in sitemap.xml for index.html but is otherwise fine. 
* If you want multiple paragraphs, consider using `excerpt_separator: <!--more-->` in `_config.yml`, for my own use I didn't need this. 
* My own posts have lots of extra stuff left over from my old jekyll design ("author", long descriptions, etc.), feel free to ignore them
* I use thumbnails, so I can upload arbitrary sized images but then only display small ones. The `_make_thumbnails.sh` script generates them and the html template looks in `tn/` for all images. 
* I have three categories of post with slightly differerent formatting, so changing sizing requires edits in multiple paces. 
* If you use this, I'd appreciate a link back either to this repo or my personal website so others can find this too. 
