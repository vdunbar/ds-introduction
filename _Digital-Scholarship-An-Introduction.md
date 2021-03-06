## Markdown Flavours

**Pandoc**

There are several different applications that are able to convert your marked up, plain text document, into a formatted document. We'll look at a couple of these, and in so doing, also become a little more familiar with the command line.

Pandoc is an amazing document conversion tool; there is virtually no document format that Pandoc cannot handle. Pandoc does not have an interface that we can interact with the point and click of a mouse. We access it exclusively through the command line. We're not going to explore it in depth here, we're just going to work through one example of what we can do with our markdown document.

Pandoc, at its simplest take two arguments, the name of an output file and the name of an input file. The input file is the file you've created and will include the file type designation, that is <code>.md</code> The output file name will be whatever you wish to call the new file and will include the file type designation that you want to convert to. To keep things simple, we'll keep the same file name. And since we're planning on publishing to the web, we'll convert this to html using the file ending <code>.html</code>

The formula is

```
pandoc -so outputFile inputFile
```

The <code>-so</code> ensures that we have a stand alone html web page that is sent to a file. The details of this are of little consequence at this stage, but we can discuss further if people are interested.

```
pandoc -so myfile.html myFile.md
```

Now that we've done the conversion, let's look at the product!

**Typora**

When it comes to applications in which we can author markdown documents, all you need is a plain text editor that comes packaged with your operating system.

There are, however, numerous applications that allow you to interact with your content in different ways. One that I like to use exclusively for writing prose is Typora, which does live rendering of your markdown content. In fact, this content was all written using Typora, but was rendered to html using RMarkdown which uses Pandoc, and then published to GitHub pages.

Let's take a quick look at what our content looks like in Typora

Mac

```
open -a Typora myFile.md # open file in Typora
```

PC

```
? myFile.md
```

There are numerous other markdown editors out there. You can access a comprehensive list from the [Markdown Guide](https://www.markdownguide.org/tools/).

Three others which I think are worth noting in terms of how they use markdown to implement some interesting authoring formats include

**Obsidian** which build a network mind map of all the documents that you author it allowing you to easily connect documents

**Joplin** which is designed for note taking and takes elements from EverNote or OneNote and implements them in markdown

**Atom** which is a popular text editor for all kinds of editing and coding and provides you with a side by side window to see your raw markdown content alongside a formatted rendition.

## GitHub Pages

### How GitHub Pages Works

In the same way that we converted our markdown document to html using Pandoc, GitHub pages uses another application called Jekyll to render your markdown files as html. And Jekyll requires much less work to get a nice, functional webpage.

A note on how web pages work. The landing page for any website is always called <code>index.html</code> This is a web authoring standard. GitHub Pages and Jekyll thus require that your landing page markdown document be called <code>index</code>, but we're working in markdown, so we'll call it <code>index.md</code>

Let's do that now in our terminal...

```
mv myFile.md index.md # rename to index.md
```

### Moving into GitHub

Let's log in to our [GitHub account](https://github.com/).

We'll now create a repository. We're going to strictly engage with GitHub as a web authoring tool at the moment. GitHub is, first and foremost, and web based implementation of the version control system Git, which is brilliant, but a workshop for another day.

So after setting up our repository, we'll select the link to \"upload an existing file\" and we'll upload out index.md file. Now it's just a matter of a couple of settings!

_config.yml

```
theme: jekyll-theme-cayman
title: Mathew's Page
github:
  is_project_page: false
```









readme file
