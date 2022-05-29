# Contributing

Adding information to the wiki is easy. 

Basically there are 2 ways to edit. You can use the web interface to propose small changes. Or you can download GitHub desktop and make large changes.

Downloading GitHub desktop is the recommended way to make changes. Please read the documentation on how to use GitHub desktop, maybe even watch some YouTube videos.

* You’ll need a GitHub account. 
* If you just want to change a few things on a specifique page then you can use the "Edit this page on GitHub" link on the bottom of a page.
* If you want to make big changes (like adding a page or a new section) then you’ll need to
     1. Download [GitHub Desktop](https://desktop.github.com/)
     2. Fork the reposity
	 3. Make your changes
	 4. Make a "pull request"

For more information on how to use GitHub check out [How to Contribute to Projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects) and [Forking a Repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo) on GitHub’s quickstart site.
For more information about GitHub Desktop check out [Installing and Configuring GitHub Desktop](https://docs.github.com/en/desktop/installing-and-configuring-github-desktop).
## Website Structure

The layout for the website is fairly simple. Each page is a `.txt` file except instead of `.txt` we call them `.md`.
Each page is a seperate `.md` file, and if a page has sub-pages below it then there will be a folder with the same name as the `.md` file.

The formatting is done automagically. Here’s a [cheatsheet](https://www.markdownguide.org/cheat-sheet/) for how to format your text.
And you can always look at other files that are already here to see how they’re formatted.

```
index.md -----------------------------------------| This is the home page.
docs/    -----------------------------------------| Everything else is under "docs/"
     auxiliary-loops/ ----------------------------| Main section
	                 12-land.md ------------------| Sub-section
	                 12-land/
	                         12-land-sorcery.md --| Sub-section
			                 deathrite-shaman.md -|
	 cabal-ritual.md  ----------------------------| These two documents stand alone
	 titanless.md     ----------------------------| and have no subsections under them.
			 
```

---

## Page Metadata

Each page has a few lines at the top to tell the program where on the website a page is supposed to live.

```
----
layout: default
title: [Name that will appear on the sidebar]
nav_order: [What order the document will be within the sidebar]
grand_parent: [Optional. Only use if the document is a sub-subsection]
parent: ["title:" of the section this document appears under]
permalink: [Optional. Only use with grand_parent. Full path to the file]
----
```

## Discussions / Other Questions

If you have *any* problems or questions (no matter how dumb you may think they are) talk to KJ in Discord or you can make a post on the GitHub [discussion](https://github.com/TheGitrogServer/thegitrogserver.github.io/discussions) page.
