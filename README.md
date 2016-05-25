# Website Deploy Instructions

From [Hosting on Github Pages Tutorial](https://gohugo.io/tutorials/github-pages-blog/).

Because the blog has already been made and all of the settings have mostly been configured, this document contains the deploy instructions for future reference.

The Git workflow has been configured using the `deploy script`.

## Hosting Personal/Organization Pages

* This website is hosted underneath the `mragsac.github.io` naming scheme
* Content from the `master` branch will be used to build and publish the site 

`/mragsac/blog-hugo` - contains all development files
`/mragsac/blog-hugo/public` - contains files to deploy to **mragsac.github.io**

--------
#### Step by Step Process to Complete This:

1. Create on GitHub `blog-hugo` repository
2. Create on GitHub `mragsac.github.io` repository
3. git clone `<blog-hugo-url> && cd blog-hugo`
4. Make your website work locally (`hugo server -t <yourtheme>`)
5. Once you are happy with the results, `Ctrl+C` and `rm -rf public` (this can always be regenerated with `hugo -t <yourtheme>`)
6. `git submodule add -b master git@github.com:mragsac/mragsac.github.io.git public`
7. Almost done: add a `deploy.sh` script to help you (and make it executable: `chmod +x deploy.sh`)
--------

In order to deploy, always run `bash deploy.sh "<commit message>"` to get the personal page running at `http://mragsac.github.io`!