# SWE-boookdown
A small working example of a bookdown site.

To get started, [download the zip file](https://github.com/NixImagery/SWE-bookdown/archive/refs/heads/main.zip) (or [fork this repository](https://github.com/login?return_to=%2FNixImagery%2FSWE-bookdown)) to a convenient place for development. You will need to have a working R installation, preferably with RStudio (currently changing its identify to Posit) - instructions are at https://posit.co/download/rstudio-desktop/. Install the bookdown package from the R console in RStudio:

```r
install.packages("bookdown")
```

Build the site (target is the `docs` directory):

```r
rmarkdown::render_site(encoding = 'UTF-8')
```
Now, from the command line or terminal, you can test your site locally using (for example) python's built-in http server:

```sh
% cd docs
docs % python -m http.server
```
You will see the website in your browser at http://localhost:8000/. 

## Where to start editing

Your main page is always the "index" file that generates the home page `index.html`. The source file is the one you edit, and it is in the `source` folder. You will see that it is an **R markdown** or `.Rmd` file. Bookdown looks for markdown files to make your pages, and those that are running R code should be Rmarkdown files to function within the RStudio IDE.

John Gruber is the originator of Markdown and his site contains [the documentation](https://daringfireball.net/projects/markdown/) you need to get writing very quickly.

You can use any plain text editor to edit markdown files. I prefer [MacDown](https://macdown.uranusjr.com/) as a stand-alone editor for lone documents, or when I am making a collection, book or website, I use Microsoft's (yes, *Microsoft*) [Visual Studio Code](https://code.visualstudio.com/). It works very nicely as an editing environment and is in fact, a very powerful *Integrated Development Environment* or IDE. RStudio is the natural IDE for working with R but you can configure Visual Studio to play nicely with R, too.

As you make changes to your documents, remember to refresh your browser. Edit and build the site as you go.

## Deploy

You have already been building the site in a folder called `docs`. This folder contains all of the files you need for your website; you should upload the contents of `docs` to your server's home folder, often called the document root, and located at `/var/www/html/exmaple.com/public_html/`. Your ISP should tell you where to find it and how to upload files to your server.

If you forked this repository, then (once you have pushed the changes to the repository) you can adjust the settings in your own github repository to serve the content from the `docs` directory. It should look a bit [like this](https://niximagery.github.io/SWE-bookdown).

## Bonus pdf

This small working example includes not only a website from your content but also a nice pdf, including and diagrams your R code generated. Find it in the `docs` folder or download it from the website.

## Try it!

I hope that's enough to get you started with your own site. Good luck!