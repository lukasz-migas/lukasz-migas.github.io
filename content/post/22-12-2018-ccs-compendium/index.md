+++
title = "CCS Compendium - embedding scatter plots using ORIGAMI"
subtitle = "Interactive example of a scatter plot with ~4000 CCS/z vs m/z points from recent [paper](https://pubs.rsc.org/en/content/articlepdf/2019/sc/c8sc04396e) from [Prof. McLean's lab](https://www.vanderbilt.edu/chemistry/faculty/mclean.php)."

date = 2018-12-22T00:00:00
lastmod = 2018-12-22T00:00:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Lukasz G. Migas"]

tags = ["ORIGAMI"]
summary = "Interactive plot of CCS/z vs m/z created in ORIGAMI"

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = ["origami-project"]

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
[image]
  # Caption (optional)
  # caption = "Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"

  # Show image only in page previews?
  preview_only = false

+++
## Some background

I recently came across this nice paper from John McLean's lab at Vanderbilt which discusses how we can use a relatively large (~4000 values) database of measured standards in omics studies. They have created a *R Shiny* app which provides interactivity to explore the dataset. Since I have been recently improving ORIGAMI's interactive capabilities, I've decided to embed their dataset in ORIGAMI and export it as a self-sufficient HTML document. This took me about ~10 minutes altogether (mostly rearranging columns and annotating text document). I think the results are quite close to the original publication (Figure 2a). 

## Interactive figure

<iframe 
    width="825" 
    frameborder="0" 
    height="1100"
    src="https://lukasz-migas.com/assets/post-22-12-2018-ccs-compendium/CCS-Compendium.html"
    style="background: #FFFFFF;"
></iframe>

## Data structure

In order to implement this example, I've used ORIGAMI's metadata format that provides straightforward access to load annotated data. You can look in the example available for download. The format of the metadata text files is still not finalised, however, it contains several columns that permit ORIGAMI to figure out how to plot the data. Tags used in this example include:

**Column tags**:

*axis_x, axis_y, axis_label, axis_url, axis_color* 

**Header tags**:

*title, plot_type, x_label, y_label, hover_labels*.

You can have a look at the way the data is structured below.

<iframe 
    src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRqOJpxBvUagahpBvQzM78FjHLRWnfVbkEYXJsUMYLtO_TnN-9cT2X9JlR1iS16K-2qfl4pr-iWS7dn/pubhtml?widget=true&amp;headers=false"
    width="650" 
    height="400">
</iframe>

## Download formatted data:

You can download the data used for this figure from [here](https://lukasz-migas.com/assets/post-22-12-2018-ccs-compendium/ccs_compendium.txt.zip)


*Last updated: 1/1/2019*