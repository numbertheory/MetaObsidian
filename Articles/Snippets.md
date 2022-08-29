# Snippets

## Install
Snippets are how you can inject additional CSS into the rendered pages without having to mess with your theme. Snippets are also independently enabled, so when you change themes, the snippets are still enabled.

To enable snippets in your vault:
- Go to Settings: `⌘+,`
- Go to Appearance
- Scroll down to CSS Snippets

If you do this in this vault, you'll see `metastyle` is already enabled. If there are no snippets enabled for your vault, click the 📂 icon to browse to the `.obsidian/snippets` folder. Create a blank file called `metastyle.css` (or whatever you want to call it). This will be where you'll save the CSS snippets described in this page, and any other CSS you want to enable for your vault.

Once created click the 🔁 icon to rescan the folder, and enable the CSS file you've created:

![[snippets-enabled.png | three-quarters]]


## Examples
### Image resizing
Source: [Elijah Yap - YouTube](https://www.youtube.com/watch?v=_nPHXKvPUi4)

By default, the image embedding in Obsidian is the full size of the image. If you're using screenshots, this can produce image embeddings that are too big for any reasonable markdown page.

```
![[Calendar.png]]
```

To enable resizing, go to your installed CSS snippets and copy this into the file. You may add as many different keywords as you need, and set the widths to whatever size you want for each keyword.
```css
img[alt~="half"] {
  width: 50%;
}

img[alt~="third"] {
  width: 33%;
}

img[alt~="quarter"] {
  width: 25%;
}
```

Finally, to set the size, use the pipe character to set the size. In this example, the `third` keyword will set the width to 33%.

```
![[Calendar.png | third]]
```