# Hugo repro

This repo is intended to reproduce the following [Hugo](https://www.gohugo.io) bug report: https://github.com/gohugoio/hugo/issues/7609

The problem is with the page `/news`. I would like this to contain a paginated list of all the stories from all three years, but I cannot find a way to do it.

**UPDATE:** Fixed in latest commit. `cond` uses eager evaluation of parameters, and calling `.Paginate` and `.Paginator` in the same template causes bad side effects.