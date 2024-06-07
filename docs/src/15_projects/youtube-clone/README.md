# Building a YouTube Clone Step by Step: HTML and CSS Project

In this comprehensive tutorial where we will build a YouTube clone from scratch using HTML and CSS. By following this step-by-step guide, you'll learn how to create layouts and add content, ultimately gaining valuable skills in web development.

## Introduction

In this tutorial, we'll break down the YouTube clone project into smaller units, making it easier to understand and build. Here's an overview of what we'll cover:

1. Understanding the structure and layout of the YouTube clone.
2. Creating the HTML structure.
3. Styling the layout with CSS.
4. Adding content to the header, sidebar, and content sections.
5. Making the YouTube clone responsive using media queries.

Let's dive in!

## YouTube Clone Breakdown

Before we start coding, let's understand the structure of the YouTube clone we'll be building. The website consists of the following major units:

1. **Header:** Contains three sections - left, center, and right.
2. **Main Body:** Divided into sidebar and content sections.
3. **Sidebar:** Contains navigation links.
4. **Content:** Displays videos.

## Step 1: Creating the HTML Structure

Let's begin by setting up the basic HTML structure for our YouTube clone.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <link rel="stylesheet" href="styles/index.css">
    <title>YouTube Clone with HTML & CSS</title>
</head>
<body>
    <header class="header"></header>
    <main>
        <div class="side-bar"></div>
        <div class="content"></div>
    </main>
</body>
</html>
```

## Step 2: Styling the Layout with CSS

Now, let's add CSS to style our YouTube clone layout.

```css
/* Importing Google Font */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

/* Reset HTML default styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Set the font-family */
body {
  font-family: 'Roboto', sans-serif;
}

/* Style the header */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  padding: 15px;
}

/* Set the height of the main section */
main {
  height: calc(100vh - 70px);
  display: flex;
  background-color: #f9f9f9;
}

/* Style the sidebar */
.side-bar {
  height: 100%;
  width: 17%;
  background-color: white;
  overflow-y: hidden;
}

/* Add media queries for responsiveness */
@media (max-width: 768px) {
  .side-bar {
    display: none;
  }
}
```

## Step 3: Adding Content to the Header Section

Let's divide the header into three sections - left, center, and right - and add content accordingly.

```html
<header>
    <div class="logo left">
        <i id="menu" class="material-icons">menu</i>
        <img src="https://www.freecodecamp.org/news/content/images/2022/01/yt-logo.png">
    </div>

    <div class="search center">
        <form action="">
            <input type="text" placeholder="Search">
            <button><i class="material-icons">search</i></button>
        </form>
        <i class="material-icons mic">mic</i>
    </div>

    <div class="icons right">
        <i class="material-icons">videocam</i>
        <i class="material-icons">apps</i>
        <i class="material-icons">notifications</i>
        <i class="material-icons display-this">account_circle</i>
    </div>
</header>
```

## Step 4: Adding Content to the Sidebar

Now, let's add navigation links to the sidebar section.

```html
<div class="nav">
    <a class="nav-link active">
        <i class="material-icons">home</i>
        <span>Home</span>
    </a>
    <!-- Add more navigation links here -->
    <hr> <!-- Add a line to separate sections -->
    <!-- Add more navigation links here -->
</div>
```

## Step 5: Adding Videos to the Content Section

Finally, let's add videos to the content area.

```html
<div class="videos">
    <!-- Video 1 -->
    <div class="video">
        <div class="thumbnail">
            <img src="https://img.youtube.com/vi/zUwB_imVjmg/maxresdefault.jpg" alt="">
        </div>
        <div class="details">
            <div class="author">
                <img src="https://yt3.ggpht.com/bpzY-S4DYlbTeOpY5hIA7qz_hcbMkgvLAugtwKBGTTImNnWAGudX0y53bo_fJZ0auypxrWkUiw=s88-c-k-c0x00ffffff-no-rj" alt="">
            </div>
            <div class="title">
                <h3>Introverts & Content Creation | Sumudu Siriwardana</h3>
                <a href="">Francesco Ciulla</a>
                <span>2M Views • 3 Months Ago</span>
            </div>
        </div>
    </div>
    <!-- Add more videos here -->
</div>
```

## Step 6: Making the YouTube Clone Responsive

To make our YouTube clone responsive, let's use CSS media queries.

```css
@media (max-width: 768px) {
    .side-bar, .search {
        display: none;
    }
}

@media (max-width: 900px) {
    .search input {
        width: 25rem;
    }
}
```
