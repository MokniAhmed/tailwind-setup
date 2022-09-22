# Installation &amp; commissioning of Tailwind 
## Using PostCSS
Complete tutorial on how to install TailWind as PostCSS in VSCode. 
  
**Step-1 Install NodeJS**  
You need to install Node JS before starting TailWind CSS Download Node JS at nodejs.org/en/download. Then install it on your system.  
  
**Step-2 Make package.json file**
```
npm init
```
  
**Step-3 install tailwind and postcss**
```
npm install -D tailwindcss postcss-cli autoprefixer
```
  
**Step-4 make postcss.config.js**
```
touch postcss.config.js
```
  
**Step-5 add base config to postcss.config.js**
```
module.exports = {
    plugins: {
      tailwindcss: {},
      autoprefixer: {},
    }
  }
```
  
**Step-6: make tilwind.config.js file**
```
touch tailwind.config.js
```
  
**Step-7: config for tailwind.config.js**
```
module.exports = {
  content: ["./*.{php,js,html}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```
  
**Step-8: make src dirs**
```
mkdir public && mkdir public/assets/ && mkdir public/assets/css/ && mkdir public/assets/js/ && mkdir public/assets/img/
```
  
**Step-9: make tailwindcss file**
```
touch tailwind.css 
```
  
**Step-10: import base tailwind to /src/css/tailwind.css file**
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
  
**Step-11: make index.html file**
```
touch ./index.html
```
  
**Step-12: auto watch tailwind with package.json**
```
"scripts": {
  "startcss": "postcss ./tailwind.css -o ./public/assets/css/style.css --watch"
},
```
  
**Step-13: link tailwind to index.html**
```
<link rel="stylesheet" href="./public/assets/css/style.css">```
  
```
**Step-14: run tailwind compile to css taske**
```
npm run startcss
```



