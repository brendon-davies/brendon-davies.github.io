when there's angle brackets after a class declaration like this

@Output() timerOpenChange = new EventEmitter<boolean>();

that means that it emits a boolean


smart component: ts/html files that do processing or actions
dumb component: tx/html files that don't really do anything other than displaying stuff

here's the flow of how smart components interact with dumb components

smart-component.ts -> smart-component.html -> dumb-component.ts -> dumb component.html 

define something in the smart-component.ts file




in the smart-component.html use the selector defined in the dumb-component.ts file and using square brackets pass that value into the dumb component



in the dumb-component.ts set that up as an input




now you can use that either in your dumb-component.ts or dumb-component.html






when passing something down from smart component to dumb component that is done using square brackets ( [ ] )

when passing something up from the dumb component to the smart component that is done using parens ( ) 
