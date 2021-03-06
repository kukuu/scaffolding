# Webpack


Webpack is a Module bundler. It bundles a bunch of modules with require statements

Bundlers such as Browserify and Webpack are steadily taking over from Gulp and Grunt,
 and there is very little room left for both stream-based tasks. The majority of the work which you
  were previously doing with Gulp is now handled by Webpack — bundling and optimization for JavaScript,
   CSS and images; code splitting; targeted bundles for different environments (see isomorphic apps).

As a build tool Webpack puts all of your assets, including Javascript, images, fonts, and CSS, 
in a dependency graph. Webpack lets you use require() in your source code to point to local files, 
like images, and decide how they're processed in your final Javascript bundle, like replacing the path 
with a URL pointing to a CDN.


## When to use  Webpack

If you're building a complex Front End application with many non-code static assets
 such as CSS, images, fonts, etc, then yes, Webpack will give you great benefits.

If your application is fairly small, and you don't have many static assets and you only need to 
build one Javascript file to serve to the client, then Webpack might be more overhead than you need.


## The Dependency Graph property - How it works!
Webpack gives us a dependency graph. It lets you use require() on local "static assets," meaning non-code files.

When you run Webpack, it searches through all of your code for require() calls. It compares the path string for example "../../assets/logo.png" to the "loader" configuration you specify.

```

loaders: [  
    { test: /.png$/, loader: "file" }
]

```

## Key concept: 

 The require source code never actually gets executed in the browser (nor in Node.js).
  Webpack builds a new Javascript file, replacing require() calls with valid Javascript code, such as URLs. 
  The bundled file is what's executed by Node or the browser.

## What About Browserify, Grunt, Gulp?

Webpack puts your static assets (and source code) in a true dependency graph. Grunt and Gulp are only tools 
for working with files, and have no concept of a depdency graph.

Browserify is mainly a tool to transform require() calls that work in Node.js into calls that work in the browser.
 It's a dependency graph for your source code only. 






