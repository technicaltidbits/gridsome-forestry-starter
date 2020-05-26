---
date: 2020-05-21
year: 2020
title: "Vale Series: Configuring the Vale CLI (Part Two)"
category: Identity
thumbnail: "/uploads/coding-man.png"
categories:
- vale
- vale CLI
- test the docs
project_bg_color: ''
project_fg_color: ''
---

As I mentioned in the first part of the series, in the second part, you'll learn how to configure the Vale CLI for your documentation needs. If you haven't installed the CLI yet, follow [these](https://www.technicaltidbits.net/projects/install-vale-cli/) instructions first. 

You have the Vale CLI on your computer; now, you need to learn how to use it. To use Vale, you need to create a `.vale.ini` file. This is a configuration file that tells Vale what files to **lint**, or check, what styles to conform to, and what rules to ignore. 

> Q: *Why is there a period in front of the filename?* 
> 
> A: Any filename that begins with a period is called a **hidden file**. Hidden files are usually tucked away for a good reason: they're files that you probably shouldn't touch unless you know what you're doing. 

> Q: *What does `.ini` mean?*
>
> A: The `.ini` extension indicates that this is an **initialization** file.

## .vale.ini features

Here's a basic, bare-bones `.vale.ini` file:

```ini
StylesPath = styles

MinAlertLevel = suggestion

[formats]
mdx = md

[*] 
BasedOnStyles = Vale
```

### StylesPath
`StylesPath` represents the location of the folder that the `.vale.ini` file is in. In this example, the file is in the `styles` folder in the project.

### MinAlertLevel

When you run the Vale CLI, it displays the number of errors, warnings, and suggestions found in your file:

```ini
2 errors, 3 warnings and 3 suggestions in 1 file.
```

If you want, you can configure Vale to show errors only, errors and warnings, or show all three. For example, if you set `MinAlertLevel` to `error`, it only shows errors found in the file:

```ini
2 errors, 0 warnings and 0 suggestions in 1 file.
```

//TODO add formats

### BasedOnStyles

This is the fun part.

One of the great things about Vale is that it allows you to use third-party styles with it. If your company uses Microsoft's style guide, you can download a zip file containing files that Vale uses to implement the style guide's rules. You can also set `BasedOnStyles` to `Vale`, which is the default option.

If you want Vale to implement more than one style, separate them with a comma, as shown below:

```ini
BasedOnStyles = Vale, Microsoft
```

> Q: *What does [\*] mean?*
> 
> A: The asterisk means "apply these styles to all files." In the next part of the series, you'll learn how to customize Vale to apply styles to certain files.

So, you know what a `.vale.ini` file is and its basic components. Now, you'll create a `.vale.ini` file and run the CLI to check a sample Markdown file, using Vale's and Microsoft's style rules. To get started with the tutorial, click [here](https://technicaltidbits.net/journal/sample-vale-project).








