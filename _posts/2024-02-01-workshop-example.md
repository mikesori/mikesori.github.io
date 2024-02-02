---
layout: post
title: Workshop Post
subtitle: This is a workshop post!
author: Michael Soriano
---

As a prefatory note, the materials for this workshop have been retrofitted from the GitHub Introductory presentation I offered during the Digital Humanities Research Institute. Some of the language has been changed to reflect this change but I hope provides a clear sense of who this presentation was intended to support. 

As an additional note, the original presentation comprised the two activities found herein. I have taken the liberty of adding a third activity that cumulatively builds on the work conducted in the first two exercises. In this newly added exercise, we will look through the Caribbean Keywords GitHub and breakdown how the site is constructed, where posts are stored, and how to edit the site. 
__________
In this workshop, I aim to provide basic engagements with GitHub and Markdown. Our hope, for the end of this presentation, is that you will have a GitHub account, a very basic GitHub page, and a Markdown program. Our aim here is not to be comprehensive but to provide a few directions for additional engagement with online programs and services. 

These materials have been compiled from a variety of resources, including Lindsay Thomas's introduction to GitHub pages and Markdown and Ryan Cordell's Intro to DH Course. Special thanks, as well, to Lindsay Thomas, Allison Schifani, and Susanna Alles-Torrent for their help developing these introductory materials. 

# What is GitHub?
GitHub and, more specifically, GitHub Pages is a free website hosting platform that can use a combination of Markdown and HTML (that we will discuss later) to help you easily produce clean websites for various uses, such as academic blogging, personal sites, or online resumes and CVs. 

You may have heard of, encountered, or directly used such website hosting platforms as Wordpress or Squarespace. These are excellent online tools that attempt to "streamline" the website building process. While there is nothing inherently wrong with using these platforms (and, in fact, I myself have used Wordpress and Squarespace respectively), we want to open up Github as a potential, minimalist alternative to these platforms with an eye towards preservation, longevity, and the archive. 

If you have used Microsoft Word, Wordpress, or Squarespace, you will have engaged with--what is known in the computer science and coding world as--a propriety mark-up language. Mark-up are the unique ways in which software stylizes and formats documents to make them readable. This includes italics, bolding, underlining, but also marking headings, tables of content, or comments. Again, these are stylistically particular to the infrastructure you use. In simple terms, that means that in order to read, write, or work with documents written in, for example, the Microsoft suite one must first have access to the Microsoft suite. If we can engage in a bit of speculation: what happens to our documents if, for example, Microsoft simply vanishes? Or, goes bankrupt? Or, simply stops updating and supporting the Microsoft Office suite? It seems almost inconceivable to imagine this but online software can, and regularly does, go defunct. 

Wordpress and Squarespace are also simple to think through as their website construction exists on their server space. In the unfortunate situation that any of these companies disappear or the software becomes inaccessible, what happens to the material that we have written or produced for our sites? In no easy terms, they vanish. 

Markdown and GitHub are just a few platforms and tools that digital humanists, programmers, and computer scientists use in order to preserve their documents and work. Over the course of this presentation, we will show you how to create a GitHub page, how to use Markdown, and return to the question of how Markdown and Github function, in small ways, to preserve digital ecosystems,  infrastructures, and materials. 

# Create Username & Activate GitHub Pages

For the sake of transparency, we will be creating two github repositories for today's workshop. One will be a very simple, low-tech "page with text" and the second will be a slightly more complicated webpage with a few flourishes. 

