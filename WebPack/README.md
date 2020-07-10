import './dom';

console.log('index file');

// import runs './dom' but does not share functions and variables
// in the file we can put export keyword in front of the files we want to export! and we have to import them

import {styleBody, addTitle} './dom';


// in other page --> 

export const styleBody() => {};
export const string = 'string';

// or at the bottom

export {styleBody, string };


// after all (npm run webpack)


export default users;
import users from '.data';
// but can call other way --> webpack knows it the default export
// adding named exports
// at the bottom export {getPremUsers, users as default};
import users, {getPremUsers} from './data';


// problem so far. have to npm run webpack
// fix --> in json scripts "node_modules/.bin/webpack -w"
// ctrl + c  cancel watching


// Aleternative work flow --> webpack dev serer 
// npm install webpack-dev-server@3.2.1

module.exports = {
    entry: './src/index.js',
    output: {
        path: path.resolve(__dirname, 'dist/assets'),
        filename: 'bundle.js'
    },
    devServer: {
        contentBase: path.resolve(__dirname, 'dist'),
        publicPath: '/assets'
    }
};

// new script: "serve": "webpack-dev-server"
// npm run serve
// problem it is phisiclly changing bundle.js --> great for development
// new script: "build": "node_modules/.bin/webpack"
// delete babel script --> will be incorporated later

/* two scripts now
"build": "node_modules/.bin/webpack --mode production"
"serve": "webpack-dev-server --mode development"
/*

//npm install babel-loader --save-dev

module.exports = {
    entry: './src/index.js',
    output: {
        path: path.resolve(__dirname, 'dist/assets'),
        filename: 'bundle.js'
    },
    devServer: {
        contentBase: path.resolve(__dirname, 'dist'),
        publicPath: '/assets'
    },
    module: {
        rules: [{
            test: /\.js$/,
            exclude: /node_modules/
            use: {
                loader: 'babel-loader',
                options: {
                    presets:['@babel/preset-env']
                }
            }
        }]
    }
};

// any file that ends with .js// but exclude node_modules
// now this will do the transformation to older syntax





// Boilerplate
// just download boilerplate -> npm install
// npm run serve
// at the end npm run build
