in root of each repo you can run `npm run cy-dev-open`  to open the cypress gui you can select what you want to run from

package.json in each repository contains cypress command and they begin with `cy-`

if you run `npm cy-dev` then it just starts running it and eventually opens the browser

headed shows the browser when it runs the browser
headless does not show the browser

cypress/support/commands.js defines custom cypress commands

to figure out what you want to write a test for

to start writing a test
do imports at the top of the .cy.js file `const merge = require('lodash/merge')`

`describe` block is a summation of what the test is about

in the actual javascript files you can include `:data-cy="something"` in any element that basically creates an id that the cypress tests can grab
