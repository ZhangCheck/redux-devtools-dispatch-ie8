# Redux DevTools Dispatch for ie8
Dispatch your actions manually to test if your app reacts well.

### Installation

`npm install --save-dev redux-devtools-dispatch-ie8`

### Usage

You can declare your Dispatcher the same way you declare a Monitor in your Dev Tools.

```jsx
import React from 'react';
import { createDevTools } from 'redux-devtools-ie8';
import Dispatcher from 'redux-devtools-dispatch-ie8';

export default createDevTools(
  <Dispatcher />
);
```

### Props

Name                  | Description
-------------         | -------------
`theme`               | _Same as in LogMonitor's package_ Either a string referring to one of the themes provided by [redux-devtools-themes](https://github.com/gaearon/redux-devtools-themes) (feel free to contribute!) or a custom object of the same format. Optional. By default, set to [`'nicinabox'`](https://github.com/gaearon/redux-devtools-themes/blob/master/src/nicinabox.js).
`initEmpty`           | When `true`, the dispatcher is empty. By default, set to `false`, the dispatcher contains : `{ "type": "" }`.
`actionCreators`      | Either a array of action creators or an object containing action creators. When defined, a selector appears to choose the action creator you want to fire, you can fill up the arguments and dispatch the action.
`dispatchFn`          | Function to be called for dispatching actions. By default it is using component's `this.context.store.dispatch`. 

### Contributing

As this package is my first, any comment, pull request, issue is welcome so I can learn more from everyone.

### License

MIT
