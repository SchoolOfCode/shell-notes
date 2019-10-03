|[home](../README.md)|

# Day 2

- Download VSCode (make sure downloaded into and run from applications)

## cmd line

- change directory `cd <path>`/ `cd ..`(up a folder)
- list directory contents `ls`
- print current path (print working directory) `pwd`
- create file `touch <newfilename>`
- create folder `mkdir`
- delete file `rm <filename>`
- delete folder and it's contents `rm -r <foldername>`
- edit file `nano <filename>`

### Git version control

- `git init`
- `git add .`
- `git commit -m "<commit message>"`
- `git status`
- `git log`

### Remote repos and colaboration with GitHub

- `git clone`
- `git pull`
- `git push`
- `git branch <newbranchname>`
- `git checkout <existingbranch>`
- `git checkout -b <newbranchname>`
- `git fetch -p`
- [Git Cheat Sheet](../resources/atlassian-git-cheatsheet.pdf)

## HTML

### Meta Tags

- The `<meta>` tag provides metadata about the HTML document.
- Metadata will not be displayed on the page, but will be machine parsable.
- Meta elements are typically used to specify page description, keywords, author of the document, last modified, and other metadata.

  ```html
  <head>
    <meta charset="UTF-8" />
    <meta name="description" content="Free Webtutorials" />
    <meta name="keywords" content="HTML,CSS,XMLJavaScript" />
    <meta name="author" content="John Dough" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  </head>
  ```

### Linking to external style sheet:

```html
<link rel="stylesheet" type="text/css" href="path_to_somthing.css" />
```

### Adding a title

```html
<title>Title Goes Here</title>
```

### Parent/Child relationship

```html
<div id="parent">
  <div id="child" />
</div>
```

## CSS

### Units

- `px`
- `%`
- `vh`
- `vw`

### Display Property

- `inline`: Displays an element as an inline element (like `<span>`). Any height and width properties will have no effect.
- `block`: Displays an element as a block element (like `<p>`). It starts on a new line, and takes up the whole width.
- `inline-block`: Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values.
- `flex`: Displays an element as a block-level flex container.

### Flex Properties

- `justify-content`
- `flex-direction`
- `flex-wrap`
- `justify-content`
- `align-items`
- `align-content`
- `flex-flow`
- [flex guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### box-sizing

- `content-box`: Default. The width and height properties (and min/max properties) includes only the content. Border and padding are not included.
- `border-box`: The width and height properties (and min/max properties) includes content, padding and border.

## Resources

- [flexboxfroggy](http://flexboxfroggy.com/)
- [flexboxdefense](http://www.flexboxdefense.com/)
- [css guide](https://cssreference.io/)

## Challenge

- Recreate [Shell Energy homepage](https://www.shellenergy.co.uk) (keep working on this)
