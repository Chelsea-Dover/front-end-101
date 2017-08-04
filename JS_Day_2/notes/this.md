# this
`this` is a global keyword that's value depends on where you are in the scope.

While the JavaScript interpreter evaluates JavaScript code. It maintains `ThisBinding` which holds a reference to an object.

By default `ThisBinding` is holds the reference to the `window` object so if you console log `this` outside of anything it will log out the window object.

Let's say we select a node and attach a function on it. That will make `ThisBinding` change to the object that you selected, so if we console log `this` it will log out the element we selected.
