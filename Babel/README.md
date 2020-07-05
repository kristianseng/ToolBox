// All browser support

// allows to use all modern features --> converts them to old methods




//npm init --> then answer questions

//npm install @babel/core @babel/cli --save-dev

// npm install @babel/preset-env --save-dev

// create .babelrc and define what preset you want to use

/*
{
    "presets": ["@babel/preset-env"]
}



1. install Node.js (and npm) on our computer
2. use npm to init to create a package.json file in the project dir
3. user npm to install babel/core & babel/cli packages
4. install the babel preset (env) & register it in .babelrc


// Usage
make sure you are in the right dir
// node_modules/.bin/babel before.js -o after.js

// package.json shows packages to be installed ----> npm install
// ----> never download or upload node_modules (too big file) --> package.json keeps track

** Project structure example and scripts **

dist/assets/bundle.js --> convert all code to here
dist/index.html

src/index.js --> node_modules/.bin/babel src/index.js -o dist/assets/bundle.js -->

We can make script in package.json so we dont have to write this command all the time
in scripts section -->
"babel": "node_modules/.bin/babel src/index.js -o dist/assets/bundle.js"
---> then we can use "npm run babel"
or change script to "node_modules/.bin/babel src/index.js -w -o dist/assets/bundle.js" (-w watches for changes, automatic change)


*/
