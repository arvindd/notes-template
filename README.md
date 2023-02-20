# Introduction
This template is for creating org-mode notes system on your own local computer. Optionally, it also allows you to publicly share your notes on the internet via a [hugo](https://gohugo.io/)-generated static website.

# Getting started
Just use the "Use Template" button above to create a repo in your own github account. Once done, clone that repo to your local machine. That's it - you now have a note-taking system on your machine.

# Where should I add my notes?
All notes are in the "content" folder. You can have the notes written in markdown, emacs org-mode or any format that hugo supports.

# How can I write my notes?
Use any text editor for writing your notes. Emacs can help in creating org-mode files, but there are also other editors that can be used to create markdown files. 
  
# How can I share my notes publicly on the internet?
The whole point of having this template is precisely to enable this (otherwise, you should have simply got an emacs with org-mode for your local notes and not have to go through cloning this template).

The template contains a hugo site pre-configured with [docsy theme](https://www.docsy.dev/). This allows all your notes to be built bu hugo to generate a static website that you can host anywhere - github pages, netlify, etc.

# Do you have any emacs tips for me?
## Use of pre-configured emacs
Well, to use a pre-configured emacs environment, [clone this repo](https://github.com/arvindd/.emacs.d) in your home directory. Copy the file .emacs in the cloned .emacs.d repo to the home directory. 

Now, when you open emacs, it will automatically open a notes.org file in a directory ".notes" in your home directory.

## Using .emacs.d with this template
Emacs opened after cloning .emacs.d repo will search for notes in the ~/.notes folder. Since the notes repo that you cloned above will have a "content" folder in which notes are present, the best way to use .emacs.d with notes repo is by creating a symbolic link ".notes" in home directory to that content folder:

On linux:

```
ln -s <path-to-notes>/content ~/.notes
```

On windows (powershell), from the home directory:

```
cmd /c mklink /d <path-to-notes>/content .notes

```

On windows (command prompt), from the home directory:

```
mklink /d <path-to-notes>/content .notes
```

Now, whenever you write notes, you can use emacs to write. When you want to share the notes on a public static-page, use hugo from the root directory of notes. 

# Automation
When you connect github-actions or netlify to trigger a hugo build whenever you push a commit to github - you'll see magic happen! Netlify (or github pages, or any other similar service) can automatically build the static web page with your notes content and also deploy them on the web. 

This will make sure that your notes is accessible not just on your own computer, but also on a page that you can access anywhere.



