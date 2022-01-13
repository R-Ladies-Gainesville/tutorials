Tutorial Title
================
Author
2022-01-12

This is a template for tutorials, which are instructive documents that
guide a learner through a skill using examples.

Replace this text with a description of you tutorial. Include clear
learning objectives. For example:

Have you ever learned a skill in R and wanted to share it with others?
In this tutorial, we’ll walk through how to create tutorials so that you
can easily share your skills!

### Learning objectives

-   Become familiar with the tutorial template
-   Adapt the tutorial template to your needs
-   Create beautiful and clear tutorials for learneRs

## R Markdown

This template is written in an R Markdown document. This type of
document is best opened and edited in RStudio. R Markdown documents
allow you to include text (like this), code (see below), and output of
code, like figures, in a single document. You can learn more about R
Markdown [here](https://rmarkdown.rstudio.com/lesson-1.html) (check out
the Cheatsheet!).

If you haven’t already, replace the `Tutorial Title` and `Author`
information in the metadata block at the top of this document with your
information.

This section is titled **R Markdown**, but your tutorial won’t
necessarily need this section. Consider the sections that you want in
your tutorial and revise the headers throughout (the text that starts
with \#\#) or create your own section headers.

## Examples

Examples are key to meeting your learning objectives. The learner needs
to be able to reproduce examples from your tutorial on their computer.
To do this, we look to advice on how to create a [minimal, reproducible
example](https://stackoverflow.com/a/5963610). Examples may include:

-   Problem or goal
-   Necessary information (about your computing environment)
-   Minimal dataset
-   Minimal runnable code

## Necessary information

R and R packages are continuously updated and examples that work under a
certain set of conditions may not work under another set. Ideally, you
would update your tutorial when key software is updated to maintain
working examples. However, that may not be feasible, and the next best
option is to provide learners with all the necessary information about
your computing environment. This can help them identify differences with
their computing environment that may be preventing the example from
running as expected.

**My computing environment:**

Session information

``` r
sessionInfo()
#> R version 4.1.1 (2021-08-10)
#> Platform: x86_64-apple-darwin17.0 (64-bit)
#> Running under: macOS Big Sur 10.16
#> 
#> Matrix products: default
#> BLAS:   /Library/Frameworks/R.framework/Versions/4.1/Resources/lib/libRblas.0.dylib
#> LAPACK: /Library/Frameworks/R.framework/Versions/4.1/Resources/lib/libRlapack.dylib
#> 
#> locale:
#> [1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8
#> 
#> attached base packages:
#> [1] stats     graphics  grDevices utils     datasets  methods   base     
#> 
#> loaded via a namespace (and not attached):
#>  [1] compiler_4.1.1  magrittr_2.0.1  fastmap_1.1.0   tools_4.1.1    
#>  [5] htmltools_0.5.2 yaml_2.2.1      stringi_1.7.6   rmarkdown_2.11 
#>  [9] knitr_1.36      stringr_1.4.0   xfun_0.29       digest_0.6.29  
#> [13] rlang_0.4.12    evaluate_0.14
```

RStudio version

``` r
rstudioapi::versionInfo()$version
#> [1] '1.4.1717'
```

## Minimal dataset

Almost all examples require an input. That is what is meant by
“dataset”. You can create your own dataset or use one that is built into
R.

**Create-your-own:**

Known values

``` r
x <- c(1, 5, 9, 10)
```

Random values (set seed to make it reproducible)

``` r
set.seed(20)
y <- rnorm(4)
```

See guidance on [minimal, reproducible
example](https://stackoverflow.com/a/5963610) for more examples.

**Built-in:**

Available datasets in R (run in R to see list)

``` r
data() 
```

A popular example dataset is ‘iris’

``` r
head(iris)
#>   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
#> 1          5.1         3.5          1.4         0.2  setosa
#> 2          4.9         3.0          1.4         0.2  setosa
#> 3          4.7         3.2          1.3         0.2  setosa
#> 4          4.6         3.1          1.5         0.2  setosa
#> 5          5.0         3.6          1.4         0.2  setosa
#> 6          5.4         3.9          1.7         0.4  setosa
```

Another great example dataset is ‘penguins’

``` r
# install the package if it's not already installed
if(!("palmerpenguins" %in% installed.packages()[,"Package"]))
  install.packages("palmerpenguins")

# load package
library(palmerpenguins)

# show data
head(penguins)
#> # A tibble: 6 × 8
#>   species island bill_length_mm bill_depth_mm flipper_length_… body_mass_g sex  
#>   <fct>   <fct>           <dbl>         <dbl>            <int>       <int> <fct>
#> 1 Adelie  Torge…           39.1          18.7              181        3750 male 
#> 2 Adelie  Torge…           39.5          17.4              186        3800 fema…
#> 3 Adelie  Torge…           40.3          18                195        3250 fema…
#> 4 Adelie  Torge…           NA            NA                 NA          NA <NA> 
#> 5 Adelie  Torge…           36.7          19.3              193        3450 fema…
#> 6 Adelie  Torge…           39.3          20.6              190        3650 male 
#> # … with 1 more variable: year <int>
```

## Minimal runnable code

We will use an example from the [palmerpenguins
vignette](https://allisonhorst.github.io/palmerpenguins/articles/intro.html)
to demonstrate minimal runnable code. For this example, the goal is to
create a scatterplot for data with different categories.

**Install packages if they’re not already installed**

This handy code is from
[Stackoverflow](https://stackoverflow.com/a/4090208).

``` r
list.of.packages <- c("palmerpenguins", "dplyr", "ggplot2")
new.packages <- list.of.packages[!(list.of.packages %in% installed.packages()[,"Package"])]
if(length(new.packages)) install.packages(new.packages)
```

**Load packages**

We use the code chunk option “message = F” to suppress messages
generated when packages load.

``` r
library(palmerpenguins)
library(dplyr)
library(ggplot2)
```

**Settings**

Include figure settings, saved variables, and create-your-own datasets.

``` r
theme_set(theme_minimal())
```

**Minimal code**

Code to create scatterplot.

``` r
ggplot(data = penguins, aes(x = flipper_length_mm, y = body_mass_g)) +
  geom_point(aes(color = species,
                 shape = species),
             size = 2) +
  scale_color_manual(values = c("darkorange","darkorchid","cyan4"))
#> Warning: Removed 2 rows containing missing values (geom_point).
```

![](html_tutorial_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

If there are variations on your solution, provide more examples!

## Publish your tutorial

**Github**

*Add Github instructions here*
