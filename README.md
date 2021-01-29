# SRM-Ecology website

Status: DRAFT

This is the code for creating the website for the srm-ecology working group.   The draft is currently hosted on https://srm-ecology.netlify.com

## Content and contributing

Content is from the work group members.  Work group members who have content to add or edits contact Phoebe Zarnetske or use the github issues. 

Additionally/alternatively, materials may be uploaded to our google drive folder and doc.   Documents for editing the code are forthcoming, but group member may request access to this repository.  Once granted, clone the repository, edit and push.  chan

## Site Technology 

This site uses the "Wowchemy Research Group" Template for [Hugo](https://github.com/gohugoio/hugo)

- [**Get Started**](https://wowchemy.com/templates/)
- [View the **documentation**](https://wowchemy.com/docs/)
- 
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
