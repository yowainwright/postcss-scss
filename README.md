# Postcss scss 🎨

The setup of this repository is to be able to smoothly transition from scss to postcss and not need a postcss config in another project. 

I think I was able to do it. Look at the [config](https://github.com/yowainwright/postcss-scss/blob/master/package.json#L31-L37) to decide for yourself! 

> **Note:** I made the [browserlist](https://github.com/yowainwright/postcss-scss/blob/master/package.json#L31) really broad to ensure that [autoprefixer](https://github.com/postcss/autoprefixer) is working (and it is!).

---

## Install

```sh
npm install autoprefixer postcss postcss-advanced-variables postcss-cli postcss-nested postcss-scss
# 🚀
```

---

## Setup

```javascript
"devDependencies": {
  "autoprefixer": "^10.2.5",
  "postcss": "^8.2.8",
  "postcss-advanced-variables": "^3.0.1",
  "postcss-cli": "^8.3.1",
  "postcss-nested": "^5.0.5",
  "postcss-scss": "^3.0.5"
},
// do not use this browserlist
// it was just used to insure autoprefixer is working
// Read https://github.com/postcss/autoprefixer#browsers for more detail 📚
"browserslist": [
  ">0.2%",
  "not dead"
],
// the order of postcss execution matters below 👮‍♀️
"scripts": {
  "build": "postcss src/index.scss --syntax postcss-scss -u postcss-nested -u postcss-advanced-variables autoprefixer -o dist/index.css"
}

```
---

Thanks to [Craig Buckler](https://twitter.com/craigbuckler) for his great Sitepoint [post](https://www.sitepoint.com/postcss-sass-configurable-alternative/). 🙏



