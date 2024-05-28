---
title: "Creating a CV using LaTeX"
date: 2024-05-28T23:52:44+02:00
draft: false
tags: ["Libre Software"]
---

# LaTeX Overview
LaTeX is a document typesetting and creation tool. It's what you use if you want to create professional looking documents, letters, presentations, lecture notes, and so on... Once you graduate from using Microsoft Office, you don't look back. There is a little bit of a learning curve in getting used to using LaTeX, since you have to get used to the fact that you're not going to be typing directly "into" your document, but it is well worth it. [Overleaf](https://www.overleaf.com/) have many very useful guides in both learning how to use LaTeX, and tools to let you create LaTeX documents in your browser. For myself personally, I use [TeXstudio](https://www.texstudio.org/) as a program for creating LaTeX documents.

# CV Template
The best way to learn how to make beautiful-looking LaTeX documents is to simply look at and copy from what other people have made. To this end, here is a [GitHub Repo](https://github.com/IzaacMammadov/CV) which contains the code that I use to make my CV, which you can find [here](https://izaac.mammadov.co.uk/CV.pdf). It has a very minimalistic finance-style layout, and only uses three very common LaTeX packages. It was created without ever manually drawing a horizontal line, or even creating an invisible table like you'd have to do if you were using Word.

# KaTeX
LaTeX becomes invaluable when it comes to typesetting mathematical equations and formulae. It is quite easy to get LaTeX to render properly on Hugo static websites using the [KaTeX API](https://katex.org/). I'd recommend following [this guide](https://mertbakir.gitlab.io/hugo/math-typesetting-in-hugo/), which is what I personally do for this website.
