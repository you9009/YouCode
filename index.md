---
layout: default
title:  "Welcome to Jekyll!"
---

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/youux/youux/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/youux/youux/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.


```js
// 这题有点歧义,所以我就都写了
// 第一种:绿灯1秒亮一次,黄灯2秒亮一次,红灯3秒亮一次
const promise = new Promise((resolve) => resolve())
promise.then(() => {
  setInterval(green, 1000)
  setInterval(yellow, 2000)
  setInterval(red, 3000)
})

// 第二种:依次亮起,每隔1秒绿灯亮一次,每隔2秒黄灯亮一次,每隔3秒红灯亮一次
const lamp = (openLamp, timer) => {
  return new Promise((resolve) => {
    setTimeout(() => {
      openLamp()
      resolve()
    }, timer)
  })
}

const lampRun = () => {
  lamp(green, 1000)
    .then(() => lamp(yellow, 2000))
    .then(() => lamp(red, 3000))
    .finally(() => lampRun())
}
lampRun()
```
