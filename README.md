# NATURE TOURS

A template website made using SASS (SCSS) [A CSS pre-processor] for a touring business/company. The template is live **[here](https://naturetours-ram.netlify.app/)**. The parent repository is **[here](https://github.com/Ch-sriram/css-sass)**.

## Details on package.json

<pre>
{
  "name": "nature-tours",
  "version": "1.0.0",
  "description": "landing page for nature tours",
  "main": "index.js",
  "scripts": {
    "watch:sass": "node-sass ./sass/main.scss ./css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel watch:sass devserver",

    "compile:sass": "node-sass ./sass/main.scss ./css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b \"last 10 versions\" css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.min.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },
  "author": "Ch Sriram",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^9.7.6",
    "concat": "^1.0.3",
    "node-sass": "^4.13.1",
    "npm-run-all": "^4.1.5",
    "postcss-cli": "^7.1.1"
  }
}
</pre>

We can see that **node-sass**, **autoprefixer** (needs **postcss-cli** to run), **concat** & **npm-run-all** packages are installed as devDependencies (under **devDependency**). 

We can see how the **"scripts"** are defined in package.json file. The two main scripts related to development and deployment are <code>npm run start</code> and <code>npm run build:css</code>.