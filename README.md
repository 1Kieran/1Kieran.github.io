# **Hosting a Resume on GitHub**
***
## **Content**
***
  - [**Purpose**](#purpose)
  - [**Prerequisites**](#prerequisites)
  - [**Instructions**](#instructions)
  - [**More Resources**](#more-resources)
  - [**Authors and Acknowledgments**](#authors-and-acknowledgments)
  - [**FAQ**](#faq)
***
## **Purpose**
***  
This document will serve as a guide on how to host a resume on GitHub. Additionally, this document will introduce the principles of technical writing outlined in Andrew Etter's book [_Modern Technical Writing_][Andrew's Book]. Hosting a resume will serve as an example of how to apply Etter's principles. After completing this tutorial, the reader should be able to host a Markdown formatted resume with their GitHub profile.
***
## **Prerequisites**
***
1. A MarkDown formatted resume
2. A GitHub account

Information on how to get started with MarkDown [More Resources](#more-resources) section
***
## **Instructions**
***
_Modern Technical Writing_ outlines three key principles.
1. Use a lightweight markup language
2. Share/host documents on a distributed version control system
3. Format a document with a static site generator

These principles will be used as guides for creating a static site for your resume 

### **Lightweight Markup Language** 

Etter's Book suggests the uses of lightweight markup languages to create technical documents. This type of document has several clear advantages over pure XML or PDFs. Namely, lightweight markup languages are easy to create, easy to host and many are free to use. One such example is MarkDown. MarkDown is easy to learn, [this MarkDown tutorial][MarkDown tutor] claims it can be completed in 10 minutes. Because there is little for syntax lightweight markup languages are much easier that XML to read. These languages can easily be converted into XML so they can generate static sites. 
 
Since a MarkDown formatted resume is a prerequisites, this guide will not go into detail on the creation of a Markdown Resume. Please refer to [More Resources](#more-resources) for helpful links to get started writing in MarkDown.

### **Host Documents on a Distributed Version Control System** 

The next important principle from _Modern Technical Writing_ is the use of distributed version control systems. Distributed version control systems allow users to easily concurrently collaborate with others and revise. This means that a document can easily be updated so that other users can see. It also means that users can view older versions of a document. In the case of a resume, it is extremely important that it is a living document as the writer gains new experience or even jobs.  

One of the most popular distributed version control systems is GitHub. GitHub hosts repository. Repositories are a  collection of document. GitHub makes it easily to update this collection. GitHub will serve as this guide's distributed version control system. For a more detailed introduction to GitHub refer to the [More Resources](#more-resources) section.


### **Format with Static Site Generator**

The final principle is the use of a static site generator. Static sites have many benefits, including quickly load times and extreme portability. Static site generators can help to create these sites quickly with a Markdown file and some styling. This simplicity means that updating a static site is as simple as changing the Markdown file and run the generator again. This tutorial will use Jekyll as a static site generator. Jekyll allows the user to easily create a static site through a GitHub repository. With Jekyll, this site can be  customized easily but changing the Jekyll theme employed. This static site generation means that the style of a resume and its content can be changed in a matter of minutes.

### **Website Generation**

With these three tool we can now generate a website for your resume
1. Begin by creating a [GitHub account][GitHub Create]
2. Navigate to your GitHub profile page
3. Go to the Repositories page 
4. Create a new repository and title it "your-user-name.github.io" replacing "your-user-name" with your github user name
5. Click add new while in the repository
6. Upload your Markdown resume
7. commit this upload
8. Change the file name of your resume to index.md
9. Add the below text to the top of your resume
    ```
      ---
      title: "new title"
      ---
    ```
    Replace new title with what ever you would like your resumes page to be called. The three lines on top and bottom indicate that this is Jekyll code. This Jekyll code is setting the static websites title.
10. Commit the file name change and the edit of the resume
11.  Next create a new file called _config.yml this is the Jekyll configure file that will be used to style the presentation of your resume
12. Find the GitHub supported Jekyll themes in the [More Resources](#more-resources) section 
13. Pick a theme from the list of supported themes. For example the cayman theme
14.  Return to the _config.yml file and add this line
      ```
        theme: jekyll-theme-cayman   
      ```
      here we are configuring how Jekyll (a static site generator) will create the static site for the resume
      This example uses cayman but this can be replace by any other GitHub supported Jekyll themes from the list found in [More Resources](#more-resources)

15. Commit the new _config.yml to your repository
16.   The static website is now ready to be generated. Simply go the domain "your-user-name.github.io" replacing your-user-name with your GitHub user name.  
  GitHub pages has used Jekyll to generate a static site for your resume. This happen by index.md file into XML and then the Jekyll theme uses CSS and Javascript to stylize your page.

Here is an example with cayman styling
![Hosted Resume](TechCommA2.gif)
 
***
## **More Resources**
***
* [How to work on MarkDown with VSCode][MarkDown VSCode]
* [Getting Started with writing MarkDown][MarkDown tutor]
* [Create a GitHub Account][GitHub Create]
* [GitHub Introduction Course][GitHub Intro]
* [Andrew Etter's book][Andrew's Book]
* [GitHub Supported Jekyll Themes][GitHub Themes]

***
## **Authors and Acknowledgments**
***
* Written by Kieran Ketelsen
* Reviewed by Chowdhury Abdul Mumin Ishmam, PokYee Tsu, SungJae Hyun and Zhong He
* [Credit to Cayman theme][Cayman Theme]

***
## **FAQ**
***
1. Why is Markdown better than a word 
processor?

    Markdown allows us to use tools like Jekyll to quickly change the styling of our document as well as markdown easily translates in to XML. Word lacks both of these features.  

2. Why does is my static site not displaying the changes i made to my styling or content?

      GitHub can take awhile to sync up old files with new ones. Try checking again in a few minutes.


[MarkDown VSCode]: https://code.visualstudio.com/docs/languages/markdown
[MarkDown tutor]: https://www.markdowntutorial.com
[Andrew's Book]: https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS
[GitHub Create]: https://github.com/join
[GitHub Intro]: https://lab.github.com/githubtraining/introduction-to-github
[GitHub Themes]: https://pages.github.com/themes/
[Cayman Theme]: https://github.com/pages-themes/cayman