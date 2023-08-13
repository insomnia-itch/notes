---
layout: post
title:  "Jekyll Cheatsheet"
categories: jekyll
author: Jelani
---
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file (use `md` or `markdown`). After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Each post should start with [Front Matter][jekyll-fm].

At the bare minimum, add: `layout`, `title`, `author` (`layout` should always be `post`). 

{% highlight yaml %}
layout: post
title:  "Welcome to Jekyll!"
categories: jekyll
author: Jelani
{% endhighlight %}

You can run the jekyll site locally if you have Ruby installed. First, make sure you `bundle install` to install all the required gems in the `Gemfile`. Then, you can run `bundle exec jekyll serve --livereload` to host the site on `localhost:4000`.

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

This [blog post][unofficial-quickstart] might be helpful.

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[jekyll-fm]: https://jekyllrb.com/docs/front-matter/
[unofficial-quickstart]: https://www.aleksandrhovhannisyan.com/blog/getting-started-with-jekyll-and-github-pages/#2-setting-up-your-first-jekyll-site
