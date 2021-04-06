# SRM-Ecology website

Status: As of Feb 2, 2021, 9pm, the website is live.

This is the code for creating the website for the srm-ecology working group. The website is currently hosted on https://www.climateinterventionbiology.org/

## Content and contributing

Content is from the work group members.  Work group members who have content to add or edits contact Phoebe Zarnetske or use the github issues. 

Additionally/alternatively, materials may be uploaded to our google drive folder and doc.   Documents for editing the code are forthcoming, but group member may request access to this repository.  Once granted, clone the repository, edit and push.  

## Site Technology 

This site uses the "Wowchemy Research Group" Template for Hugo 
- hugo static site generator https://gohugo.io/
- [Get Started with wowchemy](https://wowchemy.com/templates/)
- the site is published via "https://netlify.com" automatically after this repository is changed. 

## editing on github

if you have permission you may edit files directly in this repository.   If you don't you may fork and make a pull request.  


## local development

 - install Hugo (see site above)
 - clone this repository
 - hugo has a 'server' to run a local version  (command line `hugo serve` ) 
 - edit the sites pages and confirm the render with hugo on your own computer by browsing to http://localhost:1313/
 - use git to commit your changes
 - `git push` and the site will be updated by Netlify (if the changes render ok)
 
 See the hugo and wowchemy docs and tutorials for much more info. 
 
## Adding images

there are several ways to add an image to a page.  

to use the standard markdown image code.  Place the image in the same folder as the page (e.g. to add an image to the about page, put it in the /about folder next to the index.md file), and  ![alternative text for search engines](<imagefilename>)  e.g. if the file is `cornflakes.jpg` the code is `![plot of preferences for breakfast cereals](cornflakes.jpg)`

You can also put images in the folder /static/media and use a "shortcode" from the wowchemy theme `{{< figure library="true" src="image.jpg" title="A caption" >}}`   where `library` here refers to what the theme is calling the image library in the /static/media folder. 

To documentation for adding a single image from wowchemy theme is https://wowchemy.com/docs/content/writing-markdown-latex/#single-image

You can also add images as a 'header' image that is above the title fills the horizontal space (use only for very narrow images). In the front matter, add something like

```
# # Optional header image (relative to `static/media/` folder).
header:
   caption: "Great Barrier reef"
   image: "gbr.jpg"
```

and put the image (`gbr.jpg` in this case) in the same folder as the page.  

## Adding publications

see https://wowchemy.com/docs/content/publications/

## Adding/editing people

People pages are in `/content/authors/<PersonName>/_index.md` and may be edited directly.    To add a new person, copy and paste an existing person's file into a new folder under /content/authors.   The folderr naming schema of  FirstnameLastname is not special, it was just convenient.     To add a new picture, put a jpg-formatted picture file in the folder that is at most 1000px on a side, and name it `avatar.jpg`   It does not have to be square or round - Hugo will resize and make it round.   

## Adding 'news' item

The front page has section for 'news' items which is simply a placeholder that shows the latests few blog posts.  To add news, you first add a 'post' item.   Review the "Create a blog post" intructions from Wowchemy.   From the command line/terminal you could try 

```bash
hugo new  --kind post post/my-article-name
```

To do so manually, create a new folder under content/post folder, starting with the date (in YY-MM-DD format) and then a short name. E.g. 21-04-06-pnas-paper-published

Inside that folder, create a file "index.md" and an optional image 'featured.jpg' (note that I think it must be jpg format, not PNG).   see the other `index.md` files in the posts folder for an example but it must minimally have title and date items in the front matter section, and a summary below that.    If you have a featured image include the optional "image" tag.    For more info about featured imaged see [Page Features Documentation](https://wowchemy.com/docs/content/page-features/)

example post page:  

```
---
title: Session for the 2021 AAAS conference
date: 2020-12-01
image:
  placement: 3
  caption: ""
  focal_point: "Center"
  preview_only: false
  alt_text: Logo of the AAAS
---
this is a summary of the blog post from which the site will automatically create a summary for the front page.  If you include the code <!--more--> in this article body, the site will use that as a break to determine where the summary ends.  
```
