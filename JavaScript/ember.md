# Installation

1. Install dependencies
  1. [nodejs](https://nodejs.org/en/)
  2. [npmjs](https://www.npmjs.com/)
  3. [bower](https://bower.io/)
  4. [git](https://git-scm.com/)
  5. [watchman](brew install watchman)

1. [Install EMBER](https://ember-cli.com/)
  * `npm install -g ember-cli`

# Docs

* [ember getting started docs](https://ember-cli.com/user-guide/#getting-started)
* [routes](https://guides.emberjs.com/v2.4.0/routing/defining-your-routes/)

# Commands

* `ember --help` - Gives us a list of subcommands with their own list of options. `help`
* `ember -v` - Shows version info
* `ember --help new` - show command info
* `ember new` - Create a new directory/app structure, initial commit, runs npm install and bower install (generate a project)
* `ember serve` - Serve a project. alias `s`
* `ember g route <routename>` - creates a new route + template for that route


# Creating an app

1. Run the command: `ember new <AppName>`

# Folder structure

Specific folders:

public holds your static assets
Ember copies files into dist when building the site
Configuration values go in config
Finally, app holds your application's source code.
Inside the app folder:

router.js holds routes
index.html has a template for the whole page, but includes the header, body and footer so you will be working in those instead (via app/templates)
app.js is the project's main setup file
styles holds style sheets
routes holds additional routing information
models holds schema files for data
helpers holds helper files for templates
controllers is being phased out in favor of components
components holds custom html elements. The code lives in components and the HTML lives in templates/components


# templates

## Navigate between routes

`{{#link-to "index"}}<img class="logo">{{/link-to}}`

## Handlebar

The html
```
<div id="brick-container"></div>

<script id="brick-template" type="text/x-handlebars-template">
    <div class="brick">
        <h1>{{name}}</h1>
        <div class="desc">
            {{description}}
        </div>
    </div>
</script>
```

The following JavaScript will get the template, compile it, call the template with data, and update brick-container element with the resulting HTML:
```
// get template from HTML
var brickContainer = document.querySelector( '#brick-container' );
var brickTemplate = document.querySelector( '#brick-template' );

// compile source template into a template function
var template = Handlebars.compile( brickTemplate.innerHTML );

// the app's data
var context = {name: 'Red Brick', description: 'A colored brick that can be used to...'};

// build the HTML template with the supplied data
var html = template(context);

// fill the page with content
brickContainer.innerHTML = html;
```
