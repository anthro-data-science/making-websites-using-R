# Getting started with a personal professional website using R, blogdown, hugo and the academic theme

Delaney Glass and Ben Marwick

This workshop was based on materials prepared by [Alison Hill](https://alison.rbind.io/) and [Dan Quintana](https://www.dsquintana.com/). 

### 1. Finding your way around R and RStudio (DG)
- Check everyone could download and open R & RStudio
- Check version numbers for R (we want 4.0.0)
- A brief tour of the main panes (Console, Files, Environ, text editor, pkgs and help) 
- Have to make sure everyone can make the console work before we move on, e.g. console as a calculator 
- Backup: https://rstudio.cloud/ with blogdown and hugo (note: need to set relativeurls = true in config.toml)

### 2. Starting a new RStudio project & installing R pkgs (DG) 
- Create a new RStudio project because it takes care of working direction (no git)
- `install.packages("blogdown")`
- `blogdown::install_hugo(force = TRUE)`
- `blogdown::new_site(theme = "gcushen/hugo-academic", theme_example = TRUE)`
- Backup: https://bwaycer.github.io/hugo_tutorial.hugo/tutorials/installing-on-mac/

### 3. Getting started with your website (BM) 
- we want to remove the big header image, called the “hero” widget. Let's open up the content/home/hero.md file and change active = true to active = false
- we want to remove the demos section, called the “demo” widget. Let's open up the content/home/demo.md file and change active = true to active = false
- Edit title of your website, which can be changed in the config.toml
- Edit the color theme and font style of your website config/_default/params.toml file 

### 4. Previewing the results locally (BM)
- `blogdown:::serve_site()` run this in the console to check how edits to your md files change your website.

### 5. Adding biographical & contact details (BM)
- Edit your biography details (e.g, position, affiliation, education details) in the content/authors/admin/_index.md file
- Edit your contact details, navigate to config/_default/params.toml and scroll down to the "Contact Widget setup" section.
 
### 6. Adding images and publications, presentations, etc. (BM)
- Edit the profile photo. Just save your profile in the content/authors/admin folder, calling the file avatar.jpg (only one image file named ‘avatar’ is allowed in here) 
- Edit your publications, go to the files found in the content/publication/ folder. Each publication has a dedicated folder. To include your first publication, navigate to the content/publication/journal-article folder, and open up the index.md file.
- Ordering sections: The order that the homepage sections are displayed in is defined by the weight parameter in each of the files in the content/home/ directory. The sections are displayed in ascending order of their weight, so you can simply edit the weight parameters as desired.

### 7. Sharing your site with the world  (DG)
- There are many ways, we will show the simplest
just drag the public folder into Netlify within the "deploys" section of your admin settings. It should take about 5-10 seconds for your site to go live.
- Change the site name to something meaningful in General -> site details -> change site name
- To update, go to “production deploys” -> “Drag and drop your site folder here”
- To delete site, go to netlify -> settings -> scroll to bottom “delete this site”
- If you want to put your site on a UW server, we can do that in a future workshop. (cf. https://itconnect.uw.edu/connect/web-publishing/shared-hosting/)  

Further reading:
- [blogdown: Creating Websites with R Markdown](https://bookdown.org/yihui/blogdown/) 
- [Academic theme for Hugo](https://sourcethemes.com/academic/)
- [Overwhelmed by Hugo academic theme: a beginner's guide](https://andreaczhang.rbind.io/post/my-1st-blogpost/)
- [Managing content | Chuck's Webpage](https://www1.icsi.berkeley.edu/~wooters/post/managing-content/)
- [How to make a free personal website in R](https://www.dsquintana.blog/free-website-in-r-easy/) 
- [Up & Running with blogdown](https://alison.rbind.io/post/2017-06-12-up-and-running-with-blogdown/)

Here's a list of many sites made using this technology:
- [Awesome Blogdown](https://awesome-blogdown.com/) 

Examples of some sites we love:
- https://alison.rbind.io/
- https://earo.me/
- https://angela-li.github.io/


Content on this site is licensed under a [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/).
