---
layout: blog
title:  "What you need to know for Jekyll 3.3"
date:   2016-10-31 07:43:20 -0400
categories: jekyll update
---

## What's New For 3.3
* **New command for starting server**<br/>
  ```bundle exec jekyll serve```
* **No need to use `--watch` anymore**<br/>
  Watch happens automatically with `jekyll serve` now
* **No more default folders....sigh**<br/>
  Jekyll is has a default theme that is hidden in the depths of your Ruby installation. To overwrite the default themes and get back the default folders you can:
  1. [**Download the folders here**](https://github.com/usabilitydesign/website/tree/master/downloads/minima-2.0.0_override) and add them to your project.
  2. Use the command `bundle show minima` (or whatever theme you are using besides minima) while in the same directory as your project. This will show you the the default folders and you can copy and past the ones you want to override into your project.
  3. Manually make the folders and assets yourself.<br/>

  At any rate your folder structure should look like this:

  ![folders]({{site.urlimg}}/jekyll_folders.png)

* **If you are on EL Capitan, you need to do one more thing!**<br/>
  Follow these instructions:
  ```https://jekyllrb.com/docs/troubleshooting/#jekyll-amp-mac-os-x-1011```

## How To Edit These Files

### 1. Markdown Files

These are your "content" files for your pages.

These files have two parts:
* the "metadata" that is located between the set of "---"
  * this area is written in YML. Here you can write any variable you want such as "mynameis: Bob" and reference it with {{page.mynameis}}
* the "content" area that is anything below the second "---"
  *  these and are written in markdown (but you can also use HTML)

You will notice that the index file doesn't have any content. That is because most of its content sits in the layout (aka template) called "home.html"




