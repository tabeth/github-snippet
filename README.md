# GitHub Snippet

GitHub Snippet is a way to embed a snippet of a GitHub file of your choosing into 
a website via a script tag. It leverages [highlight.js](https://highlightjs.org/) to do the
code highlighting. 

### Usage

Copy the entirety of `script.html` into the `head` of your HTML after reviewing its contents.
After that, check out the API below and use it to your satisfaction.

Here's an example
```html
<html>
<head>
<!-- script.html stuff -->
</head>
<body>
<script>(function() { loadGithubSnippet(l(), 'tabeth/blog/contents/package.json') })()</script>
</body>
</html>
```

### API

The API is simple. There are two functions you need to be aware of:

---

* `l()` 

Named for brevity, `l` should be called in the `<script>` tag directly. It will return the parent
node at the time when the `<script>` tag is being loaded. In short, this will allow you to place
the snippet where the `<script>` tag is placed.

---

* `loadGithubSnippet()`

This accepts two two parameters, an element that you want to append the snippet to the *end* of, 
and a snippet URL. The snippet URL follows the [Github
API](https://developer.github.com/v3/repos/contents/) and has the same limitations thereof. 

---

### Other Notes
The styling can be changed at your discretion by simply modifying the source code, changing 
the stylesheet in highlight.js or adding classes and using an additional stylesheet. 

### Contributing
This was made in literally an hour, so there are bound to be issues. If it's minor, open up
a request and I'll take care of it relatively quickly. Otherwise, create a pull request after
explaining the problem via an issue and I'm sure it'll be merged in.
