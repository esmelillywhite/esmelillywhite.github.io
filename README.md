# esmelillywhite.github.io

https://esmelillywhite.github.io/

Why it is important? Why R markdown? Why github


# Getting started

*R setup*

* Download and install R and RStudio
* On Rstudio, type into the console:
`install.packages("rmarkdown")`

*GitHub setup*

* Create a github account
* Download GitHub Desktop

# Creating a website from scratch

* First, we create the GitHub repository on github.com using your account.
* Create a repository, and make sure to initialise it with a readme file.
* Once this has been created, open GitHub desktop. Click file, clone repository, and it should show an option for your new repository if you have linked your account. Alternatively, you can use the url of your repository. This can be retreived by going to your repository on github.com, and clicking the code button. Copy and paste the link that appears. Be careful where you clone the repository to- this is where you will add your R project, and it will be difficult to move the file location after this. 
* This should clone your remote repository to your computer. 

* On RStudio, create a new project. Add it to the folder you cloned your repository to. 
* Type into the console `file.create("_site.yml")` This creates the navigation bar that will be the basis of the website
* Type `file.create(“index.Rmd”)` which creates the RMarkdown file for the home page
* These two files will have appeared in the files box in the bottom right hand corner, open both files by double clicking on them
* In the _site.yml_ file, type the following: (directly editting the file, not typing into the console)

```
name: "Yourname"
navbar:
  title: "Your name"
  left:
    - text: "Home"
      href: index.html
```
Into the _index.Rmd_ file type:

```
---
title: "Home"
output: html_document
---
```
And then type what you want to appear on your home page. 
* Make sure you save changes to both files, and on the _index.Rmd_ file, click knit.
* This knits the document into a html format, and a window will apear giving you a preview of what you've just created. Make sure you knit before going to the next step.
* In the top right hand box there will be a 'build' tab. Click on this, and then click on 'Build website'. Alternatively, you might not have the build option yet on RStudio, which only appears when it knows you're making a website. Either save and close and go back into the project, or type into the console ``` rmarkdown::render_site(encoding = 'UTF-8') ```
* Now you need to push these changes to your remote repository. On GitHub Desktop, the changes you have made should appear on the column at the left handside.
* Type a short summary of your changes, and click commit to master at the bottom.
* The option will appear to push origin. Click this. This pushes your changes to the remote repository.


On the GitHub, go to the settings, and then go to pages. Make sure that the folder it is being built from is the folder where the HTML files are being saved (which you can configure in R in buld configuration). 
