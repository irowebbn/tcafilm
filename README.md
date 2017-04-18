# TCA French Film Festival
Every year, the students in Trinity Christian Academy's French program compete in a the prestigious Trinity Cannes Film Festival, vying for the coveted Palm d'Or. All films are student made and must be entirely in French. All the entries that are recieved in the correct format are listed in under the class level for which they were produced (French I - IV), while the winners are listed on the home page.

## How to edit

 You must be in the _gh-pages_ branch for changes to work 

### Adding a video for a class

Each class level has its own file in the main folder. These are named _French1.md_, _French2.md_, etc. 

Each file has a header with the information about the page. This is so Jekyll can show the file correctly on the site. The header is bounded by three hyphens like below:

  ```
  ---
  layout: page
  title: French 1
  published: true
  ---
  ```

Below that there is a year heading. Beneath this, but above ther other content is where the video will be placed. Notice there is a pound sign before the year. This is because it is a first level heading, and headings are made with pound signs in Markdown, the type of file this is. If you need to learn markdown, here's a [good source](https://daringfireball.net/projects/markdown/syntax).

Make a level-3 heading (3 pound signs and a space, ### ) with the tile of the film. If it has accented characters, use copy and paste to place them in the code.

Enter down another line and paste the embed code for the video. If the video is from YouTube, this is as simple as clicking share under the title on YouTube, selecting embed and copying everything in the box.

![Copying embed code from youtube image](https://www.easygenerator.com/wp-content/uploads/2016/05/1.png)

For a video on Google Drive, select the embed code in the same manner:

![Copying embed code Google Drive](http://blogs.acu.edu/adamscenter/files/2015/01/6.-Choose-embed.png)

For Google Drive videos, it is necessary to change the size to `width="560" height="315"` in order to match the size of the YouTube embeds.

If there is a description for the video, just paste it below the embed.

When all else fails, just look at the pattern that's already there and follow it.

### Adding a Palm d'Or Winner

Winners are special. To help make them more special, they have a speacial place on the website. Each one has its own page, and also automatically appears on the home page. To this create a file in the _posts_ folder and name it `yyyy-mm-dd-name-with-dashes-for-spaces` where `yyyy` is the year, `mm` is the month, and `dd` is the day. Each of the winner posts is called _2016 Palm d'Or_ or something, so the year will be in the filename twice, like `2017-4-16-2017-Palm-d'Or`.

Each of these files is structured like the class level pages. There needs to be a header that looks like the following:

```
---
published: true
---
```

Below that there is a third level header with the title, the embed code for the video, and a short description of the video (hopefully in French).

Once this file is created and committed, it will show up on the homepage. Again, look at the existing examples for reference.

Bon chance!

-- Isaac

Below is information about how the site works, from the original creator of the site design.

## About the theme

# Hyde

Hyde is a brazen two-column [Jekyll](http://jekyllrb.com) theme that pairs a prominent sidebar with uncomplicated content. It's based on [Poole](http://getpoole.com), the Jekyll butler.

![Hyde screenshot](https://f.cloud.github.com/assets/98681/1831228/42af6c6a-7384-11e3-98fb-e0b923ee0468.png)


## Contents

- [Usage](#usage)
- [Options](#options)
  - [Sidebar menu](#sidebar-menu)
  - [Sticky sidebar content](#sticky-sidebar-content)
  - [Themes](#themes)
  - [Reverse layout](#reverse-layout)
- [Development](#development)
- [Author](#author)
- [License](#license)


## Usage

Hyde is a theme built on top of [Poole](https://github.com/poole/poole), which provides a fully furnished Jekyll setup—just download and start the Jekyll server. See [the Poole usage guidelines](https://github.com/poole/poole#usage) for how to install and use Jekyll.


## Options

Hyde includes some customizable options, typically applied via classes on the `<body>` element.


### Sidebar menu

Create a list of nav links in the sidebar by assigning each Jekyll page the correct layout in the page's [front-matter](http://jekyllrb.com/docs/frontmatter/).

```
---
layout: page
title: About
---
```

**Why require a specific layout?** Jekyll will return *all* pages, including the `atom.xml`, and with an alphabetical sort order. To ensure the first link is *Home*, we exclude the `index.html` page from this list by specifying the `page` layout.


### Sticky sidebar content

By default Hyde ships with a sidebar that affixes it's content to the bottom of the sidebar. You can optionally disable this by removing the `.sidebar-sticky` class from the sidebar's `.container`. Sidebar content will then normally flow from top to bottom.

```html
<!-- Default sidebar -->
<div class="sidebar">
  <div class="container sidebar-sticky">
    ...
  </div>
</div>

<!-- Modified sidebar -->
<div class="sidebar">
  <div class="container">
    ...
  </div>
</div>
```


### Themes

Hyde ships with eight optional themes based on the [base16 color scheme](https://github.com/chriskempson/base16). Apply a theme to change the color scheme (mostly applies to sidebar and links).

![Hyde in red](https://f.cloud.github.com/assets/98681/1831229/42b0b354-7384-11e3-8462-31b8df193fe5.png)

There are eight themes available at this time.

![Hyde theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

To use a theme, add anyone of the available theme classes to the `<body>` element in the `default.html` layout, like so:

```html
<body class="theme-base-08">
  ...
</body>
```

To create your own theme, look to the Themes section of [included CSS file](https://github.com/poole/hyde/blob/master/public/css/hyde.css). Copy any existing theme (they're only a few lines of CSS), rename it, and change the provided colors.

### Reverse layout

![Hyde with reverse layout](https://f.cloud.github.com/assets/98681/1831230/42b0d3ac-7384-11e3-8d54-2065afd03f9e.png)

Hyde's page orientation can be reversed with a single class.

```html
<body class="layout-reverse">
  ...
</body>
```


## Development

Hyde has two branches, but only one is used for active development.

- `master` for development.  **All pull requests should be to submitted against `master`.**
- `gh-pages` for our hosted site, which includes our analytics tracking code. **Please avoid using this branch.**


## Author

**Mark Otto**
- <https://github.com/mdo>
- <https://twitter.com/mdo>


## License

Open sourced under the [MIT license](LICENSE.md).

<3
