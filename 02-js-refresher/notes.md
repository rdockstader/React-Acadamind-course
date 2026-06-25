# Javascript Refresher

## Adding JavaScript to a page

### Javascript can be ran anywhere these days

You can run javascript in the browser, on any computer (server-side, with node, etc.) and even on mobile (i.e. react native)

### Adding Javascript to a website

You can add javascript in two places:

* between script files
* dedicated javascript files (prefered)

### adding a dedicated javascript file

1. Add the file to the project structure
1. Add script tag to the html file
1. add a src attribute to point at the file from the html file

You can also add other tags, like the defer tag. 

The defer tag tells the browser not to load the script until it finishes loading the rest of the DOM

another option is type, such as type="module". This ulocks the import syntax inside the Javascript file.

A note about react: You don't usually add your own script tags, react handles that on it's own as part of its' build process.

## React uses a build process

If you take a look at a react app, you don't have any script tags in the default index.html. How does the react app work? It's because react uses a build process. The code you write is NOT the code that actually gets executed. It gets transformed behind the scenes, and then the browser uses the transformed code. 

### Why does react need a build process?

1. JSX code simply will not run in the browser. it has to be compiled to native web languages to work. 
1. The code wouldn't be optimized for production (such as it wouldn't be minified)

## import/export

Import export is how you use code in other files in the file you're currently using. That'll be really important in react, because that's how you pull components into other components/pages. There is an example of this in util.js and app.js

for import/export to work, you have to have type="module" on the script tag in the html file

type="module" isn't required for react, because of the build process.

if you want to export something from a file without calling the  {} syntax, you can use:

```
export default "test-api-key"
```

then in the import file:
```
import assignedName from "path/to/file.js"
```

## variables and values

there are type and objects in javascript. 

javascript uses camelcase for variable naming. The rest of the regular variables rules apply to javascript. 

you create variables using let, or const. let allows you to modify values at will. const is immutable and should be prefered.