# beardown

This project was inspired by the [bookdown](http://github.com/rstudio/bookdown) and [thesisdown](https://github.com/ismayc/thesisdown) packages.

Currently, the PDF version is developmental.

If you are new to working with `bookdown`/`rmarkdown`, please read over the documentation.

Under the hood, the Baylor University LaTeX template is used to ensure that documents conform precisely to submission standards. At the same time, composition and formatting can be done using lightweight [markdown](http://rmarkdown.rstudio.com/authoring_basics.html) syntax, and **R** code and its output can be seamlessly included using [rmarkdown](http://rmarkdown.rstudio.com).


### Using beardown from Grant's GitHub

Using **beardown** has some prerequisites which are described below. To compile PDF documents using **R**, you are going to need to have LaTeX installed.  It can be downloaded for Windows at <http://http://miktex.org/download> and for Mac at <http://tug.org/mactex/mactex-download.html>.  Follow the instructions to install the necessary packages after downloading the (somewhat large) installer files.  You may need to install a few extra LaTeX packages on your first attempt to knit as well.

To use **beardown** from RStudio:

1) Install the latest [RStudio](http://www.rstudio.com/products/rstudio/download/).
Only the version as of Oct 2017 has a recent enough Pandoc included so you may need to upgrade this
separately or install a newer RStudio.

    ```r
    rmarkdown::pandoc_available("1.2")
    #> [1] TRUE
    ```

2) Install the **bookdown** and **beardown** packages: 

```
install.packages("devtools")
devtools::install_github("rstudio/bookdown")
devtools::install_github("GrantInnerst/beardown")
```

3) Use the **New R Markdown** dialog to select **Thesis**:

    ![New R Markdown](thesis_rmd.png)

    Note that this will currently only **Knit** if you name the directory `index` as shown above.

4) After choosing which type of output you'd like in the YAML at the top of index.Rmd, **Knit** the `index.Rmd` file to get the book in PDF or HTML formats.
5) Edit the individual chapter R Markdown files as you wish and then re-run step (4) again.
