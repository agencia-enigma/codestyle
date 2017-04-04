# Enigma's codestyle
These are brief guidelines to follow when you are writing or contributing on any Enigma's projects, to keep our sanity and to grow a concise and reliable legacy code. Enjoy it!

## Index

- [Commits]()
- [HTML]()
- [Template Engines]()
- [CSS]()
- [CSS Pre Processors]()

### Commits
To keep contributions easier across the globe, all of our commit messages, pull request titles, comments and issues discussions **must be in english**.

Before any commit in project, please check if exist an issue to that feature or fix you are commiting, and if true, link your commit through the use of `#` in your commit message.

Also, we need some kind of short labels on each commit message, it makes easier to identify the purpose of any commit. Our labels are divided into:

- **Fix**: When your commit fix any identified bug.
- **Feature**: When your commit introduces a new feature to the project.
- **Redo**: When you refactor anything to be better or run smoothier.

```javascript
// Bad
commit -m "New navigation dropdown menu"

// Good
commit -m "Feature: New navigation dropdown menu #302"
```

Also, always write imperative present tense:

```javascript
// Bad
commit -m "Feature: Added feature x #999"

// Bad
commit -m "Feature: Adding feature x #999"

// Good
commit -m "Feature: Add feature x #999"
```

When realeasing a new version, write a commit message in the following format "Release - v1.0.0" instead of "v1.0.0".

> Why: Makes it easier to track version releases in git history. For example, you could run git log --pretty=format:"%H %s" | grep 'Release' to fetch only version bump commits.

### HTML
Always use soft tabs with two spaces. It's highly recommended you set your editor to show invisible characters to avoid skip this.
```html
<!-- Bad -->
<div>
    <p>Lorem ipsum</p>
    
    <ul>
        <li>Item 1</li>
        <li>Item 1</li>
    </ul>
</div>

<!-- Good -->
<div>
  <p>Lorem ipsum</p>
    
  <ul>
    <li>Item 1</li>
    <li>Item 1</li>
  </ul>
</div>
```

Always use double quotes. Never single ones.
```html
<!-- Bad -->
<div class='container'></div>

<!-- Good -->
<div class="container"></div>
```

Do not include `/` to [Void Elements](https://www.w3.org/TR/html51/syntax.html#writing-html-documents-elements).
```html
<!-- Bad -->
<input name="name" />

<!-- Good -->
<input name="name">
```

Separate block elements with a single blank line and group children inner blocks.
```html
<!-- Bad -->
<div>

  <ul>
    
    <li>...</li>
    
    <li>...</li>
    
  </ul>
  
</div>
<div>
  ...
</div>

<!-- Good -->
<div>
  <ul>
    <li>...</li>
    <li>...</li>
  </ul>
</div>

<div>
  ...
</div>
```

When writing any element, you should follow this attributes order for fast reading:

1. `class`
2. `id`, `name`
3. `data-*`
4. `src`, `for`, `type`, `href`
5. `alt`, `title`
6. `aria-*`, `role`
5. `alt`, `title`

```html
<!-- Good -->
<input class="field" name="name" data-format="name" type="text" placeholder="Lorem ipsum" aria-label="Dolor sit amet">
```

You don't need to specify `type` when including CSS or JS files on your document, and always keep `rel` attribute at the end of the tag.

```html
<!-- Bad -->
<link rel="stylesheet" href="assets/css/style.css" type="text/css">
<script src="scripts.min.js" type="text/javascript"></script>

<!-- Good -->
<link href="assets/css/style.css" rel="stylesheet">
<script src="scripts.min.js"></script>
```

For better performance, always call your javascripts file before the closing `<body>`:

```html
<!-- Bad -->
<link rel="stylesheet" href="assets/css/style.css" type="text/css">
<script src="scripts.min.js" type="text/javascript"></script>

<!-- Good -->
<link href="assets/css/style.css" rel="stylesheet">
<script src="scripts.min.js"></script>
```
