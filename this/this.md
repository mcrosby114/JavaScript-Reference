# The `this` keyword

`this` is a binding to the call-site of an executing function. The value of `this` is determined by how a function was invoked, and has nothing to do with a function's lexical scope.

The value of `this` is derived from one of four possible function invocation types, in order of precedence:
1. **new Binding**: A function was called with the `new` operator. In this case, the newly constructed object is set as the `this` binding for that function call.
2. **Explicit bindings**: A function was called with `call(..)`, `apply(..)`, or `bind(..)` methods of the `Function` prototype. The value of `this` is whatever object is passed in as the first argument to `call`, `apply`, or `bind`.
3. **Implicity binding**: A function was called directly off of a context object (as a property value: e.g., `obj.myFunction()`. The value of `this` is the context object owning the function call.
4. **Default binding**: The value of `this` is `undefined` in if the call occurs within `"use strict";`; otherwise it's the `global` object (`window` in browsers).