Go to [https://github.com/join](https://github.com/join) and create your account. Be careful with which username you choose because it will be the name it appears in your url.

![Create Username](https://susannalles.github.io/tutorials/docs/img/github_01.png)

Once you are signed in, you have to create a new repository where you will host your project.

![Create Repository](https://susannalles.github.io/tutorials/docs/img/github_02.png)

Or go to My Account > Your Repositories and click on “New”

![Text](https://susannalles.github.io/tutorials/docs/img/github_03.png)

For the name, it has to be ‘username.github.io’ where username is the one that you chose to create your Github account. As in “Description”, you can say something like “My GitHub Pages Repo” or whatever you want. Leave it “Public”, and click on “Initialize this repository with a README” file.

![Text](https://susannalles.github.io/tutorials/docs/img/github_05.png)

Once it is created you will see this:

![Text](https://susannalles.github.io/tutorials/docs/img/github_06.png)

Now let’s create directly into GitHub a simple html page that we will name “[index.html](https://github.com/susannalles/DHPracticum/blob/gh-pages/practice/index2.html)”:

![Text](https://susannalles.github.io/tutorials/docs/img/github_07.png)

You can write a simple code with just a title and a paragraph or copy and paste this code:

```
<!DOCTYPE html>
<html>
    <head>
        <title>GitHub Workshop Exercise 1</title>
        <style>
            body {
                background-color: #e6e2d3;
                font-family: "PT Sans", Helvetica, Arial, sans-serif;
            }
            
            h1 {
                color: #bd5734;
            }
            p {
                color: #587e76;
            }</style>
    </head>
    <body>
        <h1>My name is [Input Name Here]</h1>
        <p>Welcome to my Website for the GitHub Workshop Exercise #1.</p>
    </body>
</html>
```

Once this has been entered into the file, click the green button on the top right of your screen that reads, "Commit Changes".

Upon clicking "Commit Changes," you will be shown a screen with several text boxes. The first will read, "Commit message". The second will read, "Extended description". Further, at the bottom of this box you should see a radial menu that reads either a) commit directly to the gh-pages branch or b) create a new branch for this commit and start a pull request. For our purposes, we will click "Commit directly to the gh-pages branch".
- Commit Message: This first text box allows you to title the changes you are making to your GitHub file. Github will automatically generate titles but you can change them if you require greater specificity and clarity. 
- Extended Description: This larger text box allows you to directly document and account for the changes you have made to the file. Since this is the first time we have created the file, we do not need to add extensive descriptions. Yet, as you iterate on this file, you may want to document the exact work that you completed on this to create a clear genealogy of this file's development. 

Now, you should be able if you go to https://username.github.io/ (the name of your repository) to see your new online space where you will create your eportofio:

![[Screenshot 2024-02-02 at 1.57.48 PM.png]]

Enjoy your new virtual space!

If you review the code, you can see that the specifications we noted have been reflected in the image above. You can edit those images and add additional complexities if you are interested in doing so. The structure of HTML code is universal and will follow a nested structure. It will require specifying your DOCTYPE to ensure that the computer accurately reads the code. You will notice that the code is nested as follows:
- HTML
	- Head
		- Title
		- Style
	- /Head
	- Body
		- Heading 1
		- Paragraph
	- /Body
- /HTML

In the simplest terms, the Head nest will read your code for the Title that will appear on your internet browser's tab, as well as the style for the site. The color code's and font selection shown in the code are reflected on your basic HTML site. The Body section will specifically read the code for the content that the user will see when they visit your website.  

# Advanced Practices

In this section, we will be forking a GitHub theme using Jekyll. Jekyll is a static-site generator with various free and paid themes. For the purposes of this presentation, it isn't entirely relevant that you know what Jekyll is. Instead, it's more important that you see it in action. At the end of this presentation, I will provide an additional readings if you would like to learn more. 

Before we go into the interactive portion, I want us to briefly navigate the main theme that we will be using today. The theme is [beautifulJekyll](https://beautifuljekyll.com//). Follow the link and take note of the main page. What are some of the central features that we see here?
- A header on the top-left of the screen.
- A link to an about page on the top-right.
- Various blog post entries.
- A description box on the bottom left. 
- Links to various social media or academic sites on the bottom of the screen. 
Now that we have observed these features, we can now move to the interactive portion. 

## Step-By-Step
- Visit [the beautiful Jekyll Github page](https://github.com/daattali/beautiful-jekyll#readme)
- On the top right of the screen, you will see a button that says "fork".
	- Forking allows us to effectively copy the original markdown, html, and css files provided from a creator to use for our own purposes. This is another benefit of GitHub--the free exchange of digital tools, kits, and materials. 
- Name your repository [YOURNAME.github.io]. 
- Ensure that "Copy the Master branch only" is selected.
- Click "Create Fork".
- You will see a new repository that looks identical to the Beautiful Jekyll GitHub repository. 
	- While it may seem initially intimidating, you will only ever be engaging with a select few folders and files. Before we continue, if you would like to read more about what each file and folder represents, you can read more. This specific folder has been written for Minima but it equally applies to Beautiful Jekyll: [[Minima Folder and Files Breakdown]]. 
- Enter the config.yml file and input the information below:
	- Title
	- Name
	- Email
	- Description
- Do not add to the "Author" tab. Leave that blank. 
- Once you have finished inputting the information in the config.yml file, make sure that you commit (save) the file. 

What happens to our site now that we have changed the information?

Let us return to our GitHub repository. Where would we go to change the information in the "About" tab? 

## About 
- In the "aboutme.md" file, click "edit this file" (the icon should look like a pencil on your screen).
- Delete the information beneath the three dashes.
- Copy [this information](https://raw.githubusercontent.com/susannalles/DHPracticum_Spring23/gh-pages/exercises/2.Jan_25_2023.md) into your "About" file.
	- Only copy and paste the text that begins with "# Your Name" and ends with "Write some useful links for you". 
- Fill out the information.
- You should now have a customized "home" page and "about" page.

Where would we go if we wanted to change, edit, or add to the posts that we see on our home page? 

## Posts
- Click on the "posts" folder in our GitHub repository. 
- We are going to try our hand at creating a simple post with a few additional elements. 
- Click "add file" and "create new file".
- You will be asked to input a file name and content. For the file name, you must put a very specific set of information to have Jekyll register your post. For this exercise, title your file: "2024-02-08-workshop-example.md". 
	- As a reminder, for blog style themes using Jekyll, you should always title your posts "YYYY-MM-DD-title-post.md".
- In the "Edit new file" box, we must first add our metadata. 
- In line 1, add three dashes (---)
- In line 2, write "layout: post"
- In line 3, give your post any title. 
	- For a title, make sure that it is written between quotation marks.
- In line 4, close this out with three dashes (---).
- Skip one line after the final three dashes. 
	- It should look something like this:

```
---
layout: post
Title: "Workshop Post"
---

This is a sample post. 

# This is a sample post
I have written this post for the workshop with Professor Josephs!
```

- At this point, feel free to free write while also using the Markdown syntax guide. Experiment with the syntax guide. Feel free to post once you feel ready. 
- After a few moments, your post should appear on your home page!

Throughout this presentation, we have attempted to show you the various ways that you can design and populate a GitHub page. We have shown you a very simple GitHub repository and a more advanced, but still manageable, GitHub theme using Jekyll. The information that you have learned here is transferable to any other Jekyll themes you may use. 

If, after leaving here, you would like to experiment with other GitHub and Jekyll themes, I have left a list of themes for you to peruse and explore. 

Here are some sample sites that were built following the above instructions:
1. https://mrileysoriano.github.io/githubworkshop/
2. https://mikesori.github.io/

# Caribbean Keywords Site
![[keywords_1.png]]

![[keywords_2.png]]

Now that we have built our own sites, and seen how the backend operates, we can now explore the "keywords-caribbean-studies" GitHub. You can find the repository here: https://github.com/roopikarisam/keywords-caribbean-studies.

Navigating the keywords Github is much like navigating the [[Minima Folder and Files Breakdown]] from earlier. 

Let's go ahead and take a look at one of the keywords. For this exercise, we will be looking at this link: https://raw.githubusercontent.com/roopikarisam/keywords-caribbean-studies/master/_posts/2020-11-11-spirituality.md. 

Together, we will look at this link against the user-facing material: https://thecaribbeandigital.org/keywords/2020/11/11/spirituality/.

Here, you can see how raw code translates to the webpage. Notice that all of the keywords are included in the posts section, whereas additional materials are located outside of the posts page. 

We can review these two links together during the course of our session but if you have any questions, feel free to reach out!

# Concluding Thoughts
We recommend, in order to streamline your GitHub workflow, downloading a Markdown editor, such as [Obsidian](https://obsidian.md) or [Visual Studio Code 2](https://code.visualstudio.com/Download). There are many excellent free and paid Markdown editors. We recommend experimenting with the free software to determine the one that you like the best.  

Using these editors, you will no longer need to write directly in GitHub, as we have done throughout this presentation. Instead, you can write posts or webpages in your Markdown editing software and upload these files (stored locally in your machine) to the GitHub servers using [GitHub desktop](https://desktop.github.com). With GitHub desktop, you can upload Markdown files directly from your computer into the GitHub desktop interface without needing to enter the online GitHub repository.

Again, we believe that GitHub and Markdown function as important tools not only for digital humanists but humanists more generally. Using these tools, we can produce light-weight, non-technologically taxing static websites that exist online or as a series of files on a computer. Using GitHub and Markdown allows us, as humanists and researchers, to compile online resources or written materials and provide these materials to communities with low-data bandwidth or limited phone usage. While these tools are not perfect, we believe they function as an important step in maintaining and preserving digital materials and digital footprints that are liable to disappear if improperly stored and maintained. 
