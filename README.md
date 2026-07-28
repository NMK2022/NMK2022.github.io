# Personal Website 
![](files/images/logo.png)
## 
This repository contains the code files and images related to my personal website. The layout of the website uses the Quarto Academic Website [Template](https://drganghe.github.io/quarto-academic-website-template/). However, I have included updated the template to include my personal information and some changes to the page layouts.

<br>

## Table of Contents
* [Technologies](#technologies)
* [Setup](#setup)
* [R Coding Resource](#r-coding-resources)
* [Acknowledgments](#acknowledgments)

##

### Technologies
This project was created with:

* Homebrew Version 6.0.9
* Git Version 2.50.1 
* R Studio Version 4.5.3
* 2023 Macbook Pro with 16GB running macOS Sequoia 15.7.7 

##

### Setup
Install the following packages
1. [RStudio](https://posit.co/download/rstudio-desktop/)
2. [Set up Git and GitHub](https://rfortherestofus.com/2021/02/how-to-use-git-github-with-r)
3. [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-from-a-branch)
4. [Quarto Academic Template](https://drganghe.github.io/quarto-academic-website-template/)
   
In addition, the following packages were installed via the console in R Studio:

```
> install.packages("tidyverse")
> install.packages("quarto")
> install.packages("dplyr")
> install.packages("usethis")
> install.packages("gitcreds")
```

##

### R Coding Resources
Below are links to additional R Studio setup help:

[Documentation for Installing RStudio
](https://rstudio-education.github.io/hopr/starting.html)

[Video Walkthrough of Installing RStudio for Mac and Windows](https://youtu.be/R9yIexc5T2g?si=FAuGyd1GeV7c3cQD)

##

### Acknowledgments
Thank you to the Bakulski lab team for your continued support and expertise!

The following pages were used for coding and creating this repo:
* My repo for the edx [Harvard-cs50x](https://github.com/NMK2022/Harvard-cs50x) online course for additional HTML/CSS options
* https://epirhandbook.com/en/index.html
* https://r4ds.had.co.nz
* https://docs.github.com/en/pages/quickstart
* https://www.w3schools.com/w3css/w3css_templates.asp 
* https://rfortherestofus.com/2021/02/how-to-use-git-github-with-r
* https://rcdsdocs.it.northwestern.edu/tutorials/r/git-with-r.html
* https://www.r-bloggers.com/2017/04/r-best-practices-r-you-writing-the-r-way/
* https://happygitwithr.com/



Welcome! This is a simple and customizable template for building your own academic website using [Quarto](https://quarto.org/). You can easily fork, edit, and publish your site with just a few steps.

If you achieve this milestone, congratulations! You are now ready to start updating your website:

1. **Update** the `_quarto.yml` file to configure your site’s basic settings.  
1. **Add or edit content** in the following files and folders:
   - `/posts/` – posts about publications, news, events  
   - `teaching.qmd` – teaching information  
   - `projects.yml` – research or other projects  
   - `people.qmd` and `/people/` – team or collaborators  
   - `/files/` - profiles, images, pdfs, and includes 
1. [**Render and preview**](https://quarto.org/docs/websites/#website-preview) your site locally.  
1. **`Commit` to publish** your updates.
1. **Refine and polish** your content and design as needed.  
1. ✅ Enjoy your new website!
1. **Link** your website on your official pages to let Google and AI bots include in their search results.


## Automatically Generate a Neat Publication List

1. **Prepare your publication source file**:
   - Recommended: maintain `publications.xlsx` (already supported by this template, you can convert a bib file to Excel using online tools).
2. **Fill `publications.xlsx` using the expected column names**:
   - `Section`, `Authors`, `Year`, `Date`, `Title`, `Paper Link`, `Journal`, `Volume`, `Issue`, `Pages`, `DOI`
   - Optional links/metadata: `PDF`, `Preprint`, `ShareIt`, `Supplemental Information`, `GitHub`, `Code`, `Data`
   - Optional flags/info: `Highly Cited`, `Hot Paper`, `Awards`, `Media Coverage`, `Invited Presentation`, `Categories`
3. **Install Python dependency** (one-time):
   - `pip install openpyxl`
   - Optional validation support: `pip install pyyaml`
4. **Convert Excel to YAML**:
   - `python xlsx_to_yml.py`
   - Or with custom files: `python xlsx_to_yml.py input.xlsx output.yml`
   - Force conversion: `python xlsx_to_yml.py --force`
5. **Render your site**:
   - `quarto render`
   - The project is already configured with `pre-render: python xlsx_to_yml.py` in `_quarto.yml`, so conversion will run automatically before rendering if there is any update in `publications.xlsx`.
6. **Check publication page output**:
   - Main auto-generated page: `pub-listing.qmd`
   - Listing template: `pub-listing.ejs`
   - Styling: `pub-listing.css`
   - Filter: The `remove-stray-divfence.lua` filter is added to remove excessive ::: in html after rendering.
7. **Categorize records correctly**:
   - Use `Section` as either `Selected Work` or `Peer-reviewed Journal Paper` to place entries into corresponding sections. You can add other Section as needed.
   - Use `Categories` with separators like `,`, `;`, or `|` for listing filters.
8. **Publish changes**:
   - Enjoy your neat automatically generated publication list. You can customize style and template if you need to add new links and flags.


## 🛠 Requirements

- Install [Quarto](https://quarto.org/docs/get-started/)
- Learn the basics from the [official Quarto documentation](https://quarto.org/docs/websites/)

## 📚 More Examples & Tips

- [Quarto Academic Site Examples and Tips](https://drganghe.github.io/quarto-academic-site-examples.html)
