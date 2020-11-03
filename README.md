# Development Files Introduction

1. **./** => This is the folder in which all the development work will be done on CSS and JS files
1. **./.git** => Used for git versions controlling purpose. We don't need to do anything in this folder. It is auto generated.
1. **./node_modules** => Used for storing node packages. This folder will not available at first stage when downloaded Git repo. We don't need to do anything in this folder. It is auto generated.
1. **./src** => This is the main folder. It contains all sass and js files we will work on.
1. **./gulpfile.js** => This is gulp configuration file. You have to configure couple of things in it at first.
1. **./package.json, package-lock.json** => These files keeps record of all the Node packages we will be using. Don't modify it.
1. **./.gitignore** => This file contains list of files that don't need to be pushed to the Repo. I have already updated this file so no need to touch it aswell.
1. **./.browserslistrc** => This is a configuration file for CSS autoprefixer. No need to touch it.
1. **./.tailwind.config.js** => This is a configuration file for Tailwind CSS framework.
1. **./README.md** => Just a file for Github repo for instruction purpose.

---

# Steps for GULP

**STEP 1** - Open terminal and run below commands to setup project

```
cd myproject
git clone git@github.com:aslamdoctor/gulp-tailwind-boilerplate.git dev
cd dev
npm install
```

**STEP 2** - Open **./dev/gulpfile.js** and edit line where it says **"theme_folder"** as below and update the folder name. Keep the folder path as it is.

```
var theme_folder="../wp-content/themes/my_theme/"
```

**STEP 3** - Open terminal and run below commands as per your need.

```
npm run watch # to watch the css/js files changes
npm run build # to build the css/js files by minimizing and purging them
npm run watchwp # to watch the css/js files changes and save them inside theme folder for production use
npm run build # to build the css/js files by minimizing and purging them and save them inside theme folder for production use
```

**STEP 4** - The files on which you will be working are under

```
/dev/src/*.scss
/dev/src/*.js
```

**STEP 5** - Once development is done, close the compiler by pressing **"ctrl + c"** key on terminal.

**STEP 6** - After all is done, don't forget to push the changes on Git repo using below command so we can stay in sync.

```
git push
```

**STEP 7** - If you want to add any new SASS file, simply add it inside **/dev/src/css/** folder and it will compile automatically. Don't forget to stop gulp compiler and restart it.

**STEP 8** - If you want to add any new JS file, put them inside **/dev/src/js/** folder. After that update gulpfile.js file and add path to this JS file inside Array variable that says like below. Make sure scripts.js entry stays as last element of array.
Don't forget to stop gulp compiler and restart it.

```
// add all the js files here to compile
var js_files = [
	'./src/js/jquery-3.3.1.min.js',
	'./src/js/slick/slick.min.js',
    ... add our js files here ...
	'./src/js/scripts.js',
]
```
