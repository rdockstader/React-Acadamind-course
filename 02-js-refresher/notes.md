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