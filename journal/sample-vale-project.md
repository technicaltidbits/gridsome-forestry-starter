---
date: 2020-05-28
title: "How to apply the Vale CLI"
author: Deanna 
excerpt: Learn how to apply the Vale CLI to Markdown files in this tutorial.
---

## Prerequisites

* A code editor, like VS Code or Atom
* The Vale-compatible implementation of the Microsoft Style Guide, which you can download [here](https://github.com/errata-ai/Microsoft/releases/download/v0.7.0/Microsoft.zip).

## Assumptions

* You've read [this](https://technicaltidbits.net/projects/config-vale/) post about the basics of the Vale configuration file.
* You have some familiarity with the command line.

## Step 1. Create project folder

In the terminal, create a new folder called `vale-tutorial`:

```bash
user$ mkdir vale-tutorial
```

## Step 2. Add project files

Change directories to the `vale-tutorial` folder:

```bash
user$ cd vale-tutorial
```

Create a `.vale.ini` file in the `vale-tutorial` folder:

```bash
user$ touch .vale.ini
```

Next, create a Markdown file called `sample-file`:

```bash
user$ touch sample-file.md
```

Finally, create a `styles` folder:

```bash
user$ mkdir styles 
```

Your project structure now looks like this:
```
vale-tutorial
├── .vale.ini
├── sample-file.md
└── styles  
```

## Step 3. Add Microsoft rules to styles folder

Download and open the zip file containing the Microsoft style guide's rules. Then move the `Microsoft` folder to the `styles` folder. Now, your project structure looks like this:

```
vale-tutorial
├── .vale.ini
├── sample-file.md
└── styles
    └── Microsoft  
```

## Step 4. Edit the .vale.ini file in your code editor

### StylesPath

In the `.vale.ini` file, set the `StylesPath` to `styles`. Remember: this is where you tell Vale where to look for any external styles. 

### MinAlertLevel

Next, set `MinAlertLevel` to `suggestions`. If you remember, you can set this value to show errors, errors and warnings, or errors, warnings, and suggestions. 

//TODO format

### BasedOnStyles

Set `BasedOnStyles` to `Vale, Microsoft`. Don't forget to add [\*] so these styles are applied to all files.

Your `.vale.ini` file looks like this once you're done:

```ini
StylesPath = styles

MinAlertLevel = suggestions

[formats]
mdx = md

[*] 
BasedOnStyles = Vale, Microsoft
```

## Step 5. Add content to sample-file.md

Copy these three paragraphs and paste them into the `sample-file.md` file: 

> `This is a sampl file that we can use to tst the Vale CLI. There are 2 things that you need to know about using it. Ergo There are plenty of cool things you can do with this linter...`

> `In this tutorial, you will learn how to install Vale, a style linter this tool allows you to tst your doc file for style and grammar.`

> `When a software developr tests their code, he may test the application's functionality or look for any security issues in their code. When technical writers test their documentation, we may check to assure that the links are not broken, the style is consistent, and that there are not grammar, spelling, or punctuation errors.`

Some of the errors are a bit obvious (e.g. "sampl" for "sample"), but the point is to show you how Vale brings these errors to your attention so you can address them *before* you publish your documentation.

## Step 6. Run the linter

In your code editor, run the command `vale sample-file.md`. You'll see the errors, warnings, and suggestions Vale finds in the files, in addition to the number of errors, warnings, and suggestions:

```ini
6 errors, 4 warnings and 5 suggestions in 1 file.
```

You can see that most of the errors, warnings, and suggestions break Microsoft's rules. `Vale.Spelling` caught several typos: 

```ini
1:11   error       Did you really mean 'sampl'?    Vale.Spelling
1:41   error       Did you really mean 'tst'?      Vale.Spelling  
4:94   error       Did you really mean 'tst'?      Vale.Spelling            
6:17   error       Did you really mean             Vale.Spelling            
                    'developr'? 
```