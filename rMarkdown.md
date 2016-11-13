#Basic Markdown

## This is a secondary heading
### This is a tertiary heading


Unordered Lists

* first item
* second item
* third item

http://daringfireball.net/projects/markdown
http://www.rstudio.com/ide/docs/authoring/using_markdown



http://rmarkdown.rstudio.com/authoring_basics.html
*italic*   **bold**
_italic_   __bold__

# Header 1
## Header 2
### Header 3

* Item 1
* Item 2
    + Item 2a
    + Item 2b

1. Item 1
2. Item 2
3. Item 3
    + Item 3a
    + Item 3b

Inline R: `r nrow(cars)` cars studied

> Block
> Quotes

> This is a "lazy form" of block quote. This
paragraph has two lines.

> 1. This is a list inside a block quote.
2. Second item.

> This is a block quote.
>
> > A block quote within a block quote.

>     to put an indented code block in a block quote, you need five spaces after the right angle bracket

```
Plain Code Block
```

### Inline code
We defined the `add` function to
compute the sum of two numbers.
LaTeX Equations

Inline equation $equation$
Display equation $$ equation $$

### Horizontal rule / page break
***
---

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
Reference Style Links and Images

A [linked phrase][id].

then, sometime later, at the bottom of the document, for example,
[id]: http://example.com/ "Title"
Images
![alt text][id]

At the bottom of the document:
[id]: figures/img.png "Title"

superscript^2^

~~strikethrough~~




http://rmarkdown.rstudio.com/lesson-1.html

install.packages("rmarkdown")
install.packages("knitr")

Extension .rmd
Contains 3 types of data:
YAML metadata
Text to display
Code chunks to execute (R, Python, SQL, etc.)

Open and edit in RStudio.
Export to html, pdf, Word, notebook, etc.

R Notebooks (only available in RStudio Preview Release)
http://rmarkdown.rstudio.com/r_notebooks.html

Inside a notebook the CWD is where the notebook file exists.
Relative pathing works.


https://nicercode.github.io/guides/reports/
knit("myPath/example.Rmd")  # produces the md file
markdownToHTML("example.md", "example.html")  # converts an md file to html



https://nicercode.github.io/guides/reports/

Markdown was the original (Daring Fireball)
There are variations, including:
Github flavour
Pandoc flavour
RMarkdown (in R-studio, R-flavoured), which has the extension .Rmd
These can include "code blocks"
e.g.,
```{r}
mean(1:10) # or some other code
```

knitr lets you combine RMarkdown and R code within a single document.
A bit like how a LaTeX document gets processed into PDF.

This block of code will run, but leave no trace of its running in the final document:
```{r,results="hide",echo=FALSE,eval=TRUE}
a <- 1
```

You can click the "Knit HTML" button in RStudio, or perform knitting within R,
```{r,eval=FALSE}
library(knitr)
library(markdown)
knit("myPath/example.Rmd")  # produces the md file
markdownToHTML("example.md", "example.html")  # converts an md file to html
```

To convert to other formats instead of HTML, use pandoc
```{r,eval=FALSE}
library(knitr)
library(markdown)
knit("example.Rmd")  # produces the md file
pandoc("example.md", format = "docx")  # converts md file into docx
```
