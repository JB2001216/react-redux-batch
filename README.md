redux-batched-updates
=====================

Batch React updates that occur as a result of Redux dispatches, to prevent cascading renders. See https://github.com/gaearon/redux/issues/125 for more details.

```js
npm install --save redux-batched-updates
```

## Usage

```js
// Use as higher-order store
import { batchedUpdates } from 'react-redux-batch';
const store = batchedUpdates(createStore)(reducer, intialState);

// Or as middleware
import { batchedUpdatesMiddleware } from 'react-redux-batch';
const m = composeMiddleware(thunk, promise, batchedUpdatesMiddleware);
const store = applyMiddleware(m)(createStore)(reducer, initialState)
```
